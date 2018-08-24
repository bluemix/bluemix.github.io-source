---
title: رُخصَةِ الكُوْدْ
direction: rtl
dir: rtl
lang: ar
date: 2018-01-22 08:23:21
tags:
    - برامج
    - مفتوحة المصدر
    - تراخيص
    - حقوق
    - ملكية
    - open source
    - licenses
    - arabic
    
---

{% ltr %}
شكراً  لـ<a href="https://www.facebook.com/mustafa1024m">مصطفى محمد</a> على التقويم و التصحيح
{% endltr %}

<br>


الكُود المفتوح المصدر ، لا يعني أن الكود _مباحٌ لكَ أنى شئت_😏. رُخصةِ الكود تفرض عليك متطلبات و في نفس الوقت تعطي لك صلاحيات.

في البداية ، المقالة طويلة ، و تحتاج بالقليل إلى نصف ساعة من وقتك لكي تفهم و تتكون صورة عن طبيعة الرُّخص بين البرامج و ما هي الحقوق التي لكَ و عليكَ كمستخدم للكود.
إذاً ، أما أن ترجع إلى تصفح الفيسبوك أو أن تستمر في قراءة و تعلم ما موجود عن رُخص الكود المفتوح المصدر 😶.
<!-- أثناء تطوير مكتبة ، أو تعديل على مكتبة موجودة ، أو أي تغيير تحب أن تساهم به للـ open-source ، على الـ GitHub مثلاً ، عليكَ إختيار إحدى الرُّخص المفتوحة المصدر ، و لكن يجب أن تعرف ما هو الفرق بينهن ، بين الـ Apache 2.0 أو الـ MIT ، على سبيل المثال. -->


هناك الكثير من تراخيص البرامج و المكتبات المفتوحة المصدر  ذات MIT أو Apache 2‪.‬0 أو GPL ، سواءاً ذُكِرت في مشروعهم على الـ GitHub أو معلوماتها على الـ Wikipedia أو الموقع الرسمي للمكتبة أو البرنامج ... لكن يا ترى ما هو الفرق الرئيسي بينهن ، و لماذا تطلب وجود و تخصيص جزء من معلومات المكتبة أو المشروع أنها تابعة إلى رخصة معينة.


<center>
{% img /images/github-licenses-menu.png 225 New project licences list on GitHub  %}
</center>
<br>

