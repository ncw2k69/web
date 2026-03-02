# Vite

## Add SSL support with local certs

Inside of `vite.config.ts` add the following:
```typescript
import { defineConfig } from "vite";
import { resolve, dirname } from "node:path";
import { readFileSync } from "node:fs";
import { fileURLToPath } from "node:url";

// Get the directory name of the current config file
const __dirname = dirname(fileURLToPath(import.meta.url));

export default defineConfig({
  server: {
    host: "model-analyzer",
    https: {
      key: readFileSync(resolve(__dirname, "../certs/model.key")),
      cert: readFileSync(resolve(__dirname, "../certs/model.crt")),
    },
  },
});

```
