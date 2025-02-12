# Interactive Narratives Svelte Starter Template

This starter template includes some elements that you can use to get started on your projects.

I'd recommend going through both of these, especially if you haven't coded much before. Please reach out if you have questions!

* [A basic overview of HTML, CSS, and Javascript](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Your_first_website)
* [Svelte tutorial](https://svelte.dev/tutorial/svelte/welcome-to-svelte)

## Get Started 🚦
* Click the green `Use this template` button above.
* Choose `Create a new repository`
* Give the repository a name and click `Create repository`
* Click the green `Code` button and copy the URL to your clipboard.
* Open your Terminal, and in the folder where you want this folder to go, run `git clone [copied url]`
* In Terminal, go into that repo (`cd repo-name`)
* [Make sure you have Node.js and npm installed](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm).
* Run `npm install`
* Run `npm run dev` to enter development mode.
* Go to http://localhost:5173/, and it should be running!


## How to Deploy to GitHub Pages 🚀

GitHub Pages allows you to host your repo as a website for free. To push and deploy your site, **run these 2 commands**:
* `npm run build` - This generates a directory called `build` with the statically rendered app.
* `make github` - This updates GitHub pages.
* The site will now be live at [your github handle].github.io/[your repo name]

The first time you do this, you'll need to configure your repo to connect to GitHub Pages.
* In your repo on github.com, go to `Settings`
* On the lefthand side, click `Pages`
* Under `Source` you should have `Deploy from a branch` selected.
* Under `Branch`, select `main` and then change the repo from `/root` to `/docs` and click `Save`.
* Now, when you run the 2 commands above, you should be able to see your site live at [your github handle].github.io/[your repo name]


## Helper Components 🧱

There are a couple of helper components located in `$components/helpers`. These are meant to be building blocks that might be used often in your website, so you can easily plug them in. I'll keep adding to this as we go, and you can let me know if you have specific requests.

A demonstration of each helper component can be found in `$components/demo/Demo.svelte`.

* `Scrolly.svelte`: Scrollytelling.
* `Hero.svelte`: A full-bleed hero image for the top of your story (can also use video).
* `Image.svelte`: An image with an optional caption.
* `Video.svelte`: A video with an optional caption.


## Advanced/Optional Features 🤓

### Google Docs and Sheets

This repo is configured to bring in data or copy from Google Docs or Google Sheets. Google Docs should be written in [ArchieML]([url](https://archieml.org/)).

* Create a Google Doc or Sheet
* Click `Share` -> `Advanced` -> `Change...` -> `Anyone with this link`
* In the address bar, grab the ID - eg. "...com/document/d/**1IiA5a5iCjbjOYvZVgPcjGzMy5PyfCzpPF-LnQdCdFI0**/edit"
* paste in the ID above into `google.config.js`, and set the filepath to where you want the file saved
* If you want to do a Google Sheet, be sure to include the `gid` value in the url as well

Running `npm run gdoc` at any point (even in new tab while server is running) will fetch the latest from all Docs and Sheets.


### Actions

Located in `src/actions`.

```js
// Usage
import example from "$actions/action.js";
```

* `canTab.js`: enable/disable tabbing on child elements.
* `checkOverlap.js`: Label overlapping detection. Loops through selection of nodes and adds a class to the ones that are overlapping. Once one is hidden it ignores it.
* `focusTrap.js`: Enable a keyboard focus trap for modals and menus.
* `keepWithinBox.js`: Offsets and element left/right to stay within parent.
* `inView.js`: detect when an element enters or exits the viewport.
* `resize.js`: detect when an element is resized.

### Runes

These are located in `src/runes`. You can put custom ones in `src/runes/misc.js` or create unique files for more complex ones.

```js
import { example } from "$runes/misc/misc.js";
```

* `useWindowDimensions`: returns an object `{ width, height }` of the viewport dimensions. It is debounced for performance.
* `useClipboard`: copy content to clipboard.
* `useFetcher`: load async data from endpoints (local or external).
* `useWindowFocus`: determine if the window is in focus or not.

For more preset runes, use [runed](https://runed.dev/docs) which is preloaded. 

### Utils

Located in `src/utils/`.

```js
// Usage
import example from "$utils/example.js";
```
* `checkScrollDir.js`: Gets the user's scroll direction ("up" or "down")
* `csvDownload.js`: Converts a flat array of data to CSV content ready to be used as an `href` value for download.
* `generateId.js`: Generate an alphanumeric id.
* `loadCsv.js`: Loads and parses a CSV file.
* `loadImage.js`: Loads an image.
* `loadJson.js`: Loads and parses a JSON file.
* `loadPixels.js`: Loads the pixel data of an image via an offscreen canvas.
* `localStorage.js`: Read and write to local storage.
* `mapToArray.js`: Convenience function to convert a map to an array.
* `move.js`: transform translate function shorthand.
* `transformSvg.js`: Custom transition lets you apply an svg transform property with the in/out svelte transition. Parameters (with defaults):
* `translate.js`: Convenience function for transform translate css.
* `urlParams.js`: Get and set url parameters.
