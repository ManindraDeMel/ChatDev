# وكلاء الاتصال لتطوير البرمجيات

<p align="center">
  <img src='./misc/logo1.png' width=550>
</p>

<p align="center">
    *الإنجليزية <unk> <a href="readme/README-Chinese.md">الصينية</a> <unk> <a href="readme/README-Japanese.md">اليابانية</a> <unk> <a href="readme/README-Korean.md">الكورية</a> <unk> <a href="readme/README-Filipino.md">الفلبيني</a> <unk> <a href="readme/README-French.md">الفرنسية</a> <unk> <a href="readme/README-Slovak.md">السلوفاكية</a> <unk> <a href="readme/README-Portuguese.md"></a> <unk> <a href="readme/README-Spanish.md">الإسبانية</a> <unk> <a href="readme/README-Dutch.md">الهولندية</a> <unk> <a href="readme/README-Hindi.md">الهندي</a>
</p>
<p align="center">
    <unk> 📚 <a href="wiki.md">Wiki</a> <unk> 🚀 <a href="wiki.md#local-demo">العرض التجريبي المحلي</a> <unk> 👥 <a href="Contribution.md">البرنامج المدمج</a> <unk> 🔧 <a href="wiki.md#customization">التخصيص</a> ث
</p>

## 📖 نظرة عامة

- **ChatDev** stands as a **virtual software company** that operates through various **intelligent agents** holding different roles, including Chief Executive Officer <img src='online_log/static/figures/ceo.png' height=20>, Chief Product Officer <img src='online_log/static/figures/cpo.png' height=20>, Chief Technology Officer <img src='online_log/static/figures/cto.png' height=20>, programmer <img src='online_log/static/figures/programmer.png' height=20>, reviewer <img src='online_log/static/figures/reviewer.png' height=20>, tester <img src='online_log/static/figures/tester.png' height=20>, art designer <img src='online_log/static/figures/designer.png' height=20>. These agents form a multi-agent organizational structure and are united by a mission to "revolutionize the digital world through programming." يتعاون الوكلاء داخل ChatDev **مع** من خلال المشاركة في الحلقات الدراسية الفنية المتخصصة، بما في ذلك مهام مثل التصميم والبرمجة والاختبار والتوثيق.
- The primary objective of ChatDev is to offer an **easy-to-use**, **highly customizable** and **extendable** framework, which is based on large language models (LLMs) and serves as an ideal scenario for studying collective intelligence.
<p align="center">
  <img src='./misc/company.png' width=600>
</p>

## 🎉 الأخبار

