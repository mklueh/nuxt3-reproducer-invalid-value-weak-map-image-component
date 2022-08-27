# Nuxt 3 Reproducer

Reproducer for the issue https://github.com/nuxt/framework/issues/6990

````
ℹ Vite server warmed up in 345ms                                                                                                                                                                                              14:03:33
ℹ Vite client warmed up in 1050ms                                                                                                                                                                                             14:03:33
✔ Vite server built in 800ms                                                                                                                                                                                                  14:03:33
✔ Nitro built in 446 ms                                                                                                                                                                                                 nitro 14:03:34
[Vue warn]: Failed to resolve component: nuxt-page
If this is a native custom element, make sure to exclude it from component resolution via compilerOptions.isCustomElement.
[nuxt] [request error] [unhandled] [500] Invalid value used as weak map key
  at WeakMap.set (<anonymous>)  
  at normalizePropsOptions (./node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:3966:11)  
  at createComponentInstance (./node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:6957:23)  
  at renderComponentVNode (./node_modules/@vue/server-renderer/dist/server-renderer.cjs.js:171:22)  
  at Module.ssrRenderComponent (./node_modules/@vue/server-renderer/dist/server-renderer.cjs.js:608:12)
  at ./.nuxt/dist/server/server.mjs:3390:37
  at renderFnWithContext (./node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:847:21)
  at ssrRenderSlotInner (./node_modules/@vue/server-renderer/dist/server-renderer.cjs.js:624:21)
  at Module.ssrRenderSlot (./node_modules/@vue/server-renderer/dist/server-renderer.cjs.js:614:5)
  at _sfc_ssrRender (./.nuxt/dist/server/server.mjs:3528:25)
[Vue warn]: Failed to resolve component: nuxt-page
If this is a native custom element, make sure to exclude it from component resolution via compilerOptions.isCustomElement.
[nitro] [dev] [unhandledRejection] TypeError: Invalid value used as weak map key
    at WeakMap.set (<anonymous>)
    at normalizePropsOptions (/home/user/workspace/nuxt3-reproducer-invalid-value-weak-map-image-component/node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:3966:11)
    at createComponentInstance (/home/user/workspace/nuxt3-reproducer-invalid-value-weak-map-image-component/node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:6957:23)
    at renderComponentVNode (/home/user/workspace/nuxt3-reproducer-invalid-value-weak-map-image-component/node_modules/@vue/server-renderer/dist/server-renderer.cjs.js:171:22)
    at Module.ssrRenderComponent (/home/user/workspace/nuxt3-reproducer-invalid-value-weak-map-image-component/node_modules/@vue/server-renderer/dist/server-renderer.cjs.js:608:12)
    at file:///home/user/workspace/nuxt3-reproducer-invalid-value-weak-map-image-component/.nuxt/dist/server/server.mjs:3390:37
    at renderFnWithContext (/home/user/workspace/nuxt3-reproducer-invalid-value-weak-map-image-component/node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:847:21)
    at ssrRenderSlotInner (/home/user/workspace/nuxt3-reproducer-invalid-value-weak-map-image-component/node_modules/@vue/server-renderer/dist/server-renderer.cjs.js:624:21)
    at Module.ssrRenderSlot (/home/user/workspace/nuxt3-reproducer-invalid-value-weak-map-image-component/node_modules/@vue/server-renderer/dist/server-renderer.cjs.js:614:5)
    at _sfc_ssrRender (file:///home/user/workspace/nuxt3-reproducer-invalid-value-weak-map-image-component/.nuxt/dist/server/server.mjs:3528:25)

````

## Setup

Make sure to install the dependencies:

```bash
# yarn
yarn install

# npm
npm install

# pnpm
pnpm install --shamefully-hoist
```

## Development Server

Start the development server on http://localhost:3000

```bash
npm run dev
```

## Production

Build the application for production:

```bash
npm run build
```

Locally preview production build:

```bash
npm run preview
```

Checkout the [deployment documentation](https://v3.nuxtjs.org/guide/deploy/presets) for more information.
