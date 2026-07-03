# TradeSmart Website — Setup Guide

## 1. Files ko customize karo (upload karne se pehle)

### `index.html` mein replace karo:
- `VIDEO_ID_HERE` → tumhara hero intro video ka YouTube ID (link: `youtube.com/watch?v=XXXX` mein XXXX wala part)
- `assets/photo.jpg` → apni actual photo isi naam se `assets` folder mein daal do (ya naam badal ke HTML mein bhi update kar do)
- `RAZORPAY_PAYMENT_LINK_HERE` → apna Razorpay Payment Link (neeche steps hain)
- `91XXXXXXXXXX` → apna WhatsApp number (country code ke saath, bina + ke)

### `indicator.html` mein replace karo:
- `YOUR_UNLISTED_INDICATOR_VIDEO_ID` → indicator wale video ka YouTube ID (Unlisted upload karna)
- `YOUR_GOOGLE_FORM_LINK_HERE` → apna Google Form ka link

### `copy-trading.html` mein replace karo:
- `YOUR_UNLISTED_STEP1_VIDEO_ID` → Step 1 (IB join) wale video ka ID (Unlisted)
- `YOUR_GOOGLE_FORM_LINK_HERE` → same Google Form ya alag form, jismein Vantage account number + email maangoge
- Step 2 wala video abhi locked hi rahega — jab tak koi verify na ho, uska link kisi ko mat do. Verify hone ke baad us banda ko personally (WhatsApp/email) unlisted link bhej dena.

---

## 2. Razorpay Payment Link kaise banayein (Free)

1. [razorpay.com](https://razorpay.com) par free account banao (business details verify karni hongi — PAN/bank account chahiye hoga)
2. Dashboard → **Payment Links** → **Create Payment Link**
3. Amount: ₹830 (~$10) ya jo bhi rakhna ho, Title: "1-on-1 Trading Call"
4. Link generate hoga — usi ko `index.html` mein `RAZORPAY_PAYMENT_LINK_HERE` ki jagah paste kar dena

---

## 3. Google Form kaise banayein (Free)

1. [forms.google.com](https://forms.google.com) par jao → naya form banao
2. Fields: Name, Email, Vantage Account Number
3. Top-right **Send** button → link copy karo → wahi link HTML mein daal do
4. Responses **Google Sheets** mein automatically aayenge (Form ke "Responses" tab mein Sheets icon)

---

## 4. YouTube videos Unlisted kaise upload karein

1. YouTube Studio → Upload
2. Visibility mein **"Unlisted"** choose karo (Public ya Private nahi)
3. Video ka link kisi ko bhi bhej sakte ho, search mein nahi aayega
4. Video ID: link ka last part — `youtube.com/watch?v=ABC123XYZ` mein `ABC123XYZ`

---

## 5. GitHub Pages par Free Host kaise karein

1. [github.com](https://github.com) par account banao (agar nahi hai)
2. New Repository banao — naam kuch bhi, e.g. `tradesmart-website`
3. Is poore folder (`tradesmart-site`) ke saare files us repo mein upload kar do:
   - GitHub website par "Add file" → "Upload files" → sab files drag-drop karo → Commit
4. Repo ke **Settings** → **Pages** (left sidebar mein) jao
5. **Source**: "Deploy from a branch" → Branch: `main` → folder: `/ (root)` → Save
6. 1-2 minute mein tumhara site live ho jayega: `https://tumhara-username.github.io/tradesmart-website/`

Custom domain chahiye to (optional): Settings → Pages mein "Custom domain" field mein apna domain daal do (domain khareedna paid hai, but agar already hai to attach karna free hai).

---

## File Structure
```
tradesmart-site/
├── index.html          (homepage)
├── indicator.html       (free indicator page)
├── copy-trading.html    (copy trading page)
├── style.css            (saara design)
└── assets/
    └── photo.jpg         (apni photo replace karo)
```
