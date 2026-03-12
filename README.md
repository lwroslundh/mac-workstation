# 🚀 Apple M5 Pro Workstation

An automated, opinionated macOS setup script (using Homebrew) specifically tailored for Apple Silicon (M-series) Macs. This setup is optimized for **C# / .NET 10 development**, building **local RAG pipelines**, and running **local LLMs** efficiently.

Built with performance in mind: No heavy Docker Desktop (uses OrbStack instead), no sluggish Node managers (uses `fnm`), and zero bloatware.

## 🛠️ The Stack

### Core Development
* **.NET SDK:** Ready for .NET 10 and Semantic Kernel.
* **IDEs:** JetBrains Toolbox (for Rider) & Visual Studio Code.
* **Database Management:** DBeaver Community Edition.
* **API Testing:** Postman.

### Local AI & Containers
* **Ollama:** For running local LLMs natively on Apple Silicon.
* **OrbStack:** A lightning-fast, lightweight alternative to Docker Desktop. Perfect for spinning up PostgreSQL/pgvector containers.

### CLI & Utilities
* **Terminal:** iTerm2 + Zsh (with autosuggestions & syntax highlighting).
* **Node Management:** `fnm` (Fast Node Manager) + `pnpm`.
* **Productivity:** Raycast (Spotlight replacement), Bitwarden, GitHub CLI.
* **Font:** JetBrains Mono Nerd Font (for those perfect IDE ligatures).

---

## ⚡ Installation Guide

Got a fresh Mac? Follow these steps to transform it into a dev machine in 10 minutes.

### 1. Install Homebrew
Open your terminal and run the official Homebrew installation script:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 2. Download the Brewfile
Instead of worrying about Git credentials on a fresh machine, just download the raw configuration file directly:

```bash
mkdir ~/.mac-setup && cd ~/.mac-setup
curl -O https://raw.githubusercontent.com/lwroslundh/mac-workstation/main/brew
```

### 3. Run the Brewfile
Let Homebrew download and install everything automatically:

```bash
brew bundle
```

### 4. Post-Installation: Set up Node.js via FNM
Once the Brewfile is finished, install your preferred Node.js version (e.g., version 22) and set it as default:

```bash
fnm install 22
fnm default 22
```

You are now fully set up and ready to code. Enjoy! ☕️
