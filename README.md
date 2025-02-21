# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default tseslint.config({
  languageOptions: {
    // other options...
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

- Replace `tseslint.configs.recommended` to `tseslint.configs.recommendedTypeChecked` or `tseslint.configs.strictTypeChecked`
- Optionally add `...tseslint.configs.stylisticTypeChecked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and update the config:

```js
// eslint.config.js
import react from 'eslint-plugin-react'

export default tseslint.config({
  // Set the react version
  settings: { react: { version: '18.3' } },
  plugins: {
    // Add the react plugin
    react,
  },
  rules: {
    // other rules...
    // Enable its recommended rules
    ...react.configs.recommended.rules,
    ...react.configs['jsx-runtime'].rules,
  },
})
```
## Bun: The Package Management

### Let's use bun package management
Follow the steps below with the Linux Mint operating system

### First of all, go to the Bun documentation and choose your operating system
https://bun.sh/docs/installation

### Step by step

```
(base) aluno@aluno-caang:~/teads_project$ bun add tailwind @tailwindcss/vite
bun add v1.2.2 (c1708ea6)

installed tailwind@4.0.0
installed @tailwindcss/vite@4.0.7

260 packages installed [19.84s]

Blocked 1 postinstall. Run `bun pm untrusted` for details.
(base) aluno@aluno-caang:~/teads_project$ bun add typescript -d
bun add v1.2.2 (c1708ea6)

installed typescript@5.7.3 with binaries:
 - tsc
 - tsserver

[1.65s] done
(base) aluno@aluno-caang:~/teads_project$ bun add vite -d
bun add v1.2.2 (c1708ea6)

installed vite@6.1.1 with binaries:
 - vite

[13.00ms] done
(base) aluno@aluno-caang:~/teads_project$ ls
bun.lock  node_modules  package.json  README.md  src  tsconfig.json
(base) aluno@aluno-caang:~/teads_project$ bun create vite . --template react-ts
✔ Current directory is not empty. Please choose how to proceed: › Remove existing files and continue

Scaffolding project in /home/aluno/teads_project...

Done. Now run:

  bun install
  bun run dev

(base) aluno@aluno-caang:~/teads_project$ npm install

added 180 packages, and audited 181 packages in 37s

43 packages are looking for funding
  run `npm fund` for details

3 moderate severity vulnerabilities

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.
(base) aluno@aluno-caang:~/teads_project$ tree
Comando 'tree' não encontrado, mas poder ser instalado com:
sudo apt install tree
(base) aluno@aluno-caang:~/teads_project$ bun add tailwind @tailwindcss/vite
bun add v1.2.2 (c1708ea6)
[1.75ms] migrated lockfile from package-lock.json

installed tailwind@4.0.0
installed @tailwindcss/vite@4.0.7

245 packages installed [2.17s]

Blocked 1 postinstall. Run `bun pm untrusted` for details.
(base) aluno@aluno-caang:~/teads_project$ ls
bun.lock          package.json       src                 vite.config.ts
eslint.config.js  package-lock.json  tsconfig.app.json
index.html        public             tsconfig.json
node_modules      README.md          tsconfig.node.json
(base) aluno@aluno-caang:~/teads_project$ npm run dev

> teads_project@0.0.0 dev
> vite


  VITE v6.1.1  ready in 1746 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
  ➜  press h + enter to show help

(base) aluno@aluno-caang:~/teads_project$ bun install
bun install v1.2.2 (c1708ea6)

Checked 439 installs across 484 packages (no changes) [12.00ms]
(base) aluno@aluno-caang:~/teads_project$ bu run dev
bu: comando não encontrado
(base) aluno@aluno-caang:~/teads_project$ bun run dev
$ vite
14:59:35 [vite] (client) Re-optimizing dependencies because lockfile has changed

  VITE v6.1.1  ready in 1052 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
  ➜  press h + enter to show help
```
