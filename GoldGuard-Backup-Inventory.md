# GoldGuard backup inventory

Snapshot includes all active source, configuration, tests/fixtures, runtime assets, vendor licences and existing textual documentation, preserving paths in source/. New archive documentation is in ownership/. Source and data archives are separate. Files with private credentials/runtime state are not required and are not included.

## Major directories

| Directory | Purpose | Rebuild status |
|---|---|---|
| app | Root page/layout, styles, auth helper | required |
| components | Consumer/journey/report/rate/information UI and all shared UI components | required, including unused starter components for completeness |
| lib | Models, calculations, validation, storage, fields, journey/utilities | required |
| hooks | Mobile hook | required as referenced |
| public | SVG/icon/image runtime assets | required |
| build | Sites Vite plugin and licence | required |
| scripts | Build/dev/install/environment wrappers and historical regression script | required/recovery tooling |
| tests | Four test suites and synthetic fixture generator | test/recovery required |
| vendor | Vendored Tailwind/shadcn CSS and licence | required |
| db, drizzle, examples | Inactive database scaffolding/example | preserved, not active transaction backend |
| docs | Existing textual QA/legal/release documents | understanding/history; not build-required |
| .openai | Current hosting identity/null bindings | build imports it; identity not a secret |
| ownership | New documentation, manifests, verification | recovery required, not app runtime |

## Every included source file