* **26 أكتوبر 2023: ChatDev مدعوم الآن مع Docker للتنفيذ الآمن** (بفضل المساهمة من [ManindraDeMel](https://github.com/ManindraDeMel)). Please see [Docker Start Guide](wiki.md#docker-start).
  <p align="center">
  <img src='./misc/docker.png' width=400>
  </p>
* 25 سبتمبر، 2023: وضع **Git** متاح الآن، مما يمكن المبرمج <img src='online_log/static/figures/programmer.png' height=20> من استخدام Git للتحكم في الإصدار. لتمكين هذه الميزة، ببساطة تعيين `"git_management"` إلى `"True"` في `ChatChainConfig.json`. راجع الدليل [](wiki.md#git-mode).
  <p align="center">
  <img src='./misc/github.png' width=600>
  </p>
* 20 سبتمبر 2023: وضع **A-Agent-Interaction** متاح الآن! يمكنك المشاركة مع فريق ChatDev عن طريق لعب دور المستعرض <img src='online_log/static/figures/reviewer.png' height=20> وتقديم اقتراحات إلى المبرمج <img src='online_log/static/figures/programmer.png' height=20>؛ جرب `تشغيل python3. y --task [description_of_your_idea] --config "Human"`. راجع الدليل [](wiki.md#human-agent-interaction) و [المثال](WareHouse/Gomoku_HumanAgentInteraction_20230920135038).
  <p align="center">
  <img src='./misc/Human_intro.png' width=600>
  </p>
* 1 سبتمبر 2023: وضع **Art** متاح الآن! يمكنك تنشيط وكيل المصمم <img src='online_log/static/figures/designer.png' height=20> لتوليد صور مستخدمة في البرنامج؛ حاول `python3 run.py --task [description_of_your_idea] --تكوين "Art"`. راجع الدليل [](wiki.md#art) و [المثال](WareHouse/gomokugameArtExample_THUNLP_20230831122822).
* 28 أغسطس 2023: النظام متاح للجمهور.
* 17 أغسطس 2023: النسخة v1.0.0 كانت جاهزة للإصدار.
* 30 يوليو 2023: يمكن للمستخدمين تخصيص إعدادات الدردشة والمرحلة والدور. بالإضافة إلى ذلك، يتم الآن دعم وضع تسجيل الدخول على الإنترنت ووضع إعادة العرض .
* 16 يوليو، 2023: تم نشر ورقة الطباعة [](https://arxiv.org/abs/2307.07924) المرتبطة بهذا المشروع.
* 30 يونيو 2023: تم إصدار النسخة الأولية من مستودع ChatDev .

## ❓ ماذا يمكن أن تفعل ChatDev؟

![مقدمة](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## ⚡ البداية السريعة

### :desktop_الكمبيوتر: البداية السريعة مع المحطة الطرفية

للبدء، قم باتباع الخطوات التالية:

1. **استنساخ مستودع GitHub :** ابدأ باستنساخ المستودع باستخدام الأمر:
   ```
   git clone https://github.com/OpenBMB/ChatDev.git
   ```
2. **تعيين بيئة Python:** تأكد من أن لديك نسخة 3.9 أو أعلى من بيئة Python. يمكنك إنشاء و تنشيط هذه البيئة باستخدام الأوامر التالية، استبدال `ChatDev_conda_env` باسم البيئة المفضلة لديك :
   ```
   إنشاء -n ChatDev_conda_env python=3.9 y
   تفعيل ChatDev_conda_env
   ```
3. **التبعيات التثبيت:** انتقل إلى دليل `ChatDev` وتثبيت التبعيات اللازمة عن طريق التشغيل:
   ```
   cd ChatDev
   pip3 install -r requirements.txt
   ```
4. **تعيين مفتاح API OpenAI:** تصدير مفتاح API الخاص بك كمتغير بيئي. استبدل `"your_OpenAI_API_key"` بـ مفتاح API الفعلي الخاص بك. تذكر أن متغير البيئة هذا مخصص للدورة، لذا تحتاج إلى تعيينه مرة أخرى إذا كنت افتح جلسة طرفية جديدة. على Unix/Linux:
   ```
   تصدير OPENAI_API_KEY="your_OpenAI_API_key"
   ```
   على النوافذ:
   ```
   $env:OPENAI_API_KEY="your_OpenAI_API_key"
   ```
5. **ابني برنامجك:** استخدم الأمر التالي لبدء بناء برنامجك، استبدل `[description_of_your_idea]` بوصف فكرتك و `[project_name]` باسمك المطلوب : على يونكس/لينوكس:
   ```
   python3 run.py --task "[description_of_your_idea]--name "[project_name]"
   ```
   على النوافذ:
   ```
   python run.py --task "[description_of_your_idea]--name "[project_name]"
   ```
6. **Run Your Software:** Once generated, you can find your software in the `WareHouse` directory under a specific project folder, such as `project_name_DefaultOrganization_timestamp`. قم بتشغيل برنامجك باستخدام الأمر التالي داخل ذلك الدليل: على Unix/Linux:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python3 main.py
   ```
   على النوافذ:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python main.py
   ```

### 🐳 بداية سريعة مع Docker
- نشكر [ManindraDeMel](https://github.com/ManindraDeMel) على تقديم دعم Docker. Please see [Docker Start Guide](wiki.md#docker-start).

## ✨ مهارات متقدمة

للحصول على مزيد من المعلومات التفصيلية، يرجى الرجوع إلى [Wiki](wiki.md)لدينا، حيث يمكنك العثور على:

- مقدمة لجميع معلمات تشغيل الأمر.
- A straightforward guide for setting up a local web demo, which includes enhanced visualized logs, a replay demo, and a simple ChatChain Visualizer.
- استعراض عام لإطار تشاتديف.
- مقدمة شاملة لجميع البارامترات المتقدمة في تكوين ChatChain.
- أدلة لتخصيص ChatDev، بما في ذلك:
    - سلسلة الدردشة: تصميم عملية تطوير البرنامج الخاص بك (أو أي عملية أخرى)، مثل مثل `تحليل الطلب -> الترميز -> اختبار -> Manual`
    - مرحلت: تصميم المرحلة الخاصة بك داخل ChatChain، مثل `تحليل الطلب`.
    - الدور: تحديد مختلف الوكلاء في شركتك مثل `الرئيس التنفيذي`.

## 🤗 شارك برامجك!

**Code**: نحن متحمسون لاهتمامك بالمشاركة في مشروعنا مفتوح المصدر. If you come across any problems, don't hesitate to report them. لا تتردد في إنشاء طلب سحب إذا كان لديك أي استفسارات أو إذا كنت على استعداد لمشاركة عملك معنا! إن إسهاماتك تحظى بتقدير كبير. Please let me know if there's anything else you need assistance!

**الشركة**: إنشاء شركة ChatDev الخاصة بك هي نوع من النسيج. هذا الإعداد المخصص يحتوي على ثلاثة ملفات بسيطة إعدادات JSON. تحقق من المثال المقدم في الدليل `CompanyConfig/Defaul`. للحصول على تعليمات مفصلة بشأن التخصيص ، يرجى الرجوع إلى [Wiki](wiki.md) الخاصة بنا.

**البرنامج**: كلما قمت بتطوير البرنامج باستخدام ChatDev، يتم إنشاء مجلد مناظر يحتوي على جميع المعلومات الأساسية . مشاركة عملك معنا أمر بسيط مثل تقديم طلب الجذب. هنا مثال: تنفيذ الأمر `python3 run.py --task "تصميم لعبة 2048" --اسم "2048" --org "THUNLP" --تكوين "Default"`. This will create a software package and generate a folder named `/WareHouse/2048_THUNLP_timestamp`. في الداخل، ستجد ما يلي:

- جميع الملفات والمستندات ذات الصلة ببرنامج اللعبة 2048
- ملفات تكوين الشركة المسؤولة عن هذا البرنامج، بما في ذلك ملفات تكوين JSON الثلاثة من `CompanyConfig/Defaulative`
- سجل شامل يفصل عملية بناء البرنامج التي يمكن استخدامها لإعادة العرض (`timestamp.log`)
- الطلب الأولي المستخدم لإنشاء هذا البرنامج (`2048.prompt`)

**شاهد البرنامج المساهم به المجتمع [هنا](Contribution.md)!**

## 👨‍💻<unk> المساهمون

<a href="https://github.com/OpenBMB/ChatDev/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenBMB/ChatDev" />
</a>

صنع مع [contrib.rocks](https://contrib.rocks).
## 🔎 الاستشهاد

```
@misc{qian2023communical,
      title={Communicative Agents for Software Development}, 
      كاتب ={Chen Qian and Xin Cong and Wei Liu and Cheng Yang and Weize Chen and Yusheng Su and Yufan Dang and Jiahao Li and Juyuan Xu and Dahai Li and Zhiyuan Liu and Maosong Sun}،
      سنة ={2023}،
      eprint={2307.07924}،
      archivePrefix={arXiv}،
      PrearyClass={cs.SE}
}
```

## ⚖️ ترخيص

- رخصة رمز المصدر: رمز مصدر مشروعنا مرخص بموجب رخصة أباتشي 2.0. يسمح هذا الترخيص باستخدام التعليمة البرمجية وتعديلها وتوزيعها، رهناً ببعض الشروط المحددة في رخصة أباتشي 2.0.
- حالة المشروع المفتوح المصدر: المشروع مفتوح المصدر فعلا؛ غير أن هذا التعيين موجه أساسا لأغراض غير تجارية. وبينما نشجع المجتمع المحلي على التعاون والإسهامات في مجال البحوث والتطبيقات غير التجارية، ومن المهم الإشارة إلى أن أي استخدام لمكونات المشروع لأغراض تجارية يتطلب إبرام اتفاقات ترخيص منفصلة.
- ترخيص البيانات: البيانات ذات الصلة المستخدمة في مشروعنا مرخصة بموجب CC BY-NC 4.0. ويسمح هذا الترخيص صراحة باستخدام البيانات بصورة غير تجارية. ونود أن نشدد على أن أي نماذج مدربة باستخدام مجموعات البيانات هذه ينبغي أن تتقيد تقيدا صارما بالقيود المفروضة على الاستخدام غير التجاري، وينبغي أن تستخدم حصرا لأغراض البحوث.

## 🌟 تاريخ النجمة

[![مخطط تاريخ النجوم](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)


## 🤝 اعترافات

<a href="http://nlp.csai.tsinghua.edu.cn/"><img src="misc/thunlp.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://modelbest.cn/"><img src="misc/modelbest.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://github.com/OpenBMB/AgentVerse/"><img src="misc/agentverse.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://aibrb.com/introducing-herbie-your-super-employee-for-streamlined-productivity/"><img src="https://aibrb.com/wp-content/uploads/2023/09/Featured-on-AIBRB.com-white-1.png"  height=50pt></a>

## 📬 الاتصال

إذا كان لديك أي أسئلة، ردود فعل، أو ترغب في الاتصال، لا تتردد في التواصل معنا عبر البريد الإلكتروني على [Chatdev. penbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)
