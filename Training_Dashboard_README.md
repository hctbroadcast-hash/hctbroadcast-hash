# Training Requests Dashboard

אתר זה מיועד לפריסה ב‑GitHub Pages. הוא מציג דשבורד שבועי וטבלת בקשות על פי קובץ נתונים `data.json`.

## קבצים

- `index.html` — ממשק הדשבורד
- `data.json` — נתוני בקשות ודוגמאות
- `README.md` — הוראות פריסה ועריכה

## פריסה ב‑GitHub Pages

1. צור ריפו חדש ב‑GitHub בשם `hctbroadcast-hash` (או השתמש בריפו קיים).
2. העלה את הקבצים ל־branch `main`.
3. ב‑GitHub, עבור ל־`Settings` → `Pages`.
4. בחר `Branch: main` ו־`Folder: /root`.
5. שמור. הקישור יופיע כ־`https://hctbroadcast-hash.github.io/`.

## עדכון הנתונים

1. גלוש ל־`data.json` בריפו.
2. לחץ על Edit.
3. בצע את השינויים המבוקשים.
4. לחץ על `Commit changes`.

לאחר עדכון הקובץ, הטעינה בדף תופעל מחדש אוטומטית כל 20 שניות או על ידי רענון הדף.

## מבנה הנתונים

- `departments` — הצבע והשם לכל מחלקה.
- `weeks` — רשימת שבועות.
- בכל שבוע:
  - `weekNumber`
  - `startDate` ו־`endDate`
  - `requests` — כל בקשה.
- בכל בקשה:
  - `title`
  - `department`
  - `status` — `pending`, `approved`, או `rejected`
  - `approvedDays`
  - `approvedTimes`
  - `approvedTrainees`
  - `approvedInstructors`

## תפעול

- קורסים חסרי פרטים מופיעים באדום.
- קורסים מאושרים מופיעים בצבע לפי מחלקה.
- קורסים נדחים מוצגים עם סטטוס דחוי.

## הרצה מקומית לבדיקה

אם תרצה לבדוק מקומית, אפשר להשתמש בשרת מקומי:
```bash
python -m http.server 8000
