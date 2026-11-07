# Polyscan Hands — Public Paper Dashboard

This repository is prepared to publish the standalone Polyscan paper dashboard with GitHub Pages. The `dashboard.zip`
contains only the dashboard and its engine dependencies, not the browser extension.

The page uses public Polymarket market data to simulate paper trades. It does not sign in to Polymarket, read account
information, or submit real orders. It cannot run the extension's Polymarket "hands" in this shared browser.

## Enable deployment

1. In this repository, open **Settings → Pages** and select **GitHub Actions** as the build and deployment source.
2. Push the `main` branch, or run **Deploy paper dashboard** from the **Actions** tab.
3. Wait for the workflow to finish. Open the published URL shown in **Settings → Pages**.

Each browser stores its own paper account in local storage. The page needs an internet connection for public market
feeds. Anyone with the public repository can inspect its source, and anyone with the Pages URL can open the dashboard.
