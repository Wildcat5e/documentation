# Instructions

## WPILib

Follow instuctions in the [WPILib docs](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/wpilib-setup.html).

### Advanced Setup

If you're setting up WPILib on your personal Linux PC then you could use your existing VS Code or VS Codium installation. Just install WPILib and select everything and then select "Skip and don’t use VS Code." Then you'll need to install the WPILib extension from the extensions marketplace built into VS Code or manually install the extension (likely named `vscode-wpilib-XXXX-`) from the `/home/yourname/wpilib/year/vsCodeExtensions/` directory in the case of VS Codium. (DO NOT use the outdated VS Codium extension.)

## Formatter and VS Code Settings

### Formatter

If you set up a custom style file for formatting, if it is its own file in `.vscode/` it'll be ignored by default. Edit your `.gitignore` file and remove/comment out the line that looks like this:

```json
### VisualStudioCode ###
.vscode/*
```

### Extensions

Right CLick extensions and hit "Add to Workspace Recommendations" and it'll add the extension ID to `.vscode/extensions.json` to easily reinstall.

### Settings

If you change VS Code settings that you want anyone editing the code to have applied (such as format on save and 4 space indent), make sure you select Workspace at the top of VS Code settings.

## VisualVM

Follow the [WPILib docs](https://docs.wpilib.org/en/stable/docs/software/advanced-gradlerio/profiling-with-visualvm.html) but take note of the information below:

[Download VisualVM](https://visualvm.github.io/download.html) and put it somewhere that you'll continue to use it. On Linux, you can put a softlink to the executable in `/home/yourname/.local/bin/` and not worry about Java SDK path if the SDK is installed globally (like Debian/Ubuntu apt package manager). On Windows you'll have to specify the SDK path.

### Windows VisualVM command

(only applies to driver station as of 2026)

```sh
."C:\Users\driver\Documents\visualvm_22\bin\visualvm" --jdkhome "C:\Users\Public\wpilib\2025\jdk"
```