| File | Bytes | Category/purpose | Required to build/run? | Generated? |
|---|---:|---|---|---|
| `.gitignore` | 598 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `.npmrc` | 45 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `.openai/hosting.json` | 91 | configuration/build/tooling | Yes/as referenced | No |
| `QA.md` | 4436 | historical documentation | Recovery/test/history or supporting config | No |
| `README.md` | 7990 | historical documentation | Recovery/test/history or supporting config | No |
| `app/chatgpt-auth.ts` | 2550 | source/component | Yes/as referenced | No |
| `app/globals.css` | 34049 | source/component | Yes/as referenced | No |
| `app/journey.css` | 5650 | source/component | Yes/as referenced | No |
| `app/layout.tsx` | 608 | source/component | Yes/as referenced | No |
| `app/page.tsx` | 50423 | source/component | Yes/as referenced | No |
| `build/sites-vite-plugin.LICENSE` | 1063 | configuration/build/tooling | Yes/as referenced | No |
| `build/sites-vite-plugin.ts` | 7185 | configuration/build/tooling | Yes/as referenced | No |
| `cloudflare-env.d.ts` | 99 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `components.json` | 420 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `components/goldguard-consumer.tsx` | 29559 | source/component | Yes/as referenced | No |
| `components/goldguard-information.tsx` | 19979 | source/component | Yes/as referenced | No |
| `components/goldguard-journey.tsx` | 10037 | source/component | Yes/as referenced | No |
| `components/goldguard-rates.tsx` | 6777 | source/component | Yes/as referenced | No |
| `components/goldguard-transaction-record.tsx` | 7218 | source/component | Yes/as referenced | No |
| `components/goldguard-ui.tsx` | 3153 | source/component | Yes/as referenced | No |
| `components/ui/accordion.tsx` | 2048 | source/component | Yes/as referenced | No |
| `components/ui/alert-dialog.tsx` | 5439 | source/component | Yes/as referenced | No |
| `components/ui/alert.tsx` | 1614 | source/component | Yes/as referenced | No |
| `components/ui/aspect-ratio.tsx` | 274 | source/component | Yes/as referenced | No |
| `components/ui/attachment.tsx` | 6002 | source/component | Yes/as referenced | No |
| `components/ui/avatar.tsx` | 2916 | source/component | Yes/as referenced | No |
| `components/ui/badge.tsx` | 1776 | source/component | Yes/as referenced | No |
| `components/ui/breadcrumb.tsx` | 2350 | source/component | Yes/as referenced | No |
| `components/ui/bubble.tsx` | 4699 | source/component | Yes/as referenced | No |
| `components/ui/button-group.tsx` | 2202 | source/component | Yes/as referenced | No |
| `components/ui/button.tsx` | 2392 | source/component | Yes/as referenced | No |
| `components/ui/calendar.tsx` | 7832 | source/component | Yes/as referenced | No |
| `components/ui/card.tsx` | 1987 | source/component | Yes/as referenced | No |
| `components/ui/carousel.tsx` | 5556 | source/component | Yes/as referenced | No |
| `components/ui/chart.tsx` | 10614 | source/component | Yes/as referenced | No |
| `components/ui/checkbox.tsx` | 1214 | source/component | Yes/as referenced | No |
| `components/ui/collapsible.tsx` | 795 | source/component | Yes/as referenced | No |
| `components/ui/combobox.tsx` | 9158 | source/component | Yes/as referenced | No |
| `components/ui/command.tsx` | 4818 | source/component | Yes/as referenced | No |
| `components/ui/context-menu.tsx` | 8268 | source/component | Yes/as referenced | No |
| `components/ui/dialog.tsx` | 4303 | source/component | Yes/as referenced | No |
| `components/ui/direction.tsx` | 506 | source/component | Yes/as referenced | No |
| `components/ui/drawer.tsx` | 4255 | source/component | Yes/as referenced | No |
| `components/ui/dropdown-menu.tsx` | 8418 | source/component | Yes/as referenced | No |
| `components/ui/empty.tsx` | 2396 | source/component | Yes/as referenced | No |
| `components/ui/field.tsx` | 6159 | source/component | Yes/as referenced | No |
| `components/ui/form.tsx` | 3757 | source/component | Yes/as referenced | No |
| `components/ui/hover-card.tsx` | 1526 | source/component | Yes/as referenced | No |
| `components/ui/input-group.tsx` | 5065 | source/component | Yes/as referenced | No |
| `components/ui/input-otp.tsx` | 2254 | source/component | Yes/as referenced | No |
| `components/ui/input.tsx` | 962 | source/component | Yes/as referenced | No |
| `components/ui/item.tsx` | 4486 | source/component | Yes/as referenced | No |
| `components/ui/kbd.tsx` | 862 | source/component | Yes/as referenced | No |
| `components/ui/label.tsx` | 606 | source/component | Yes/as referenced | No |
| `components/ui/marker.tsx` | 1864 | source/component | Yes/as referenced | No |
| `components/ui/menubar.tsx` | 8389 | source/component | Yes/as referenced | No |
| `components/ui/message-scroller.tsx` | 3992 | source/component | Yes/as referenced | No |
| `components/ui/message.tsx` | 2232 | source/component | Yes/as referenced | No |
| `components/ui/native-select.tsx` | 1995 | source/component | Yes/as referenced | No |
| `components/ui/navigation-menu.tsx` | 6658 | source/component | Yes/as referenced | No |
| `components/ui/pagination.tsx` | 2717 | source/component | Yes/as referenced | No |
| `components/ui/popover.tsx` | 2357 | source/component | Yes/as referenced | No |
| `components/ui/progress.tsx` | 755 | source/component | Yes/as referenced | No |
| `components/ui/radio-group.tsx` | 1460 | source/component | Yes/as referenced | No |
| `components/ui/resizable.tsx` | 1815 | source/component | Yes/as referenced | No |
| `components/ui/scroll-area.tsx` | 1639 | source/component | Yes/as referenced | No |
| `components/ui/select.tsx` | 6353 | source/component | Yes/as referenced | No |
| `components/ui/separator.tsx` | 694 | source/component | Yes/as referenced | No |
| `components/ui/sheet.tsx` | 4188 | source/component | Yes/as referenced | No |
| `components/ui/sidebar.tsx` | 21526 | source/component | Yes/as referenced | No |
| `components/ui/skeleton.tsx` | 276 | source/component | Yes/as referenced | No |
| `components/ui/slider.tsx` | 1991 | source/component | Yes/as referenced | No |
| `components/ui/sonner.tsx` | 1034 | source/component | Yes/as referenced | No |
| `components/ui/spinner.tsx` | 331 | source/component | Yes/as referenced | No |
| `components/ui/switch.tsx` | 1408 | source/component | Yes/as referenced | No |
| `components/ui/table.tsx` | 2478 | source/component | Yes/as referenced | No |
| `components/ui/tabs.tsx` | 3782 | source/component | Yes/as referenced | No |
| `components/ui/textarea.tsx` | 759 | source/component | Yes/as referenced | No |
| `components/ui/toggle-group.tsx` | 2308 | source/component | Yes/as referenced | No |
| `components/ui/toggle.tsx` | 1565 | source/component | Yes/as referenced | No |
| `components/ui/tooltip.tsx` | 1830 | source/component | Yes/as referenced | No |
| `db/index.ts` | 423 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `db/schema.ts` | 169 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `docs/GOLDGUARD-FINAL-QA.md` | 8513 | historical documentation | Recovery/test/history or supporting config | No |
| `docs/LEGAL-REFERENCES.md` | 4829 | historical documentation | Recovery/test/history or supporting config | No |
| `docs/QA-AUDIT.md` | 9371 | historical documentation | Recovery/test/history or supporting config | No |
| `docs/RELEASE-NOTES-V1.2.md` | 2135 | historical documentation | Recovery/test/history or supporting config | No |
| `docs/TRANSACTION-UPGRADE-QA.md` | 7442 | historical documentation | Recovery/test/history or supporting config | No |
| `docs/V1.2-IMPLEMENTATION-CHECKLIST.md` | 1626 | historical documentation | Recovery/test/history or supporting config | No |
| `docs/final-regression.txt` | 7699 | historical documentation | Recovery/test/history or supporting config | No (historical test output is evidence only) |
| `drizzle.config.ts` | 148 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `drizzle/meta/_journal.json` | 61 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `eslint.config.mjs` | 846 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `examples/d1/app/api/notes/route.ts` | 1700 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `examples/d1/db/schema.ts` | 370 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `hooks/use-mobile.ts` | 565 | source/component | Yes/as referenced | No |
| `lib/goldguard/consumer-fields.ts` | 6905 | source/component | Yes/as referenced | No |
| `lib/goldguard/fields.ts` | 6420 | source/component | Yes/as referenced | No |
| `lib/goldguard/journey.ts` | 5844 | source/component | Yes/as referenced | No |
| `lib/goldguard/model.ts` | 35817 | source/component | Yes/as referenced | No |
| `lib/goldguard/storage.ts` | 2326 | source/component | Yes/as referenced | No |
| `lib/utils.ts` | 177 | source/component | Yes/as referenced | No |
| `next-env.d.ts` | 284 | configuration/build/tooling | Yes/as referenced | Yes; retained type bridge, regenerated routes by build |
| `next.config.ts` | 133 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `package.json` | 2085 | configuration/build/tooling | Yes/as referenced | No |
| `pnpm-lock.yaml` | 342352 | configuration/build/tooling | Yes/as referenced | No |
| `pnpm-workspace.yaml` | 759 | configuration/build/tooling | Yes/as referenced | No |
| `postcss.config.mjs` | 94 | configuration/build/tooling | Recovery/test/history or supporting config | No |
| `public/favicon.svg` | 303 | runtime asset | Yes/as referenced | No |
| `public/file.svg` | 392 | runtime asset | Yes/as referenced | No |
| `public/globe.svg` | 1036 | runtime asset | Yes/as referenced | No |
| `public/transaction-illustrations.png` | 963565 | runtime asset | Yes/as referenced | No |
| `public/window.svg` | 386 | runtime asset | Yes/as referenced | No |
| `scripts/build-verified.sh` | 661 | configuration/build/tooling | Yes/as referenced | No |
| `scripts/execution-profile.mjs` | 624 | configuration/build/tooling | Yes/as referenced | No |
| `scripts/final-regression.mjs` | 796 | configuration/build/tooling | Yes/as referenced | No |
| `scripts/install-ci.mjs` | 1685 | configuration/build/tooling | Yes/as referenced | No |
| `scripts/install-ci.sh` | 6783 | configuration/build/tooling | Yes/as referenced | No |
| `scripts/install-pnpm.sh` | 9024 | configuration/build/tooling | Yes/as referenced | No |
| `scripts/npm-install.mjs` | 7025 | configuration/build/tooling | Yes/as referenced | No |
| `scripts/pnpm-install.mjs` | 10642 | configuration/build/tooling | Yes/as referenced | No |
| `scripts/run-framework.mjs` | 993 | configuration/build/tooling | Yes/as referenced | No |
| `scripts/sites-env.mjs` | 906 | configuration/build/tooling | Yes/as referenced | No |
| `scripts/sites-env.sh` | 1530 | configuration/build/tooling | Yes/as referenced | No |
| `tests/consumer.test.mjs` | 14897 | tests/fixture | Recovery/test/history or supporting config | No |
| `tests/journey.test.mjs` | 4931 | tests/fixture | Recovery/test/history or supporting config | No |
| `tests/model.test.mjs` | 7983 | tests/fixture | Recovery/test/history or supporting config | No |
| `tests/release-critical.test.mjs` | 7657 | tests/fixture | Recovery/test/history or supporting config | No |
| `tests/transaction-fixtures.mjs` | 2432 | tests/fixture | Recovery/test/history or supporting config | No |
| `tsconfig.json` | 800 | configuration/build/tooling | Yes/as referenced | No |
| `vendor/shadcn-tailwind-4.13.0.LICENSE.md` | 1063 | historical documentation | Yes/as referenced | No |
| `vendor/shadcn-tailwind-4.13.0.css` | 16041 | configuration/build/tooling | Yes/as referenced | No |
| `vite.config.ts` | 2240 | configuration/build/tooling | Yes/as referenced | No |

