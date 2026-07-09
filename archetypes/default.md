---
# عنوان پست
title: "{{ replace .File.ContentBaseName "-" " " | title }}"
# تاریخ انتشار پست
date: {{ .Date }}
# اگر فالس باشه نمایش داده نمیشه
draft: false
# اوردر پست بهتره به صورت اینکریمنتال افزایش پیدا کنه
order: 1
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


{{< readmore type="" title="یکم بیشتر بدونید" open="false" >}}
متن کامل
{{< /readmore >}}

{{< readmore type="info" title="توضیحات" open="false" >}}
متن کامل
{{< /readmore >}}


{{< readmore type="warning" title="هشدار" open="false" >}}
متن کامل
{{< /readmore >}}


{{< readmore type="error" title="خطا" open="false" >}}
متن کامل
{{< /readmore >}}


{{< readmore type="project" title="پروژه" open="false" >}}
متن کامل
{{< /readmore >}}

{{< readmore type="bestPractice" title="بهتر است این کار را کنید" open="false" >}}
متن کامل
{{< /readmore >}}


{{< readmore type="excercise" title="تمرین" open="false" >}}
متن کامل
{{< /readmore >}}

<!-- کد ریوزیبل مودال مدیا وسط پست -->

<!-- این تایپ میتونه  -->

{{< 
    mediamodal type="تایپ رو بنویس"
    src="لینک مدیا"
    title="عنوان مودال"
    text="متن مودال"
>}}