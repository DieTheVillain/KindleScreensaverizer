# KindleScreensaverizer
## kindle screensaver converter

Converts images into screensavers sized for your Kindle. Runs entirely in the browser, nothing gets uploaded anywhere.

Use it here: https://DieTheVillain.github.io/KindleScreensaverizer/

Made this because I got tired of opening an image editor every time I wanted to resize something to 1236x1648 and remember which model wants which resolution. Pick your Kindle from the dropdown and it handles the rest.

**What it does**
- Resizes to the native resolution of whatever model you pick (everything from the K3 up through the Scribe and Colorsoft)
- Converts to grayscale automatically unless you picked the Colorsoft, since that's the only one with a color panel
- Keeps PNG transparency intact through the whole pipeline, including the grayscale pass
- Crop-to-fill or letterbox, your choice
- Optional Floyd-Steinberg dither down to 16 gray levels, which is what the e-ink panel actually displays anyway


Output is always PNG. Drop it in your screensaver folder (/mnt/us/documents/screensavers/ or wherever your particular hack expects them) and you're done.

**Privacy**
There is no server. The whole site is one static HTML file and the conversion happens in a canvas element in your own tab. If you want to verify that, open devtools, watch the network tab, and convert something. Zero requests. Close the tab and the image is gone.

That's also why the repo is public. You can read every line that runs.

**Not jailbroken yet?**
You'll need a jailbreak to use custom screensavers at all. Start here: https://kindlemodding.org/

**Self-hosting**
It's one file. Fork the repo or just save index.html and put it on anything that serves static files. No build step, no dependencies.

**Wrong resolution for your model?**
The model list lives in the MODELS array at the top of the script in index.html. If I got one wrong, open an issue or a PR with the correct numbers and I'll fix it.
