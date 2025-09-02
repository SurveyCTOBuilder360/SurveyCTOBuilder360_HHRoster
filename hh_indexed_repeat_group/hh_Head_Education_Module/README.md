# 🎓 SurveyCTO Head Education Module

This bilingual SurveyCTO form is designed to collect education-related data for the head of household only. Using indexed-repeat logic and conditional relevance, it ensures targeted follow-up questions while maintaining clean, scalable form structure.

---

## 📦 What’s Included

- ✅ Repeat group for listing household members
- ✅ Identification of head using relationship field
- ✅ Indexed reference to head’s name and position
- ✅ Education questions shown only for the head
- ✅ Multi-select barriers to education
- ✅ Bilingual labels (English and Bangla)

---

## 🧠 Code Logic Explained (For Learners)

| 🔧 Expression | 💡 What It Does | 🧑‍🏫 Simple Explanation |
|--------------|----------------|-------------------------|
| `position(..)` | Assigns a unique ID to each household member | Think of it like numbering each person: 1st, 2nd, 3rd... |
| `if(${relationship}='head', 1, 0)` | Flags the head of household | If someone is marked as "head", this returns 1 (true); otherwise 0 |
| `max(${is_head_local})` | Stores the index of the head | Finds the position of the person marked as head |
| `indexed-repeat(${name}, ${hh_member}, ${head_index})` | Pulls the head’s name from the repeat group | It looks up the name of the person marked as head |
| `position(..) = ${head_index}` | Flags current repeat as head | Used to trigger follow-up questions only for the head |
| `relevant: ${is_head}=1` | Shows follow-up questions only for the head | Ensures head-specific questions are hidden for others |

---

## 🌐 Languages Supported

- **English** – Default labels and hints  
- **Bangla** – Parallel labels for field-level clarity

---

## 📥 Download the XLSForm

You can download the latest version of the **Head Education Module** directly from this repository:

**🔗 [Download XLSForm](assets/SurveyCTO_Head_Education_Module.xlsx)**

This file includes:
- Indexed logic for head identification
- Education and barrier questions for head only
- Bilingual labels and hints

> Tip: After downloading, upload the `.xlsx` file to your SurveyCTO server and preview it in **Design** mode to ensure everything renders correctly before deployment.

---

## 📘 Enumerator Script (Bangla-English)

This PDF provides a bilingual script for training enumerators on how to use the Head Education Module effectively in the field.

**🔗 [Download Enumerator_Script_ENBN.pdf](Enumerator_Script_ENBN.pdf)**

Includes:
- Step-by-step instructions  
- Head identification guidance  
- Bangla-English translations  
- Tips for clean data entry

---

## 🖼️ Logic Diagram: `indexed-repeat()` Flow

To help learners visualize the skip logic and head identification process, here’s a diagram:

![Household Roster Logic Diagram](logic_diagram_indexed.png)

---

## 🙌 Credits

Developed by **Bijoy Khiang**, Research Assistant at ARCED Foundation, as part of the **RMG_Stanford_2025** project. Special thanks to field teams and collaborators who tested and refined the module.

---
