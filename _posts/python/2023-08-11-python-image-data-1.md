---
title: "Image Data(1): MacBook Pro, M1, Initial Setup"
author: Dachan Kyong
date: 2023-08-11 12:00:00 +0900
categories: [Python, Image Data]
tags: [python]
collection: blog
render_with_liquid: false
---

## Author's Development Environment
- **Device**: Macbook Pro, 2021
- **Chip**: Apple M1 Pro
- **Version**: macOS Monterey, 12.2.1

## **Development Environment Setup**
- [Visual Studio Code](https://code.visualstudio.com/download): Download Apple silicon & download Python extensions(v2023.8.0)

## Installation, on August 11, 2023

### Step 1: Homebrew
Go to <https://brew.sh/>, copy link under "Install Homebrew", and paste that in a macOS Terminal:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh) // "This will require your password."
```

To check installation status, we can type `brew help`, but it will show an error on M1 Mac:
```bash
zsh: command not found: brew
```

To fix the issue we need to type, and then to check status type `brew help`:
```bash
eval $(/opt/homebrew/bin/brew shellenv)

brew help
```

Then update brew for sure in a macOS Terminal:

```bash
brew update // "this will update brew."
```

### Step 2: Python 3
`Python` is pre-installed on macOS, but you can install the latest version from the official website or through brew if needed.

You can check the version of your current Python installation using the following command:
```bash
python --version // "This will show the Python version message: Python 2.*.*."
```

```bash
python3 --version // "This will show the Python version message: Python 3.*.*."
```

My current version is Python 3.8.9. In the next post, I will explain a simple method for extracting image data.



