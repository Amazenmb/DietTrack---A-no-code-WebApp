# DietTrack: A-no-code-WebApp
Personal Diet tracker developed using no code tools


**Built using Supabase + Lovable (No Code)**  
Track your daily meals, monitor nutrition goals, and visualize progress — all without writing a single line of code!

---

## 📌 Overview

This is a simple, responsive, and customizable **Personal Diet Tracker** built entirely using **no-code tools**. The app helps users:

- Log daily meals and nutrients
- Set calorie goals based on personal details
- Track progress via daily and weekly summaries
- Stay accountable with upcoming reminders (in progress)

---

## ⚙️ Tech Stack

| Function                  | Tool          |
|---------------------------|---------------|
| Database & Authentication| [Supabase](https://supabase.com) |
| Frontend/UI Builder       | [Lovable](https://lovable.so)   |

---

## 🧠 Features

### 👥 User Authentication
- Email login using Supabase Auth
- All user data securely stored in Supabase

### 🎯 Goal Setup
- Age, Gender, Height, Weight, Activity Level
- Choose goal: Lose, Maintain, or Gain weight
- Based on the entered data, automatically calculate TDEE (Totally Daily Energy Expenditure) and daily calorie goal

### 🍽️ Meal Logging
- Add meal name, calories, carbs, protein, fats
- Organize by meal type (breakfast, lunch, etc.)
- Edit/delete entries with ease

### 📊 Daily Summary
- View total calories and macronutrients for the day
- Compare with your calorie target

### 📈 Weekly Trends
- Line graphs and bar charts of nutrient intake
- Visualize your progress and patterns

### 🔔 Planned Feature: Meal Reminders
- Scheduled email or push notifications
- Reminder to log meals daily

---

## 🧾 Database Schema (Supabase)

### `users`
| Field       | Type     |
|-------------|----------|
| id          | UUID (PK)|
| email       | String   |
| created_at  | Timestamp|

### `user_profiles`
| Field          | Type     |
|----------------|----------|
| user_id        | UUID (FK to users) |
| age            | Int      |
| gender         | String   |
| height_cm      | Float    |
| weight_kg      | Float    |
| activity_level | String   |
| goal_type      | String   |
| created_at     | Timestamp|

### `goals`
| Field         | Type     |
|---------------|----------|
| user_id       | UUID     |
| calorie_target| Int      |
| goal_type     | String   |
| created_at    | Timestamp|

### `meals`
| Field         | Type     |
|---------------|----------|
| id            | UUID     |
| user_id       | UUID     |
| food_name     | String   |
| meal_type     | String   |
| calories      | Int      |
| carbs         | Int      |
| proteins      | Int      |
| fats          | Int      |
| logged_at     | Timestamp|

### `daily_summaries`
| Field           | Type     |
|-----------------|----------|
| user_id         | UUID     |
| date            | Date     |
| calories_total  | Int      |
| carbs_total     | Int      |
| protein_total   | Int      |
| fats_total      | Int      |
| calorie_goal    | Int      |
| met_goal        | Boolean  |

---

## 🚀 Getting Started

1. **Create a Supabase project**  
   - Enable Auth
   - Create tables as per schema above (or prompt Lovable to do so once tables are linked as in step 3.)

2. **Design UI in Lovable**
   - Use Lovable’s no-code builder to create the onboarding, meal logging, summaries, and trends views

3. **Configure Lovable to connect to Supabase**
   - Use the Supabase REST API or client libraries via Lovable integrations

4. **Publish app** using Lovable's deployment options

---

## 🧪 Demo
**Started with this**: 

![image](https://github.com/user-attachments/assets/8ffafe10-0de9-4b5e-91f4-10a37318143f)

![image](https://github.com/user-attachments/assets/99ff6ad4-ae73-49d5-ad48-0c844a37146b)

![image](https://github.com/user-attachments/assets/afa9c91b-de21-487e-a669-2e2ea7f01133)

**Built this**:

![image](https://github.com/user-attachments/assets/492f9bc6-1ffb-42f0-88ee-45e0d6831151)

![image](https://github.com/user-attachments/assets/2e12df75-e1c1-4ff2-a6fc-9dc2e36de399)

![image](https://github.com/user-attachments/assets/6eb32b43-54e7-4699-a9a2-657863bcd8f6)

![image](https://github.com/user-attachments/assets/c74ae5bf-9fb6-41db-a8ca-512b9041e55d)




Do check the website and let me know how was it!

## 📚 Future Enhancements

- Add push notifications (via OneSignal)
- AI-powered meal suggestions
- Health API integrations (Fitbit, Apple Health)
- Weekly recap emails
- Community challenges

---

## 🙌 Acknowledgments

- [Supabase](https://supabase.com) for backend and auth
- [Lovable](https://lovable.so) for intuitive no-code UI building
- Youtube

---

## 📬 Contact

Have ideas, feedback, or questions?  


---


