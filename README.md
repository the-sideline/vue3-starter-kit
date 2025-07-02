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
│   └── base/             # Base components (e.g. BaseButton, LanguageSwitcher)
├── composables/          # Reusable logic (Composition API)
├── constants/            # Global constants/enums
├── layouts/              # App layout components
├── locales/              # i18n translation files (en.json, nl.json)
├── pages/                # Route-level components (Home, About, Welcome)
├── plugins/              # Plugins (e.g. i18n setup)
├── router/               # Router setup
├── store/                # Pinia stores
├── types/                # TypeScript types/interfaces
├── utils/                # Helper functions
├── App.vue               # Root component
├── main.ts               # App entry point
└── shims-vue.d.ts        # Vue file type support for TS
```

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
