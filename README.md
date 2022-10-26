# vue3-pinia-todolist

```sh
yarn
```

### Compiler et recharger à chaud pour le développement

```sh
yarn dev
```

### Compiler et minifier pour la production

```sh
yarn build
```

### Exécutez des tests unitaires avec [Vitest](https://vitest.dev/)

```sh
yarn test:unit
```

### Exécutez des tests de bout en bout ( End-to-End ) avec [Cypress](https://www.cypress.io/)

```sh
yarn test:e2e:dev
```

Cela exécute les tests de bout en bout ( End-to-End ) sur le serveur de développement Vite.
C'est beaucoup plus rapide que le build de la production.

Mais il est toujours recommandé de tester la version de production avec `test:e2e` avant le déploiement (par exemple dans les environnements CI) :

```sh
yarn build
yarn test:e2e
```

### Lint avec [ESLint](https://eslint.org/)

```sh
yarn lint
```
