`serverActions` seems to break date-picker

repro:

```bash
pnpm dev
```

1. open with firefox
2. open dialog
3. try to open date-picker -> wont work

switch `serverActions` to `false`.

repeat steps 1-3. should work now.

```js
/** @type {import('next').NextConfig} */
const nextConfig = {
  experimental: {
    serverActions: true,
  },
};

module.exports = nextConfig;
```
