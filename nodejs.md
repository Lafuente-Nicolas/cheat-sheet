#  Cheat Sheet Node.js 

|  **Action**                         |  **Commande / Code**                                                           |
|--------------------------------------|----------------------------------------------------------------------------------|
| Initier un projet Node               | `pnpm init` ou `pnpm init -y`                                                   |
| Lancer un fichier JS                 | `node index.js`                                                                 |
| Installer un paquet                  | `pnpm add express`                                                              |
| Installer un paquet dev              | `pnpm add -D nodemon`                                                           |
| Supprimer un paquet                  | `pnpm remove express`                                                           |
| Lancer avec nodemon                  | `npx nodemon index.js`                                                          |
| Importer un module (CommonJS)        | `const fs = require('fs')`                                                      |
| Utiliser des variables d’environnement | `require('dotenv').config(); process.env.MACLE`                               |
| Créer un fichier                     | `touch fichier.js`                                                              |
| Créer un dossier                     | `mkdir mon-dossier`                                                             |
| Compiler TypeScript                  | `npx tsc` *(nécessite un `tsconfig.json`)*                                      |
