# InvestAi (Flutter) — GitHub Actions Ready

This repo builds a fresh Android APK on each push to `main` and on `workflow_dispatch`.

## How to use
1. Create a new public GitHub repository and upload this project.
2. Go to Settings → Secrets and variables → Actions → **New repository secret**:
   - Name: `NOWPAY_API_KEY`
   - Value: your NOWPayments API key string
3. Go to Actions → run **Build InvestAi APK**.
4. Download artifact `investai-apk` → `app-release.apk`.

## Notes
- The workflow generates a **fresh Android** folder via `flutter create` (so Gradle & AGP are always up to date).
- `intl` is pinned to `^0.19.0` to match `flutter_localizations`.
- Region guard blocks likely Iran locales except whitelisted email `nimafarzadi21@gmail.com`.
- Yields and rewards are **display-only** per your requirements.
