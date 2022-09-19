# Fieldset flex bug

There appears to be a rendering inconsistency in Safari on both desktop and iOS. I also encountered this issue in safari 15 as well on all platforms.

At a high level there is some additional space that is being preserved on the `<fieldset>` element. Strangely, this behavior can be "corrected" on the fly by triggering a repaint on the whole viewport such as resizing the browser window on desktop or an orientation change on iOS.

There are two possible solutions to get the correct layout on the first pass.

1. Use a different element than `<legend>` for the same purpose
2. Forget using `display:flex;` on the `<form>` ?

## How to run

1. Install dependencies

```shell
pnpm i
```

2. Run the dev server

```shell
pnpm dev
```
