# 科學城 2024 永續報告書 — 中英翻譯作業流程

**Version:** 1.0  
**Last Updated:** 2026-05-27  
**Skill:** `esg-report-translator`

---

## 一、專案背景與挑戰

### 翻譯任務說明

本專案目標為將「新竹科學城 2024 永續報告書」（中文版）翻譯為英文版，供國際揭露使用，需符合 GRI Universal Standards 2021、SASB、TCFD、ISSB（IFRS S1/S2）審閱等級。

### 核心挑戰

永續報告書為設計複雜的排版文件（含圖表、色塊、圖示、表格），直接在 PDF 或 InDesign 原始檔上編輯會破壞版面。因此採用以下分工策略：

| 工具 | 負責事項 |
|------|----------|
| **Canva** | 版面重製與排版調整（維持視覺設計） |
| **Claude Code + Skill** | 中文原文 → 英文審閱等級翻譯、Canva 自動翻譯 QA |

---

## 二、整體作業架構

```
中文 PDF（原始報告書）
        ↓
  【Phase 1】分頁拆解
  逐章節截圖 / 文字擷取
        ↓
  【Phase 2】Canva 版面重製
  在 Canva 複製原始版面設計
  用 Canva 內建 AI 翻譯（初稿，品質不穩定）
        ↓
  【Phase 3】Claude 翻譯審查（本 Skill Package）
  輸入：中文原文 + Canva 英文初稿
  輸出：修正後英文、錯誤清單、Canva 修改指令
        ↓
  【Phase 4】Canva 修正
  依 Claude 輸出的 Find/Replace 清單修正 Canva 文字
        ↓
  【Phase 5】匯出英文版 PDF
```

---

## 三、逐 Phase 操作說明

### Phase 1 — 分頁拆解

**目標：** 取得每頁的中文原始文字內容。

**操作方法：**
1. 用 Adobe Acrobat 或 PDF Expert 開啟中文版報告書
2. 逐頁或逐章節複製文字內容（Ctrl+A → Copy）
3. 若為掃描式 PDF（文字不可選取），使用 OCR 工具（如 Adobe Acrobat OCR / Google Document AI）
4. 將文字貼入記事本，按章節儲存為 `.txt`

**注意：**
- 表格數字需人工核對，OCR 數字易出錯
- 圖說（Caption）需單獨擷取，避免與內文混淆

---

### Phase 2 — Canva 版面重製

**目標：** 在 Canva 中重製原始版面並產生英文初稿。

**操作流程：**
1. 在 Canva 建立新設計，尺寸設為 A4（210×297mm）
2. 依原始 PDF 頁面逐一重製版面元素（色塊、標題樣式、圖示位置）
3. 貼入中文原文文字
4. 使用 Canva AI 翻譯功能產生英文初稿
5. 截圖或複製 Canva 英文文字，準備送交 Claude 審查

**已知 Canva 翻譯常見錯誤（需特別注意）：**
- 專有名詞誤譯（如 "Sustainable governance" 應為 "Corporate Governance"）
- 漏句（長段落中間遺漏一句）
- 主詞混用（"We" / "the Company" 不一致）
- 時態錯誤（績效數據誤用現在式）
- 語氣過度口語化

---

### Phase 3 — Claude 翻譯審查（核心步驟）

**目標：** 將 Canva 初稿提升至審閱等級英文。

#### 啟動方式

在 Claude Code 中輸入以下任一指令：
```
/esg-translate
/esg-review
```

或直接輸入觸發詞：
```
永續報告書翻譯審查
Canva 翻譯 QA
```

#### 輸入格式

```
【中文原文】
（貼上中文原文段落）

【Canva 英文初稿】
（貼上 Canva 翻譯結果）
```

若只有中文原文（無 Canva 初稿），使用 TRANSLATE_ONLY 模式：
```
【中文原文】
（貼上中文原文）

翻譯模式：TRANSLATE_ONLY
```

若只需審查已有翻譯（不需重寫），使用 REVIEW_ONLY 模式：
```
【英文翻譯】
（貼上現有翻譯）

審查模式：REVIEW_ONLY / 只審查，不改寫
```

#### Claude 輸出說明

