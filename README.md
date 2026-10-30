<div dir="rtl">

# SafetyEye – كاشف السلامة المهنية

نظام ذكي يستخدم **الرؤية الحاسوبية** وكاميرا ويب لمراقبة مدخل الورشة، ويتحقق تلقائياً من ارتداء المتدرب لأدوات السلامة المهنية (الخوذة، السترة العاكسة...) قبل دخوله.

**🔗 صفحة المشروع والعرض التوضيحي:** https://alwadai1.github.io/SafetyEye/

**📷 التطبيق الحقيقي بالكاميرا:** https://alwadai1.github.io/SafetyEye/app.html

## المشكلة
عدم الالتزام بأدوات السلامة من أبرز أسباب إصابات العمل في الورش التدريبية ومواقع العمل. الرقابة البشرية وحدها لا تكفي، فالمدرب لا يستطيع التحقق من كل شخص عند كل دخول، ولا يوجد عادةً سجل دقيق للمخالفات.

## الحل
- كاميرا عند مدخل الورشة ترصد المتدرب لحظة دخوله.
- نموذج ذكاء اصطناعي، مدرّب على صور من بيئة الورشة نفسها، يحدد خلال أقل من ثانية: **ملتزم** أو **غير ملتزم**.
- عند الالتزام: رسالة "مسموح بالدخول" باللون الأخضر.
- عند المخالفة: تنبيه صوتي بالعربية وتنبيه مرئي، مع تصوير المخالفة وتسجيلها بالوقت.
- إحصائيات لنسبة الالتزام، وتصدير السجل إلى Excel (CSV).

## المميزات
- يعمل في المتصفح مباشرة، ولا يحتاج إلى أي تثبيت.
- لا يحتاج سوى لابتوب وكاميرا ويب.
- يمكن تنزيل نسخة تعمل **بدون إنترنت** من داخل التطبيق، وتشغيلها من فلاش USB.
- يحفظ النموذج المدرَّب في ملف لإعادة استخدامه على أي جهاز.
- تبقى الصور على الجهاز نفسه ولا تُرسل لأي خادم.

## التقنيات المستخدمة
| التقنية | الاستخدام |
| --- | --- |
| TensorFlow.js | تشغيل الذكاء الاصطناعي داخل المتصفح |
| MobileNet | استخراج خصائص الصورة (Transfer Learning) |
| KNN Classifier | تصنيف الحالة: ملتزم / غير ملتزم / لا يوجد شخص |
| HTML / CSS / JavaScript | واجهة التطبيق |
| Web Speech API | التنبيه الصوتي بالعربية |

## طريقة الاستخدام
1. افتح التطبيق في متصفح Chrome أو Edge، واسمح باستخدام الكاميرا.
2. انتظر حتى تظهر عبارة **"النظام جاهز ✔"**.
3. **التدريب:** اضغط مطولاً على زر "التقاط" لكل حالة، 50 صورة على الأقل لكل حالة:
   - متدرب يرتدي أدوات السلامة.
   - نفس المتدرب في نفس المكان بدون أدوات السلامة.
   - المدخل خالٍ.
4. اضغط **"حفظ التدريب"** للاحتفاظ بالنموذج.
5. **المراقبة:** اضغط "بدء المراقبة".

> نصيحة: درّب النموذج في مكان العرض نفسه وبإضاءته، واستخدم أدوات كبيرة وواضحة الألوان للحصول على أعلى دقة.

## بيئات التطبيق
ورش التدريب التقني والمهني، المصانع وخطوط الإنتاج، مواقع البناء، المختبرات، المستودعات، منشآت النفط والغاز والطاقة.

## فريق العمل
| الاسم | الدور |
| --- | --- |
| يوسف علي أحمد آل خرصان الوادعي | متدرب |
| عبدالقادر مسفر دواس آل جميل الوادعي | متدرب |
| المهندس: عبدالله محمد حسين الوادعي | مشرف المشروع |

**تخصص الدعم الفني للحاسب الآلي — قسم الحاسب الآلي وتقنية المعلومات**
**الكلية التقنية والمعهد الصناعي الثانوي بظهران الجنوب — المؤسسة العامة للتدريب التقني والمهني**

</div>

---

## English

**SafetyEye – Occupational Safety Detector** is a computer-vision system that monitors a workshop entrance with a webcam and checks whether each trainee is wearing the required personal protective equipment (helmet, high-visibility vest, …) before entering.

- **Compliant:** a green "Entry allowed" message.
- **Non-compliant:** an audible Arabic voice alert and a visual alert, plus a snapshot of the violation logged with its time.
- Compliance statistics, with CSV export of the log.
- Runs entirely in the browser, needs only a laptop and a webcam, and can be downloaded as an offline single-file copy.

**Tech:** TensorFlow.js · MobileNet (transfer learning) · KNN classifier · HTML/CSS/JavaScript · Web Speech API

**Team:** Yousef Ali Ahmed Al Khirsan Alwadai and Abdulqader Musfer Dawas Al Jameel Alwadai (trainees); Eng. Abdullah Mohammed Hussein Alwadai (supervisor). Computer Technical Support, Department of Computer & Information Technology, Technical College and Secondary Industrial Institute in Dhahran Al-Janoub (TVTC).

## License
MIT
