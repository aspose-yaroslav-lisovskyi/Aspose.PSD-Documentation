---
title: שימוש בממשק ה-Graphics API כדי לערוך שכבות בקבצי PSD
weight: 100
type: docs
description: דוגמה לשימוש בממשק ה-Graphics API ב-Aspose.PSD עבור Java
keywords: [עדכון שכבה, ציור מעגל, ציור אליפסה, מילוי מעגל, גרפיקה, PSD API, Java, קוד דוגמא]
url: he/java/graphics-api/
---

## **סקירה**
כדי להתחיל, טענו את קובץ ה-PSD באמצעות השיטה Image.load() או צרו תמונת Psd Image מהתחלה. השתמשו במשתנה inputFile כדי לייצג את הנתיב לקובץ ה-PSD שלכם, וציינו כל אפשרויות טעינה ב־loadOpt, אם נדרש.

לאחר מכן, גשו לשכבה הראשונה של התמונת PSD באמצעות התחביר psdImage.getLayers()[0] על מנת לקבל התייחסות לאובייקט השכבה למטרת עיבוד.

כדי לערוך את השכבה, צרו אובייקט מסוג Graphics על ידי מעבר השכבה כפרמטר. אובייקט זה מספק שיטות שונות לציור צורות והחלת מברשות.

השתמשו באובייקט Pen על מנת להגדיר את צבע המקו ועוביו של קווי הצורות. באופן דומה, מברשות כמו LinearGradientBrush משמשות להגדרת צבעי מילוי.

ציירו צורות על השכבה באמצעות שיטות כמו graphics.drawEllipse() כדי לקוות צורות ו־graphics.fillEllipse() כדי למלא אותן.

לאחר ביצוע שינויים הנדרשים בשכבה, שמרו את התמונה ש־PSD עם השינויים באמצעות psdImage.save().

בנוסף, תוכלו לשמור את התמונה ששונתה בפורמטים אחרים כמו PNG על ידי שימוש באפשרויות מתאימות.

זהו! בהצלחה בשימוש בממשק ה-Graphics API של Aspose.PSD עבור Java על מנת לערוך שכבות בקובץ PSD. תיקחו חלק ותשפרו את יכולות העריכה שלכם באמצעות ספריית Aspose.PSD.

נא לבדוק דוגמה מלאה.

## **דוגמה**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}