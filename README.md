# Shrisha Garments — Netlify Deployment Guide

## 📁 Folder Structure
```
shrisha-netlify/
│
├── index.html              ← Main website
├── netlify.toml            ← Netlify configuration
│
├── admin/
│   ├── index.html          ← CMS Admin Panel (yoursite.com/admin)
│   ├── config.yml          ← CMS field definitions
│   └── site-settings.json  ← Site-wide settings (phone, email, tagline...)
│
└── products/
    ├── classic-white-crew-neck.md
    ├── urban-graphic-tee.md
    ├── heritage-polo.md
    ├── oversized-drop-shoulder.md
    ├── mandala-print-tee.md
    └── gold-edition-tee.md
```

---

## 🚀 Step 1 — Push to GitHub (Required for CMS)

1. Go to **github.com** → Sign up free
2. Click **New Repository** → Name it `shrisha-garments`
3. Set to **Public** → Create
4. Upload ALL files (drag & drop the entire folder)
5. Click **Commit changes**

---

## 🌐 Step 2 — Deploy on Netlify

1. Go to **netlify.com** → Sign up with GitHub
2. Click **Add new site** → **Import an existing project**
3. Choose **GitHub** → Select `shrisha-garments` repo
4. Build settings:
   - Build command: *(leave empty)*
   - Publish directory: `.`
5. Click **Deploy site**
6. Your site is live at: `https://shrisha-garments.netlify.app`
   *(You can change this subdomain in Site Settings)*

---

## 🔐 Step 3 — Enable Admin Panel (Netlify Identity)

1. In Netlify dashboard → Go to **Identity** tab
2. Click **Enable Identity**
3. Under **Registration** → Set to **Invite only** (important!)
4. Scroll to **Git Gateway** → Click **Enable Git Gateway**
5. Go to **Identity** → **Invite users** → Enter your email → Send invite
6. Check your email → Click the invite link → Set your password

**Your Admin Panel is now live at:**
`https://your-site-name.netlify.app/admin`

---

## ✏️ Step 4 — Using the Admin Panel

### To Add a Product:
1. Go to `/admin` → Log in
2. Click **T-Shirts** in left sidebar
3. Click **New T-Shirts**
4. Fill in: Name, Price, Category, Sizes, Colors, Badge, etc.
5. Click **Publish** → Product appears on site within seconds

### To Edit a Product:
1. Go to `/admin` → **T-Shirts**
2. Click the product name
3. Change any field
4. Click **Save** → Live instantly

### To Delete a Product:
1. Open the product in admin
2. Click the **⋮** menu → **Delete**

### To Change Site Settings (phone, email, tagline):
1. Go to `/admin` → **Site Settings** → **General Settings**
2. Update any field → **Save**

---

## 📝 Manual Edit (Alternative — No Admin)

Open any file in `/products/` with Notepad and change values:
```yaml
price: 899         ← Change price
badge: "Sale"      ← Add sale badge
inStock: false     ← Mark out of stock
```
Then re-upload to Netlify (drag & drop).

---

## 🎨 Badge Options
| Badge      | Color      |
|------------|------------|
| New Arrival| Black      |
| Bestseller | Gold       |
| Sale       | Terracotta |
| Limited    | Terracotta |
| Trending   | Gold       |
| (empty)    | No badge   |

## 🎨 Card Color Options
| Color Name     | Hex      |
|----------------|----------|
| Dark Charcoal  | #1A1A1A  |
| Warm Ivory     | #F5F0E8  |
| Navy Blue      | #1B2A4A  |
| Forest Green   | #2D4A3E  |
| Terracotta     | #C4856A  |
| Dusty Rose     | #D4A5A5  |
| Slate Blue     | #3D5A80  |
| Warm Tan       | #C9A97A  |

---

*Built for Shrisha Garments — 2025*
