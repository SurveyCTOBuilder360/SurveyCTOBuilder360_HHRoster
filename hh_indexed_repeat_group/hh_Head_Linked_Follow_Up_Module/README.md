# 🏠 SurveyCTO Household Roster – Head Linked Follow-Up Module

This module is a field-ready, bilingual SurveyCTO form designed to capture household member details and trigger follow-up questions for the identified head of household. Built using **indexed-repeat()**, **conditional logic**, and **modular design**, it’s ideal for researchers, NGOs, and data collection teams seeking clean, scalable roster templates.

## 📥 Download the XLSForm

You can download the latest version of the **SurveyCTO Household Roster – Head Linked Follow-Up Module** directly from this repository:

**🔗 [Download XLSForm](https://github.com/SurveyCTOBuilder360/SurveyCTOBuilder360_HHRoster/blob/main/hh_indexed_repeat_group/SurveyCTO_Household_Roster_Head_Linked_Follow_Up_Module.xlsx)**

## 📦 What’s Included

- ✅ Repeat group for listing household members
- ✅ Auto-generated member IDs using `position()`
- ✅ Relationship tagging with head identification logic
- ✅ Indexed reference to head’s name via `indexed-repeat()`
- ✅ Conditional follow-up questions for the head only
- ✅ Bilingual labels (English and Bangla)
- ✅ Summary view of head’s name and position

## 🧠 How It Works

1. Enumerators list each household member with:
   - Name
   - Age
   - Gender
   - Relationship to head

2. The form automatically:
   - Flags the head using `if(${member_relationship}='head', 1, 0)`
   - Stores the head’s index for referencing
   - Displays follow-up questions only for the head

3. Head-specific questions include:
   - Education level
   - Employment status
   - Main income source

## 🌐 Languages Supported

- **English** – Default labels and hints
- **Bangla** – Parallel labels for field-level clarity

## 🛠 Technical Highlights

| Feature                     | Logic Used                                |
|----------------------------|--------------------------------------------|
| Member ID generation       | `position(..)`                             |
| Head flagging              | `if(${member_relationship}='head', 1, 0)`  |
| Indexed name reference     | `indexed-repeat(${name}, ${hh_member}, ${head_index})` |
| Conditional follow-up      | `relevant: ${is_head}=1`                   |

## 📁 File Structure

- `SurveyCTO_Household_Roster_Head_Linked_Follow_Up_Module.xlsx` – Main form definition
- `README.md` – Documentation for learners and implementers

## 🚀 Getting Started

1. Upload the `.xlsx` file to your SurveyCTO server.
2. Review and test the form in **Design** and **Collect** modes.
3. Customize choice lists or add constraints as needed.
4. Deploy for pilot or full-scale data collection.

## 📚 Learning Resources

- [SurveyCTO Expression Reference](https://docs.surveycto.com/01-designing-forms/expressions/)
- [Indexed Repeat Tutorial](https://docs.surveycto.com/01-designing-forms/repeat-groups/#indexed-repeat)
- [Bilingual Form Design](https://docs.surveycto.com/01-designing-forms/form-languages/)

