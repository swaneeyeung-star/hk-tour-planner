# Changelog

### v1.0.2 — 2026-11-19
- **Guest disclaimer modal** after "Enter as guest": warns that all progress (collected coins, mascots, constructed routes) disappears if you leave the website during guest mode and is only saved with an account; offers **Sign up / Create account** (existing create-account flow, carry-over preserved) or **Continue as guest** (original guest entry). Translated in all 7 languages (en, zh-Hant, zh-Hans, fr, ja, ko, es).
- **Guest mode custom routes default to 0** — fresh guest sessions start with zero user-constructed routes ("My routes (0)"); logged-in account route storage unchanged.
- Unchanged: coins default 100 (guest + new accounts), guest → account carry-over, +15 🪙 first-review reward, all coin spending.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.2

### v1.0.1 — 2026-11-19
- Coins default set to **100** for guest sessions and freshly created accounts (previously 0).
- Guest entry (`authEnterGuest`) now seeds 100 coins instead of forcing 0.
- Account creation now injects a 100-coin default when no browser progress carries over; earned carry-over balances are preserved unchanged.
- Unchanged: saved balances, +15 🪙 first-review reward, mascot rewards (+30 / hidden +60), all coin spending.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.1

## v1.0.0 — 2026-11-19
- First tracked build: 42 real Sai Kung restaurants with source-labelled ratings; misplaced pins re-geocoded to building level (incl. Chuen Kee Seafood both branches); guest-mode sign-in from the map sidebar; first-person walk mode; in-page reviews with photo upload; 7-language UI.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.0
