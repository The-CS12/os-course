# NTB Theme

![Hugo](https://img.shields.io/badge/Hugo-Extended-blue)

![License|122](https://img.shields.io/github/license/farhantbyte/ntb-theme)

![Stars](https://img.shields.io/github/stars/farhantbyte/ntb-theme)

![Last Commit](https://img.shields.io/github/last-commit/farhantbyte/ntb-theme)

![Repo Size](https://img.shields.io/github/repo-size/farhantbyte/ntb-theme)

NTB Theme یک تمپلیت ساده نوشته شده با **Hugo** است که برای انتشار آموزش‌ها به شکل **Thread-based** طراحی شده است. هدف این پروژه این است که مطالب آموزشی به جای یک مقاله طولانی، در قالب مجموعه‌ای از پست‌های کوتاه و زنجیره‌ای منتشر شوند.

در این ساختار، هر موضوع آموزشی به چند **Chapter** تقسیم می‌شود و هر Chapter شامل چند **Thread** است که هر کدام یک مفهوم کوچک را توضیح می‌دهند. این روش باعث می‌شود خواندن مطالب ساده‌تر، پیگیری روند آموزش واضح‌تر و مدیریت محتوا برای نویسنده راحت‌تر باشد.

این تمپلیت برای استفاده در کامیونیتی **CS12** طراحی شده است اما می‌توان از آن برای هر نوع پروژه آموزشی مبتنی بر Hugo استفاده کرد.

---

# پیش‌نیازها

برای استفاده از این پروژه باید موارد زیر روی سیستم شما نصب شده باشد:

- Git
- Hugo Extended

بررسی نصب Hugo:

                                            _content_copy_                        text

`hugo version`

در خروجی باید عبارت **extended** دیده شود.

اگر Hugo نصب نیست می‌توانید از راهنمای رسمی استفاده کنید:

[https://gohugo.io/installation/](https://gohugo.io/installation/)

---

# دریافت پروژه

ابتدا این ریپازیتوری را در GitHub **Fork** کنید.

پس از Fork کردن، پروژه را روی سیستم خود Clone کنید:

                                            _content_copy_                        text

`git clone https://github.com/YOUR-USERNAME/ntb-theme.git`

سپس وارد دایرکتوری پروژه شوید:

                                            _content_copy_                        text

`cd ntb-theme`

---

# تنظیم اولیه سایت

در ریشه پروژه فایلی به نام `hugo.toml` وجود دارد. این فایل تنظیمات اصلی سایت را مشخص می‌کند.

این فایل را باز کنید و مقادیر زیر را مطابق با سایت خود تغییر دهید.

                                            _content_copy_                        text

`baseURL = "https://yourdomain.com/" title = "نام سایت شما" languageCode = "fa" theme = "ntb-theme"  [params] author = "نام نویسنده" description = "توضیح کوتاه درباره سایت"  [params.github] repo = "https://github.com/YOUR-USERNAME/ntb-theme"`

توضیح پارامترها:

`baseURL`

آدرس دامنه سایت شما است. اگر سایت را روی GitHub Pages یا Vercel منتشر می‌کنید باید این مقدار برابر با دامنه نهایی سایت باشد.

`title`

عنوان اصلی سایت.

`author`

نام نویسنده یا صاحب سایت.

`description`

توضیح کوتاه درباره سایت که در متادیتا و SEO استفاده می‌شود.

`params.github.repo`

آدرس ریپازیتوری GitHub شما. این مقدار برای لینک **Edit on GitHub** در پایین هر پست استفاده می‌شود.

---

# اجرای سایت در محیط محلی

برای اجرای سایت در حالت توسعه دستور زیر را اجرا کنید:

                                            _content_copy_                        text

`hugo server -D`

پس از اجرا، Hugo یک سرور محلی ایجاد می‌کند.

سایت در این آدرس در دسترس خواهد بود:

                                            _content_copy_                        text

`http://localhost:1313`

هر تغییری که در فایل‌ها ایجاد کنید به صورت خودکار در مرورگر رفرش می‌شود.

---

# ساختار محتوای پروژه

محتوای اصلی سایت در مسیر زیر قرار می‌گیرد:

                                            _content_copy_                        text

`content/threads`

در این مسیر هر پوشه نمایانگر یک **Chapter** است و داخل هر Chapter مجموعه‌ای از پست‌ها (Threadها) قرار می‌گیرد.

نمونه ساختار:

                                            _content_copy_                        text

`content └── threads     ├── linux-basics     │   ├── _index.md     │   ├── 01.md     │   ├── 02.md     │   └── 03.md     │     └── networking         ├── _index.md         ├── 01.md         └── 02.md`

---

# ساخت Chapter جدید

برای ایجاد یک Chapter جدید ابتدا یک پوشه داخل `content/threads` ایجاد کنید.

مثال:

                                            _content_copy_                        text

`content/threads/linux-basics`

سپس داخل این پوشه فایلی با نام زیر بسازید:

                                            _content_copy_                        text

`_index.md`

محتوای این فایل باید به شکل زیر باشد:

                                            _content_copy_                        text

`+++  title = "Linux Basics"  # وضعیت فصل # done -> پایان یافته # running -> در حال اجرا  group_status = "running"  # هرچه عدد کمتر باشد فصل بالاتر نمایش داده می‌شود weight = 1  +++`

توضیح پارامترها:

`title`

عنوان Chapter که در سایت نمایش داده می‌شود.

`group_status`

وضعیت فصل. اگر آموزش کامل شده باشد مقدار `done` و اگر هنوز در حال تکمیل باشد مقدار `running`.

`weight`

ترتیب نمایش Chapterها. هرچه مقدار کمتر باشد آن Chapter بالاتر نمایش داده می‌شود.

توجه داشته باشید مقدار `weight` از **1** شروع می‌شود. مقدار **0** برای فصل اصلی سایت رزرو شده است.

---

# ساخت یک پست جدید

برای ساخت پست جدید از دستور زیر استفاده کنید:

                                            _content_copy_                        text

`hugo new threads/<chapter-dir>/<nameOfPost>.md`

مثال:

                                            _content_copy_                        text

`hugo new threads/linux-basics/01.md`

پیشنهاد می‌شود نام فایل‌ها **عددی** باشد تا ترتیب Threadها ساده‌تر مدیریت شود.

نمونه نام‌گذاری مناسب:

                                            _content_copy_                        text

`01.md 02.md 03.md`

---

# ساختار فایل پست

پس از اجرای دستور بالا، فایلی با ساختار زیر ایجاد می‌شود:

                                            _content_copy_                        text

`---  title: "01"  date: 2026-06-18T13:27:33+03:30  draft: true  order: 1  description: ""  image: ""  comments: true  ---`

توضیح فیلدها:

`title`

عنوان پست.

`date`

تاریخ انتشار پست.

`draft`

اگر مقدار آن `true` باشد پست در سایت منتشر نمی‌شود.

`order`

ترتیب پست در داخل Chapter.

`description`

توضیح کوتاه برای SEO.

`image`

تصویر شاخص پست.

برای استفاده از تصویر:

1. تصویر را در مسیر زیر قرار دهید

                                            _content_copy_                        text

`static/assets/img`

2. سپس فقط نام فایل را در فیلد `image` قرار دهید.

---

# استفاده از Shortcode ها

این تمپلیت شامل چند Shortcode قابل استفاده در پست‌ها است.

## Read More

برای ایجاد بخش بازشونده:

                                            _content_copy_                        text

`{{< readmore title="یکم بیشتر بدونید" open="false" >}}  متن کامل  {{< /readmore >}}`

پارامتر `open` مشخص می‌کند که بخش به صورت پیش‌فرض باز باشد یا بسته.

---

## Media Modal

برای نمایش تصویر یا مدیا در یک مودال:

                                            _content_copy_                        text

`{{< mediamodal type="image" src="/assets/img/example.jpg" title="عنوان" text="توضیح" >}}`

---

# ساخت نسخه نهایی سایت

پس از پایان ویرایش محتوا، برای ساخت نسخه نهایی سایت دستور زیر را اجرا کنید:

                                            _content_copy_                        text

`hugo --gc --minify`

این دستور نسخه بهینه شده سایت را در پوشه زیر تولید می‌کند:

                                            _content_copy_                        text

`public`

تمام فایل‌های استاتیک سایت در این پوشه قرار خواهند گرفت.

---

# انتشار سایت

پوشه `public` را می‌توانید روی هر سرویس **Static Hosting** منتشر کنید.

پلتفرم‌های رایج:

- GitHub Pages
- Vercel
- Cloudflare Pages

قبل از Deploy مطمئن شوید مقدار `baseURL` در `hugo.toml` برابر دامنه سایت شما باشد.

---

# ویرایش محتوا از طریق GitHub

در پایین هر پست لینکی با عنوان **Edit on GitHub** قرار دارد.

با استفاده از این لینک کاربران می‌توانند:

1. ریپازیتوری را Fork کنند
2. تغییرات موردنظر را اعمال کنند
3. Pull Request ارسال کنند

تمام تغییرات از طریق Pull Request بررسی و سپس Merge می‌شوند.

---

# مشارکت در پروژه

اگر قصد مشارکت در توسعه این پروژه را دارید:

1. ریپازیتوری را Fork کنید
2. تغییرات موردنظر را اعمال کنید
3. Pull Request ارسال کنید

در صورت وجود مشکل یا سوال می‌توانید یک **Issue** در GitHub ثبت کنید.

---

# خلاصه روند استفاده

روند کلی استفاده از این پروژه به شکل زیر است:

Fork کردن پروژه

ویرایش فایل hugo.toml

ساخت Chapter

ساخت Thread

اجرای hugo server برای مشاهده محلی

ساخت نسخه نهایی با hugo --gc --minify

انتشار پوشه public روی یک سرویس هاست استاتیک

:::

فَرِهان، این نسخه از نظر مستندسازی چند مزیت مهم دارد:

- احتمال خطای کاربر در راه‌اندازی بسیار کم می‌شود
- ساختار **Chapter / Thread** کاملاً شفاف توضیح داده شده
- تمام مسیرها و فایل‌ها دقیق نوشته شده‌اند
- برای کسی که Hugo بلد نیست هم قابل استفاده است
- برای GitHub کاملاً استاندارد و حرفه‌ای به نظر می‌رسد