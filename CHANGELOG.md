# Changelog

### v1.0.4 — 2026-11-19
- **Walk speed default 1×** — simulated walks now start at 1× instead of 8× (1× button pre-selected).
- **Mascot popups no longer block the screen** — the mascot-discovery overlay is now a compact bottom-centered card (no full-screen dim) that auto-dismisses after ~4.5 s.
- **Mascots less intrusive during walks** — during a simulated walk only the first find shows the full card; subsequent finds appear as a small non-blocking top toast (rewards, coins and hidden finds unchanged).
- **More source-labeled ratings** — The Picture House 4.2/5·11 (TripAdvisor), Chip In Fish & Chips 4.1/5·42 (TripAdvisor), Sawadee Thailand 4.1/5·314 (Magicpin), The Conservatory 4.1/5·47 (TripAdvisor), Arm Coffee 4.1/5·214 (Magicpin), The Square 4.5/5·202 (Google). OpenRice "See live rating ↗" pointers added for Novas Pizzeria, Man Tsai Kee, Golden Chicken, Law of Yogurt (platforms block automated reads; no numbers invented).
- **Photo strips** — Sai Kung Public Pier, Waterfront Promenade, Seafood Street and both Chuen Kee branches now show multi-photo strips (Wikimedia Commons, credited).
- **Website chips** — place popups show an official-website link where verified: The Square, Winstons Coffee, 28 Restaurant, Paisano's, McDonald's, Volcano Discovery Centre (plus the existing Google Maps chip on every place).
- **Bigger icons** — POI pins 30→38 px, transport badges 34×26→42×32, start pin 26→34, floating mascots 38→46.
- Unchanged: desktop layout, mobile map-first layout, all features, coins, 7-language UI.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.4

### v1.0.3 — 2026-11-19
- **Mobile map-first layout** — on phones the map now fills the entire screen; the sidebar becomes a slide-in drawer behind a ☰ toggle (☰, backdrop tap or Escape closes it), so no feature permanently covers the map.
- **On-demand panels** — Leaflet place popups capped to 40vh with scroll; guest disclaimer, account, finish-picker and tutorial boxes constrained to ≤84dvh with scroll; welcome card fits small screens; compact banner/toast placement; safe-area (notch / home-indicator) padding.
- **Desktop untouched** — every new rule is scoped inside one new media block `@media (max-width:900px),(pointer:coarse) and (max-height:520px)`; the legacy 820px block is preserved (overridden) and all base rules are byte-identical.
- Unchanged: all features, coins default 100 (guest + new accounts), guest routes default 0, guest disclaimer, +15 🪙 first-review reward, 7-language UI.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.3

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

### v1.0.0 — 2026-11-19
- First tracked build: 42 real Sai Kung restaurants with source-labeled ratings; misplaced pins re-geocoded to building level (incl. Chuen Kee Seafood both branches); guest-mode sign-in from the map sidebar; first-person walk mode; in-page reviews with photo upload; 7-language UI.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.0
