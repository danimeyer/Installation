## Install VS Code
https://code.visualstudio.com/
Update settings:
- Type ⌘,
- Scroll down to find "edit in settings.json"
{
    "editor.renderIndentGuides": true,
    "editor.renderWhitespace": "boundary",
    "editor.renderControlCharacters": false,
    "editor.rulers": [80, 100],
    "editor.tabSize": 2,
    "editor.trimAutoWhitespace": false,
    "editor.wordWrap": "on",
    "files.trimTrailingWhitespace": true,
    "files.insertFinalNewline": true,
    "files.associations": {
      ".gitignore": "shellscript"
    },
    "emmet.syntaxProfiles": { "javascript": "jsx" },
    "window.title": "${activeEditorMedium}${separator}${rootName}",
    "workbench.colorCustomizations": {
      "editorWarning.foreground": "#ec0"
    }
  }
- Set up `code .`:
    - Type ⌘ + P
    - Search >Shell command: Install 'code' command in PATH

## Install NodeJS
https://nodejs.org/en/

## Install Homebrow:
https://brew.sh/
- Make sure to follow commands after installation is complete in order to get Homebrew working
    - run code `brew` to test
- Run `brew install zsh` to get current version of zsh shell

## Install Git:
https://git-scm.com/

## Check machine is ready:
- `node -v` should show what version of Node is installed
- `npm -v` should show what version of NPM is installed
- `git --version` should show what version of Git is installed
- `git config --global user.name "{NAME}` to set name for Git
- `git config --global user.email "{EMAIL}` to set email for Git

## Install Prettier:
`sudo npm install --global prettier` // Note that using sudo shouldn't be necessary, google it to learn more
- Type ⌘ + Shift + P and select Extensions: Install Extensions
    - Find Prettier and install
- Create a prettier config file titled .prettierrc.js and enter below code (comments show default styling)
    - ~~~
    module.exports = { printWidth: 80, // 80
      tabWidth: 2, // 2
      useTabs: false, // false
      semi: true, // true
      singleQuote: true, // false
      trailingComma: 'es5', // none | es5 | all
      bracketSpacing: true // true
      jsxBracketSameLine: false // false
      arrowParens: avoid // avoid | always
    };
    ~~~
- Go to VS Code settings and enable Editor: Format on save
- To set Prettier as the default, open a file and type ⌘ + Shift + P and "Format Document" and select Prettier
