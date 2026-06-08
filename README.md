# CSP451 CheckPoint 1 — Version Control & GitHub

A small static website used to demonstrate Git and GitHub version-control practices.

## Description

This project demonstrates core Git and GitHub workflows through a minimal static
website. It contains a landing page and an "About Me" page built with **HTML5**,
styled with **CSS3**, and made interactive with vanilla **JavaScript**. The
repository showcases a clean commit history using Conventional Commits, a
feature-branch workflow, pull requests with code review, and professional
open-source documentation.

**Technologies used:** HTML5, CSS3, JavaScript (ES6), Git, and GitHub.

## Installation Instructions

### Prerequisites
- [Git](https://git-scm.com/) installed on your system
- A modern web browser (Chrome, Firefox, Edge, or Safari)
- A GitHub account (to clone over HTTPS or SSH)

### Steps
1. Clone the repository (replace `<your-username>` with your GitHub username):
   ```bash
   git clone https://github.com/jahidul47/CSP451-CheckPoint1-Mdjahidulislam.git
   ```
2. Move into the project folder:
   ```bash
   cd CSP451-CheckPoint1-MdjahidulIslam
   ```
3. Open `index.html` in your web browser — double-click the file, or use the
   **Live Server** extension in VS Code.

## Usage

### Viewing the project
Open `index.html` to see the welcome page, then follow the navigation link to the
**About Me** page. Open your browser's developer console (press `F12`) to see the
messages printed by `script.js`.

### Useful Git commands
```bash
# View the commit history as a graph
git log --oneline --graph --all --decorate

# See uncommitted changes
git diff

# Check the configured remotes
git remote -v
```

## Contributing

Contributions follow a **feature-branch workflow**:

1. Create a feature branch off `main`:
   ```bash
   git checkout -b feature/your-feature-name
   ```
2. Commit using the **Conventional Commits** convention:
   - `feat:` — a new feature
   - `fix:` — a bug fix
   - `docs:` — documentation only
   - `style:` — formatting, no logic change
   - `refactor:` — code change that neither fixes a bug nor adds a feature
3. Push your branch and open a Pull Request:
   ```bash
   git push -u origin feature/your-feature-name
   ```
4. Request a review, address any feedback, then merge with a merge commit and delete
   the branch.

## Project Structure
```
csp451-checkpoint1/
├── index.html                  # Landing page
├── about.html                  # About Me page (added via feature branch)
├── style.css                   # Styles: reset, layout, typography
├── script.js                   # Console output + a function definition and call
├── README.md                   # This file
├── VERSION_CONTROL_WRITEUP.md  # Part 1 conceptual write-up
├── .gitignore                  # Ignored files (OS, editor, logs, deps, build)
└── LICENSE                     # MIT License
```

## License

This project is licensed under the **MIT License** and was created for educational
purposes as part of CSP451 coursework at Seneca College.

```
MIT License

Copyright (c) 2026 [Your Full Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

See the [LICENSE](LICENSE) file for the full text.
