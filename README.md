# Mythchain Signed Bootstrap Mirror — provisioned, not activated

This public repository is an independent HTTPS hosting origin candidate for
MYTHCHAIN `mythchain-testnet-v2`. It is hosted on GitHub Pages, independently
of the existing Cloudflare Pages `mythchain.pages.dev` website.

**PUBLIC BOOTSTRAP STATUS: HOLD / NOT ACTIVATED.**

The route `/bootstrap/v1/directory.json` is intentionally **NOT PUBLISHED**
until all of the following have been proven:

- A NEW operational root Ed25519 public key is pinned and its private key
  kept offline/encrypted (not the disposable unencrypted P1F27 LAB key).
- A fresh root-signed delegate certificate and revocation epoch, plus an
  individually signed, expiring directory for canonical
  `mythchain-testnet-v2` and pinned genesis.
- Approval from independent operator(s) and verification against canonical
  CometBFT AWS and ARDEC Node IDs.
- Same signed envelope published unchanged on Cloudflare Pages and this
  GitHub Pages origin; both independently validated from 3+ physical machines.
- Rejection of expired, revoked, malformed, wrong-chain and stale-sequence
  manifests and an actual WAN authenticated joiner handshake test.

Never put a signing **private key**, privileged RPC, operator secrets, cloud
tokens, validator state or keystore files in this repository. GitHub Pages
delivers PUBLIC JSON only, and is not a transaction relay or validator.

**IMPORTANT:** an HTTP 200 response on this status homepage does not imply
`/bootstrap/v1/directory.json` exists or is trusted.
