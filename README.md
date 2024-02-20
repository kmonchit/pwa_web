# pwa_web
https://web.dev/articles/what-are-pwas 

# You might need to install npm
https://docs.npmjs.com/downloading-and-installing-node-js-and-npm 

# Step by step
We need four files index.html, logo, manifest.json to describe and service-worker.js
In HTML index file, reference to manifest and load service worker
<link rel="manifest" href="manifest.json"> 
Add script 
    <script>
            if ('serviceWorker' in navigator) {
                navigator.serviceWorker.register('./service-worker.js');
            }
    </script>

https://www.npmjs.com/package/pwa-asset-generator 
Install pwa-asset-generator
> npm install pwa-asset-generator 
> npx pwa-asset-generator logo.png icons

Copy generated json and paste them in icons of manifest.json file. 

To enable caching, add importScripts, add routing module in service-worker.js.

# To run
npx serve

Open Chrom dev tool, Ctrl+Shift+J, go to Application, Manifest to check icons and Service Workers

It will create local host. You can view from your web browser with localhost:3000

Keep it running, 
Open command prompt, find the IPv4 address and copy it. 
For example, 
192.168.1.55 and add http://192.168.1.55:3000 

# next task for kiosk_enabled
https://developer.chrome.com/docs/apps/manifest/kiosk_enabled/ 

I added the kiosk_enabled code to manifest file. Just like the case from stackoverflow, kiosk mode hasn't turned on yet. 
https://stackoverflow.com/questions/63799266/kiosk-mode-in-pwa-on-android

