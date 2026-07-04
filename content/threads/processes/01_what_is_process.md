---
title: پراسس چیه؟
date: 2026-07-01T09:08:08+03:30
draft: false
order: 2
description: تو این ترد با مفهوم پراسس ها آشنا میشیم
license: CC BY-SA 4.0
image: ""
comments: true
mathEnable: false
---
____________________
به زبان ساده پراسس یک برنامه در حال اجراست 💡 <br>
**Program** ها فایل های ساکن **(Passive entity)** روی *دیسک* هستن اما **Process** ها یک موجود فعال **(Active entity)** هستن که توی مموری اجرا میشن! <br>


بیاید با نرم افزار موردعلاقم یعنی **Firefox** 🦊 یه مثال بزنم :) <br>
فرض کنید فایلی به نام `firefox.exe` دارید. این فایل یه Program محسوب میشه که روی دیسک (Storage) ذخیره شده. وقتی اجراش میکنید سیستم عامل میاد و یه Process از روش میسازه که توی مموری ذخیره میشه. اگر چندبار اجراش کنید چند تا Process جداگانه خواهید داشت که همگی از یه Program ساخته شدن. <br>
هر Process شامل بخش های زیر هستش: 
<br>
- Program code (text) | کد برنامه
- Data | مقادیر متغیر های Global , Static
- Heap | حافظه ای که حین اجرای برنامه قابل رزور هستش
- Stack | حافظه ای که به صورت خودکار توسط کامپایلر و سیستم عامل رزرو میشه
- CPU Register | AC,PSW,IR, ...
- Program Counter | PC (آدرس دستوالعمل بعدی)
- Process Control Block (PCB) | مهم ترین بخش هر Process 



{{< readmore type="" title=" یکم بیشتر بدونید (مهم)" open="true" >}}
Process control block یا همون PCB مهم ترین بخش سیستم عامل هستش! توی این بخش اطلاعات مربوط به هر پراسس ذخیره میشه! اطلاعاتی از قبیل: <BR>
- Process ID
- State
- Priority
- Memory information
- Open files
- Accounting information
- Scheduling information

یه جورایی PCB شناسنامه Process هستش!
{{< /readmore >}}

{{< readmore type="info" title="استک چیه؟" open="false" >}}
استک **(Stack)** نوعی ساختمان داده هسنش که به صورت فنی توی رم ذخیره میشه. انواع مختلفی از استک (پشته) ها وجود داره مثل `Control stack` که توی فصل قبل دیدیم. ولی استکی که تو این ترد ازش گفتیم بخشی از مموری هستش که کامپایلر یا سیستم عامل برای یه برنامه در حال اجرا رزرو میکنه و متغیر های Local , توابع و دیتاهاش , Function argument ها و ... توش ذخیره میشن! این فضا محدود هستش و مدیریتش به صورت خودکار توسط خود کامپایلر یا سیستم عامل انجام میشه. <br>
استک از الگوریتم **LIFO** (Last in First out) استفاده میکنه (در آینده بیشتر آشنا میشیم!)
{{< /readmore >}}

{{< readmore type="info" title="PCB دقیقا چیه؟" open="false" >}}
‍`PCB` نوعی ساختمان داده هستش که در هسته **(Kernel)** سیستم عامل وجود داره. 🧠 <br>
PCB توی RAM و در حافضه Kernel space ذخیره میشه. این بعنی کاربر و برنامه هاش مستقیما به PCB دسترسی ندارن! همچنین این ساختمان داده توسط OS ساخته و مدیریت میشه.

{{< /readmore >}}