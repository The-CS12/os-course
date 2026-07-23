---
# عنوان پست
title: "نگاهی عمیق تر به PCB"
# تاریخ انتشار پست
date: 2026-07-05T11:33:59+03:30
# اگر فالس باشه نمایش داده نمیشه
draft: false
# اوردر پست بهتره به صورت اینکریمنتال افزایش پیدا کنه
order: 6
# توضیح کوتاه پست برای seo
description: ""

# لایسنس این مطلب رو بنویسید مثلا MIT
license: "CC BY-SA 4.0"

# تصویر شاخص پست فقط کافیه که نام تصویر رو بزارید
# اول تصویر رو در /static/assets/img قرار بدید
# سپس نام تصویر رو اینجا بگزارید مثلا x.jpeg

image: ""
# اگر میخوای این مطلب کامنت داشته باشه...
comments: true
mathEnable: false
---
____________________

توی ترد های قبل با `PCB` آشنا شدید و درک پایه ای ازش دارید اما بیاید یکم عمیق تر به PCB نگاه کنیم. اطلاعات درون PCB به سه دسته اصلی تقسیم میشه: <BR>
1. 🔍 Process Identification
2. 📊 Processor State Information
3. 🎛️ Process Control Information


هر پراسس باید یکتا و قابل شناسایی باشه. <br> 
- **PID** (Process ID - آیدی خود پراسس)، 
- **PPID** (Parent Process ID - شناسه والدش)، 
- **UID** (User ID - شناسه کاربری که پراسس بهش تعلق داره) <br>
 دیتاهای مربوط به دسته Identification میشه!

دیتا های دسته بندی state information شامل آیتم های زیر میشه:
- User-Visible Registers
- Control and Status Registers
- Condition Codes (Flags)
- Stack Pointer (SP)

دیتا های دسته بندی control information شامل آیتم های زیر میشه:
- Scheduling and State Information
- Data Structuring
- Interprocess Communication (IPC)
- Process Privileges
- Memory Management Information
- Resource Ownership and Utilization

شاید با خودتون بگید چرا `PCB` انقد بزرگه؟ دلیلش مشخصه چون سیستم عامل باید اجرای یه پراسس رو متوقف کنه و مجددا از همون نقطه شروع به اجرا کنه، منابع رو مدیریت کنه، امنیت برقرار کنه، دسترسی ها رو کنترل کنه و زمان بندیشون کنه. این ها همه نیازمند اطلاعات وضعیت لحظه ای یه پراسس هستند🤯

{{< readmore type="project" title="پروژه" open="false" >}}
من توضیحات مربوط به دسته اول یعنی Identification رو گفتم. <br>
به عنوان پروژه میتونید درباره آیتم های دو دسته بعدی دیگه تحقیق کنید و کاربرد هر کدوم رو یاد بگیرید❗ <BR>
(میتونید متن تحقیقتون رو کامنت کنید تا دیگران هم ببینند.)
{{< /readmore >}}