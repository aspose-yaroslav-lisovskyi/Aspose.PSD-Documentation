---
title: مشاكل معروفة
type: docs
weight: 40
url: /ar/net/known-issues/
---

## **.NET Compact Framework**
- يُلاحَظ أنه على بعض إصدارات ويندوز الخاصة، مثل Windows Mobile 5.0-6.0، أن تجميعات الإطار المدمج تطلب شهادة (أو شهادات مزدوجة) لا تعمل كما هو متوقع ولا يمكن تحميلها بشكل صحيح (يتم رميّ استثناء TypeLoadException). للتغلب على هذه المشكلة، يحتاج المستخدم إلى إزالة أي شهادة واستخدام التجميع المُحدّث. يُرجى الملاحظة أن تقوم بذلك على مسؤوليتك الشخصية ولا نُضمن عملًا صحيحًا نتيجة لهذا التغيير في التجميع. ولا نُرسل التجميعات بدون توقيع لأن هذا يُعتبر تهديدًا أمنيًّا محتملًا. بدلاً من ذلك، ينبغي للعملاء تجنب استخدام أنظمة تشغيل قديمة من هذا النوع، إذا كان ذلك ممكنًا، و/أو ترقية النظام إلى إصدارات أحدث أو حزم تحديثية تحل مشكلة توقيع الشهادة.