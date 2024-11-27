---
title: שינוי תמונות
type: docs
weight: 50
url: /he/java/modifying-images/
---

## **הדיתורינג עבור תמונות רסטר**
הדיתורינג הוא טכניקה ליצירת ההרגשה של צבעים וגוונים חדשים על ידי שינוי בתבנית הנקודות שבאמת יוצרות את התמונה. זהו הדרך הנפוצה ביותר להפחתת טווח הצבעים של התמונות לתוך 256 (או פחות) צבעים. Aspose.PSD מספק תמיכה בדיתורינג עבור מחלקה RasterImage על ידי הכנסת שיטת Dither המקבלת שני פרמטרים. הפרמטר הראשון הוא מסוג DitheringMethod להיושמו עם שני אפשרויות אפשריות FloydSteinbergDithering ו- ThresholdDithering. הפרמטר השני לשיטת Dither הוא ה-BitCount בסוגריים מרובעות. ה-BitCount מגדיר את גודל הדגימה עבור תוצאת הדיתורינג. הערך ברירת המחדל הוא 1 שמייצג שחור ולבן, והערכים המותרים הם 1, 4, 8 שיוצרים פלטות עם 2, 4 ו- 256 צבעים בהתאמה.

## **התאמת בהירות, ניגודיות וגאמה**
כיווני צבע בתמונות דיגיטליות הם אחת התכונות המרכזיות שרוב ספריות עיבוד התמונה מספקות. התאמות צבע יכולות להיות מסויגות בהמשך.

הבהירות מתייחסת לבהירות או כהות של הצבע. עליה בבהירות של תמונה מאירה את כל הצבעים כאשר ירידה בבהירות הופכת את כל הצבעים לכהים.
הניגודיות מתייחסת להפיך האובייקטים או הפרטים בתמונה לניכרים יותר. עליה בניגודיות של תמונה מגבירה את ההבדל בין אזורי האור והחושך עבור כך שהאזורים האורים מתהדקים והאזורים השחורים מתחממים. ירידה בניגודיות תפורר אזורים מוארים וחשוכים עם קצת הבדל, אבל התמונה בכלליותה משתפרת יותר.
גאמה מותאמת אופטימלית את הניגודיות והבהירות של התאורה העקיפה המאירה אובייקט בתמונה.
### **התאמת בהירות**
Aspose.PSD עבור Java API ספק את שיטת ה-AdjustBrightness עבור מחלקה RasterImage שניתן להשתמש בה כדי להתאים את בהירות התמונה על ידי מעבר ערך שלם כפרמטר. ערך הפרמטר הגבוה ביותר מציין תמונה מוארת יותר. הנה התמונה המקורית והתמונה התוצאה להשוואה.

### **התאמת ניגודיות**
השיטה להתאם הניגודיות שנחשפת על ידי מחלקת RasterImage יכולה לשמש כדי להתאים את הניגודיות של תמונה על ידי מעבר ערך מחושב כפרמטר.

### **התאמת גאמה**
השיטה להתאם את הגאמה שנחשפת על ידי מחלקת RasterImage ישנם גירסאות של כפול. אחת מגרסאות העומק מקבלת ערך רך אחד ומבצעת תיקון גאמה עבור מקדים חורים, כחולים וערכים ירוקים. והגירסה האחרת מקבלת שלושה פרמטרים רכים מייצגים את כל המקדים של הצבע בנפרד. הדוגמה לקוד הבא מדגימה כיצד לאייש גאמה על גבי תמונה.

## **הטשה על תמונה**
מאמר זה מדגים את השימוש ב-Aspose.PSD עבור Java לביצוע אפקט הטשה על תמונה. עבור Java, Aspose.PSD חשפה מחלקה מבצעת אפקט הטשה. המחלקה זקופה GaussianBlurFilterOptions הנותנת אפשרות ליצירת אפקט טשה בצורה ברורה. המחלקה GaussianBlurFilterOptions דורשת ערכי רדיוס ו-סיגמא כדי ליצור אפקט טשה על תמונה. 

## **אימות שקיפות תמונה**
מאמר זה מדגים את השימוש ב Aspose.PSD עבור Java כדי לבדוק את שקיפות התמונה. 
## **מממש דחס גיף באופן מפיק**
באמצעות Aspose.PSD עבור Java, מפתחים יכולים להגדיר הבדל פיקסל. דחיסת ה-GIF מבוססת על "מילון" של מחרוזות של פיקסלים שנתקלו. הקוד של המקודד הרגיל מחפש את המחרוזות הארוכות ביותר שמתאימות בדיוק לפיקסלים בתמונה. המקודד הרגיל בוחר במחרוזת הארוכה ביותר שהיא "דומה מספיק" לפיקסלים בתמונה.
## **מממש מעטפת Bicubic**
הערכה משמעה שאתה משנה את ממדי הפיקסלים של תמונה. כאשר אתה מפחית רזולוציה, אתה מוחק פיקסלים ולכן מוחק מידע ופרטים מהתמונה שלך. כאשר אתה מגדיל רזולוציה, אתה מוסיף פיקסלים. פוטושופ מוסיף את הפיקסלים הללו באמצעות שימוש באינטרפולציה.
## **שכבת התאמת Invert**
מאמר זה מדגים כיצד ניתן לבצע את שכבת התאמת הInvert באמצעות Aspose.PSD עבור Java. שכבת ההתאמה היא סוג מיוחד של שכבה המשמשת בעיקר לתיקון צבע. במקום להכיל תוכן משלה, היא מתאימה את המידע בשכבות שהוא מתחת לה. השכבת ההפיכה מייצרת אפקט תמונה שלילית על ידי הפיכת הצבעים של תמונה.