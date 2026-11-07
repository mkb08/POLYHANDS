# Polyscan Hands — Public Paper Dashboard

This repository is prepared to publish the standalone Polyscan paper dashboard with GitHub Pages. The `dashboard.zip`
contains only the dashboard and its engine dependencies, not the browser extension.

The page uses public Polymarket market data to simulate paper trades. It can connect to a WalletConnect wallet without
requesting signatures and show public positions for a Polymarket account address. It does not sign in to Polymarket,
show private account cash, or submit real orders. It cannot run the extension's Polymarket "hands" in this shared
browser. WalletConnect requires a public project ID entered in the dashboard.

The wallet-connected position view is read-only. The requested live limits ($20 per order, $50 open exposure, and
$20 daily realized-loss stop) are not enforced or active. Do not enter a seed phrase, private key, or CLOB API secret.

Paper entries require a supported market version, fresh CLOB tick/minimum-size and negative-risk metadata, an open
order book, and a market not marked geo-restricted. Missing or inconsistent metadata blocks the simulated order.
This only tightens known order-level checks: the dashboard cannot verify private balance, collateral approvals,
account-specific eligibility, queue priority, hidden liquidity, or matching at submission time. Strict-fill friction
values are simulation assumptions, not measured venue behavior. No zero-mismatch or real-order acceptance guarantee
is possible.

## Enable deployment

1. In this repository, open **Settings → Pages** and select **GitHub Actions** as the build and deployment source.
2. Push the `main` branch, or run **Deploy paper dashboard** from the **Actions** tab.
3. Wait for the workflow to finish. Open the published URL shown in **Settings → Pages**.

Each browser stores its own paper account in local storage. The page needs an internet connection for public market
feeds. Anyone with the public repository can inspect its source, and anyone with the Pages URL can open the dashboard.
