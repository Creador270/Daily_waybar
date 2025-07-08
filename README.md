<!-- <div -->
  <h1 align="center">🟩🟩⬛🟩⬛</h1>
<!-- </div> -->

# My daily Waybar cofigs

It's made base on [**weekly-github-waybar-module**](https://github.com/ad1822/weekly-github-waybar-module) and [**mechabar**](https://github.com/sejjy/mechabar), fetches your **GitHub contribution activity for the current week (Sunday to Today)** using the GitHub GraphQL API and has the desing and adjustments from the original dseing of **mechabar**.

---

## Features

- Pulls real-time contribution data from GitHub's GraphQL API.
- Displays a **7-day contribution heatmap** (Sunday–Saturday layout).
- Uses a **color-coded square** (■) system similar to GitHub's own UI.
- Provides a **detailed tooltip** with:
  - Date-wise contribution breakdown.
  - Total contributions in the week.

- shows de defalt desing of **mechabar** with some changes
  - shows the ssd of the wifi and with a click shows the ip address
  - conserve the menu wifi next the name of the module
  - has a power profiles selector next to the power button
  - the clock shows the seconds pass
 
---

## Color Levels

#### Dark Theme (By Default, If no argv passed)
| Contributions | Color Hex  | Meaning            |
|---------------|------------|--------------------|
| 0             | `#161b22`  | No contributions   |
| 1–3           | `#0e4429`  | Low activity       |
| 4–6           | `#006d32`  | Moderate activity  |
| 7–9           | `#26a641`  | High activity      |
| 10+           | `#39d353`  | Very high activity |


#### Light Theme
| Contributions | Color Hex  | Meaning            |
|---------------|------------|--------------------|
| 0             | `#ebedf0`  | No contributions   |
| 1–3           | `#9be9a8`  | Low activity       |
| 4–6           | `#40c463`  | Moderate activity  |
| 7–9           | `#30a14e`  | High activity      |
| 10+           | `#216e39`  | Very high activity |


---

## 1. Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Creador270/Daily_waybar.git ~/.config/waybar/
cd ~/.config/waybar/
````

---

### 2. GitHub Authentication

To make this module work, you need to provide:

* Your **GitHub username**
* A **Fine-Grained Personal Access Token (PAT)**

  * Scope: `Repository access → All repositories`
  * Minimum required permissions for reading contribution data

➡ **Generate your token here:**
[https://github.com/settings/personal-access-tokens/new](https://github.com/settings/personal-access-tokens/new)

---

### 3. Create `.env` File

Inside the project directory, create a `.env` file with the following content:

```env
GITHUB_USERNAME=your_github_username
GITHUB_PAT=ghp_yourGeneratedTokenHere
```
---

### 4. Install Python Dependencies

```bash
pip install -r requests datetime json OrderedDict dotenv
```
> Requires Python 3.7 or higher.
> Dependencies: `requests`, `python-dotenv`, `json`, `datetime`, `OrderedDict`

---
> Ensure the script is executable:
>
> ```bash
> chmod +x ~/.config/waybar/scripts/weekly_commits
> ```

👉 Check out the original proyects: [**weekly-github-waybar-module**](https://github.com/ad1822/weekly-github-waybar-module) and [**mechabar**](https://github.com/sejjy/mechabar)
I hope you like it and gieve some fidback in case errors!
