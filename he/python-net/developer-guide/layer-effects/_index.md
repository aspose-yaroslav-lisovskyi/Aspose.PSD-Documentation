---
title: שימוש באפקטי שכבה בקובצי PSD
weight: 100
type: docs
description: דוגמה לשימוש באפקטי שכבה ב-Aspose.PSD עבור Python
keywords: [צל מתחת, חפיפת צבע, זוהם פנימי, זוהם חיצוני, API של PSD, Python, דוגמת קוד]
url: he/python-net/layer-effects/
---

## **סקירה**
ב-Aspose.PSD עבור Python, ניתן ליצור אפקטים שונים על שכבות כדי לשפר את המראה הוויזואלי של התמונות שלך. תהליך זה ניתן להשגתו באמצעות המחלקה BlendingOptions, המספקת שיטות להוספת סוגים שונים של אפקטים כגון קו חיצוני, צל פנימי, צל מתחת, החספסה של גרדיינט, חפיפת צבע, חפיפת דפוס, וזוהם חיצוני.

כדי להדגים את יצירת האפקטים על שכבות, נניח את קוד הדוגמה הבא

בקוד הדוגמה הזה, אנו טוענים תמונת PSD ראשית ושומרים את התמונה המקורית כקובץ PNG. לאחר מכן, אנו יוצרים אפקטים שונים על שכבות שונות באמצעות מחלקת BlendingOptions. הנה הסבר קצר על כל אפקט:

קו חיצוני: אנו מוסיפים קו גרדיינט לשכבה 1, כשאנו מציינים את גודל הקו, נקודות הצבע בגרדיינט, ונקודות השקיפות.

צל פנימי: אנו מוסיפים זוהם פנימי לשכבה 2, כשאנו מציינים את הזווית ואת צבע הצל.

צל מתחת: אנו מוסיפים צל מתחת לשכבה 3, כשאנו מציינים את הזווית ואת צבע הצל.

גרדינט חצי שקוף: אנו מוסיפים חפיפת גרדיינט לשכבה 4, כשאנו מציינים את נקודות הצבע בגרדיינט ונקודות השקיפות.

חפיפת צבע: אנו מוסיפים חפיפת צבע לשכבה 5, כשאנו מציינים את הצבע ואת השקיפות של החפיפה.

חפיפת דפוס: אנו מוסיפים חפיפת דפוס לשכבה 6, כשאנו מציינים את נתוני הדפוס, הרוחב, והגובה.

זוהם חיצוני: אנו מוסיפים זוהם חיצוני לשכבה 7, כשאנו מציינים את הגודל ואת צבע המילוי של הזוהם.

לבסוף, אנו שומרים את התמונה המודפסת כקובץ PNG ו-PSD.

זוהי סתם דוגמה בסיסית לאיך ניתן ליצור אפקטים על שכבות באמצעות Aspose.PSD עבור Python. תוכל להתאים אישית את האפקטים עוד יותר על ידי כיוון הפרמטרים והמאפיינים של כל אפקט. הספרייה מספקת אפשרויות והגדרות שונות ליצירת אפקטים מורכבים ומרהיבים מבחינה ויזואלית.

אני מקווה שמאמר זה יעזור לך להבין איך ליצור אפקטים על שכבות ב-Aspose.PSD עבור Python. נשמח אם תזמין את מסמכי הספרייה עבור פרטים נוספים ודוגמאות.

אנא בדוק את הדוגמה המלאה.

## **דוגמה**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-layer-effects.py" >}}
