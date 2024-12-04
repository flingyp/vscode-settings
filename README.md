# VSCode Settings

## ⛏️ Settings

`.vscode/settings.json`

```json
{
  // Window
  "window.zoomLevel": -1,

  // Editor
  "editor.fontSize": 14,
  "editor.formatOnSave": true,
  "editor.stickyScroll.enabled": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.fontFamily": "Input Mono, Fira Code, monospace",
  "editor.smoothScrolling": true,
  "editor.cursorSmoothCaretAnimation": "on",

  // Workbench
  "workbench.colorTheme": "Vitesse Dark",
  "workbench.iconTheme": "file-icons",
  "workbench.tree.indent": 10,
  "workbench.list.smoothScrolling": true,
  "workbench.editorAssociations": {
    "git-rebase-todo": "gitlens.rebase"
  },

  // Terminal
  "terminal.integrated.smoothScrolling": true,

  // Files
  "files.associations": {
    "*.nvue": "vue",
    "*.uvue": "vue",
    "*.uts": "typescript"
  },

  // Unknown words
  "cSpell.userWords": [
    "animationfinish",
    "chooseavatar",
    "esbenp",
    "Fira",
    "flingyp",
    "statechanged",
    "Stylelint",
    "Tabnine",
    "tailwindcss",
    "todohighlight",
    "uniapp",
    "uvicon",
    "Vitesse"
  ],

  // Git
  "git.confirmSync": false,
  "git.autofetch": true,
  "git.ignoreRebaseWarning": true,

  // JavaScript
  "javascript.updateImportsOnFileMove.enabled": "always",

  // Plugin: Prettier
  "prettier.enable": true,

  // Plugin: ESLint
  "eslint.enable": true,
  "eslint.format.enable": true,
  "eslint.useFlatConfig": true,
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact",
    "jsx",
    "tsx",
    "vue",
    "html",
    "markdown",
    "json",
    "jsonc",
    "json5",
    "yaml"
  ],

  // Plugin: Stylelint
  "stylelint.enable": true,
  "stylelint.validate": ["css", "less", "scss", "sass", "vue", "postcss"],

  // Plugin: TailwindCSS
  "tailwindCSS.validate": true,
  "tailwindCSS.rootFontSize": 16,
  "tailwindCSS.includeLanguages": {
    "plaintext": "html"
  },

  // Plugin: Black Formatter (Code Formatting for Python files)
  "[python]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "ms-python.black-formatter"
  },

  // Plugin: CodeGeeX
  "Codegeex.Privacy": true,
  "Codegeex.SidebarUI.LanguagePreference": "中文",
  "Codegeex.EnableExtension": true,
  "Codegeex.Comment.LanguagePreference": "中文",
  "Codegeex.License": "",

  // Plugin: GitLens
  "gitlens.graph.minimap.enabled": false,
  "gitlens.graph.minimap.additionalTypes": ["stashes"],
  "gitlens.views.stashes.files.layout": "tree",
  "gitlens.views.branches.files.layout": "list",
  "gitlens.views.branches.branches.layout": "list",

  // Plugin: TODO Tree
  "todo-tree.highlights.defaultHighlight": {
    "background": "#19be6b",
    "foreground": "#fff",
    "fontStyle": "italic",
    "fontWeight": "bold"
  },
  "todo-tree.general.tags": [
    "BUG",
    "HACK",
    "FIXME",
    "TODO",
    "XXX",
    "CHORE",
    "TIP",
    "[ ]",
    "[x]"
  ]
}
```

## ✒️ Code Snippets

`.vscode/global.code-snippets`

- [Code Snippets Generate Website](https://snippet-generator.app/)

```json
{
  "import-module": {
    "scope": "javascript,typescript,vue",
    "prefix": "im",
    "body": ["import { $2 } from $1;"],
    "description": "Import a module"
  },
  "export-all": {
    "scope": "javascript,typescript,vue",
    "prefix": "ex",
    "body": ["export * from '$1';"],
    "description": "Export a module"
  },
  "vue-script-setup": {
    "scope": "vue",
    "prefix": "vus",
    "body": [
      "<script setup lang=\"ts\">",
      "const props = defineProps<{",
      "  modelValue?: boolean,",
      "}>()",
      "$1",
      "</script>",
      "",
      "<template>",
      "  <div>",
      "    <slot/>",
      "  </div>",
      "</template>"
    ]
  },
  "vue-computed": {
    "scope": "javascript,typescript,vue",
    "prefix": "com",
    "body": ["computed(() => { $1 })"]
  },
  "vue-watch": {
    "scope": "javascript,typescript,vue",
    "prefix": "wat",
    "body": [
      "watch(",
      "  () => $1,",
      "  () => { $2 },",
      "  {",
      "    immediate: true,",
      "  }",
      ");"
    ]
  },
  "vue-watch-effect": {
    "scope": "javascript,typescript,vue",
    "prefix": "watE",
    "body": ["watchEffect(() => {", "  $1", "})"]
  }
}
```

## ⛸️ Plugins

`.vscode/extensions.json`

```json
{
  "recommendations": [
    // VSCode Plugins
    "antfu.theme-vitesse",
    "file-icons.file-icons",

    // Git Plugins
    "eamodio.gitlens",
    "donjayamanne.githistory",
    "GitHub.vscode-pull-request-github",
    "fabiospampinato.vscode-open-in-github",

    // Python Plugins
    "ms-python.python",
    "ms-python.vscode-pylance",
    "ms-python.black-formatter",
    "donjayamanne.python-environment-manager",

    // Frontend Plugins
    "Vue.vscode-typescript-vue-plugin",
    "ZixuanChen.vitest-explorer",
    "antfu.unocss",
    "bradlc.vscode-tailwindcss",
    "stylelint.vscode-stylelint",
    "mrmlnc.vscode-scss",
    "esbenp.prettier-vscode",
    "rvest.vs-code-prettier-eslint",
    "csstools.postcss",
    "xabikos.JavaScriptSnippets",
    "antfu.iconify",
    "afzalsayed96.icones",
    "lokalise.i18n-ally",
    "ecmel.vscode-html-css",
    "dbaeumer.vscode-eslint",
    "rodrigovallades.es7-react-js-snippets",
    "EditorConfig.EditorConfig",
    "formulahendry.auto-rename-tag",
    "steoates.autoimport",
    "rodrigovallades.es7-react-js-snippets",

    // Uniapp Plugins
    "uni-helper.uni-helper-vscode",
    "uni-helper.uni-app-schemas-vscode",
    "uni-helper.uni-app-snippets-vscode",
    "uni-helper.uni-cloud-snippets-vscode",
    "uni-helper.uni-ui-snippets-vscode",
    "mrmaoddxxaa.create-uniapp-view",

    // Other Plugins
    "Perkovec.emoji",
    "redhat.vscode-yaml",
    "kaiyi.qwerty-learner",
    "RichardZhang.quickly-log",
    "christian-kohler.path-intellisense",
    "unifiedjs.vscode-mdx",
    "shd101wyy.markdown-preview-enhanced",
    "ritwickdey.LiveServer",
    "wix.vscode-import-cost",
    "kisstkondoros.vscode-gutter-preview",
    "flingyp.vscode-plugin-hot-news",
    "usernamehw.errorlens",
    "IronGeek.vscode-env",
    "streetsidesoftware.code-spell-checker",
    "mikestead.dotenv",
    "Codeium.codeium",
    "Gruntfuggly.todo-tree",
    "pnp.polacode"
  ]
}
```
