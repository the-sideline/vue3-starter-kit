# Vue 3 Starter Kit

A modern, opinionated Vue 3 + Vite + TypeScript starter project with Pinia, Vue Router, ESLint, Prettier, and built-in localization (i18n) support.

## 🚀 Features
- **Vue 3** with Composition API
- **TypeScript**
- **Vite** for lightning-fast development
- **Pinia** for state management
- **Vue Router** (history mode)
- **vue-i18n@9** for localization (English & Dutch included)
- **ESLint** & **Prettier** for code quality
- **Beautiful, responsive UI components**

## 📁 Folder Structure
```
src/
├── assets/               # Static assets (images, fonts, icons)
├── components/           # Reusable UI components
│   ├── base/             # Base components (e.g. BaseButton, LanguageSwitcher)
│   └── icons/            # Icon components
├── composables/          # Reusable logic (Composition API)
├── constants/            # Global constants/enums
├── directives/           # Custom Vue directives
├── layouts/              # App layout components
├── locales/              # i18n translation files (en.json, nl.json)
├── middleware/           # Route guards and middleware
├── pages/                # Route-level components (Home, About, Welcome)
├── plugins/              # Plugins (e.g. i18n setup)
├── router/               # Router setup
├── services/             # API calls and external services
├── store/                # Pinia stores
├── types/                # TypeScript types/interfaces
├── utils/                # Helper functions
├── views/                # Alternative to pages (some teams prefer this)
├── App.vue               # Root component
└── main.ts               # App entry point
```

### 📋 Folder Purpose Guide
- **`assets/`** - Static files like images, fonts, and icons
- **`components/`** - Reusable Vue components
  - **`base/`** - Primitive/base components (buttons, inputs, etc.)
  - **`icons/`** - SVG icon components
- **`composables/`** - Vue 3 Composition API reusable logic
- **`constants/`** - Application-wide constants and configuration
- **`directives/`** - Custom Vue directives for DOM manipulation
- **`layouts/`** - Page layout components (header, footer, sidebar)
- **`locales/`** - Internationalization translation files
- **`middleware/`** - Route guards and navigation middleware
- **`pages/`** - Route-level page components
- **`plugins/`** - Vue plugin configurations
- **`router/`** - Vue Router configuration and routes
- **`services/`** - API calls and external service integrations
- **`store/`** - Pinia state management stores
- **`types/`** - TypeScript type definitions and interfaces
- **`utils/`** - Pure utility functions and helpers
- **`views/`** - Alternative to pages (some teams prefer this naming)

## 🛠️ Getting Started

```bash
npm install
npm run dev
```

- Visit [http://localhost:5173](http://localhost:5173) to view the app.

## 🌐 Localization (i18n)
- All translations are in `src/locales/en.json` and `src/locales/nl.json`.
- Use the language switcher in the header to change languages instantly.
- To add a new language:
  1. Add a new JSON file in `src/locales/` (e.g. `fr.json`)
  2. Update `src/plugins/i18n.ts` to import and register the new language
  3. Add it to the language switcher in `LanguageSwitcher.vue`

## 🧩 Extending the Starter Kit
- **Add new pages:** Create a `.vue` file in `src/pages/` and add a route in `src/router/routes.ts`.
- **Add new components:** Place them in `src/components/` or `src/components/base/` for base UI elements.
- **Add new stores:** Create a new file in `src/store/` using Pinia.
- **Add new translations:** Update the relevant JSON files in `src/locales/`.
- **Add new composables:** Create reusable logic in `src/composables/`.
- **Add new utilities:** Add helper functions in `src/utils/`.
- **Add new types:** Define TypeScript interfaces in `src/types/`.
- **Add new constants:** Add application constants in `src/constants/`.
- **Add new services:** Create API calls in `src/services/`.
- **Add new middleware:** Create route guards in `src/middleware/`.
- **Add new directives:** Create custom Vue directives in `src/directives/`.
- **Add new layouts:** Create layout components in `src/layouts/`.

## 🧹 Linting & Formatting
```bash
npm run lint      # Lint code with ESLint
npm run format    # Format code with Prettier
```

## 💡 Recommended IDE Setup
- [VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (disable Vetur)

## 👥 Maintainers / Contact

- **Rahat Ali** – [rahat@sideline.agency](mailto:rahat@sideline.agency)
- **Mohsin Khan** – [mohsin@sideline.agency](mailto:mohsin@sideline.agency)

Feel free to reach out with questions, suggestions, or contributions!

---

Happy coding! 🎉
