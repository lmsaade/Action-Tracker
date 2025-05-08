# Power BI Action Tracker

This dashboard monitors task health using conditional formatting and icons, offering users clear, actionable insights through an intuitive and interactive layout.

## 📖 Table of Contents

- [The Ask](#the-ask)
- [Process](#process)
- [Features](#features)

---

## ❓ The Ask

My team came to me asking for a dashboard to help us keep better tabs on task health for our weekly meetings. They usually tracked everything in Microsoft Teams Planner: tasks, updates, due dates—you name it.

I’d built action trackers before using SharePoint lists as the data source, but this time I wanted to try something new. The goal? Make the tracker as hands-off as possible. I set out to create a dashboard that worked mostly behind the scenes—with some help from Power Automate—so my team didn't need to do any additional work.

## 🛠️ Process

First, I jumped into Power Automate and built a scheduled cloud flow that pulls our team's Planner data and saves it as a JSON file in a designated folder. The flow runs daily at 6:00 A.M. EST. Setting it up was pretty straightforward, although I did have to get creative with mapping some of the Planner buckets and label colors to the tags we actually use.

Once I confirmed the JSON file was coming through cleanly and consistently, I used it as the data source for my Power BI dashboard. To improve the user experience, I added a few fun touches—icons to indicate task progress, list formatting with checkboxes, and conditional formatting to highlight overdue tasks.

And of course, because who doesn’t love a good button—I created a dummy table so the slicer could operate off static values rather than dynamically changing ones. These buttons act as slicers and give users a more intuitive, streamlined way to filter and explore the data.

## 🚀 Features

- 🏁 **Automated Planner Sync**  
  A scheduled Power Automate flow runs daily at 6:00 A.M. EST to pull Microsoft Planner data into a structured JSON file—no manual steps needed.

- 🎨 **Smart Label Mapping**  
  Planner label colors are mapped to team-specific tags to ensure consistent categorization.

- 📊 **Power BI Dashboard Integration**  
  The dashboard pulls directly from the JSON file for real-time, dynamic visualizations.

- 🌓 **Task Progress Icons**  
  Icons provide a visual cue for task completion status at a glance.

- ✅ **Formatted Lists with Checkboxes**  
  Checklist-style formatting improves readability and makes task tracking easy.

- ⏰ **Overdue Task Highlighting**  
  Conditional formatting helps quickly flag tasks that need immediate attention.

- 🔴 **Intuitive Button Slicers**  
  Slicers powered by a static dummy table offer a clean, user-friendly way to filter views.