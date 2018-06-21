# atom-settings

## список полезный плагинов
```js

// автоформатирование сжатых файлов
atom-beautify

// помогает писать jsdoc комментарии
docblockr

// настройки форматирования в рамках проекта
editorconfig

// иконки для файлов в TreeView
file-icons

// настройка подсветки синтаксиса для кастомных расширений файлов
file-types

// помогает находит очепятки, 
// выделяешь имя переменной или функции 
// и подсвечиваются повторения в рамках файла
highlight-selected

// runtime валидация ситаксиса js, 
// строки с ошибками подсвечивает красным
linter
// в настройках нужно указать use global eslint
linter-eslint

// помогает писать .md файлы
language-markdown
markdown-preview-plus

// помогает находить изменения в файле
git-diff-details
line-diff-details

// мини карта кода
minimap

// терминал (cmd) прямо в atom
platform-ide-terminal

// помогает писать регулярки
// что-то типо https://www.debuggex.com
regex-railroad-diagram

// специфично для проекта логось, переключение регистров
upper-case-toggle

// ничего полезного, просто прикольный плагин
activate-power-mode
```
## keymap.cson
```coffee
'atom-workspace atom-text-editor:not([mini])':
    'ctrl-d': 'editor:duplicate-lines'
'.platform-win32 atom-text-editor':
    'ctrl-b': 'find-and-replace:toggle-whole-word-option'
'atom-text-editor':
    'ctrl-u': 'upper-case:toggle'
'.platform-win32':
    'ctrl-o': 'fuzzy-finder:toggle-file-finder'
```

## config.cson
```coffee

"*":
  ...
  // у atom по умолчанию табы как 2 пробела
  editor:
    fontSize: 12
    invisibles: {}
    tabLength: 4
  ...
  // настройка для file-types
  "file-types":
    ".html": "text.html.jsp"
  ...
  whitespace:
    removeTrailingWhitespace: false
  ...
```
## .eslintrc.json
```js
{  
    "extends": "eslint:recommended",
    "rules": {  
        "quotes": ["error", "double"],
        "semi": ["error", "always"],
        "no-console": "off",
        "comma-dangle": ["error", "never"],
        "one-var": "off"
    },
    "parserOptions": {
        "ecmaVersion": 8
    },
    "env": {
        "browser": true,
        "amd": true
    },
    "globals": {
        "system": true,
        "console": true
    }
}
```
