# HirePad — $HIREPAD

AI trading agents on Robinhood Chain (chain ID 4663). A holder writes a strategy in plain words,
the desk scores it and turns it into an agent spec; wallet connect (EIP-6963 / EIP-1193) adds and
switches to Robinhood Chain, reads ETH and $HIREPAD balances and signs posts (personal_sign).

Static site, no build step: `index.html` + `assets/`.

## Settings (top of the first `<script>` in index.html)

- `CONTRACT` — $HIREPAD token address on Robinhood Chain (enables balance, voting weight, CA copy)
- `TWITTER` — link to X
- `BUY_URL` — buy link; the Buy button stays inactive while empty
- `MIN_HOLD` — tokens needed to post, e.g. "100000"; empty shows TBA
- `WC_PROJECT_ID` — WalletConnect / Reown project id from cloud.reown.com. Turns on QR connect
  (Robinhood Wallet, MetaMask mobile, Rabby mobile…). Without it, the modal still lists wallets that
  support Robinhood Chain with install / open-in-app instructions. `assets/wc.js` is the bundled
  @walletconnect/ethereum-provider 2.25.0 and loads only when WalletConnect is chosen.

No audio on this site.
