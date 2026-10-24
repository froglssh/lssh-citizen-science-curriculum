# 公民科學培訓課程 課程子知識庫規範 (Curriculum Sub-Wiki Rules)

本文件定義本知識庫（LLM Curriculum Sub-Wiki）之架構、元數據規範、母子知識庫雙向聯動協議與維護工作流。

---

## 1. 母子知識庫雙向聯動架構 (Parent-Child Wiki Hierarchy)

本子知識庫作為**母知識庫**之垂直聚焦衍生體系：

- **母知識庫 (Master Knowledge Base)**：
  - 路徑：`file:///Users/froglssh/Library/CloudStorage/GoogleDrive-frog@lssh.tp.edu.tw/我的雲端硬碟/12生物營隊/生物營隊知識庫/`
  - 職掌：沉澱 10 年跨學年營隊大歷史、大型野外實察、專案行政核銷、校外行動研究得獎論文。
- **課程子知識庫 (Curriculum Sub-Wiki)**（本庫）：
  - 路徑：`file:///Users/froglssh/Library/CloudStorage/GoogleDrive-frog@lssh.tp.edu.tw/我的雲端硬碟/01專題教材/公民科學培訓課程/`
  - 職掌：落實「高二多元選修（10週密集）」與「高一彈性學習（18週）」之正式校本選修課程開課、每週課堂指引、任務學習單、麗山校訂課程成績評量常態分佈規準與學生學習歷程檔案（OPQN）輔導。

---

## 2. 目錄結構

```
公民科學培訓課程/
├── README.md               # 儲存庫介紹與子庫定位
├── wiki-rules.md           # 子庫 Schema、規範與母庫對接指引
├── index.md                # 課程全域主索引 (Curriculum Knowledge Map)
├── log.md                  # 時間軸維護日誌 (Append-only Log)
├── SKILL.md                # 公民科學課程專屬教學與開課助理 Skill
├── 01_課程綱要與設計/       # 官方填報表單、10週/18週進度、素養圖像對齊
├── 02_單元教案與教學指引/   # 七大模組單元深度教案、教學流程與器材
├── 03_學習單與評量規準/     # 任務卡、成績 90/85 常態分佈、口語與海報 Rubrics
├── 04_教學資源與講義/       # 講義精粹、圖鑑清單、數位工具、外部合作網絡
└── 05_學生專題與成果產出/   # 學習歷程檔案上傳指南、海報範例、解說嘉年華
```

---

## 3. YAML Frontmatter 規範 (Dataview Ready)

所有單元筆記必須包含標準 YAML Frontmatter：

```yaml
---
type: curriculum_doc  # 可選: course_syllabus, unit_plan, worksheet_rubric, resource, student_guide
title: "文件標題"
course_type: "多元選修" # 或 "彈性學習"
author: "林獻升 老師"
grade: "高二"          # 或 "高一"
school_vision: [科學力, 築夢力, 跨界力, 公民力]
parent_wiki: "file:///Users/froglssh/Library/CloudStorage/GoogleDrive-frog@lssh.tp.edu.tw/我的雲端硬碟/12生物營隊/生物營隊知識庫/index.md"
tags: [公民科學, 多元選修, 108課綱, 課程教案]
created: 2026-10-24
last_modified: 2026-10-24
---
```

---

## 4. 麗山校訂課程成績評量強制遵循規範
依據麗山高中「校訂課程學生成績評量補充規定」：
1. **高分群人數上限**：
   - 90 分以上：**不得超過選課人數 20%**。
   - 85 分以上：**不得超過選課人數 50%**。
2. **GPA 等第制對照**：
   - A+ (94-100, GPA 4.0)、A (87-93, GPA 4.0)、A- (80-86, GPA 3.7)、B+ (77-79, GPA 3.3)、B (74-76, GPA 3.0)。
3. 所有單元評量與學期總成績配分，必須內建常態校準機制。
