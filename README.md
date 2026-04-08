# Helpers

A repository with configurations and settings for various development tools.

## Structure

### VSCode (`vscode/`)

Configuration files for Visual Studio Code:

- **`settings.json`** — main editor settings (formatting, indentation, extensions)
- **`launch.json`** — configurations for running and debugging projects
- **`extensions.json`** — recommended extensions for the project

### Git Bash (`bash/`)

Themes and configurations for Git Bash terminal:

- **`.minttyrc`** — configuration for dark theme
- **`.minttyrc (light)`** — configuration for light theme

### Git (`git/`)

Global Git settings:

- **`.gitconfig`** — Git user configuration (name, email, aliases)
- **`.gitignore_global`** — global exclusion file for all repositories

### GitHub Rulesets (`rulesets/`)

Protection rules for GitHub:

- **`Branch Protection.json`** — branch protection rules
- **`Tag Protection.json`** — tag protection rules

## Usage

### Installing VSCode Configuration

Copy files from the `vscode/` folder to your VS Code user directory:

- Windows: `%APPDATA%\Code\User\`
- macOS: `~/Library/Application Support/Code/User/`
- Linux: `~/.config/Code/User/`

### Installing Git Configuration

```bash
# Copy global gitconfig
cp git/.gitconfig ~/.gitconfig

# Copy global gitignore
cp git/.gitignore_global ~/.gitignore_global

# Enable gitignore in Git configuration
git config --global core.excludesfile ~/.gitignore_global
```

### Installing Git Bash Theme

Copy the required `.minttyrc` file to your home directory:

```bash
cp bash/.minttyrc ~/ # for dark theme
cp bash/.minttyrc\ \(light\) ~/.minttyrc # for light theme
```

### Applying GitHub Rulesets

1. Go to your repository on GitHub
2. Settings → Rules → New branch ruleset / New tag ruleset
3. Upload the corresponding JSON file from the `rulesets/` folder

## Notes

- All configurations can be customized for your needs
- When updating your system, it's recommended to check configuration compatibility
- Make sure you have all necessary extensions installed for VSCode
