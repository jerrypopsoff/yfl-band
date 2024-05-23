# Your Fearless Leader

Source code for [yfl.band](https://yfl.band).

## Making basic content changes

1. Visit [constants.ts](https://github.com/ghaagsma/yfl-band/blob/main/src/lib/constants.ts).
1. Select the pencil icon (`Edit this file`).
1. Make desired changes.
1. Select the `Commit changes...` button.
1. Ensure the `Create a new branch for this commit and start a pull request` option is enabled.
1. Select the `Propose changes` button.
1. Select the `Create pull request` button.
1. Wait for all checks to finish (should take less than one minute).
1. Open the `Details` link in a new tab, and verify your change in the preview deployment.
   1. **Make sure the change looks good for narrow and wide screens!**
1. Close the preview deployment and select `Merge pull request`.
1. Select `Confirm merge`. The changes should automatically deploy and be live within two minutes.

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev
```

## Building

To create a production version of the application:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

## This repository was created via `create-svelte`

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/main/packages/create-svelte).
