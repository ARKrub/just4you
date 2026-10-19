# Just4you.th NFC + AR Chibi Prototype

## Included
- `index.html`: static personalized landing page with Google's model-viewer and an AR button.
- `models/demo-chibi.glb`: simple placeholder chibi character (approximately 25 cm tall), generated from primitive meshes. Replace with your own optimized GLB.

## Publish on GitHub Pages
1. Create a GitHub repository, e.g. `just4you-ar`.
2. Upload `index.html` and the `models` folder, preserving their paths.
3. Under Settings > Pages, choose Deploy from a branch, `main`, `/ (root)`, and Save.
4. Wait for the published HTTPS URL (often `https://YOURUSERNAME.github.io/just4you-ar/`).
5. Open the published URL in Safari on a supported iPhone or Chrome on a compatible Android phone. Do not test AR using a local file:// URL.
6. Tap `View in your space`, scan a tabletop/floor, and place the model.
7. Encode that exact published HTTPS URL as an NFC NDEF URI record using your NFC writing app.

## Personalize
- Use a URL such as `https://YOURUSERNAME.github.io/just4you-ar/?name=Alex` to customize the heading.
- Replace `models/demo-chibi.glb` with a customer's GLB, or duplicate the page and change its `src` for each customer.
- The NFC tag holds only the webpage URL, not the 3D model.
- For production, use unique unguessable URLs and access controls if customers need privacy; GitHub Pages content is public.

## iOS and Android
- `model-viewer` supports AR Quick Look on compatible iPhones and Scene Viewer/WebXR on supported Android phones.
- If iPhone automatic USDZ generation fails for a complex model, export a separate USDZ and add `ios-src="./models/customer.usdz"` to the `model-viewer` tag.
- Native AR viewers will not display the webpage's HTML overlays inside AR.

## Physical keychain starting measurements
- Character: 50–60 mm high, compact reinforced arms/neck.
- NFC base: 32 mm diameter, 5–6 mm total thickness, cavity sized to your measured NFC sticker.
- Print a top shell of ~0.8–1.2 mm plastic above the tag and test before sealing.
- Keep the metal keyring away from the NFC antenna; test both iOS and Android.

## References
- https://modelviewer.dev/docs/index.html
- https://modelviewer.dev/examples/augmentedreality/
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
