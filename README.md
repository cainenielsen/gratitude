# 🦃 gratitude

A Thanksgiving gratitude site — one page per person, each with a personal
"Thank you" note. Built with Nuxt 2, generated to static HTML, deployed
via Firebase Hosting.

## How it works

Every person gets their own route (`pages/<name>.vue`), which just
supplies a name and a message to the shared [`Sheet`](components/Sheet.vue)
component — a torn-paper card with a wiggling turkey and a signature line.
Adding someone new is adding a new page file.

```vue
<template>
  <Sheet name="Alex">
    <template #message>
      <p>Your message here.</p>
    </template>
  </Sheet>
</template>

<script>
export default {};
</script>
```

## Project setup

```bash
npm install
```

### Serve with hot reload at localhost:3000

```bash
npm run dev
```

### Generate the static site

```bash
npm run generate
```

### Deploy to Firebase Hosting

```bash
npm run deploy
# or, generate + deploy in one step:
npm run launch
```

Firebase project: `caineandrebekah-gratitude` (see [.firebaserc](.firebaserc)).

## Tech

[Nuxt 2](https://nuxtjs.org) (static target) + [@nuxt/content](https://content.nuxtjs.org/).
