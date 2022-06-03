The DevSecOps Platform Independent Model uses Cameo Enterprise Architecture to create the model. This application can export the model to a self-contained web application. Once exported, you must perform several steps before pushing a new version of the repository to SEI's GitHub.

# Instructions
## Step 1: Update fav icon
Copy the `favicon.ico` to the docs/ directory and overwrite the one that's already there.

## Step 2: Update default images
Copy all files in images directory to the docs/images directory and overwrite what's already there.
* `loader.png` - Image displayed as the application loads.
* `icon.png` -  Image replaces the magicdraw image.
* `logo.png` - Logo displayed in the header.
* `process_portal.png` - Image in header that reads DevSecOps Platform Independent Model.

## Step 3: Update the default HTML filename
When the export is created, there is a single HTML file in the root directory.
* `git mv docs/DSO_PIM.html docs/index.html`

## Step 4: Update the filename that links to the homepage
The logo is a hyperlink to the HTML file in the `docs/` directory. Since we renamed that file to `index.html`, we need to update the `docs/data.js` file to specify `index.html` as the link to the homepage. Search for `window.indexPageDir` and update the value to `index.html`.

## Step 5: Update '<title>' tag
Edit the `docs/index.html` and change the `<title>` tag to be "DevSecOps Platform Independent Model | Software Engineering Institute".

## Step 6: Add overriden CSS to the 'docs/index.html' file.
We overwrite several styles to apply SEI/CMU branding. Insert the marked CSS `<style>` from the reference index.html into `docs/index.html`

## Step 7: Add footer to 'docs/index.html'
Copy the marked footer from the reference `index.html` too `docs/index.html`

