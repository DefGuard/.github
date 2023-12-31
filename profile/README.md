![](https://github.com/DefGuard/docs/blob/docs/screencasts/defguard.gif?raw=true)

defguard is an **SSO & VPN Server** based on **OpenID and Wireguard VPN** with unique secure&private architecture for building **secure and privacy-aware organizations**.

By design defguard core is meant to be deployed in your secure network segments (available only from an internal network or by VPN) and operations that require public access (like user onboarding, enrollment, password reset, etc.) are done using a secure proxy.
By design **defguard core is meant to be deployed in your secure network segments** (available only from an internal network or by VPN) and operations that require **public access** (like user onboarding, enrollment, password reset, etc.) are done using a **secure proxy**.

Read more about this in [our documentation](https://defguard.gitbook.io/defguard/#what-is-defguard).

**Implemented & production tested features:**

* [OpenID Connect provider](https://openid.net/developers/how-connect-works/) - with **unique features**:
  - Secure remote (over the internet) [user enrollment](https://defguard.gitbook.io/defguard/help/remote-user-enrollment)
  - User [onboarding after enrollment](https://defguard.gitbook.io/defguard/help/remote-user-enrollment/user-onboarding-after-enrollment)
  - LDAP (tested on [OpenLDAP](https://www.openldap.org/)) synchronization
  - nice UI to manage users
  - Users **self-service** (besides typical data management, users can revoke access to granted apps, MFA, Wireguard, etc.)
* [Wireguard:tm:](https://www.wireguard.com/) VPN management with:
  - multiple VPN Locations (networks/sites) - with defined access (all users or only Admin group)
  - multiple [Gateways](https://github.com/DefGuard/gateway) for each VPN Location (**high availability/failover**) - supported on a cluster of routers/firewalls for Linux, FreeBSD/PFSense/OPNSense
  - **import your current WireGuard server configuration (with a wizard!)**
  - *in-development*: [Desktop Clients!](https://github.com/defguard/client)
  - automatic IP allocation
  - kernel (Linux, FreeBSD/OPNSense/PFSense) & userspace WireGuard support with [our Rust library](https://github.com/defguard/wireguard-rs)
  - dashboard and statistics overview of connected users/devices for admins
  - *defguard is not an official WireGuard project, and WireGuard is a registered trademark of Jason A. Donenfeld.*
* [Multi-Factor/2FA](https://en.wikipedia.org/wiki/Multi-factor_authentication) Authentication:
  - [Time-based One-Time Password Algorithm](https://en.wikipedia.org/wiki/Time-based_one-time_password) (TOTP - e.g. Google Authenticator)
  - WebAuthn / FIDO2 - for hardware key authentication support (eg. YubiKey, FaceID, TouchID, ...)
  - Web3 - authentication with crypto software and hardware wallets using Metamask, Ledger Extension
* [Yubikey hardware keys](https://www.yubico.com/) provisioning for users by *one click*
* [Email/SMTP support](https://defguard.gitbook.io/defguard/help/setting-up-smtp-for-email-notifications) for notifications, remote enrollment and onboarding
* Easy support with [sending debug/support information](https://defguard.gitbook.io/defguard/help/sending-support-info)
* Webhooks & REST API
* Web3 wallet validation
* Build with [Rust](https://www.rust-lang.org/) for portability, security, and speed
* [UI Library](https://github.com/defguard/ui) - our beautiful React/TypeScript UI is a collection of React components:
  - a set of custom and beautiful components for the layout
  - Responsive Web Design (supporting mobile phones, tablets, etc..)
  - [iOS Web App](https://www.macrumors.com/how-to/use-web-apps-iphone-ipad/)
* **Checked by professional security researchers** (see [comprehensive security report](https://defguard.net/images/decap/isec-defguard.pdf))
* End2End tests
