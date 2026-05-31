# 🚀 Auto Clicker Pro — Google Play Store Publishing Checklist

## 📦 PART 1: Technical Requirements

### 1.1 App Icons (Multiple sizes)

Aap AI se 1024x1024 icon banao, phir online resize karo. Sizes needed:

| Folder | Size | Purpose |
|---|---|---|
| `mipmap-mdpi` | 48×48 | Standard density |
| `mipmap-hdpi` | 72×72 | Hi-density |
| `mipmap-xhdpi` | 96×96 | Extra-hi |
| `mipmap-xxhdpi` | 144×144 | Most modern phones |
| `mipmap-xxxhdpi` | 192×192 | Latest flagships |
| Play Store listing | **512×512** | Required for upload |
| Feature graphic | **1024×500** | Banner on Play Store |

**Tool to resize:** https://romannurik.github.io/AndroidAssetStudio/icons-launcher.html

### 1.2 Signed APK / AAB (Release Build)

Sketchware Pro me:
1. Project Settings → **App Signing**
2. Generate keystore (PEHLI BAAR ONLY — bahut zaroori, isi se future updates sign karoge!)
3. Save keystore file in safe place (Google Drive, etc.) — agar lost ho gaya, future me app update NAHI kar sakte
4. Build → **Sign APK** → release mode

**Better:** **AAB (Android App Bundle)** export karo — Play Store recommend karta hai, APK se chhoti size.

### 1.3 App Details

| Field | Suggested |
|---|---|
| Package name | `com.you.autoclickerpro` (already set) |
| App name | Auto Clicker Pro |
| Version code | 1 |
| Version name | 1.0.0 |
| Min SDK | 21 (Android 5.0) |
| Target SDK | **34** (Android 14) — Play Store requires |
| Compile SDK | 34 |

### 1.4 Screenshots (Required)

Minimum **2 screenshots**, recommended **4-8**:
- **Phone**: 1080×1920 or 1080×2400 (PNG/JPG)
- **7-inch tablet** (optional): 1200×1920
- **10-inch tablet** (optional): 1800×2560

**What to show:**
1. Home screen with floating panel
2. Markers placed on a target app (e.g., game/calculator)
3. Settings screen
4. Scripts list
5. Playing/working demonstration

---

## ⚖️ PART 2: Legal/Policy Requirements (CRITICAL)

### 2.1 Privacy Policy (MANDATORY)

Auto-clicker apps **MUST** have a privacy policy because they use:
- Accessibility Service
- Overlay permission

Free privacy policy generator: **https://app-privacy-policy-generator.firebaseapp.com/**

