# بناء APK عبر GitHub Actions (بدون كمبيوتر قوي)

هذا المشروع تطبيق متابعة تقدّم AnyPS5، وليس محاكيًا لتشغيل ألعاب PS5.

## طريقة إنشاء APK

1. فك ضغط `AnyPS5ProgressPro_Android_Project.zip`.
2. أنشئ مستودعًا جديدًا في GitHub من حسابك، مثل `AnyPS5ProgressPro`.
3. ارفع **محتويات المجلد** إلى المستودع، بحيث يظهر `app/` و`build.gradle.kts` و`.github/workflows/build-apk.yml` في جذر المستودع.
4. افتح تبويب **Actions** في المستودع.
5. اختر **Build AnyPS5 Progress Pro APK** ثم اضغط **Run workflow** (أو انتظر انتهاء البناء بعد رفع الملفات إلى الفرع `main`).
6. افتح عملية البناء الأخيرة وانتظر أن تصبح خضراء.
7. في أسفل صفحة العملية، ضمن **Artifacts**، نزّل `AnyPS5ProgressPro-debug-apk`.
8. فك ضغط ملف Artifacts وستجد `app-debug.apk`. انقله إلى هاتف Android وثبّته. قد تحتاج إلى السماح بالتثبيت من هذا المصدر.

## ملاحظات
- البناء يتم على خوادم GitHub Actions؛ لا يتطلب وجود Android Studio على الهاتف.
- هذا APK من نوع debug للاختبار، وليس إصدارًا منشورًا على Google Play.
- لم أتمكن من تشغيل البناء في بيئة المحادثة نفسها لعدم توفر Android SDK وGradle محليًا؛ يجب أن تنجح عملية GitHub Actions أولًا قبل اعتبار APK مبنيًا.