في هذهِ المقالة ، مجموعة من التراخيص المشهورة و المستخدمة بكثرة في مشاريع على الـ GitHub ، و الأهم هو مُوافَق عليها من قِبل الـ [(OSI) Open Source Initiative](https://opensource.org/licenses/alphabetical).

 قبل البدء ، هذهِ تعاريف لأجل تجنب الإلتباس بين صاحب المكتبة و مستخدمها.
>**المطور**: صاحب المكتبة التي عَمَل في تطويرها تحت إحدى الرُّخص.
**المستخدم**: مطور أو مبرمج الذي يستخدم مكتبة المُطور.
**المكتبة** أو **الكود** أو **البرنامج** أو **المشروع** ، كلها تعني تعني و تشير إلى معنىً واحداً ألا و هو الـ _software_.


<center>
{% img /images/رخصة-الكود.png 250 رخصةِ الكود  %}
</center>
<p></p>

##  رخصة الـ MIT
الرخصة (MIT License) تسمح للمستخدم بأن يعمل أي شيء في مكتبةِ المطور ، سواءاً كان عملك (مشروعك) الناتج مجاني أو تجاري ، مفتوح المصدر أو مغلق ، فقط تذكر أن الكود منسوب للمطور.
<center>
{% img /images/non-copy-left-license_ar_5.png 700 non-copyleft licenses توضيح  %}
</center>
<br>

  يمكنك أيضاً تغيير الرخصة نفسها لو عملت تغييرات في كود المطور ، مثلاً ، لو كانت المكتبة الأصلية تحت رخصة الـ MIT و قُمت بالتعديلات على بعض الأجزاء ، فتستطيع أن تنشرها تحت رخصة مختلفة غير الـ MIT ، مثلاً  تنشرها تحت رخصة الـ Apache 2.0 أو تحت رخصة الـ  Proprietery License (مغلق المصدر) ، و أن تذكر في مشروعك ، أنك إستخدمت مكتبة الـ MIT هذه.

<center>
{% img /images/mit-change-license.png 425  توضيح تغيير رخصة الـ MIT %}
</center>
<br>


تتطلب منك أن تُرفق نسخة من الرخصة بالإضافة إلى حقوقك (Copyright) ، المتمثل بذكر إسمك أو الجهة التي طورت الكود <sup>[مثال](https://github.com/gleue/TGLStackedViewController/blob/master/LICENSE)</sup>.
تعتبر من أقصر و أوضح الرخص المكتوبة (تتكون من فقرتين فقط) <sup>[✢][MIT License on Wikipedia]</sup>.
من أشهر المكاتب التي تستخدم رخصةِ الـ MIT هي [Bootstrap](https://github.com/twbs/bootstrap) و [Vuejs](https://github.com/vuejs/vue) و [VSCode](https://github.com/Microsoft/vscode) و [NET Core.](https://github.com/dotnet/core) و [React](https://github.com/facebook/react) و [غيرها الكثير](https://github.com/search?o=desc&q=license%3Amit&s=stars&type=Repositories&utf8=%E2%9C%93).


## رخصةِ الـ Apache 2.0
هذهِ الرخصة ، هي مشابهة رخصة الـMIT ، لكن بالإضافة ،  فيها يمنح المطور حق إستعمال براءة الإختراع للمستخدم ، أي أنَّ المطور لا يقاضيه أو يأجره في إستخدامه لكود المطور (من المعروف ،  لو أنت تملك شهادة براءة إختراع في عمل أو فكرةٍ ما ، فيجب منع أي شخص من إستخدام نفس عملك أو فكرتك ، أو أن *يشتري* هذا الشخص براءةِ الإختراع منك.)

فقرة أخرى ، هي أنه  لا يجوز لك ذِكر أو ترويج أسماء المطور (شخص أو شركة  أو أعضائها) في مَدح عملك. أي ، لو عملت تعديلات مُعينة على مكتبة تحت هذهِ الرخصة ، مثلاً ، RxJava ، فلا يجوز أن تقول أن تعديلاتي هي تابعة إلى الـ RxJava.
يجب عليك أن تُلحق الكود بنسخة من هذهِ الرخصة ، و تذكر حقوقك ، و تبين التغييرات التي عملتها في الكود (مثلاً ، بإستخدام الـ git لتتبع التغييرات).
الأندرويد و لغة البرمجة Swift و الـ ASP.NET Core و الـ TensorFlow و لغة البرمجة TypeScript و [غيرها الكثير](https://github.com/search?utf8=%E2%9C%93&q=license%3Aapache-2.0&type=) ، جميعها تحت رخصة الـ Apache 2.0.


## رخصة الـ BSD
بصورة عامة ، هذهِ الرخصة (و أنواعها) مشابهة للـ MIT ، لكن هناك فروقات _تُعتبر _ بسيطة سيتم ذكرها مع كل نوع .
تتكون هذهِ الرخصة ، من ثلاثة أنواعٍ أو ثلاث فقرات ، لكن غالباً ما يتم كتابة فقط BSD License و المقصود منها هي الـ Two-Clause BSD Licence .

####  Two-Clause BSD Licence
تسمح لكَ هذهِ الرخصة بحرية مطلقة تماماً في الكود ، من إستخدام تجاري و التعديل و النشر  ، فقط عليك أن تُرفِق مستند الرخصة مع الكود و حقوقك.
من أقرب الرُّخص إلى الـ MIT Licence هي هذهِ النوع من الـ BSD ، و أحياناً تجدها تُكتب بجانب الـ MIT مسبوقة بـ forwared slash ، أي ، MIT/BSD.
إطلع على مكتبات على الـ GitHub تحت [BSD-2-Clause](https://github.com/search?utf8=%E2%9C%93&q=license%3Absd-2-clause&type=Repositories).


####  Three-Clause BSD Licence 
نفس السابقة ، لكن هنا ، لا يجوز لك ذِكر أو ترويج أسماء المطور (شخص أو شركة  أو أعضائها) في عملك. على سبيلِ المثال ، لو كانت مكتبة مُطوَّرة من شركة Facebook ، مثل React Native ، تحت رخصة الـ Three-Clause BSD Licence ، فأنه لا يجوز أن تستخدم مكتبتك المعدلة و تقول أنها من شركة Facebook أو أن هذهِ تابعة إلى الـ React Native. 

من المكتبات تحت هذهِ الرخصة ، هي d3 و React Native و لغة البرمجة Go و PhantomJS. 
إطلِع على [المزيد](https://github.com/search?utf8=%E2%9C%93&q=license%3Absd-3-clause&type=Repositories). ستلاحظ ، الكثير من مكتبات الـفيسبوك تحت هذهِ الرخصة.

####  Four-Clause BSD Licence 
عكس سابقتها الـ Three-Clause BSD Licence  ، أي تُجبرك أن تذكر في مكتبتك ، أن الكود تم تطويره من قِبل المطور أو الشركة الفُلانية.
_لم يُوافق_ على هذهِ الرخصة من قِبل الـ OSI.
<br>
كل الرخص أعلاه ،  تتطلب منك أن تُرفق نسخة من الرخصة بالإضافة إلى حقوقك ، المتمثل بذكر إسمك أو الجهة التي طورت الكود.


## رخصة الـ GPL-3
هذهِ الرخصة ، GNU General Public License v3 (GPL-3) ، و الإثنين القادمات التابعة لها ، هي أقوى الرخص فيما يتعلق بالبرامج المفتوحة المصدر و ما يميزها عن البقية ، هو _إجبار_ المستخدم  أن تكون التعديلات مفتوحة المصدر.
أي ، لو قمت بعمل تعديلات على محرر الصوتيات [Audacity](https://github.com/audacity/audacity) ، و الذي تحت رخصة الـ GPL-2 ، فعليك أن تقوم بنشر هذهِ التعديلات (غالباً ما تكون عن طريق عمل Fork لمشروعهم على الـ GitHub).
تتضمن أيضاً ، فقرة منح حقوق البراءات للمستخدمين ، كما في رُخصة الـ Apache 2.0.

للتفصيل أكثر ، تستطيع نسخ و نشر و تعديل الكود ، لكن **يجب** عليكَ أن
#### تُرفق الكود الأصلي
#### تَذكُر و تنشر التغييرات للعامة (لا يجوز أن تكون مغلقة)
#### تُلحِق الرخصة
#### تُلحِق حقوقك
#### تَذكُر كيفية التنصيب
####  تُخلي المطالبة في إستعمال براءةِ الإختراع لو أراد المستخدم كود المطور في مشروعهِ

بالإضافة ، **لا يمكنك أن تُغير الرخصة** ، أي تغيير كود المطور الذي كان تحت رخصة الـ GPL-3 إلى رخصة أخرى ، و إنما ، بعد أن تعمل التغييرات ، يجب أن يكون كود المشروع ، سواءاً كانَ مكتبة أو برنامج ، تحت هذهِ الرخصة نفسها ، إلا إذا كان كود المطور غير مُدمج مع كود مشروعك ، إي dynamically linked <sup>[✢][If GitHub interacts with Git, and Git is licensed under GPLv2, shouldn't GitHub be open source?]</sup>. 

<center>
{% img /images/gpl-license_ar_5.png 700 GPL-3.0 توضيح  %}
</center>
<br>

هناك شروط ، في كون البرنامج الكُلي الناتج تحت الـ GPL <sup>[✢][Can I use GPL software in a commercial application]</sup>
#### لو كان برنامجك خاص ، أي يعمل في بيئة خاصة ، سواءاً يُستخدم في شركة فقط ، عندئذٍ ، تبقى رخصة برنامجك حسب إختيارك.
#### أما لو نشرت برنامجك ، و البرنامج يستخدم كود تحت رخصة GPL ، فيجب عليك أن تفتح كود برنامجك.

<br>
قبل فترة ، إستخدمت [مكتبة أندرويد](https://github.com/ChenLittlePing/RecyclerCoverFlow) ، و عملت بعض التعديلات عليها. المشكلة ، أني لم أعلم أنها تحت رخصة GPL-3 😁 ، لذلك ، كان عليَّ أن أعمل Fork للمكتبة ، و أُبين كل التغييرات التي طرأت عليها ، و [عرض هذهِ التغييرات](https://github.com/bluemix/LusciousRecyclerView) ، بالإضافة ، _نشر_ كود برنامجي الذي يستخدم هذهِ المكتبة لو طلبهُ أحدُّ مني😐 <sup>[✢][Using a GPL licensed library in a commercial app]</sup>.

 _متى ما وطئ الـ GPL كودك ، على كودك أن يكون مفتوح المصدر😋_ .
 <br>
 
من البرامج المعروفة تحت هذهِ الرخصة ، هي قاعدة البيانات [MariaDB](https://mariadb.org/) و محرر النصوص [Geany](https://www.geany.org/) و الـ [++Notepad](https://notepad-plus-plus.org/). تعرَّف على المزيد [في قائمة على الويكيبيديا](https://en.wikipedia.org/wiki/Category:Software_using_the_GPL_license) و [على الـ GitHub](https://github.com/search?p=6&q=license%3Agpl-3.0&type=Repositories&utf8=%E2%9C%93).



### رخصة الـ GPL-2.0 
هذهِ الرخصة أقدم من لاحقتها الـ GPL-3 ، ترجع إلى عام 1991 ، الفرق بينها ، أنَّ هذهِ لم تكُن تتضمن فقرة براءةِ الإختراع ، و لا فقرة إجبار المستخدم أن يذكر كيفية التنصيب.
 لكنها مستخدمة في العديد من البرامج ، أهمها هو نواة الـ Linux ، و الـ Git ، و الـ [Systemd](https://github.com/systemd/systemd) و MySQL Server. إطلع على المزيد [على الـGitHub](https://github.com/search?p=1&q=license%3Agpl-2.0&type=Repositories&utf8=%E2%9C%93).
<br>

> الـ Git تحت رخصة الـ GPL-2.0 ، و الـ GitHub هو مغلق المصدر ، لكنه يستخدم الـ Git. إذاً من المفروض أن يكون الـ GitHub مفتوح المصدر ، لإستخدامه مكتبة تحت هذهِ الرخصة.
الجواب أن الـ GitHub يستخدمون نسخة من تطوريهم مختلفة عن الـ Git ، التي هي libgit2 ، تحت رخصة GPLv2 with Linking Exception ، أي أنه نفس رخصة GPL-2.0 لكن مسموح أن يُدمج كود المكتبة مع كود مشروعك ، static linking ، و بالتالي ، يمكنك أن تُكمل مشروعك تحت أي رخصة كانت ، و في نفس الوقت تنشر التغييرات التي عملتها في المكتبة فقط و ليس جميع كود مشروعك.



## رخصة الـ  AGPL-3.0
المشكلة في الرخصة السابقة ، ما يُسمى بالـ GPL loophole ، هو أنه لو كان لديك Web back-end server ، و مشروعك يستخدم كود مكتبة تحت رخصة GPL ، **فتستطيع** أن تُبقي كود مشروعك مغلق ، لأنه في الحقيقة ، لا يُنقل (distribute) كود مشروعك عند جهاز المستخدم و من ثم يرى النتائج ، و إنما هناك API ( أو أي طريقة تواصل تتم بين الويب و بين server الخاص بكَ) في تبادل النتائج و من ثم تُعرض للمستخدم.

<center>
{% img /images/gpl-loophole_ar.png 370 GPL Loophole توضيح  %}
</center>
<br>

أفَّيرو GPL-3.0 ، أو GNU Affero General Public License v3 (AGPL-3.0) هي تعتمد تماماً على رخصة الـ GPL-3 ، لكن بفرق أنها مُحدَّثة لحل هذهِ المشكلة ، أي أنه يجب على الـ server أن يسمح للمستخدمين تنزيل كود المشروع الذي يتعاملون معه.

[Pelican](https://github.com/getpelican/pelican) ، الذي هو static site generator (لا أعرف ترجمتها بالعربي 😄) ، فيجب أن يكون كود موقعك الذي ولَّدهُ الـ Pelican مفتوح المصدر  ؛  و الـ Ghostscript  و  Gitorious (قبل أن تستحوذ عليه GitLab و توقف تطويره). إطلع على المزيد في [في قائمة على الويكيبيديا](https://en.wikipedia.org/wiki/List_of_software_under_the_GNU_AGPL) و [على الـ GitHub](https://github.com/search?p=1&q=license%3Aagpl-3.0&type=Repositories&utf8=%E2%9C%93).
> [Odoo](https://www.odoo.com/) (سابقاً OpenERP) كان تحت رخصة GNU AGPL ، لكن بعد نسخة 9.0 ،  تم التبديل إلى نوعين من الإصدارات: إصدار الـ _Community_ تحت رخصة الـ LGPL و إصدار الـ _Enterprise_ تحت رخصة الـ proprietery ، أي مغلقةِ المصدر.


## رخصة الـ LGPL-3.0
هذهِ الرخصة أو GNU Lesser General Public License v3 (LGPL-3.0) ، هي مطابقة تماماً لكل فقرات الـ GPL-3.0 ، لكنها موجهة إلى المكتبات خصوصاً.  كود المكتبة و التغييرات يجب يُنشر تحت هذهِ الرخصة ، و لكن ، ليس على البرنامج الذي يستخدمها.
أي أن التعديلات التي يعملها المستخدم على مكتبة معينة في مشروعهِ ، فلا يجب عليه أن يكون مشروعه بالكامل تحت هذهِ الرخصة ، و إنما فقط تُطبَّق على جزء المكتبة التي إستعملها ، بشرط أن تكون معزولة و غير مدمجة مع كوده الأصلي (أن تكون dynamically linked) ، لضمان إستمرارية المكتبة التي تحت رخصة LGPL أن تبقى مفتوحة المصدر. 

<center>
{% img /images/lgpl-license_ar_5.png 640 LGPL-3.0 توضيح  %}
</center>
<br>

مثلاً ، لو لديك تطبيقك الشخصي ، و لكن تطبيقك مغلق المصدر ، فيمكنك  أن تستخدم مكتبة تحت هذهِ الرخصة مع الحفاظ تماماً على أي رخصة تستخدمها في تطبيقك. [wkhtmltopdf](https://github.com/wkhtmltopdf/wkhtmltopdf) و [Toasty](https://github.com/GrenderG/Toasty) كأمثلة تحت هذهِ الرخصة. إطَّلع على [المزيد](https://github.com/search?p=2&q=license%3Algpl-3.0&type=Repositories&utf8=%E2%9C%93).



<!-- ### الفروقات

‏(image: MPL) -->

## رخصة الـ MPL-2.0
الـ MIT و الـ BSD و الـ Apache 2.0 تسمح لكَ مطلق الحرية في كود المطور ، سواءاً تعمل تغييراتك مفتوحة أو مغلقة ، و بين رُخصة الـ GPL التي تُجبِرُك أن يكون المشروع بالكامل مفتوح المصدر لو دمجت كود المطور مع كودك أو في رُخصة الـ LGPL أن تكون المكتبة فقط من المشروع ، فإن رخصة موزيلا أو Mozilla Public License 2.0 (MPL-2.0) ، تتعامل على مستوى الفايل فقط الذي تحت رخصة الـ MPL أن يكون مفتوح المصدر ، بغض النظر عن رُخصة مشروعك.
الصراحة ، أنه هذهِ النسخة هي مطابقة لفكرة الـ GPL with static linking ( كما ذُكرت فوق) ، فهي تسمح لك بدمج فايلات الكود الذي تحت هذهِ الرخصة ، statically linked ، و إن تتحفظ برخصة مشروعك ، حتى لو كان مغلق المصدر ، ما دامهُ معزولاً عن ملفات الـ MPL.

<center>
{% img /images/mpl-license_ar_5.png 640 Mozilla Public License 2.0 توضيح  %}
</center>
<br>

طبعاً ، متصفح الفايرفوكس (Firefox) ، تحتَ هذهِ الرخصة ، و [Servo](https://servo.org/) (الذي هو أيضاً تابع إلى موزيلا) و غيرها [على الـ GitHub](https://github.com/search?p=1&q=license%3Ampl-2.0&type=Repositories&utf8=%E2%9C%93).

> نسخة الـ VLC إلى الـ iOS كانت تحت رخصة الـ GPLv2 (التي كانت نفسها للـ VLC)  ، فتم قبول التطبيق في الـ AppStore. لكن المشكلة ، لم يكُن توافُق بين سياسات الـ AppStore و بين أن يكون تطبيق تحت رخصة الـ GPLv2 في الـ AppStore ، حيث أرسل شكوى إلى Apple أحد مطوري الـ VLC حول هذهِ المشكلة ، ما أدى إلى سحب التطبيق من الـ AppStore.
بعدها ، قام جماعة الـ VLC بتغيير رُخصة برنامج الـ VLC من GPLv2 إلى LGPLv2 ، من أجل الحصول على توافقية أكبر ، مثلاً مع الـ AppStore. 
بالنسبة إلى نسخة الـ iOS ، فقد تم إعادة رفعها إلى الـ AppStore تحت رخصة الـ MPL 🙂.


<!-- 
### WTF license
كُل ما تريد عمله في الكود هو لكَ مطلق الحرية تماماً.
‏[a link for GitHub search sorted by license]


## Beerware License 🍺
إعمل ما تشاء في الكود ، ربما في يومٍ من الأيام تشتري لي جِعةً واحدة أو إثنين.
‏[a link for GitHub search sorted by license] -->


Facebook post link for comments
<!-- فيما لو سألتني ما هي الرخصة التي أستخدمها ، فأنا أستخدم رخصة الـ Apache 2‪.‬0 🙂. -->

## الخِتام

بين الرخصة التي تعطي لك مطلق الصلاحية في الكود إلى التي تُجبِرُك على بقاء الكود مفتوح المصدر ، يمكن الإختصار في الرُّخص أعلاه إلى تلاث
#### MIT لو أردت مطلق الصلاحية للمستخدم ، في أن يعمل أي شيء في كود المطور
#### Apache 2.0 لو أردت مطلق الحرية للمستخدم في الكود ، فيها يمنح المطور حق إستعمال براءة الإختراع للمستخدم
#### GPLv3 لو أردت أي شخص يستخدم أو يعدل كودك ، يجب يكون الكود مفتوح المصدر 

<center>
{% img /images/gpl-apache-mit.png 250 MIT, Apache 2.0 and GPLv3  %}
</center>
<p></p>

<br>
أخيراً ، الجدول التالي ، فيه بعض من البرامج و المكتبات و الرخصة التابعة له (لها).

<center>
{% img /images/software-licenses-table.png 700 رُخص بعض البرامج  %}
</center>
<br>


> أعتذر أن  تجد فراغات في التعبير أو نقص في إيصال الصورة ، و أرحب بكل تعديل يسعى لتحسين المحتوى.
> شكراً جزيلاً لكَِ.

## المصادر
هذهِ مجموعة من المصادر ، حبذا لو إطلعت عليهن ، التي جمعتها لأجل معرفة الرخص و الفرق بينهن.

{% ltr %}
<div dir="ltr">
{% endltr %}
[MIT License on Wikipedia]: https://en.wikipedia.org/wiki/MIT_License

‏[Choose an open source license](https://choosealicense.com/)

[BSD 2-Clause License (FreeBSD/Simplified)](https://tldrlegal.com/license/bsd-2-clause-license-(freebsd))
[BSD 3-Clause License (Revised) ](https://tldrlegal.com/license/bsd-3-clause-license-(revised))
[What are the essential differences between BSD and MIT licences?](https://opensource.stackexchange.com/questions/217/what-are-the-essential-differences-between-bsd-and-mit-licences)

[The four clause license has not been approved by OSI. ](https://github.com/timoxley/osi-licenses-full/blob/master/licenses/BSD-3-Clause.md)
‏[What are the differences between open-source licenses?](http://zgp.org/~dmarti/qanda/what-are-the-differences-between-open-source-licenses/#.Wlcb1UtLdTb)
‏[Top 10 Apache License Questions Answered](https://www.whitesourcesoftware.com/whitesource-blog/top-10-apache-license-questions-answered/)

‏[Against what does the Apache 2.0 patent clause protect?](https://opensource.stackexchange.com/questions/1881/against-what-does-the-apache-2-0-patent-clause-protect)

‏[tldrlegal.com - Apache License 2.0 (Apache-2.0)](https://tldrlegal.com/license/apache-license-2.0-(apache-2.0))

[Using a GPL licensed library in a commercial app]: https://softwareengineering.stackexchange.com/questions/37231/using-a-gpl-licensed-library-in-a-commercial-app
[Can I use GPL software in a commercial application]: https://softwareengineering.stackexchange.com/questions/47032/can-i-use-gpl-software-in-a-commercial-application


[If GitHub interacts with Git, and Git is licensed under GPLv2, shouldn't GitHub be open source?]: https://softwareengineering.stackexchange.com/questions/340913/if-github-interacts-with-git-and-git-is-licensed-under-gplv2-shouldnt-github

[Can I use GPL software binaries in commercial environment? (closed)](https://stackoverflow.com/questions/5437501/can-i-use-gpl-software-binaries-in-commercial-environment)
[Can I use GPL software in a commercial application](https://softwareengineering.stackexchange.com/questions/47032/can-i-use-gpl-software-in-a-commercial-application)

[GNU General Public License (v2): can a company use the licensed software for free? (closed)](https://stackoverflow.com/questions/3046150/gnu-general-public-license-v2-can-a-company-use-the-licensed-software-for-fre)
[Using GPL libraries without modification on a commercial website, do I need to make my source code available? (duplicate)](https://softwareengineering.stackexchange.com/questions/93269/using-gpl-libraries-without-modification-on-a-commercial-website-do-i-need-to-m)

[Using a GPL V3 library in a Android app published on Google Play, do I need to release the application's source code?](https://opensource.stackexchange.com/questions/4840/using-a-gpl-v3-library-in-a-android-app-published-on-google-play-do-i-need-to-r)

[Can I use GPL, LGPL, MPL licensed packages with my application and make it closed source?](https://softwareengineering.stackexchange.com/questions/125606/can-i-use-gpl-lgpl-mpl-licensed-packages-with-my-application-and-make-it-close)

[What constitutes “distributing” for LGPL v3](https://softwareengineering.stackexchange.com/questions/131264/what-constitutes-distributing-for-lgpl-v3)
[Can I use GPL libraries in a closed source project if only the output is distributed?](https://opensource.stackexchange.com/questions/2338/can-i-use-gpl-libraries-in-a-closed-source-project-if-only-the-output-is-distrib)
[MPL 2.0 FAQ](https://www.mozilla.org/en-US/MPL/2.0/FAQ/)
[Writing open-source? Pick MPL 2.0](http://veldstra.org/2016/12/09/you-should-choose-mpl2-for-your-opensource-project.html)
[OpenScales is released under version 3 of the GNU Lesser Public License (LGPL, available here), with an exeption related to static linking exception](http://openscales.org/license/index.html)
[Is there a modified LGPL license that allows static linking?](https://softwareengineering.stackexchange.com/questions/179084/is-there-a-modified-lgpl-license-that-allows-static-linking)
[libgit2/COPYING](https://github.com/libgit2/libgit2/blob/development/COPYING)
[If GitHub interacts with Git, and Git is licensed under GPLv2, shouldn't GitHub be open source?](https://softwareengineering.stackexchange.com/questions/340913/if-github-interacts-with-git-and-git-is-licensed-under-gplv2-shouldnt-github)
[Mozilla Public License (MPL 2.0) vs Lesser GNU General Public License (LGPL 3.0)](https://softwareengineering.stackexchange.com/questions/221365/mozilla-public-license-mpl-2-0-vs-lesser-gnu-general-public-license-lgpl-3-0)
[Free Software License](https://en.wikipedia.org/wiki/Free_software_license)
[GNU General Public License](https://en.wikipedia.org/wiki/GNU_General_Public_License)
[Mozilla Public License (MPL 2.0) vs Lesser GNU General Public License (LGPL 3.0)](https://softwareengineering.stackexchange.com/questions/221365/mozilla-public-license-mpl-2-0-vs-lesser-gnu-general-public-license-lgpl-3-0)
[Linux_kernel#Licensing_terms](https://en.wikipedia.org/wiki/Linux_kernel#Licensing_terms)
[Mozilla Public License](https://en.wikipedia.org/wiki/Mozilla_Public_License)
[VLC media player returns to the iOS App Store after 30-month hiatus](https://arstechnica.com/gadgets/2013/07/vlc-media-player-returns-to-the-ios-app-store-after-30-month-hiatus/)
[License compatibility](https://en.wikipedia.org/wiki/License_compatibility#GPL_compatibility)
[MongoDB#Licensing](https://en.wikipedia.org/wiki/MongoDB#Licensing)
[GNU Affero General Public License](https://en.wikipedia.org/wiki/GNU_Affero_General_Public_License)
[Git](https://en.wikipedia.org/wiki/Git)
[MIT License](https://en.wikipedia.org/wiki/MIT_License)
[Expat License](https://en.wikipedia.org/wiki/MIT_License)
[MIT vs. BSD vs. Dual License](https://softwareengineering.stackexchange.com/questions/121998/mit-vs-bsd-vs-dual-license)
[What are the essential differences between BSD and MIT licences?](https://opensource.stackexchange.com/questions/217/what-are-the-essential-differences-between-bsd-and-mit-licences)
[The BSD 3-Clause License](https://github.com/timoxley/osi-licenses-full/blob/master/licenses/BSD-3-Clause.md)
[tl;dr Legal: GNU General Public License v3 (GPL-3)](https://tldrlegal.com/license/gnu-general-public-license-v3-(gpl-3))
[tl;dr Legal: Apache License 2.0 (Apache-2.0)](https://tldrlegal.com/license/apache-license-2.0-(apache-2.0))
[tl;dr Legal: MIT License (Expat)](https://tldrlegal.com/license/mit-license)
[tl;dr Legal: GNU Affero General Public License v3 (AGPL-3.0)](https://tldrlegal.com/license/gnu-affero-general-public-license-v3-(agpl-3.0))
[tl;dr Legal: GNU General Public License v3 (GPL-3)](https://tldrlegal.com/license/gnu-general-public-license-v3-(gpl-3))
[tl;dr Legal: Mozilla Public License 2.0 (MPL-2.0)](https://tldrlegal.com/license/mozilla-public-license-2.0-(mpl-2))
[tl;dr Legal: GNU Lesser General Public License v3 (LGPL-3.0)](https://tldrlegal.com/license/gnu-lesser-general-public-license-v3-(lgpl-3))
[tl;dr Legal: GNU General Public License v2.0 (GPL-2.0)](https://tldrlegal.com/license/gnu-general-public-license-v2)
[tl;dr Legal: GNU Lesser General Public License v2.1 (LGPL-2.1)](https://tldrlegal.com/license/gnu-lesser-general-public-license-v2.1-(lgpl-2.1))
[tl;dr Legal: BSD 3-Clause License (Revised)](https://tldrlegal.com/license/bsd-3-clause-license-(revised))
[Difference between Affero-GPL and GPLv3 (closed)](https://stackoverflow.com/questions/2127246/difference-between-affero-gpl-and-gplv3)
[The AGPL, MongoDB](https://www.mongodb.com/blog/post/the-agpl)
[Are you supposed to fork a repo if you're porting it to another language?](https://softwareengineering.stackexchange.com/questions/364609/are-you-supposed-to-fork-a-repo-if-youre-porting-it-to-another-language)

[What does “express grant of patent rights from contributors to users” mean?](https://opensource.stackexchange.com/questions/6302/what-does-express-grant-of-patent-rights-from-contributors-to-users-mean)

{% ltr %}
    </div>
{% endltr %}

<br>

> تم كتابة هذهِ المقالة بإستخدم المحرر [CotEditor](http://coteditor.com/) البسيط و العَمَلي بنفس الوقت ، لأنه يدعم إتجاه الكتابة العربية من اليمين لليسار.
[شكراً لهُم على هذا التعديل](https://github.com/coteditor/CotEditor/issues/759).
CotEditor تحت رخصة الـ Apache 2.0 🙂.



