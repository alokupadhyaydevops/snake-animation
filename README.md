# 🐍 GitHub Contribution Snake Animation

A professional GitHub Actions automation that generates an animated snake eating your GitHub contribution graph. Perfect for adding visual appeal to your GitHub profile README.

![Snake Animation](https://raw.githubusercontent.com/alokupadhyaydevops/snake-animation/output/github-contribution-grid-snake-dark.svg)

## 📋 Purpose

This project automatically generates a dynamic snake animation that visualizes your GitHub contribution history. The snake "eats" your contributions, creating an engaging visual representation that's perfect for:

- Showcasing your GitHub activity on your profile
- Demonstrating your commitment to open source
- Adding professional visual appeal to your profile README
- Impressing recruiters and potential collaborators

## ✨ Features

- **🌙 Dark Mode**: Optimized dark theme that looks professional on GitHub
- **⚡ Automated**: Runs daily via GitHub Actions
- **📦 Zero Configuration**: Works out of the box with minimal setup
- **🚀 GitHub Pages**: Automatically deploys to a dedicated output branch
- **🎨 Two Variants**: Light and dark mode SVG files generated

## 🚀 Setup Instructions

### 1. Fork or Use This Repository

1. Fork this repository or use it as a template
2. Enable GitHub Actions in your repository settings (Settings → Actions → General)

### 2. Configure GitHub Pages

1. Go to **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Choose the **output** branch and **/ (root)** folder
4. Click **Save**

### 3. Run the Workflow

You can trigger the workflow in three ways:

- **Automatic**: The workflow runs daily at midnight UTC
- **Manual**: Go to **Actions** tab → **Generate Snake Animation** → **Run workflow**
- **On Push**: Automatically runs when you push to the main branch

### 4. Add to Your Profile README

Once the workflow runs successfully, add this to your profile README:

```markdown
![Snake Animation](https://raw.githubusercontent.com/YOUR_USERNAME/snake-animation/output/github-contribution-grid-snake-dark.svg)
```

Replace `YOUR_USERNAME` with your GitHub username.

## 📖 Usage

### Using the Dark Mode Animation (Recommended)

```markdown
![Snake Animation](https://raw.githubusercontent.com/YOUR_USERNAME/snake-animation/output/github-contribution-grid-snake-dark.svg)
```

### Using the Light Mode Animation

```markdown
![Snake Animation](https://raw.githubusercontent.com/YOUR_USERNAME/snake-animation/output/github-contribution-grid-snake.svg)
```

### HTML Alternative (with better control)

```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/YOUR_USERNAME/snake-animation/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/YOUR_USERNAME/snake-animation/output/github-contribution-grid-snake.svg">
  <img alt="GitHub Contribution Snake" src="https://raw.githubusercontent.com/YOUR_USERNAME/snake-animation/output/github-contribution-grid-snake.svg">
</picture>
```

## 🔧 Configuration

The workflow is located at `.github/workflows/snake.yml`. Key configurations:

- **Schedule**: Runs daily at midnight UTC (customizable via cron expression)
- **Branch**: Deploys to `output` branch (can be changed to `gh-pages`)
- **Theme**: Dark mode palette by default (configurable in workflow file)

### Customizing the Schedule

Edit the cron expression in `.github/workflows/snake.yml`:

```yaml
schedule:
  - cron: "0 0 * * *"  # Runs at midnight UTC daily
```

## 📁 Project Structure

```
snake-animation/
├── .github/
│   └── workflows/
│       └── snake.yml          # GitHub Actions workflow
├── README.md                   # This file
└── output/                     # Generated files (auto-created)
    ├── github-contribution-grid-snake.svg
    └── github-contribution-grid-snake-dark.svg
```

## 🛠️ Technical Details

- **Action Used**: [Platane/snk](https://github.com/Platane/snk) v3
- **Deployment**: [crazy-max/ghaction-github-pages](https://github.com/crazy-max/ghaction-github-pages) v3
- **Runner**: Ubuntu Latest
- **Permissions**: Contents write for branch deployment

## 🤝 Contributing

This is a personal profile project, but feel free to fork and customize for your own use!

## 📝 License

This project is open source and available under the MIT License.

## 🔗 Links

- [My GitHub Profile](https://github.com/alokupadhyaydevops)
- [Platane/snk Action](https://github.com/Platane/snk)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)

---

<div align="center">
  <strong>Made with ❤️ for showcasing GitHub contributions</strong>
</div>