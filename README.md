# Awesome-Mobile-Point-Of-Sale-MPOS

# Top Mobile Point of Sale (mPOS) Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Handheld Payment Terminals, Mobile Checkout & Self-Hosted POS Apps*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Mobile Point of Sale (mPOS)**. These tools enable merchants to accept payments and manage sales from handheld devices—smartphones, tablets, or dedicated mobile terminals—bringing checkout to the customer instead of the counter, whether in retail, hospitality, field service, or pop-up environments.

**Examples** include Shopify POS Go, Square Terminal, Clover Flex, Poynt, Toast Go, PAX Technology, Castles Technology, Ingenico Move, Newland N910, and Verifone Carbon (the category leaders).

**Open-source emphasis**: mPOS is a domain where open-source tooling is **fragmented and largely immature for production payment processing**. The strongest open-source *applications* are mobile POS apps built with Flutter and React Native—**EasySell** and **flutter_pos** demonstrate offline-first architectures with thermal printing, while **Taler POS** provides a GNU-endorsed payment terminal for the Taler ecosystem . For crypto-native mPOS, **Numo** offers a tap-to-pay Bitcoin app on standard Android devices , and **Monero Merchant** provides a self-hosted Monero POS . However, **no open-source project replicates the integrated card-present payment processing, PCI-certified hardware, and acquiring relationships** of Square Terminal or Clover Flex. Open-source mPOS apps typically handle the *storefront and order management* layer while relying on commercial payment SDKs or crypto rails for actual money movement.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Shopify POS Go](https://www.shopify.com/pos)**  
  Shopify's handheld POS device with integrated barcode scanner and receipt printer; runs Shopify POS software for in-person selling, inventory lookup, and customer management.

- **[Square Terminal](https://squareup.com/us/en/hardware/terminal)**  
  All-in-one mobile POS with built-in receipt printer and long-lasting battery; $299 or $27/month over 12 months . Supports chip, tap, and swipe payments with offline mode for up to 24 hours . Compact design suits countertops and pop-up locations .

- **[Clover Flex](https://www.clover.com/pricing/flex)**  
  Handheld POS for tableside and mobile checkout; pricing starts at $40/month for 36 months or $749 purchase, with transaction fees from 2.6% + 10¢ . Supports card, cash, checks, mobile wallets, Venmo, and PayPal; includes inventory tracking, discounts, and optional appointment management . Used in restaurants for tableside orders and payments .

- **[Poynt](https://poynt.com/)**  
  Smart terminal platform (acquired by GoDaddy) with an open developer platform for building custom POS applications on Android-based devices.

- **[Toast Go](https://pos.toasttab.com/)**  
  Handheld POS for restaurants, enabling tableside ordering, payment, and kitchen communication; integrates with Toast's restaurant management platform.

- **[PAX Technology](https://www.pax.us/)**  
  Manufacturer of Android-based payment terminals (A-series, Q-series) used by acquirers and ISOs; provides SDKs for custom application development on certified hardware.

- **[Castles Technology](https://www.castlestech.com/)**  
  Payment terminal manufacturer with Android and Linux-based devices for mobile and countertop scenarios; offers SDKs and device management.

- **[Ingenico Move](https://www.ingenico.com/)**  
  Portable payment terminal series (e.g., Move 5000) with 4G/Wi-Fi/Bluetooth connectivity, built-in thermal printer, and PCI PTS certification; designed for tableside, curbside, and mobile payments .

- **[Newland N910](https://www.newland-id.com/)**  
  Android-based smart POS terminal with large touchscreen and integrated printer; used by acquirers and developers for custom payment applications.

- **[Verifone Carbon](https://www.verifone.com/)**  
  Android-based terminal series (Carbon 10, Carbon Mobile 5) with merchant and customer displays, contactless/EMV support, and developer SDKs for custom POS apps .

## Open-Source GitHub Projects

### Mobile POS Applications (Flutter / Cross-Platform)

- **[EasySell (Flutter)](https://github.com/fachrinfl/easy-sell-flutter-app)**  
  Comprehensive Flutter-based POS application with Firebase backend (Firestore, Auth, Storage) and local Hive storage . Features real-time inventory management, transaction processing, analytics, and cross-platform support (Android, iOS, desktop). Architecture uses Riverpod state management, Freezed models, and a clean separation of presentation/domain/data layers. **A solid reference implementation for building a mobile POS app with Firebase**, though it does not integrate card-present payment processing.

- **[flutter_pos (elrizwiraswara)](https://github.com/elrizwiraswara/flutter_pos)**  
  Flutter POS app demonstrating Clean Architecture and **offline-first design** with SQLite ↔ Firestore synchronization . Features product management, sales transactions, thermal receipt printing (USB/Bluetooth/network, 58mm/72mm/80mm), Firebase authentication, and queued actions for offline operations. **The most architecturally complete open-source Flutter POS reference** for developers building custom mobile POS apps.

- **[flutter-pos-system (Buddhima-JD3)](https://github.com/Buddhima-JD3/flutter-pos-system)**  
  Open-source Flutter app for small restaurants and businesses . Features inventory management, customer information capture, cash register, data export/backup, analytics (line/pie charts), and Bluetooth receipt printing. **Offline-first and privacy-focused**—no personal data stored remotely. Available on Google Play.

### Crypto-Native mPOS

- **[Numo](https://numopay.org/)**  
  Free, open-source (MIT) Android app that turns any NFC-enabled phone into a **Bitcoin tap-to-pay terminal** using the Cashu ecash protocol . Settles in seconds; compatible with Cashu wallets and standard Lightning wallets. Includes inventory management, tipping, offline payment support, and auto-sweep to a Lightning address. **Zero platform fees**—merchants keep 100% of earnings. Available as direct APK download .

- **[Monero Merchant](https://github.com/Monero-Merchant/monero-merchant)**  
  FOSS Android POS for accepting **Monero (XMR)** payments . Self-hosted, trustless architecture with backend interfacing to `monerod` and MoneroPay. Features QR/NFC payment generation, 0-confirmation support (5–10 seconds), Bluetooth ESC/POS receipt printing, and unlimited POS clients. GPL-3.0 licensed. **For merchants wanting private crypto payments** without third-party processors .

- **[Taler Point-of-Sale Terminal](https://fdroid.gitlab.io/jekyll-fdroid/en/packages/net.taler.merchantpos/index.html)**  
  GNU Taler merchant POS terminal for Android (available on F-Droid) . Processes orders, calculates totals, and accepts Taler payments via QR code or NFC. **Part of the GNU Taler privacy-preserving payment ecosystem**—requires Taler merchant backend infrastructure.

- **[Kasway POS](https://github.com/Kasway-Tech/pos)**  
  Flutter-based POS accepting **Kaspa (KAS)** payments via QR code . Features multi-currency display (26 currencies with live rates), SQLite catalog, order history, table layout editor, and external display mirroring. **Crypto-native**—no payment processor or custodian required.

### Web-Based & PWA Mobile POS

- **[react-native-pos-cashier (ProPOS)](https://github.com/mazkev/react-native-pos-cashier)**  
  React Native (Expo) mobile POS with Google Sheets backend via Apps Script . Features PIN-based staff lock, shift/drawer audit, loyalty points, promotions, and sales analytics. **Lightweight and deployable** for small businesses wanting a mobile cashier without server infrastructure.

- **[minimarket-pos](https://github.com/tomasvergaraj/minimarket-pos)**  
  POS system with a **PWA mobile interface** installable on Android/iOS from the browser; works offline with service workers . Backend is FastAPI + PostgreSQL; features sales, inventory, cash management, and feature-flagged modules. **Spanish-language focused** but the PWA approach is notable for cross-platform mobile deployment without app stores.

### Additional Strong Open-Source Options

- **Adyen Android POS app** — A free, open-source POS app that runs directly on Adyen Android payment terminals; ring up products, take payment, deliver receipt, and refund on the terminal itself . **Hardware-specific**—requires Adyen terminal and merchant account.
- **myPOS SDKs** — myPOS provides Android SDKs (Glass SDK, Smart SDK, Slave SDK) for integrating apps with myPOS terminals via Bluetooth or on-device APIs . **SDK, not an app**—enables building custom mPOS apps on myPOS hardware.

**Frameworks for building custom systems**: For **general mobile POS app development**, EasySell and flutter_pos provide production-quality Flutter reference architectures with offline sync and thermal printing . For **crypto payments**, Numo (Bitcoin/Cashu) and Monero Merchant provide complete self-hosted solutions . For **custom Android terminal apps**, PAX/Castles/Verifone SDKs enable development on certified hardware. No open-source project handles **card-present acquiring and settlement**—those require commercial processor relationships and PCI-certified infrastructure.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- mPOS platforms handling payment card data must comply with **PCI DSS** requirements; self-hosted solutions require careful security hardening and should never store raw card data unless fully certified.
- **Open-source mPOS is strongest for app development and crypto payments**—Flutter reference apps provide the storefront/order layer, and Numo/Monero Merchant handle crypto rails. However, **no open-source project replicates the integrated card acquiring, settlement, and hardware certification** of Square Terminal or Clover Flex. Merchants requiring card-present payments should use commercial terminals or integrate certified SDKs from PAX, Castles, or Ingenico.
- Verify license terms for commercial use; EasySell and flutter_pos are open-source (check repositories), Numo uses MIT , and Monero Merchant uses GPL-3.0 .

---

**Made for retail operators, restaurant managers, mobile developers, and payment terminal engineers.**  
Let's make mobile point of sale more open, but with clear eyes about the card acquiring and hardware certification gap that remains.