| 輸出區段 | 內容 |
|----------|------|
| Section 1: Final English Translation | 修正後英文全文（REVIEW_ONLY 模式跳過） |
| Section 2: Error List | 每個錯誤的位置、類型、嚴重度、原文、修正、原因 |
| Section 3: Consistency Check | 清單勾選（術語、時態、無漏譯、無增譯、數字） |
| Section 4: Notes for Canva Fixes | Find/Replace 清單 + 版面注意事項 |

---

### Phase 4 — Canva 修正

**目標：** 將 Claude 審查結果套用回 Canva。

**操作方法：**
1. 開啟 Canva 設計檔
2. 使用 Canva「尋找與取代」功能（Ctrl+F）逐一執行 Claude 提供的 Find/Replace 清單
3. 針對版面注意事項（文字長度改變、換行位置）手動調整
4. 全頁視覺檢查：確認排版未跑版

**版面常見問題：**
- 英文文字較中文長 15–25%，文字框可能溢出
- 解決方法：縮小字體 0.5–1pt，或縮寫部分非關鍵詞

---

### Phase 5 — 匯出

**目標：** 產出英文版最終 PDF。

**操作方法：**
1. Canva → 下載 → PDF（印刷品質）
2. 全文再次校對數字與術語（最終人工核查）
3. 版本命名規則：`ScienceCity_SR2024_EN_v1.0.pdf`

---

## 四、分章節翻譯建議順序

依重要性與複雜度排序，建議翻譯優先順序：

| 優先順序 | 章節 | 理由 |
|----------|------|------|
| 1 | 封面、目錄、關於本報告 | 框架資訊，後續章節依賴 |
| 2 | 董事長致詞 | 高能見度，語氣代表全司 |
| 3 | 永續治理（公司治理、重大性分析） | GRI/ISSB 核查重點 |
| 4 | 環境永續（溫室氣體、能源、水資源） | 數字密集，需最高精確度 |
| 5 | 員工與社會（幸福職場、社會共融） | 文字較多，需時態控制 |
| 6 | 永續價值鏈（供應商管理） | 術語複雜 |
| 7 | 附錄（GRI Index、資料表格） | 格式固定，相對容易 |

---

## 五、Skill Package 安裝位置

本 Skill Package 需放置在 Claude Code 可讀取的路徑：

**選項 A（專案層級，推薦）：**
```
.claude/
  skills/
    esg-report-translator/
      SKILL.md                ← 主 skill 進入點
      glossary.md
      translation_guidelines.md
      quantitative_standards.md
      examples.md
      notebooklm_reference.md
```

**選項 B（直接使用 ESG-SkillPack 資料夾）：**
將整個 `ESG-SkillPack/` 資料夾複製至 `.claude/skills/esg-report-translator/`，或在 Claude Code 工作目錄中直接引用。

**啟動指令：**
```bash
/esg-report-translator
```
或使用 manifest.md 中列出的任何觸發詞。

---

## 六、品質管控清單

每章節翻譯完成後，執行以下核查：

### 術語核查
- [ ] 所有 glossary.md 術語正確使用
- [ ] 無 Section K 禁用詞出現

### 時態核查
- [ ] 政策描述 → 現在式
- [ ] 2024 年績效 → 過去式
- [ ] 未來目標 → aims to / will

### 數字核查
- [ ] 所有數字與單位與中文原文一致
- [ ] ROC 年份（民國）已換算為西元年
- [ ] 千位分隔符號（,）正確使用
- [ ] CO₂e 下標格式正確

### 版面核查
- [ ] 英文文字框未溢出
- [ ] 表格欄位對齊正常
- [ ] 章節標題與 Section Heading 清單一致

---

## 七、迭代維護說明

本 Skill Package 為可迭代文件，建議每次翻譯完成後更新：

| 發現問題 | 更新位置 |
|----------|----------|
| 新術語 / 新禁用詞 | `glossary.md`（A–K 章節） |
| 新翻譯模式案例 | `examples.md` |
| 新數字格式需求 | `quantitative_standards.md` |
| 新語氣規則 | `translation_guidelines.md` |
| Skill 觸發條件調整 | `SKILL.md` frontmatter |

更新後請同步更新 `manifest.md` 中的版本號與 Change Log。
