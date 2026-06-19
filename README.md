# Pasha-GFW
<p align="center">
  <h1 align="center">🚀 Pasha-GFW</h1>
  <p align="center">
    Cloudflare Workers Based Subscription Panel
  </p>
</p>

---

## <img src="https://static.wixstatic.com/media/fbe150_de0ae4fc01c348d59b8d27f34a4fbeb5~mv2.png/v1/fill/w_503,h_288,al_c,q_85,enc_auto/Untitled%20design%20(8).png" alt="پرچم شیر و خورشید" width="28" height="16"> معرفی

Pasha-GFW یک پنل مدیریت اشتراک مبتنی بر Cloudflare Workers است که برای مدیریت کاربران، ساخت لینک اشتراک، مشاهده مصرف، تعیین محدودیت حجم و زمان انقضا طراحی شده است.
این پروژه بدون نیاز به VPS اجرا می‌شود و از زیرساخت Cloudflare استفاده می‌کند.

---

## ✨ امکانات
- 👥 مدیریت چند کاربر
- 📊 نمایش مصرف کاربران
- ⏳ محدودیت زمانی
- 📦 محدودیت حجم مصرفی
- 🔗 لینک اشتراک اختصاصی
- ⚡ پشتیبانی از Clash
- ⚡ پشتیبانی از Sing-box
- ⚡ پشتیبانی از Base64
- 🤖 اتصال به تلگرام
- ☁️ ذخیره اطلاعات در Cloudflare D1
- 🌙 رابط کاربری مدرن و دارک مود

---

# 📋 پیش‌نیازها
قبل از نصب موارد زیر را داشته باشید:
- Cloudflare Account
- GitHub Account
- یک دامنه متصل به Cloudflare
- Wrangler (اختیاری)

---

# ⚙️ آموزش نصب

## مرحله 1 - ساخت Worker
وارد داشبورد Cloudflare شوید.
مسیر:
```
Workers & Pages
```
روی:
```
Create Application
```
کلیک کنید.
سپس:
```
Create Worker
```
را انتخاب کنید.
نام Worker را وارد کنید:
```
pasha-gfw
```
سپس Worker را ایجاد کنید.

---

## مرحله 2 - ساخت پایگاه داده D1
از منوی Cloudflare وارد بخش:
```
Storage & Databases
```
شوید.
سپس:
```
D1 SQL Database
```
را انتخاب کنید.
روی:
```
Create Database
```
کلیک کنید.
مثال:
```
Pasha-GFW-DB
```

---

## مرحله 3 - اتصال D1 به Worker
وارد Worker شوید.
سپس:
```
Settings
```
↓
```
Bindings
```
↓
```
Add Binding
```
↓
```
D1 Database
```
را انتخاب کنید.
نام Binding:
```
IOT_DB
```
Database:
```
Pasha-GFW-DB
```
سپس ذخیره کنید.

---

## مرحله 4 - قرار دادن کد
فایل:
```
_worker.js
```
را باز کنید.
کل محتوای Worker را جایگزین کنید.
سپس:
```
Deploy
```
را بزنید.

---

## مرحله 5 - ورود به پنل
پس از Deploy آدرس زیر را باز کنید:
```
https://YOUR-WORKER.workers.dev/sync/dash
```
یا مسیر تنظیم شده در پنل.

---

## 🤖 راه‌اندازی تلگرام
یک ربات از:
```
@BotFather
```
بسازید.
سپس:
- Bot Token
- Chat ID

را دریافت کنید.
در پنل وارد بخش تنظیمات شوید و مقادیر را وارد کنید.

---

## 📦 ساخت کاربر
از پنل:
```
Users
```
↓
```
Create User
```
کاربر جدید بسازید.
برای هر کاربر می‌توانید:
- محدودیت حجم
- تاریخ انقضا
- نام کاربری
- یادداشت

تعریف کنید.

---

## 🔗 دریافت لینک اشتراک
بعد از ساخت کاربر، لینک اختصاصی به صورت:
```
https://example.workers.dev/sync?sub=username
```
ایجاد می‌شود.

---

## 🛠️ تکنولوژی‌های استفاده شده
- Cloudflare Workers
- Cloudflare D1
- JavaScript
- TailwindCSS
- Telegram Bot API

---

## 📄 License
MIT License

---

## 👨‍💻 Developer
**Pasha**
Pasha-GFW Project
