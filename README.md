# قناة إصدارات المنظم (MyNotes-releases)

مستودع **عام** يحوي ملفات التحديث التلقائي — بلا توكن.

## للأندرويد
- `latest.json` يحوي: versionCode / versionName / apkUrl.
- ارفع الـ APK الموقّع كأصل في «Release» باسم `app-release.apk`، وحدّث `latest.json`.
- التطبيق يقارن versionCode تلقائياً عند الإقلاع وينزّل ثم يطلب التثبيت.

## لويندوز (electron-updater)
- انشر مثبّت NSIS + `latest.yml` كأصول «Release» عبر:
  `npx electron-builder --publish always` (مع GH_TOKEN لهذا المستودع).
- التطبيق يحدّث نفسه صامتاً.

⚠️ مهم: وقّع APK بنفس المفتاح دائماً، وإلا فشل تثبيت التحديث.
