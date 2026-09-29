# ME382-demos
Demonstration webpages for ME382, Mechanical Behavior of Materials

## Crystal planes demo

The standalone page is [`index.html`](index.html). To preview it on your computer, open the repository in a terminal and run:

```sh
python3 -m http.server 8000
```

Then visit <http://localhost:8000> in a browser. Serving it this way is recommended because the page loads Three.js as a JavaScript module.

To publish it with GitHub Pages, push this branch to GitHub, merge it into `main`, then open the repository's **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, and save. GitHub will provide the published site URL on that settings page.
