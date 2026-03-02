# Creating Vite Project
Create project
```shell
bun create vite
```
Add Bun support inside Bun/Vite project
```shell
bun add -d @types/bun
```
To make autocomplete work in `.ts` files, go to `tsconfig.json`, in `compilerOptions > types` add `bun-types`
```json
{
  ...
  "compilerOptions": {
    ...
    "types": ["vite/client","bun-types"]
    ...
  }
  ...
}
```