## Intentionally excluded

- `tsconfig.tsbuildinfo` (585845 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `docs/GoldGuard-upgrade-desktop.jpg` (112353 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `docs/dashboard-preview.jpg` (87038 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `docs/GoldGuard-store-guide.png` (128390 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `docs/GoldGuard-app-info.png` (151876 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `docs/GoldGuard-upgrade-sample-report.pdf` (46419 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `docs/GoldGuard-sample-report.pdf` (38025 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `docs/GoldGuard-final-mobile.png` (39910 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `docs/GoldGuard-final-desktop.png` (89104 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `docs/GoldGuard-print-contact.png` (371211 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `docs/GoldGuard-v12-print-contact.png` (357782 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `docs/GoldGuard-final-customer-report.pdf` (51645 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `docs/GoldGuard-v12-sample-report.pdf` (40170 bytes): generated build cache or historical PDF/image QA output; reproducible, not a runtime asset. SHA-256 in EXCLUDED-FILES.json.
- `.sites-runtime/`: 5 observed files, 501484 bytes; generated dependencies, runtime/build state or caches; excluded.
- `node_modules/`: 51691 observed files, 1008376401 bytes; generated dependencies, runtime/build state or caches; excluded.
- `.next/`: 1 observed files, 990 bytes; generated dependencies, runtime/build state or caches; excluded.
- `.git/`: 300 observed files, 3092183 bytes; Git internals/history/config excluded to avoid credentials and obsolete content; current source commit preserved.
- `dist/`: 64 observed files, 3136291 bytes; generated dependencies, runtime/build state or caches; excluded.
- `.wrangler/`: 8 observed files, 45858 bytes; generated dependencies, runtime/build state or caches; excluded.

The full prearchive file inventory and aggregated generated-directory counts are in PREARCHIVE-INVENTORY.json; every included source file has size/SHA-256 in SOURCE-FILE-MANIFEST.json. No project .env files were present in the inspected root. No required untracked source was found other than generated next-env.d.ts, retained for type-check setup. No browser cache or customer JSON is in the source archive.

## Unavailable/external ownership items

Hosting platform infrastructure and authentication configuration exports, registrar account/nameserver ownership proof, SSL private keys, credentials, records from other devices/profiles/origins, deleted/unexported data and a complete offline npm package mirror are not included. See DISASTER-RECOVERY.md, THIRD-PARTY-SERVICES.md and DOMAIN-DNS.md. The current browser export is separate and contains only the accessible synthetic record; it is not a whole-account customer-data backup.
