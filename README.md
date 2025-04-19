# 🏋️ Workout Tracker with Nutritionix + Google Sheets 📊

This Python app uses **Natural Language Processing** to understand your workout descriptions, calculate calories burned, and log everything to a **Google Sheet** automatically. Just type what exercise you did — and it handles the rest!

---

## ✨ Features

- 🧠 Uses [Nutritionix API](https://www.nutritionix.com/) to interpret natural language workout descriptions
- 🔢 Calculates duration, calories burned, and exercise names
- 📄 Stores all workout logs in a [Google Sheet](https://sheety.co/) using the Sheety API
- 🔐 Secure API key management via environment variables
- 💻 Designed for use in PyCharm, Replit, or any IDE with environment support

---

## 📦 Tech Stack

- Python 3
- `requests`
- Nutritionix API
- Sheety API
- Google Sheets

---

## 🚀 Getting Started

### 1. Clone the Repo
```bash
git clone https://github.com/your-username/workout-tracker.git
cd workout-tracker
```

### 2. Install Dependencies
```bash
pip install requests
```

### 3. Setup Environment Variables

Set these variables in your environment (e.g. `.env` file, Replit Secrets, or PyCharm Config):

```
ENV_NIX_APP_ID=your_nutritionix_app_id
ENV_NIX_API_KEY=your_nutritionix_api_key
ENV_SHEETY_ENDPOINT=https://api.sheety.co/your-endpoint/workouts
ENV_SHEETY_USERNAME=your_username
ENV_SHEETY_PASSWORD=your_password
```

You can refer to the included file `env_for_pycharm.txt` for the format.

### 4. Run the Script
```bash
python main.py
```

Then enter your workout in plain English:
```
Tell me which exercises you did: Ran 5km and did 20 push-ups
```

---

## 📝 Sample Output

```
Nutritionix API call:
[{'name': 'running', 'duration_min': 30, 'nf_calories': 270}, ...]
Sheety Response:
Success! Logged in Google Sheets ✅
```

Google Sheet Preview:
| Date       | Time     | Exercise | Duration (min) | Calories |
|------------|----------|----------|----------------|----------|
| 19/04/2025 | 08:32:15 | Running  | 30             | 270      |

---

## 🛠 Troubleshooting

### ❗ KeyError
Check that your environment variable names match what your Python code expects.

### ❗ Sheety "Bad Request"
Make sure your sheet name is singular in code but camelCase in your Sheety API. Ex: `"workouts"` sheet → use `"workout"` in the JSON.

### ❗ Sheety "Insufficient Permission"
Ensure you've authorized Sheety properly in your Google Account's security settings.

---

## 🙏 Credits

- [Nutritionix](https://www.nutritionix.com/) for exercise data
- [Sheety](https://sheety.co/) for easy Google Sheet API access

---

## 🌟 Like this project?

Give it a ⭐ on GitHub — and feel free to contribute!
