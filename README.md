## Create new Quasar webpack project with Quasar-Cli - https://quasar.dev/start/quasar-cli

## And follow vuetiful getting started - https://vuetiful.dev/docs/getting-started

```yarn add @code-coaching/vuetiful```

```yarn add -D tailwindcss postcss autoprefixer prettier-plugin-tailwindcss```

```npx tailwindcss init```

```change tailwind.config.js```

```create prettier.config.js```

```change postcss.config.js```

```change quasar.config.js - only remove app.css, don't need dedupe 'vue' (until to compile this started project...)```

```change App.vue```

## If the project is compiled with 'quasar dev', an error is raised:

```'...\node_modules\@code-coaching\vuetiful\src\styles\variants.css `@layer components` is used but no matching `@tailwind components` directive is present.'```

## Add 'postcss-import': https://github.com/tailwindlabs/tailwindcss/discussions/5934

```yarn add -D postcss-import```

## and include plugin postcss.config.cjs:

```plugins: [ ... require('postcss-import'), ... ]```

## and 'quasar dev' worked...

