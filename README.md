# truoLive

Public, non-secret StoreXpanse release metadata lives under `trustore/`:

- `release-index.json` is the exact signed release index.
- `release-index.signature.json` is its detached Ed25519 signature.
- `release-index-public.pem` is the public key clients pin to verify the
  signature. The corresponding private key is non-exportable OpenBao Transit
  material and is never stored in this repository.

Plugin ZIPs remain GitHub release assets in the private `truStore` source
repository. The public index contains checksums and sizes; the authenticated
update service authorizes installations and proxies the matching asset.
