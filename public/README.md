# ArakhaTime - Decap CMS Setup

## 📋 ဖိုင်တွေ GitHub ကို Upload လုပ်ပါ

### Option 1: GitHub Web Interface သုံးပြီး Upload

1. GitHub repository **arakhatime** သွားပါ
2. **public/** folder ထဲကို ဝင်ပါ
3. အောက်ပါ folders နှင့် files တွေကို upload လုပ်ပါ:

```
public/
├── admin/
│   ├── index.html
│   └── config.yml
├── _posts/
│   ├── news/.gitkeep
│   ├── casualties/.gitkeep
│   └── idp/.gitkeep
├── images/
│   └── uploads/.gitkeep
```

### Option 2: Git Command Line

```bash
# သင့် project folder သွားပါ
cd /path/to/arakhatime/public

# ဖိုင်တွေ copy လုပ်ပါ (ဒီ folder မှာ ရှိပြီးသား)
# အောက်က commands တွေ run ပါ

git add admin/
git add _posts/
git add images/
git commit -m "Add Decap CMS setup"
git push origin main
```

## 🚀 Netlify Setup လုပ်ပါ

### အဆင့် 1: Netlify Account ဖွင့်ပါ
1. [https://netlify.com](https://netlify.com) သွားပါ
2. **Sign up with GitHub** နှိပ်ပါ

### အဆင့် 2: Site Deploy လုပ်ပါ
1. **Add new site** → **Import an existing project**
2. **GitHub** ရွေးပါ
3. **arakhatime** repository ရွေးပါ
4. Build settings:
   - **Base directory**: `public`
   - **Build command**: (ဘာမှမထည့်ပါနဲ့)
   - **Publish directory**: `public`
5. **Deploy site** နှိပ်ပါ

### အဆင့် 3: Netlify Identity ဖွင့်ပါ
1. Site dashboard → **Site settings** → **Identity**
2. **Enable Identity** နှိပ်ပါ
3. **Registration preferences** → **Invite only** ရွေးပါ
4. **External providers** → လိုအပ်ရင် GitHub, Google ထည့်ပါ

### အဆင့် 4: Git Gateway ဖွင့်ပါ
1. **Identity** → **Services** → **Git Gateway**
2. **Enable Git Gateway** နှိပ်ပါ

### အဆင့် 5: Admin User ဖန်တီးပါ
1. **Identity** tab → **Invite users**
2. သင့် email ထည့်ပါ
3. Email ထဲက invitation link ကို နှိပ်ပါ
4. Password သတ်မှတ်ပါ

## 📝 CMS အသုံးပြုနည်း

ဒီ URL မှာ ဝင်ပါ:
```
https://YOUR-SITE-NAME.netlify.app/admin/
```

Login ဝင်ပြီး posts တွေ စရေးလို့ရပါပြီ!

## 📂 Folder Structure

```
public/
├── admin/              # CMS Dashboard
│   ├── index.html     # CMS UI
│   └── config.yml     # CMS Configuration
├── _posts/            # Content Storage
│   ├── news/          # Breaking News Articles
│   ├── casualties/    # Casualty Reports
│   └── idp/           # IDP Camp Data
├── images/
│   └── uploads/       # Uploaded Images
├── css/
├── js/
└── index.html         # Main Website
```

## 🎯 Content Collections

### 1. Breaking News (🔥)
- ခေါင်းစဉ်၊ ရက်စွဲ၊ အမျိုးအစား
- Status: HOT, ACTIVE, WATCH, CALM
- ဓာတ်ပုံ၊ အကျဉ်း၊ အကြောင်းအရာ
- သတင်းရင်းမြစ်၊ Tags

### 2. Casualties (💀)
- ဖြစ်ရပ်အမျိုးအစား (Airstrike, Ground Battle, etc.)
- တည်နေရာ (Township, Village, Lat/Lng)
- သေဆုံး/ဒဏ်ရာရမှု အရေအတွက်
- သေဆုံးသူများ အသေးစိတ်

### 3. IDP Camps (🏕️)
- စခန်းအမည်၊ တည်နေရာ
- လူဦးရေ၊ မိသားစုအရေအတွက်
- စခန်းအခြေအနေ
- လိုအပ်ချက်များ

## ⚠️ အရေးကြီးချက်

1. **Identity ဖွင့်ရမယ်** - မဟုတ်ရင် CMS login မရပါ
2. **Git Gateway ဖွင့်ရမယ်** - မဟုတ်ရင် GitHub ကို save မရပါ
3. **Invite only** သုံးပါ - လုံခြုံမှုအတွက်

## 🆘 အကူအညီ

- Netlify Docs: https://docs.netlify.com
- Decap CMS Docs: https://decapcms.org/docs/

---

**Setup ပြီးရင် ပြန်ပြောပါ၊ နောက်ထပ် ကူညီပါ့မယ်!** 🚀
