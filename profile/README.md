![](https://github.com/DefGuard/docs/blob/docs/screencasts/defguard.gif?raw=true)

defguard is an open-source security *swiss army knife* (Identity, MFA, VPN, Yubikey, Web3). Building a secure organization has always been difficult and costly. Defguard provides a beautiful, easy-to-use (business users) and deploy (admin/devops) fundament to make your organization secure.

**Why?**

The story and motivation behind defguard [can be found here: https://teonite.com/blog/defguard/](https://teonite.com/blog/defguard/)

**Features:**

* OpenID Connect provider (with OpenLDAP synchronization)
* [Wireguard:tm:](https://www.wireguard.com/) VPN management with:
  - import your current WireGuard server configuration (with a wizard!)
  - *easy* device setup by users themselves (self-service)
  -  automatic IP allocation
  -  kernel & userspace WireGuard support
  - dashboard and statistics overview of connected users/devices for admins
  - *defguard is not an official WireGuard project, and WireGuard is a registered trademark of Jason A. Donenfeld.*
* Multi-Factor Authentication:
  - Time-based One-Time Password Algorithm (TOTP - e.g. Google Authenticator)
  - WebAuthn / FIDO2 - for hardware key authentication support (eg. YubiKey, FaceID, TouchID, ...)
  - Web3 - authentication with crypto software and hardware wallets using Metamask, Wallet Connect, Ledger Extension
* [Yubikey hardware keys](https://www.yubico.com/) provisioning for users by *one click*
* Webhooks & REST API
* Web3 wallet validation
* Build with [Rust](https://www.rust-lang.org/) for portability, security, and speed
* Fronted in TypeScript with:
  - a set of custom and beautiful components for the layout
  - Responsive Web Design (supporting mobile phones, tablets, etc..)
  - [iOS Web App](https://www.macrumors.com/how-to/use-web-apps-iphone-ipad/)
* **Checked by professional security researchers** (see [comprehensive security report](https://defguard.net/images/decap/isec-defguard.pdf))
* End2End tests
