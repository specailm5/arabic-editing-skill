# مهارة التحرير والنقد والتدقيق
### (Arabic Editing & Critique Skill)

**Arabic editing skill for AI agents** — edits in layers (structural, paragraph, line, copy, proof, fact-check), produces an editorial report with severity and reasons, preserves the author's voice, and refuses silent rewrites. Works with Claude Code, Codex, Antigravity and VS Code agent harnesses.

🔗 **الموقع المرجعي: [specailm5.github.io/arabic-editing-skill](https://specailm5.github.io/arabic-editing-skill/)**

> مهارة برمجية لتحرير النصوص العربية ونقدها وتدقيقها، مبنية على **«الأسلوب»** و**«أصول النقد الأدبي»** لأحمد الشايب، و**«معجم الصواب اللغوي»** لأحمد مختار عمر.

---

## 📖 ما هي المهارة؟

خمس وظائف:

1. **التحرير البنيوي:** الأطروحة، البناء، الحجة.
2. **تحرير الفقرة:** وحدة الفكرة، الترابط، الانتقال.
3. **تحرير الجملة:** الطول، الترتيب، الحشو، العرنجية.
4. **التدقيق:** النحو، الإملاء، الترقيم، الاتساق.
5. **التحقق:** المراجع، الأرقام، الأسماء، التواريخ.

**القواعد الأربع:**
> **صوت الكاتب أولاً. أقل تدخل. كل تعديل بسببه. التحقق قبل التسليم.**

---

## 📂 بنية المهارة

```
arabic-editing-skill/
│
├── skills/arabic-editing-skill/
│   ├── SKILL.md
│   ├── references/
│   │   ├── structural_edit.md    # البنية والأطروحة والفقرة
│   │   ├── line_edit.md          # الجملة والكلمة والحشو
│   │   ├── proofreading.md       # النحو والإملاء والترقيم
│   │   ├── fact_check.md         # المراجع والأرقام
│   │   └── editorial_report.md   # قالب التقرير
│   └── examples/
│       ├── before_after_editing.md
│       └── editorial_reports.md
│
├── docs/
├── .agents/skills/arabic-editing-skill/
└── .claude/skills/arabic-editing-skill/
```

---

## 🚀 التثبيت

```bash
npx skills add specailm5/arabic-editing-skill -g -y
```

أو لبيئات محددة:

```bash
npx skills add specailm5/arabic-editing-skill -a claude-code -a codex
```

### يدوياً (Windows)

```powershell
$src = "skills\arabic-editing-skill"

New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills\arabic-editing-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.claude\skills\arabic-editing-skill\"

New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.agents\skills\arabic-editing-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.agents\skills\arabic-editing-skill\"

New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.gemini\config\skills\arabic-editing-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.gemini\config\skills\arabic-editing-skill\"
```

---

## ⚡ كيف تعمل؟

### ستة أسئلة

| السؤال | لماذا؟ |
| :--- | :--- |
| **ما نوع النص؟** | معايير التحرير |
| **ما مستوى التحرير؟** | عمق التدخل |
| **ما الجمهور؟** | اللغة والمثال |
| **ما الغرض؟** | وضوح/قوة/جمال |
| **هل أحفظ الصوت؟** | حجم التعديل |
| **ما المخرج؟** | تقرير/نص/كلاهما |

### المستويات الخمسة

| المستوى | ما يعالجه | مثال |
| :--- | :--- | :--- |
| **بنيوي** | الأطروحة، البناء | مقال بلا أطروحة |
| **فقرة** | وحدة الفكرة | فقرة بثلاث أفكار |
| **جملة** | الطول، الترتيب | جملة ٦٠ كلمة |
| **تدقيق** | النحو، الإملاء | همزة، فاصلة |
| **تحقق** | المراجع، الأرقام | «تشير الدراسات» |

### قالب التقرير

| الحقل | المعنى |
| :--- | :--- |
| **الموضع** | أين المشكلة؟ |
| **المشكلة** | ما الخطأ؟ |
| **الخطورة** | عالية/متوسطة/منخفضة |
| **الاقتراح** | ماذا تفعل؟ |
| **السبب** | لماذا؟ |

### أمثلة سريعة

| قبل | بعد | المستوى |
| :--- | :--- | :--- |
| «قام بدراسة» | «درس» | جملة/كلمة |
| «تم اتخاذ القرار» | «اتخذت اللجنة القرار» | جملة |
| «من خلال» | «بـ» / احذف | كلمة |
| «جملة ٦٠ كلمة» | جملتان | جملة |
| «فقرة بثلاث أفكار» | ثلاث فقرات | فقرة |
| «خاتمة بفكرة جديدة» | خاتمة تلخص | بنية |

---

## 📚 المصادر

1. **«الأسلوب: دراسة بلاغية تحليلية لأصول الأساليب الأدبية»** — أحمد الشايب:
   <https://archive.org/details/20191001_20191001_2225>
2. **«أصول النقد الأدبي»** — أحمد الشايب:
   <https://archive.org/details/aswl-alnqd-aladby>
3. **«معجم الصواب اللغوي»** — أحمد مختار عمر — عالم الكتب، القاهرة:
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

## 📜 الترخيص

هذه المهارة مفتوحة المصدر ومتاحة للاستخدام الشخصي والتجاري والبحثي لدعم التحرير العربي.
