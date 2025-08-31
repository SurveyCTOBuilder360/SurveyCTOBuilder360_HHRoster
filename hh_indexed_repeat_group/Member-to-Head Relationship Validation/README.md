# 🧠 SurveyCTO Household Roster: Member-to-Head Relationship Validation

This module helps researchers and field teams collect household member data and automatically validate relationships using **indexed-repeat()** logic in SurveyCTO. It’s designed to reduce errors, improve data quality, and simplify form design—especially when referencing the head of household.

---

## 📥 Download the XLSForm

You can download the ready-to-use XLSForm from Google Sheets:

🔗 [SurveyCTO_Household_Roster_Member_to_Head_Relationship_Validation.xlsx](https://docs.google.com/spreadsheets/d/19A_76rvGuj9YC2yqZ9k5VKvQkeQvRzSQoGGTQ5pUkn8/edit?gid=1299903768#gid=1299903768)

---

## 🔁 How the Logic Works (Explained Simply)

This module helps you:
- Automatically identify the head of household
- Retrieve the head’s name and age using indexed-repeat
- Compare each member’s age to the head’s
- Display a note showing the age difference

🧩 Simple logic:
> “We find who the head is, grab their details, and compare each member’s age to the head’s—no advanced coding
>
The form uses `position(..)` to locate the head, then pulls their data using `indexed-repeat()` and calculates `${age_gap}` for each member. These values are shown as notes to help enumerators catch inconsistencies.

---

## 🛠️ Customizing Relationship Constraints

This module is fully editable. You can:
- Add or modify relationship options (e.g., grandparent, cousin)
- Apply age logic (e.g., child must be younger than head)
- Add constraints (e.g., only one head allowed, spouse age range)

Just update the `choices` sheet and use `constraint` or `relevant` columns in the `survey` sheet. The logic is modular and adaptable to your project’s needs.

---

## 📘 Enumerator Script

Train your field team with this bilingual script:

📄 `Enumerator_Script_ENBN.pdf` *(coming soon)*

Includes Bangla-English prompts, logic explanations, and field instructions.

---

## 📊 ASCII Logic Flowchart

You can view the full logic diagram in Markdown format:

📄 [ASCII_flowchart.md](https://github.com/SurveyCTOBuilder360/SurveyCTOBuilder360_HHRoster/blob/main/hh_indexed_repeat_group/Member-to-Head%20Relationship%20Validation/ASCII_flowchart)

---

## 🧩 What’s Inside

- ✅ Indexed-repeat logic for head referencing  
- ✅ Age gap calculation  
- ✅ Bilingual labels (Bangla-English)  
- ✅ Clean README and modular structure  
- ✅ Ready for GitHub, Gumroad, or SurveyCTO deployment

---

## 💬 Questions or Feedback?

Open an issue or reach out via LinkedIn or WhatsApp.  
We’re building tools that make fieldwork smarter, faster, and easier.
