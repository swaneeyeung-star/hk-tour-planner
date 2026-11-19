# Changelog

### v1.0.3 — 2026-11-19
- **Mobile map-first layout** — on phones the map now fills the entire screen; the sidebar becomes a slide-in drawer behind a ☰ toggle (✕, backdrop tap or Escape closes it), so no feature permanently covers the map.
- **On-demand panels** — Leaflet place popups capped to 40vh with scroll; guest disclaimer, account, finish-picker and tutorial boxes constrained to ≤84dvh with scroll; welcome card fits small screens; compact banner/toast placement; safe-area (notch / home-indicator) padding.
- **Desktop untouched** — every new rule is scoped inside one new media block `@media (max-width:900px),(pointer:coarse) and (max-height:520px)`; the legacy 820px block is preserved (overridden) and all base rules are byte-identical.
- Unchanged: all features, coins default 100 (guest + new accounts), guest routes default 0, guest disclaimer, +15 🪙 first-review reward, 7-language UI.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.3

### v1.0.2 — 2026-11-19
- **Guest disclaimer modal** after "Enter as guest": warns that all progress (collected coins, mascots, constructed routes) disappears if you leave the website during guest mode and is only saved with an account; offers **Sign up / Create account** (existing create-account flow, carry-over preserved) or **Continue as guest** (original guest entry). Translated in all 7 languages (en, zh-Hant, zh-Hans, fr, ja, ko, es).
- **Guest mode custom routes default to 0** — fresh guest sessions start with zero user-constructed routes ("My routes (0)"); logged-in account route storage unchanged.
- Unchanged: coins default 100 (guest + new accounts), guest ↔ account carry-over, +15 🪙 first-review reward, all coin spending.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.2

### v1.0.1 — 2026-11-19
- Coins default set to **100** for guest sessions and freshly created accounts (previously 0).
- Guest entry (`authEnterGuest`) now seeds 100 coins instead of forcing 0.
- Account creation now injects a 100-coin default when no browser progress carries over; earned carry-over balances are preserved unchanged.
- Unchanged: saved balances, +15 🪙 first-review reward, mascot rewards (+30 / hidden +60), all coin spending.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.1

## v1.0.0 — 2026-11-19
- First tracked build: 42 real Sai Kung restaurants with source-labeled ratings; misplaced pins re-geocoded to building level (incl. Chuen Kee Seafood both branches); guest-mode sign-in from the map sidebar; first-person walk mode; in-page reviews with photo upload; 7-language UI.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.0
