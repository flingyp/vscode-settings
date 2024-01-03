# VSCode Settings

## Settings

```json
{
  // Editor
  "editor.fontSize": 14,
  "editor.formatOnSave": true,
  "editor.stickyScroll.enabled": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.fontFamily": "Input Mono, Fira Code, monospace",

  // Window
  "window.zoomLevel": -1,

  // Workbench
  "workbench.colorTheme": "Vitesse Dark",
  "workbench.preferredLightColorTheme": "Vitesse Light",
  "workbench.preferredDarkColorTheme": "Vitesse Dark",
  "workbench.iconTheme": "file-icons",

  // Prettier
  "prettier.enable": true,

  // ESLint
  "eslint.enable": true,
  "eslint.format.enable": true,
  "eslint.experimental.useFlatConfig": true,
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

  // Stylelint
  "stylelint.enable": true,
  "stylelint.validate": ["css", "less", "scss", "sass", "vue", "postcss"],

  // Git
  "git.confirmSync": false,

  // Plugin: TODO Highlight
  "todohighlight.isEnable": true,
  "todohighlight.defaultStyle": {
    "color": "#fff"
  },
  "todohighlight.keywords": [
    {
      "text": "TODO:",
      "backgroundColor": "#fbc02d"
    },
    {
      "text": "FIX:",
      "backgroundColor": "#1976d2"
    },
    {
      "text": "CHORE:",
      "backgroundColor": "#388e3c"
    },
    {
      "text": "HACK:",
      "backgroundColor": "#d32f2f"
    }
  ],

  // Plugin: Tabnine
  "tabnine.experimentalAutoImports": true
}
```

## Global Code Snippets

```json
{
  "import-module": {
    "scope": "javascript,typescript,vue",
    "prefix": "im",
    "body": ["import { $2 } from $1;"],
    "description": "Import a module"
  },
  "export-all": {
    "scope": "javascript,typescript",
    "prefix": "ex",
    "body": ["export * from '$1';"],
    "description": "Export a module"
  },
  "vue-script-setup": {
    "scope": "vue",
    "prefix": "vu",
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
  "vue-watch-effect": {
    "scope": "javascript,typescript,vue",
    "prefix": "watchE",
    "body": ["watchEffect(() => {", "  $1", "})"]
  }
}
```

## Plugins
