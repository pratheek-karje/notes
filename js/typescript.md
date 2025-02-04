# typescript

## tsconfig fields

- `rootDir` - Specify the root folder within your source files (the `scr` directory)
- `incremental` - Save `.tsbuildinfo` files to allow for incremental compilation of projects.

## initializing typescript project

```sh
mkdir my-project
cd my-project
npm init -y
npm i -D typescript
npx tsc --init
npm i -D @types/node
npm i -D ts-node-dev
```

## package.json scripts:

```json
"start": "ts-node-dev src/index.ts"
"start2": "ts-node-dev --respawn --transpile-only src/index.ts"
```

## basic tsconfig file content

```json
{
  "compilerOptions": {
    /* Visit https://aka.ms/tsconfig.json to read more about this file */

    /* Projects */
    "incremental": true,                              /* Enable incremental compilation */

    /* Language and Environment */
    "target": "es2016",                                  /* Set the JavaScript language version for emitted JavaScript and include compatible library declarations. */
    "lib": [ "ESNext" ],                                        /* Specify a set of bundled library declaration files that describe the target runtime environment. */

    /* Modules */
    "module": "commonjs",                                /* Specify what module code is generated. */
    "rootDir": "./src",                                  /* Specify the root folder within your source files. */
    "moduleResolution": "node",                       /* Specify how TypeScript looks up a file from a given module specifier. */
    "baseUrl": "./",                                  /* Specify the base directory to resolve non-relative module names. */
    "paths": {},                                      /* Specify a set of entries that re-map imports to additional lookup locations. */
    "typeRoots": ["./node_modules/@types", "./src/types"],                                  /* Specify multiple folders that act like `./node_modules/@types`. */

    /* JavaScript Support */
    "allowJs": true,                                  /* Allow JavaScript files to be a part of your program. Use the `checkJS` option to get errors from these files. */
    "checkJs": true,                                  /* Enable error reporting in type-checked JavaScript files. */

    /* Emit */
    "sourceMap": true,                                /* Create source map files for emitted JavaScript files. */
    "outDir": "./dist",                                   /* Specify an output folder for all emitted files. */

    /* Interop Constraints */
    "allowSyntheticDefaultImports": true,             /* Allow 'import x from y' when a module doesn't have a default export. */
    "esModuleInterop": true,                             /* Emit additional JavaScript to ease support for importing CommonJS modules. This enables `allowSyntheticDefaultImports` for type compatibility. */
    "forceConsistentCasingInFileNames": true,            /* Ensure that casing is correct in imports. */

    /* Type Checking */
    "strict": true,                                      /* Enable all strict type-checking options. */

    /* Completeness */
    "skipDefaultLibCheck": true,                      /* Skip type checking .d.ts files that are included with TypeScript. */
    "skipLibCheck": true                                 /* Skip type checking all .d.ts files. */
  },
  "include": [
      "src/**/*"
  ],
  "exclude": [
    "node_modules",
    "build"
  ],
  "ts-node": {
    "transpileOnly": true,
  }
}
```

### ts-node-dev

scripts for package.json

```json
  "scripts": {
    "start": "ts-node-dev src/index.ts",
    "start2": "ts-node-dev --respawn --transpile-only src/index.ts",
  },
```



