#  Cheat Sheet TypeScript (Simplifiée)

##  Commandes de base

|  **Action**                          |  **Commande / Code**                                                           |
|---------------------------------------|----------------------------------------------------------------------------------|
| Initialiser un projet TypeScript      | `pnpm init` puis `pnpm add -D typescript`                                        |
| Créer un fichier de config            | `npx tsc --init`                                                                 |
| Compiler un fichier `.ts`             | `npx tsc fichier.ts`                                                             |
| Compiler tout le projet               | `npx tsc` *(si `tsconfig.json` présent)*                                         |
| Lancer directement du TS              | `pnpx ts-node fichier.ts` *(nécessite `ts-node`)*                                |

---

## 🧠 Types de base

| TypeScript                        | Description                                  |
|----------------------------------|----------------------------------------------|
| `string`                         | Chaîne de caractères                         |
| `number`                         | Nombre (entier ou flottant)                  |
| `boolean`                        | Vrai ou faux                                 |
| `any`                            | Désactive le typage                          |
| `unknown`                        | Type inconnu (plus sûr que `any`)            |
| `void`                           | Ne retourne rien                             |
| `null` / `undefined`             | Valeurs nulles ou non définies               |

---

##  Structures de base

### Déclaration de variable
```ts
let nom: string = "Nicolas";
const age: number = 19;
