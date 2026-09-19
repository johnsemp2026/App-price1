# PPDA Price List – Native Android App

**Full native Android app** for the PPDA Uganda Common User Items Average Prices (FY 2019/20).

## Features
- Fully offline (no internet required after install)
- Fast search by item name, code, details or category
- Category filter chips
- Regional prices: Kampala, Mbarara, Mbale, Gulu + Average
- Clean Material 3 UI with your PPDA Supplies Store logo
- 1,080 items from the official survey data
- Independent of Chrome / browser

## How to build

### Requirements
- Android Studio Hedgehog (2023.1.1) or newer
- JDK 17

### Steps
1. Open the project folder `PPDAPriceList` in Android Studio
2. Let Gradle sync (it will download dependencies)
3. Connect a device or start an emulator (API 24+)
4. Click **Run** ▶

### Generate APK / AAB
- **Debug APK**: `Build → Build Bundle(s) / APK(s) → Build APK(s)`
- **Release AAB** (for Play Store):  
  `Build → Generate Signed Bundle / APK` → choose Android App Bundle

## Project structure
```
app/
  src/main/
    assets/ppda_prices.json     ← the full price list (1080 items)
    java/com/ppda/pricelist/
      MainActivity.kt
      data/
        PriceItem.kt
        PriceRepository.kt
      ui/
        PriceViewModel.kt
        Components.kt
        theme/Theme.kt
    res/
      drawable/logo.png         ← your logo
      ...
```

## Notes
- Prices are indicative averages from the PPDA 2019/20 survey.
- Always verify current market rates before procurement.
- The app is completely self-contained – no Chrome dependency.

---
Built as a true native Android app (Kotlin + Jetpack Compose).
