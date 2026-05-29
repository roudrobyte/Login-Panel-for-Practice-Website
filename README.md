# Login-Panel-for-Practice-Website
Practice project: a responsive login form with animated floating labels, dark theme, and client‑side demo validation. Perfect for learning CSS transitions and form styling.

# Login Panel – Practice Website

A modern, dark-themed login form with **floating labels** (CSS‑only) and optional client‑side validation. Perfect for practicing HTML/CSS layout, transitions, and basic JavaScript interactivity.


## 🚀 Features

- **Floating label animation** – moves up when input is focused or non‑empty (using `:valid` with `required`).
- **Fully responsive** – centered flex layout, works on desktop and mobile.
- **Dark aesthetic** – deep background (`#0d0d0d`) with subtle borders and hover effects.
- **Login button** – styled with smooth hover transition and lift effect.
- **Optional JavaScript** – simple demo validation that checks for empty fields.


> No external dependencies – everything is inline in a single HTML file.

## 🔧 How to Run

1. **Clone or download** the `index.html` file.
2. **Double‑click** to open in any modern browser (Chrome, Firefox, Edge, etc.).
3. Or use a local dev server (e.g., `npx serve .`).

## 📝 Usage

1. Enter a **surname** and **password**.
2. Click the **Login** button.
   - Without JavaScript: button does nothing (visual only).
   - With JavaScript (included in the script block): shows a demo success/error message.
3. The floating labels stay up once you start typing.

## 🎨 Customization

- **Colors** – change `#0d0d0d` (background), `#010031` (label background), or border colors in the `<style>` section.
- **Input width** – modify `width: 360px` in `.input-group input` and `.login-btn`.
- **Transition speed** – adjust `transition: .5s` for the label.

## 💻 JavaScript (Optional)

If you want to add real form handling, replace the `alert` demo with a `fetch` call to your backend. The current script:

```javascript
document.getElementById('loginBtn').addEventListener('click', () => {
    const surname = document.getElementById('surname').value;
    const password = document.getElementById('password').value;
    if (!surname || !password) {
        alert('Please fill both fields');
    } else {
        alert(`Welcome, ${surname}!`);
    }
});
