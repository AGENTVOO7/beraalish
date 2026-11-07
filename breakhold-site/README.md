# Breakhold — app-ads.txt (GitHub Pages)

Ye repo sirf ek kaam ke liye hai: `app-ads.txt` ko developer website ke **ROOT** pe serve karna, taaki AdMob app verify ho jaye.

## Files
- `app-ads.txt` — AdMob ki line (pub-2732441298536316)
- `index.html` — simple homepage (website khali na dikhe)
- `.nojekyll` — GitHub Pages ko file jaisi hai waisi serve karne ke liye

## Setup (5 minute)

### 1. Repo ka naam EXACT ye rakho
```
<aapka-github-username>.github.io
```
Example: username `rahuldev` hai to repo ka naam `rahuldev.github.io`.
Repo **Public** hona chahiye.

> Sabse common galti: repo ka naam kuch aur rakha (jaise `breakhold`) to file
> `https://rahuldev.github.io/breakhold/app-ads.txt` pe aati hai — ye ROOT nahi hai, AdMob reject kar dega.

### 2. Files upload karo
Repo kholo → **Add file → Upload files** → is zip ke andar ki saari files
(`app-ads.txt`, `index.html`, `.nojekyll`, `README.md`) seedha repo ke main folder me daalo — kisi sub-folder me nahi.
`.nojekyll` hidden file hai; upload me na dikhe to **Add file → Create new file**, naam `.nojekyll`, khali chhod ke commit.

### 3. GitHub Pages on karo
Repo → **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main` / `(root)` → Save.
1–2 minute baad check karo:
```
https://<username>.github.io/app-ads.txt
```
Browser me sirf ye ek line dikhni chahiye:
```
google.com, pub-2732441298536316, DIRECT, f08c47fec0942fa0
```

### 4. Google Play Console me website set karo (ZAROORI)
Play Console → Breakhold → **Grow users → Store presence → Store settings → Store listing contact details → Website**
```
https://<username>.github.io
```
- Aage koi `/breakhold` ya `/` ke baad path nahi.
- `www` mat lagao.
- Save karo. Play Store page pe update hone me kuch ghante lag sakte hain.

### 5. AdMob me verify karo
AdMob → Apps → Breakhold → **App settings → app-ads.txt → Check for updates**.
Verification me 24 ghante tak lag sakte hain (kabhi kabhi jaldi ho jata hai).

## Agar phir bhi fail ho
- `https://<username>.github.io/app-ads.txt` khol ke dekho — 404 aaye to repo naam / Pages setting galat hai.
- Play Store listing pe "Website" wahi URL hai jo upar hai? Ek bhi character alag hua to "details don't match" aata hai.
- Line me pub ID AdMob account wali hi ho: AdMob → Settings → Account information → Publisher ID.
- Future me koi aur ad network (Unity Ads, AppLovin...) jodo to unki line bhi isi file me nayi line pe add karna.
