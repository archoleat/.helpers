# Helpers

A repository with configurations and settings for various development tools.

## Structure

### VSCode (`vscode/`)

Configuration files for Visual Studio Code:

- **`settings.json`** — main editor settings (formatting, indentation, extensions)
- **`launch.json`** — configurations for running and debugging projects
- **`extensions.json`** — recommended extensions for the project

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

Review `git/.gitconfig` and apply only the settings you need to your existing
`~/.gitconfig`. Do not replace your configuration: the template includes a sample
identity, and your current file may contain credentials, includes, or aliases.
Keep HTTPS certificate verification enabled (Git's default).

The global ignore file is also a template. Merge the entries you need into your
existing ignore file; keep project-specific policies in each repository.
After reviewing the file, enable it with:

```bash
git config --global core.excludesfile ~/.gitignore_global
```

### Applying GitHub Rulesets

1. Go to your repository on GitHub
2. Settings → Rules → New branch ruleset / New tag ruleset
3. Upload the corresponding JSON file from the `rulesets/` folder

## Notes

- All configurations can be customized for your needs
- When updating your system, it's recommended to check configuration compatibility
- Make sure you have all necessary extensions installed for VSCode
