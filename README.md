# 🚀 Minimal Academic Homepage Template

This is a minimalist academic homepage template based on HTML/CSS, specifically designed for researchers, students, and scholars. It features a responsive design, dark mode support, elegant typography, and is easy to customize.

> [!TIP]
> If you find this template helpful, feel free to give it a Star 🌟!

---

## ✨ Features

* **Minimalist Design**: Focuses on content by removing redundancy, inspired by the visual style of [Claude.ai](https://claude.ai).
* **Responsive Layout**: Displays beautifully across mobile, tablet, and desktop devices.
* **Dark Mode**: Supports manual switching and automatic syncing with system settings.
* **Academic-Friendly**: Built-in sections for educational background, research experience, project showcases, publication lists (supporting icon links), and awards.
* **Easy Deployment**: A pure static page with no build steps required; can be hosted directly on GitHub Pages.

---

## 🛠️ Quick Start: Customize Your Homepage

You can quickly create your own homepage by following these steps:

### 1. Fork this Repository
Click the **Fork** button in the top right corner of the repository to clone the code to your own GitHub account.

### 2. Modify Personal Information
Open the `index.html` file and search for/replace the following content:
* **Basic Information**: Name, email, and avatar path.
* **Social Links**: Modify links in the `social-icons` section (GitHub, Google Scholar, LinkedIn, etc.).
* **Section Content**:
    * `About Me`: A brief self-introduction.
    * `Education`: Replace school logos and degree information.
    * `Experience`: Add your internships or research experience.
    * `Publications`: Add your papers following the provided format.
    * `Awards`: List your honors.

### 3. Replace Resource Files
* **Avatar**: Place your profile picture in `assets/img/` and name it `avatar.png`.
* **Logos**: Place school or institutional logos in `assets/img/`.
* **Resume**: Place your PDF resume in `assets/cv/`.

### 4. Enable GitHub Pages
In your repository settings:
1.  Go to `Settings` -> `Pages`.
2.  Under `Build and deployment`, select `Deploy from a branch`.
3.  Select the `main` branch and `/ (root)` folder, then click `Save`.
4.  After a few minutes, your homepage will be live at `https://<your-username>.github.io`.

---

## 🎨 Advanced Customization

### Modify Theme Colors
If you want to change the theme colors (such as link colors or accent colors), you can edit `assets/css/theme-claude.css`.

### Visitor Map
The homepage integrates [ClustrMaps](https://clustrmaps.com/). You can register on their official website to get your own map ID, then replace the relevant parameters in the `updateMap` function within `index.html`.

---

## 📄 License
This project is open-sourced under the [MIT License](LICENSE.md).

---
Maintained by [Yuheng Yang](https://github.com/wzsyyh).