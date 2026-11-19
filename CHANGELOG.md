# Changelog

### v1.0.8 — 2026-11-19
- **Tutorial spotlight: full-screen shade with a lit cutout** — during the guide a dark shade (rgba(15,25,35,.58)) now covers the entire screen except a clean cutout around the area the current step describes; the described area stays highlighted with its blue outline, glow and a subtle blue tint. Replaces the previous giant 9999px box-shadow approach (unreliable on iOS/Safari) with a real full-screen shade layer (#tourDim) that punches the hole via clip-path.
- **Tap-blocking unchanged** — the shade layer swallows every tap/touch outside the lit cutout (the tour's own Next/Back/Done buttons stay clickable), so mistaps are still impossible during the guide; sidebar-targeting steps still auto-open the mobile menu and the cutout recomputes during transitions, on resize and on menu toggles.
- **Housekeeping** — internal version comments updated to v1.0.8 (PWA + mobile-map-first comments).
- Unchanged: desktop layout, mobile map-first layout, all 8 tour steps and texts, coins, rewards, routes, PWA/offline shell, 7-language UI.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.8

### v1.0.7 — 2026-11-19
- **Review cap reworked — your own reviews, per local calendar day** — the counter now reads "Reviews used today: 0 of 2" before your first review, counts only reviews authored by the current user with today's local-date timestamp (other users' and seeded reviews never count), and locks with a translated daily-limit toast after the 2nd. +15 🪙 first-review reward untouched.
- **Rebrand: "Wanderbos"** — every user-facing "mascot" wording is now Wanderbos across the UI in all 7 languages (en, zh-Hant, zh-Hans, fr, ja, ko, es), including hardcoded English strings, aria-labels, the guest disclaimer, tour texts and the collectibles-page title (🐣 Wanderbos). Identifiers/keys unchanged.
- **Tutorial rebuilt as a spotlight tour with tap-blocking** — every step now squares the exact section it describes (solid blue outline + glow; all 8 steps targeted: map, start controls, trip settings, route buttons, sim-walk, Wanderbos gallery, coins chip). A full-screen capture layer swallows every tap outside the spotlight and the tour's own buttons, so users can't mistap during the guide. Sidebar-feature steps auto-open the mobile menu and the spotlight recomputes during the transition, on resize and on menu toggles — fixing the mobile complaint that steps 2–4 explained unseeable left-column controls. Desktop layout untouched.
- **Wanderbos looks integrated** — costume overlays now rotate with the character (per-look rot finally consumed) instead of sitting at a fixed angle, each of the 24 looks (4 packs × 6 styles) gets its own pose transform (rotate/scale/flip) and color grade, and costume art gains drop-shadow blending — no more pasted-on look. Collectible count (16) and all rewards unchanged.
- Unchanged: desktop layout, mobile map-first layout, coins, rewards (+30/+60, +15 first review), routes, PWA/offline shell, 7-language UI.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.7

### v1.0.6 — 2026-11-19
- **Mascot packs redesigned** — every collectable in a character pack now has its own distinct form: unique costume (chef toque, captain's & sailor caps, straw & sun hats, ranger & hard hats, explorer kit, baker's toque, party hat), props (lantern, incense, scroll, map, swim ring, surfboard, flower), sunglasses and individual poses — replacing the old colour-filter clones. All 24 pack-style looks are visually distinct across the 4 packs.
- **Review cap: 2 per user** — each user can submit a maximum of 2 restaurant reviews (account or guest scope); the review form shows a live "reviews used: n/2" counter, locks at the limit, and a toast explains it in all 7 languages (en, zh-Hant, zh-Hans, fr, ja, ko, es). Stops coin farming.
- **Pin position fixes** — Seafood Island Restaurant moved from open water (~11 km SE of town) to Po Toi O village; Thai Dao moved to its real Sha Ha waterfront spot; Sai Kung Seafood Street, Man Tsai Kee and Cafe Pawsitive nudged onto the promenade line (off the water); Kachimushi de-overlapped from TAPS.
- Unchanged: coins, rewards (+30/+60 mascots, +15 first review), routes, desktop & mobile layouts, 7-language UI, PWA/offline shell.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.6

### v1.0.5 — 2026-11-19
- **Installable mobile app (PWA)** — the planner installs to a phone's home screen with its own app icon and opens fullscreen in standalone mode with no browser bars (Android/desktop via native install prompt; iPhone/iPad via Share → Add to Home Screen).
- **App icon** — generated map-pin icon in the app's mint-green/sky-blue palette, published at 512/192/180 px (icons/icon-512.png, icons/icon-192.png, icons/apple-touch-icon.png).
- **Web app manifest** — manifest.webmanifest: name "Sai Kung Tour Planner", standalone display, theme color #0e7c66, regular + maskable icons.
- **Offline shell** — service worker (sw.js) precaches the app shell; navigation requests are network-first so updates land immediately, other same-origin assets are cache-first; old caches cleaned on activate.
- **Install button + help modal** — "Install app" chip at the bottom of the sidebar next to the 🌐 language chip; on devices without a native install prompt it opens a per-platform help modal.
- **7-language install strings** — the button label and help modal follow the chosen language (en, zh-Hant, zh-Hans, fr, ja, ko, es).
- Unchanged: desktop layout, mobile map-first layout, all features, coins, reviews, ratings.
- Release: https://github.com/swaneeyeung-star/hk-tour-planner/releases/tag/v1.0.5

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