Fill in:
- App name: Auto Clicker Pro
- Email: your-email@gmail.com
- Data collected: None (if you don't collect)
- Permissions used: Accessibility, System Alert Window

Host the policy on:
- **GitHub Pages** (free): Create a `.md` file → enable Pages → get URL
- **Google Sites** (free)
- **Blogger** (free)

URL example: `https://yourname.github.io/autoclicker-privacy/`

### 2.2 Accessibility Service Justification ⚠️ MOST CRITICAL

Google Play **strictly reviews** apps using AccessibilityService. App can be **rejected/removed** if not justified properly.

Aapko **Play Console me declaration** dena hoga:
- **Why accessibility?** "To programmatically dispatch touch gestures for the user's recorded automation sequences."
- **Alternative?** "No standard Android API allows touch dispatching outside the app's own window without root."
- **User benefit?** "Saves time for repetitive tasks, helps disabled users, enables UI testing."

**IMPORTANT:** Auto-clicker apps **often get rejected** by Google. To improve approval chances:
- Mention **accessibility for disabled users** prominently
- DON'T market as "game cheat" or "auto farm"
- Mention "UI testing", "productivity", "repetitive task automation"

### 2.3 Content Rating

Fill out Play Console questionnaire:
- Violence: No
- Sex/Nudity: No
- Profanity: No
- Drugs: No
- Gambling: No
- User-generated content: No

**Expected rating:** Everyone / PEGI 3

### 2.4 Target Audience

- Age: **18+** recommended (safer for app review since auto-clickers can be misused)

### 2.5 Data Safety Section

Fill in Play Console "Data Safety":
- **Data collected:** None (if true)
- **Data shared:** None
- **Data encrypted in transit:** N/A
- **Users can request deletion:** N/A

---

## 📝 PART 3: Listing Content

### 3.1 Short Description (80 chars max)
```
Record and replay screen taps. Save time on repetitive tasks.
```

### 3.2 Full Description (4000 chars max)
```
🎯 Auto Clicker Pro — Smart Tap Automation

Save hours on repetitive tasks with the easiest auto-clicker for Android!

✨ KEY FEATURES
• Add unlimited click points anywhere on screen
• Per-click custom delays (seconds, precise control)
• Smart loop count or unlimited replay
• Floating panel — works over any app
• Save scripts and replay anytime
• Smooth marker drag for pixel-perfect positioning
• Pause / Resume / Stop controls
• Beautiful dark mode

🛠 HOW IT WORKS
1. Enable Accessibility and Overlay permissions
2. Open floating panel
3. Tap "+" to place click markers
4. Drag markers to exact positions
5. Tap markers to set per-click timing
6. Press Play — your clicks auto-repeat!

💡 PERFECT FOR
• Repetitive form filling
• UI testing for developers
• Helping users with motor disabilities
• Productivity automation
• Reading/scrolling routines

🔒 PRIVACY FIRST
• No data collection
• No internet access required
• All scripts saved locally on your device
• No ads (or specify your ad policy)

⚠️ IMPORTANT NOTES
• Cannot bypass FLAG_SECURE on banking apps (Android security)
• For personal use only — please respect app terms of service
• Not affiliated with any specific game or app

📧 Contact: your-email@example.com
🌐 Privacy Policy: https://your-privacy-policy-url
```

### 3.3 Category
- Primary: **Productivity** or **Tools**

### 3.4 Keywords (in description)
auto clicker, automation, tap, click, recorder, productivity,
accessibility, macro, repeat, script

---

## 💰 PART 4: Monetization (Optional)

### 4.1 Free vs Paid
- **Free with AdMob**: Add banner ads (your `BannerAd.tsx` already has placeholder)
- **Free with in-app purchase**: Unlock premium features (unlimited scripts, no ads)
- **Paid app**: One-time fee ($1.99 - $4.99)

### 4.2 AdMob Setup (if going free + ads)
1. Sign up at https://admob.google.com
2. Create app → get App ID
3. Create ad units → get Ad Unit IDs
4. Add SDK + IDs to code (BannerAd.tsx already prepared)
5. Add AdMob app ID to AndroidManifest.xml

---

## 📤 PART 5: Submission Process

### 5.1 Google Play Console Setup
1. Pay **$25 one-time** developer fee at https://play.google.com/console
2. Create developer account
3. Verify identity (passport/ID + selfie)
4. Wait 1-3 days for approval

### 5.2 Create App in Console
1. Console → Create app
2. Fill app name, language, type (App / Game)
3. Free or paid
4. Declarations

### 5.3 Upload AAB
1. **Production** → Create release
2. Upload signed AAB
3. Release notes ("Initial release")
4. Save → Review release

### 5.4 Fill Store Listing
- App name
- Short + full description
- Icon (512×512)
- Feature graphic (1024×500)
- Screenshots (min 2)
- Privacy policy URL
- Contact email

### 5.5 Content Rating
- Fill questionnaire
- Get rating

### 5.6 Pricing & Distribution
- Free / Paid
- Countries
- Device categories (Phone, Tablet)

### 5.7 App Content Section
- Privacy policy
- App access (if any features locked)
- Ads (Yes/No)
- Content rating
- Target audience (18+)
- News app: No
- COVID-19 contact tracing: No
- Data safety
- **Government apps: No**
- **Financial features: No**

### 5.8 Send for Review
- Click "Send for review"
- Wait **1-7 days** for approval
- Auto-clicker apps often take longer or get rejected

---

## ⚠️ COMMON REJECTION REASONS (Avoid these!)

| Reason | Fix |
|---|---|
| **No privacy policy** | Add hosted privacy policy URL |
| **Accessibility misuse** | Justify with "for users with disabilities" |
| **Marketed as cheat tool** | Don't mention games, farming, cheating |
| **No data safety form** | Fill it completely |
| **Target SDK too old** | Use Android 14 (API 34) |
| **Unclear permissions** | Add tooltips explaining each permission |
| **No screenshots** | Add at least 4 phone screenshots |

---

## 🎁 BONUS: Pre-launch Recommendations

1. **Test on real devices** (not just emulator) — Android 8 through 14
2. **Internal testing track** first — invite 5-10 friends via Play Console
3. **Open testing track** — public beta to gather feedback
4. **Then production** — after stable

---

## ✅ FINAL CHECKLIST BEFORE SUBMISSION

- [ ] Signed AAB built and tested
- [ ] App icon 512×512 ready
- [ ] Feature graphic 1024×500 ready
- [ ] 4+ phone screenshots
- [ ] Privacy policy hosted online (working URL)
- [ ] Accessibility service description detailed in app + Play Console
- [ ] Target SDK 34
- [ ] Tested on Android 12+
- [ ] No crashes on launch
- [ ] All permissions explained
- [ ] Data safety form filled
- [ ] Content rating filled
- [ ] Developer account verified ($25 paid)
- [ ] Marketing language is NOT cheat/farming/game
