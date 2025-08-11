# Prestige XP for MyBB

**Prestige XP** is a MyBB plugin that adds a fully configurable XP and leveling system to your forum.  
Members earn XP for creating threads and posts, level up as they reach milestones, and display their progress directly on their postbit and profile.

---

## ✨ Features

- **Configurable XP rewards** for posts and threads (via ACP settings)
- **Customizable level system** – set XP required per level and total number of levels
- **Automatic level calculation** with prestige-style progression
- **XP progress bar** on profiles (easily editable template)
- **Level display on postbit** (`Level: X`) — placement can be changed via template editing
- **No theme lock-in** — HTML/CSS templates can be customized to match any MyBB theme

---

## 📥 Installation

1. **Upload Files**  
   - Upload `prestige_xp.php` to `inc/plugins/`

2. **Activate the Plugin**  
   - In your MyBB ACP, go to **Configuration → Plugins**
   - Click **Install & Activate** next to *Prestige XP*

3. **Configure Settings**  
   - Go to **Configuration → Settings → Prestige XP**
   - Set:
     - XP per post
     - XP per thread
     - Number of levels
     - XP required per level

4. **Templates**  
   - The plugin adds two templates:
     - `prestige_xp_postbit` — controls how the level is shown on postbit
     - `prestige_xp_profile` — controls profile level display + XP bar
   - Edit these in **ACP → Templates** to match your theme.

---

## 🖥 Usage

- Members will **start at Level 0** with 0 XP.
- When they post or create threads, XP will be added automatically.
- Levels are calculated based on the XP thresholds you set in the settings.
- The XP bar on the profile page shows **progress toward the next level**.

---

## 🎨 Template Examples

### 1. Basic Level Display (Postbit)
```html
<br />
<span class="smalltext prestige-xp-level" data-level="{$prestige_level}">
    Level: {$prestige_level}
</span>

With Fontawesome
<br />
<span class="smalltext prestige-xp-level" data-level="{$prestige_level}">
    <i class="fa-solid fa-trophy" style="color: gold; margin-right: 6px;"></i>
    Level: {$prestige_level}
</span>
```


## 🛠 Editing

All front-end HTML is handled via MyBB templates, so no PHP editing is required for visual changes.
If you want to change how XP is awarded (e.g., different values for different forums), you can modify the awarding logic inside prestige_xp.php.

