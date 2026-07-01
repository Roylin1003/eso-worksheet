# eso-worksheet

一種結構化分析方法，用表格引導使用者拆解複雜事務的內在系統——多方立場、卡關、設計困境、談判、決策——完全不需要使用者先學任何術語。

理論脈絡：[ESO 框架：一種敘事分析的方法](https://vocus.cc/article/695600d9fd89780001c83043)。本 skill 是這套框架的表格式操作版本，靈感部分來自麥肯錫「空雨傘」（Sky-Rain-Umbrella）思維法。

## 用法

### Claude Code（原生支援）

把整個資料夾複製到你的 skills 目錄：

```bash
# 使用者層級（所有專案都能用）
cp -r eso-worksheet ~/.claude/skills/

# 或專案層級（只有這個專案能用）
cp -r eso-worksheet <你的專案>/.claude/skills/
```

開新 session 後直接說「幫我跑一次 ESO 表格分析：[情境]」，或明講 `/eso-worksheet`，會自動觸發。

### 其他 LLM / agent（Codex、ChatGPT、其他 CLI agent…）

沒有原生 skill 載入機制的環境，把 `SKILL.md` 和 `references/spec.md` 整份內容貼進對話，前面加一句：

> 以下是一套分析方法的操作指南，請完全照著執行，引導我一步步填表分析我接下來要講的情境。

或如果該環境能讀取本機檔案，直接說：

> 請讀取 `SKILL.md` 和 `references/spec.md`，照裡面的九步驟程序，引導我做一次 ESO 表格式分析。

## 內容

```
SKILL.md              — 觸發條件 + 九步驟引導程序 + 邊界規約
references/spec.md    — 表格模板、三燈規則、來源注腳格式、精簡展演範例
```
