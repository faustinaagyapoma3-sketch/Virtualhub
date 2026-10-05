VirtualsHub standalone GitHub Pages package — Paystack checkout

Upload every file and folder in this directory to the root of your GitHub repository. Do not upload the ZIP file itself. The repository root must contain:

- index.html
- config.js
- .nojekyll
- assets/

GitHub Pages setup:
1. Extract the package ZIP.
2. Upload the extracted contents directly into your repository root.
3. Commit the files to your Pages branch, normally main.
4. Open Settings → Pages.
5. Select Deploy from a branch, choose main and / (root), then Save.
6. Open the generated Pages URL after deployment finishes.

The checkout now opens Paystack in GHS. The included config.js contains the Paystack public key and the existing backend URL. Public keys may be visible in browser code. Never add a Paystack secret key, Telegram bot token, database URL, or service-role key to GitHub.

Important payment note:
- The Paystack popup can open and collect payment using the public key.
- Secure server-side verification of the Paystack transaction requires the matching Paystack secret key on the private backend. Do not place that secret key in this package.
- If the backend is not configured with Paystack secret verification, do not treat a browser success callback alone as final payment proof.

Keep index.html, config.js, .nojekyll, and assets/ at the same repository level. Do not rename the assets folder.
