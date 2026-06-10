# CM-XO Website (cmxo.tech)

This repository contains the codebase for the **CM-XO** portfolio website ([cmxo.tech](https://cmxo.tech/)), built using the **Hugo** static site generator and the **Glacier** theme.

## 🚀 How to Run Locally

### Prerequisites

You need to have **Hugo** (Extended version is recommended) installed on your system.

#### macOS (via Homebrew)
```bash
brew install hugo
```

#### Windows (via Chocolatey or Scoop)
```bash
choco install hugo-extended
# OR
scoop install hugo-extended
```

#### Linux (Debian/Ubuntu)
```bash
sudo apt install hugo
```

---

### Running the Development Server

1. Navigate to the `site/` directory:
   ```bash
   cd site
   ```

2. Run the Hugo development server:
   ```bash
   hugo server
   ```
   *Note: If you want to render draft content as well, run:*
   ```bash
   hugo server -D
   ```

3. Open your browser and navigate to:
   ```
   http://localhost:1313/
   ```

---

### 📦 Building for Production

To generate the final optimized static site files:

1. Navigate to the `site/` directory:
   ```bash
   cd site
   ```

2. Run the build command:
   ```bash
   hugo --minify
   ```

3. The generated static files will be placed in the `public/` directory, ready to be deployed to your web host (Netlify, Vercel, Github Pages, etc.).

---

## 📂 Project Structure

* `/content` - Markdown files representing the website pages (Home, About, Services, Blog).
* `/data` - YAML files configuration details for the Glacier page builder.
* `/static` - Assets like images, icons, and logo graphics.
* `/themes` - The Glacier theme resources.
* `config.toml` - Main configuration file for navigation menus, social profiles, and SEO tags.
