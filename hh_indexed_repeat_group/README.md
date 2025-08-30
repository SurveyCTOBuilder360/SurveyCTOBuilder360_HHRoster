
# 🏠 Household Roster Template – Indexed Repeat Group  
**SurveyCTOBuilder360 | Bangla-English XLSForm**

---

## 📌 Overview

This template demonstrates how to use `indexed-repeat()` in SurveyCTO to dynamically reference the household head’s name and position from within a repeat group. It ensures clean data collection, enforces validation, and supports bilingual deployment for field teams.

---
## 📥 Download XLSForm

You can download the main template file here:

- 📄 [SurveyCTO_Household_Roster_Indexed_Repeat_Group.xlsx](assets/SurveyCTO_Household_Roster_Indexed_Repeat_Group.xlsx)

## 📂 Files Included

| File Name                                      | Description |
|------------------------------------------------|-------------|
| `SurveyCTO_Household_Roster_Indexed_Repeat_Group.xlsx` | Main XLSForm with indexed-repeat logic |
| `Enumerator_Script_ENBN.pdf`                  | Bangla-English script for field teams |
| `logic_diagram_indexed.png`                   | Visual flow of indexed-repeat logic |
| `README.md`                                   | This documentation file |

---

## 🧠 Key Features

- 🔁 Repeat group for household members with name, age, gender, and relationship  
- 🎯 Dynamic identification of household head using `position(..)` and `indexed-repeat()`  
- ✅ Validation to ensure exactly one head is selected  
- 🧩 Summary note displaying head’s name and position  
- 🌐 Bilingual labels (Bangla-English) for field deployment  
- 📘 Enumerator script for training and onboarding  
- 📊 Logic diagram for visual learners and reviewers

---

## 💡 How It Works

1. Enumerators list household members one by one.
2. Each member’s relationship is recorded.
3. The form calculates the position of the member marked as “head.”
4. Using `indexed-repeat()`, the head’s name is pulled and displayed dynamically.
5. A constraint ensures only one member is marked as head.

---

## 📝 Sample Logic

```excel
calculate: head_index_local → if(${relation}='head', position(..), 0)  
calculate: head_index → max(${head_index_local})  
calculate: head_name → indexed-repeat(${name}, ${hh_member}, ${head_index})  
constraint: ${head_count} = 1
