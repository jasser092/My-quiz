README - تحويل الحزمة إلى تطبيق هاتف (Android)

ما في الصندوق:
- index.html        (التطبيق PWA)
- manifest.json     (بيانات التطبيق للمتصفح)
- service-worker.js (تخزين مؤقت للعمل أوفلاين)
- (اختياري) icon-192.png و icon-512.png (مرجع في manifest - يمكنك استبدالهم إذا أردت)

خيارات لتحويل الحزمة إلى تطبيق على هاتفك:

1) أسهل - استخدم PWA مباشرة على هاتف Android:
   - انسخ الملفات إلى جهازك أو استضفها مؤقتًا على ملف محلي (تبويب file:// قد لا يعمل مع service worker).
   - الأفضل: ارفع الملفات إلى خادم ويب بسيط (مثل GitHub Pages أو أي استضافة ملفات).
   - افتح الموقع في Chrome على هاتف Android → اضغط زر القائمة → "Add to Home screen" (إضافة إلى الشاشة الرئيسية).
   - عند فتحه من الشاشة الرئيسية سيعمل كـ تطبيق مستقل (standalone) وأحيانًا أوفلاين بفضل service worker.

2) تحويل إلى APK باستخدام PWABuilder (بدون برمجة كبيرة):
   - ادخل إلى https://www.pwabuilder.com
   - اضع رابط موقعك (تحتاج استضافة الملفات على https). PWABuilder ينشئ حزمة APK/TWA جاهزة للتحميل أو لتوقيعها.
   - يمكنك اختيار خيار "Generate Android" ثم تحميل الحزمة وبناء APK عبر موقعهم أو عبر Android Studio.

3) تحويل إلى APK محليًا باستخدام Bubblewrap / Trusted Web Activity (مطورين):
   - اتبع دليل Bubblewrap: https://github.com/ PWABuilder/bubblewrap
   - يتطلب Node.js و Java و Android SDK. Bubblewrap ينشئ مشروع Android (TWA) ثم تُبنى APK باستخدام Android Studio أو عبر gradle.

4) بديل سريع (WebView wrapper):
   - استخدم أدوات مثل Android Studio لإنشاء تطبيق بسيط يعحتوي WebView يشير إلى ملفات HTML المحلية (assets).
   - هذا يحتاج بناء APK في Android Studio (ستتطلب نظام تشغيل سطح مكتب لبناء APK).

ملاحظة حول الأيقونات وHTTPS:
- أفضل تجربة تحصل عليها عندما تكون الملفات مستضافة عبر HTTPS، ومع أيقونات 192x192 و512x512 في manifest.
- إذا أردت، أستطيع إضافة أيقونات افتراضية أو توليد أيقونات PNG هنا.

إذا أردت أن أضغط هذه الحزمة في ملف ZIP لك لتحميله على هاتفك، أرسِل 'نعم ZIP' وسأجهز رابط تحميل.
أو إذا تريد أي شرح مفصّل لبناء APK عبر PWABuilder أو Bubblewrap أخبرني وسأعطي خطوات دقيقة.
