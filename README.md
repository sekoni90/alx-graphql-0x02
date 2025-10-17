# alx-graphql-0x02

This workspace contains `alx-rick-and-morty-app` prepared for the ALX GraphQL exercise.

Files added/updated:

- `alx-rick-and-morty-app/interfaces/index.ts` — TypeScript interfaces for episodes
- `alx-rick-and-morty-app/components/common/EpisodeCard.tsx` — Episode card component
- `alx-rick-and-morty-app/pages/index.tsx` — Home page using Apollo `useQuery` to fetch episodes
- `alx-rick-and-morty-app/graphql/queries.ts` — GraphQL query for episodes

How to run locally (Windows PowerShell):

1. Change directory to the project:

```powershell
cd .\alx-rick-and-morty-app
```

2. Install dependencies (if `package.json` exists). If not, initialize a Next.js app or copy `package.json` from the original `alx-graphql-0x01` project:

```powershell
npm install
```

3. Run the development server:

```powershell
npm run dev
```

4. Open http://localhost:3000 in your browser.

Notes and troubleshooting:

- The code uses the `@/` path alias (e.g. `@/interfaces`). Ensure `tsconfig.json` or Next.js config defines `baseUrl`/`paths` mapping `@/*` to the project root. Example `tsconfig.json` snippet:

```json
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@/*": ["./*"]
    }
  }
}
```

- If you get TypeScript errors about `@/` imports, either configure `tsconfig.json` paths or replace `@/` with relative imports like `../../interfaces`.

- The page imports `GET_EPISODES` from `graphql/queries.ts`. I added a minimal implementation that queries the Rick and Morty GraphQL API.

If you want, I can add a `package.json` and `tsconfig.json` so the app runs out-of-the-box. Tell me if you want me to proceed.