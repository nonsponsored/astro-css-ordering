## Case #1:

Linking global.scss via: `<link rel="stylesheet" href={Astro.resolve("../styles/global.scss")} />`

In dev, `h1` styling comes from `Component1.astro`.
In production, `h1` styling comes from `_base.scss.`

## Case #2:

Linking global.scss via: `<style global>@import "../styles/global.scss";</style>`

In dev and production, `h1` styling comes from `Component1.astro.`


## Expected Result

Component styles would always be appended to `global.scss`, allowing `h1` to render styles from `Component1.astro`.


----


| Command           | Action                                       |
| :---------------- | :------------------------------------------- |
| `npm install`     | Installs dependencies                        |
| `npm run dev`     | Starts local dev server at `localhost:3000`  |
| `npm run build`   | Build your production site to `./dist/`      |
| `npm run preview` | Preview your build locally, before deploying |
