# مهارة التحرير والنقد والتدقيق
### (Arabic Editing & Critique Skill)

<p align="center">
  <a href="https://github.com/specailm5/arabic-editing-skill/blob/master/LICENSE"><img alt="License" src="https://img.shields.io/github/license/specailm5/arabic-editing-skill?style=flat-square"></a>
  <a href="https://github.com/specailm5/arabic-editing-skill/commits/master"><img alt="Last commit" src="https://img.shields.io/github/last-commit/specailm5/arabic-editing-skill?style=flat-square"></a>
  <a href="https://specailm5.github.io/arabic-editing-skill/"><img alt="Docs" src="https://img.shields.io/badge/docs-live-brightgreen?style=flat-square"></a>
  <img alt="Agent Skills" src="https://img.shields.io/badge/Agent%20Skills-compatible-5B21B6?style=flat-square">
</p>

**Arabic editing skill for AI agents** — edits in layers (structural, paragraph, line, copy, proof, fact-check), produces an editorial report with severity and reasons, preserves the author's voice, and refuses silent rewrites: `قام بدراسة` ← `درس`, `تم اتخاذ القرار` ← `اتخذت اللجنة القرار`. Works with Claude Code, Codex, Antigravity and VS Code agent harnesses.

🔗 **الموقع المرجعي (البنية والجملة والتدقيق والتقارير): [specailm5.github.io/arabic-editing-skill](https://specailm5.github.io/arabic-editing-skill/)**

> مهارة برمجية ولغوية لنماذج الذكاء الاصطناعي والمحررات الذكية (Codex، Claude Code، Antigravity IDE، VS Code Agent Harness) لتحرير النصوص العربية ونقدها وتدقيقها، استناداً إلى **«الأسلوب»** و**«أصول النقد الأدبي»** لأحمد الشايب، و**«معجم الصواب اللغوي»** لأحمد مختار عمر.

---

## 📖 ما هي المهارة؟

**التحرير** ليس إعادة كتابة النص بصوت المحرر، بل **إزالة ما يحجب صوت الكاتب**: بنية مبعثرة، وفقرة بلا وحدة، وجملة طويلة، وكلمة غير دقيقة، ومرجع بلا مصدر. وكثير من النصوص «صحيحة اللغة، ضعيفة البناء»؛ فتُدقّق فاصلةً وتُترك أطروحةً غائبة.

تُمكِّنُ هذه المهارةُ الوكيلَ الذكيَّ من:

1. **التحرير البنيوي:** الأطروحة، البناء، الحجة، الجمهور.
2. **تحرير الفقرة:** وحدة الفكرة، الترابط، الانتقال.
3. **تحرير الجملة:** الطول، الترتيب، الحشو، العرنجية.
4. **التدقيق:** النحو، الإملاء، الترقيم، الاتساق.
5. **التحقق:** المراجع، الأرقام، الأسماء، التواريخ.
6. **تقرير التحرير:** موضع، مشكلة، خطورة، اقتراح، سبب.

**القواعد الأربع:**
> **صوت الكاتب أولاً. أقل تدخل. كل تعديل بسببه. التحقق قبل التسليم.**

---

## 📂 بنية المهارة ومكوناتها

<pre dir="rtl"><code>
arabic-editing-skill/
│
├── skills/arabic-editing-skill/          # المهارة (تركيب Agent Skills القياسي)
│   ├── SKILL.md                          # الدليل الأساسي: الطبقات والتقرير والتدقيق
│   ├── references/                       # المراجع التفصيلية
│   │   ├── structural_edit.md            # الأطروحة والبناء والفقرة
│   │   ├── line_edit.md                  # الجملة والكلمة والحشو
│   │   ├── proofreading.md               # النحو والإملاء والترقيم
│   │   ├── fact_check.md                 # المراجع والأرقام
│   │   └── editorial_report.md           # قالب التقرير
│   └── examples/                         # دراسات الحالة والنماذج
│       ├── before_after_editing.md       # نماذج قبل/بعد
│       └── editorial_reports.md          # تقارير جاهزة
│
├── docs/                                 # الموقع المرجعي (GitHub Pages)
│
├── .agents/skills/arabic-editing-skill/  # مسار Codex و Antigravity
│
└── .claude/skills/arabic-editing-skill/  # مسار Claude Code
</code></pre>

---

## 🚀 طرق التثبيت والاستخدام (Installation Guide)

تُثبَّتُ المهارةُ إما في مشروعٍ بعينه (**محلياً**)، وإما **عامةً (Global)** لتعمل في كافة المشاريع.

---

### أولاً: التثبيت بأمر واحد عبر `npx` (الطريقة الأسرع — موصى به)

```bash
npx skills add specailm5/arabic-editing-skill -g -y
```

ولاختيار بيئات بعينها أو التثبيت داخل مشروع محدد:

```bash
npx skills add specailm5/arabic-editing-skill -a claude-code -a codex
npx skills add specailm5/arabic-editing-skill --skill arabic-editing-skill -g -y
```

---

### ثانياً: التثبيت العام لبيئة Claude Code و Codex و Antigravity (يدوياً)

#### لنظام Windows (PowerShell):

```powershell
# مصدر المهارة داخل المستودع
$src = "skills\arabic-editing-skill"

# 1. تثبيت لبيئة Claude Code
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills\arabic-editing-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.claude\skills\arabic-editing-skill\"

# 2. تثبيت لبيئة Codex و Agent Skills العامة
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.agents\skills\arabic-editing-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.agents\skills\arabic-editing-skill\"

# 3. تثبيت لبيئة Google Antigravity / Gemini
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.gemini\config\skills\arabic-editing-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.gemini\config\skills\arabic-editing-skill\"
```

#### لنظام macOS / Linux (Bash):

```bash
src=skills/arabic-editing-skill

# 1. لبيئة Claude Code
mkdir -p ~/.claude/skills/arabic-editing-skill
cp -r "$src/." ~/.claude/skills/arabic-editing-skill/

# 2. لبيئة Codex و Agent Harness
mkdir -p ~/.agents/skills/arabic-editing-skill
cp -r "$src/." ~/.agents/skills/arabic-editing-skill/

# 3. لبيئة Antigravity / Gemini
mkdir -p ~/.gemini/config/skills/arabic-editing-skill
cp -r "$src/." ~/.gemini/config/skills/arabic-editing-skill/
```

---

### ثالثاً: التثبيت المحلي داخل مشروع محدد (VS Code Workspace Harness)

إذا أردت حصر المهارة داخل مستودع أو مجلد عمل واحد في VS Code:

```powershell
# داخل مجلد مشروعك الحالي:
New-Item -ItemType Directory -Force -Path ".agents\skills\arabic-editing-skill"
Copy-Item -Recurse -Force "path\to\skills\arabic-editing-skill\*" ".agents\skills\arabic-editing-skill\"
```

بمجرد فتح المشروع في **VS Code** أو تشغيل `Claude Code` / `Codex`، يكتشفُ الوكيلُ المهارةَ ويقرؤها من تلقاء نفسه عند صياغة أي نص باللغة العربية.

---

### رابعاً: الاستخدام اليدوي (Direct System Prompt / Custom Instructions)

إذا كنت تستخدم واجهات الويب (مثل ChatGPT أو Claude أو Gemini) مباشرة دون بيئة برمجية:

* افتح ملف [`skills/arabic-editing-skill/SKILL.md`](skills/arabic-editing-skill/SKILL.md) وانسخ محتواه وضعه في خانة **التعليمات المخصصة (Custom Instructions)** أو **System Prompt**.

---

## ⚡ كيف تعمل المهارة؟

### ستة أسئلة قبل التحرير

<table dir="rtl" align="right">
<thead>
<tr>
<th align="right">السؤال</th>
<th align="right">لماذا؟</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>ما نوع النص؟</strong></td>
<td>معايير التحرير</td>
</tr>
<tr>
<td><strong>ما مستوى التحرير؟</strong></td>
<td>عمق التدخل</td>
</tr>
<tr>
<td><strong>ما الجمهور؟</strong></td>
<td>اللغة والمثال</td>
</tr>
<tr>
<td><strong>ما الغرض؟</strong></td>
<td>وضوح/قوة/جمال</td>
</tr>
<tr>
<td><strong>هل أحفظ الصوت؟</strong></td>
<td>حجم التعديل</td>
</tr>
<tr>
<td><strong>ما المخرج؟</strong></td>
<td>تقرير/نص/كلاهما</td>
</tr>
</tbody>
</table>
<br clear="all">


### المستويات الخمسة

<table dir="rtl" align="right">
<thead>
<tr>
<th align="right">المستوى</th>
<th align="right">ما يعالجه</th>
<th align="right">مثال</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>بنيوي</strong></td>
<td>الأطروحة، البناء</td>
<td>مقال بلا أطروحة</td>
</tr>
<tr>
<td><strong>فقرة</strong></td>
<td>وحدة الفكرة</td>
<td>فقرة بثلاث أفكار</td>
</tr>
<tr>
<td><strong>جملة</strong></td>
<td>الطول، الترتيب</td>
<td>جملة ٦٠ كلمة</td>
</tr>
<tr>
<td><strong>تدقيق</strong></td>
<td>النحو، الإملاء</td>
<td>همزة، فاصلة</td>
</tr>
<tr>
<td><strong>تحقق</strong></td>
<td>المراجع، الأرقام</td>
<td>«تشير الدراسات»</td>
</tr>
</tbody>
</table>
<br clear="all">


### قالب تقرير التحرير

<pre dir="rtl"><code>
الموضع: ...
المشكلة: ...
الخطورة: عالية/متوسطة/منخفضة
الاقتراح: ...
السبب: ...
</code></pre>

### عيوب النصوص

<table dir="rtl" align="right">
<thead>
<tr>
<th align="right">العيب</th>
<th align="right">العلاج</th>
</tr>
</thead>
<tbody>
<tr>
<td>ركاكة</td>
<td>إحكام التركيب</td>
</tr>
<tr>
<td>غموض</td>
<td>توضيح الفكرة</td>
</tr>
<tr>
<td>تكلف</td>
<td>حذف الزخرفة</td>
</tr>
<tr>
<td>تنافر</td>
<td>قراءة صوتية</td>
</tr>
<tr>
<td>حشو</td>
<td>حذف</td>
</tr>
<tr>
<td>تناقض</td>
<td>توحيد</td>
</tr>
<tr>
<td>ابتذال</td>
<td>تجديد</td>
</tr>
<tr>
<td>أدب لفظي</td>
<td>حذف</td>
</tr>
</tbody>
</table>
<br clear="all">


---

## 📚 المراجع والاعتماد

* **«الأسلوب: دراسة بلاغية تحليلية لأصول الأساليب الأدبية»** — أحمد الشايب:
  <https://archive.org/details/20191001_20191001_2225>
* **«أصول النقد الأدبي»** — أحمد الشايب:
  <https://archive.org/details/aswl-alnqd-aladby>
* **«معجم الصواب اللغوي»** — أحمد مختار عمر — عالم الكتب، القاهرة:
  <https://archive.org/details/99325_202209>

> **إقرار بالفضل:** هذه المهارة صياغة تعليمية مستقلة لمبادئ هذه الكتب، مع نقل قواعد وأمثلة بإسنادها إلى أبوابها. ولا يتضمّن المستودع نسخاً كاملة من الكتب، ولا يُغني عن الرجوع إلى الأصل.

---

## ⚠️ حدود المسؤولية

- المهارة **للتحرير والنقد والتدقيق**، لا للكتابة من الصفر.
- لا تُعيد كتابة النص صامتة.
- لا تُقرّ رقماً أو مرجعاً بلا مصدر.
- بعض الأحكام اللغوية خلافية؛ يُذكر الخلاف ولا يُجزم.
- المستخدم مسؤول عن مراجعة النص النهائي.
- لا تُستخدم المهارة للتجريح أو التحريض.

---

## 🤝 المساهمة

نرحب بالمساهمات التي تحسّن المادة أو التحرير أو التوثيق. اقرأ [CONTRIBUTING.md](CONTRIBUTING.md) قبل فتح طلب سحب، والتزم بـ[قواعد السلوك](CODE_OF_CONDUCT.md).

## 🛡️ الأمان

إن وجدت مشكلة أمنية، فلا تفتح قضية عامة؛ راجع [SECURITY.md](SECURITY.md).

## 📄 سجل التغييرات

راجع [CHANGELOG.md](CHANGELOG.md) لمعرفة ما أُضيف في كل إصدار.

## 📬 الدعم

للأسئلة والاقتراحات: [افتح قضية](https://github.com/specailm5/arabic-editing-skill/issues).

---

## 📜 الترخيص (License)

هذه المهارة مفتوحة المصدر تحت رخصة [MIT](LICENSE)، ومتاحة للاستخدام الشخصي والتجاري والبحثي لدعم التحرير العربي.
