import React, { useMemo, useState } from "react";

/**

GIS Mauritania Daily — Interactive News + Editorial Dashboard (Multilingual)


---

NEW: Language switcher (English • Français • العربية) with RTL support.

Provide titles/briefings per language.


Link each headline to language-specific Google Doc drafts.


Arabic layout flips to RTL automatically.


🔗 Google Docs ownership: frenchgarythomas@gmail.com

➜ Replace each docUrl.{en|fr|ar} below with share links

(set Docs to "Anyone with the link can view/comment" or restrict as needed).


*/

// ----------------------------- // Config // ----------------------------- const LANGS = [ { code: "en", label: "English", dir: "ltr" }, { code: "fr", label: "Français", dir: "ltr" }, { code: "ar", label: "العربية", dir: "rtl" } ];

const TODAY = new Date().toLocaleDateString();

// Demo multilingual content — swap with live data or a JSON feed const HEADLINES = [ { id: "h1", title: { en: "Nouakchott Water Relief: Beni Nadji Station Online", fr: "Nouakchott : mise en service de la station de prétraitement Beni Nadji", ar: "نواكشوط: بدء تشغيل محطة بني ناجي لمعالجة المياه" }, briefing: { en: "PowerChina's pretreatment plant begins trial operations, easing turbidity and stabilizing supply to the capital.", fr: "La station de prétraitement entre en phase d’essai, réduisant la turbidité et stabilisant l’alimentation en eau de la capitale.", ar: "بدء التشغيل التجريبي لمحطة المعالجة المسبقة مما يقلل العكارة ويثبت إمدادات المياه للعاصمة." }, tags: ["Infrastructure", "Water"], docUrl: { en: "https://docs.google.com/document/d/EXAMPLE_WATER_EN", fr: "https://docs.google.com/document/d/EXAMPLE_WATER_FR", ar: "https://docs.google.com/document/d/EXAMPLE_WATER_AR" } }, { id: "h2", title: { en: "Mauritania–Saudi Iron JV Targets 12–14M Tons/yr", fr: "Coentreprise Mauritanie–Arabie saoudite : objectif 12–14 M t/an de minerai", ar: "شراكة موريتانية-سعودية في الحديد تستهدف 12–14 مليون طن سنويًا" }, briefing: { en: "SNIM and Hadeed launch a logistics‑backed expansion plan to raise annual ore output and export reliability.", fr: "La SNIM et Hadeed lancent un plan d’expansion soutenu par la logistique pour augmenter la production et fiabiliser les exportations.", ar: "إطلاق خطة توسع بدعم لوجستي بين SNIM وHadeed لرفع الإنتاج السنوي وتحسين موثوقية التصدير." }, tags: ["Mining", "Economy"], docUrl: { en: "https://docs.google.com/document/d/EXAMPLE_MINING_EN", fr: "https://docs.google.com/document/d/EXAMPLE_MINING_FR", ar: "https://docs.google.com/document/d/EXAMPLE_MINING_AR" } }, { id: "h3", title: { en: "Spain Pledges €200M: Migration & Development Pact", fr: "L’Espagne promet 200 M€ : pacte migration et développement", ar: "إسبانيا تتعهد بـ200 مليون يورو: اتفاق للهجرة والتنمية" }, briefing: { en: "Madrid ties funding to regulated migration, cybersecurity, and infrastructure co‑operation.", fr: "Madrid conditionne les financements à une migration régulée, à la cybersécurité et à la coopération en infrastructures.", ar: "تمويل مدريد مرتبط بالهجرة المنظمة والأمن السيبراني والتعاون في البنية التحتية." }, tags: ["Diplomacy", "Migration"], docUrl: { en: "https://docs.google.com/document/d/EXAMPLE_SPAIN_EN", fr: "https://docs.google.com/document/d/EXAMPLE_SPAIN_FR", ar: "https://docs.google.com/document/d/EXAMPLE_SPAIN_AR" } } ];

const EDITORIAL = { predictions: [ { id: "p1", text: { en: "Stock exchange groundwork accelerates; expect founding committee invites in Q2–Q3 2026 if branding and provenance pilots are visible by year‑end.", fr: "Accélération des travaux de la bourse ; invitations au comité fondateur attendues T2–T3 2026 si l’image de marque et les pilotes de traçabilité sont visibles d’ici fin d’année.", ar: "تسارع أعمال البورصة؛ دعوات اللجنة التأسيسية متوقعة في الربعين 2–3 من 2026 إذا ظهرت العلامة التجارية وتجارب التتبع بنهاية العام." }, confidence: 0.72 }, { id: "p2", text: { en: "Two large‑scale green hydrogen pilots will anchor a coastal renewable belt; local microgrids gain resale revenues by late 2026.", fr: "Deux pilotes d’hydrogène vert à grande échelle ancreront une ceinture d’énergies côtières ; les micro‑réseaux locaux généreront des revenus de revente d’ici fin 2026.", ar: "مشروعا هيدروجين أخضر كبيران سيرسيان حزامًا متجددًا ساحليًا؛ وستحقق الشبكات المصغرة المحلية إيرادات إعادة بيع بحلول أواخر 2026." }, confidence: 0.69 } ], advice: [ { id: "a1", text: { en: "Secure early listings for MineTrace‑compliant miners; negotiate branding rights on provenance certificates (Mīzān al‑Ṣafā).", fr: "Sécuriser des premières inscriptions pour les mines conformes à MineTrace ; négocier des droits de marque sur les certificats de provenance (Mīzān al‑Ṣafā).", ar: "تأمين إدراجات مبكرة للشركات المتوافقة مع MineTrace؛ التفاوض على حقوق العلامة في شهادات المنشأ (ميزان الصفاء)." } }, { id: "a2", text: { en: "Expand FisherNet + solar cold‑chain at Nouadhibou to capture price spread before peak export season.", fr: "Étendre FisherNet + chaîne du froid solaire à Nouadhibou pour capter l’écart de prix avant la haute saison d’exportation.", ar: "توسيع FisherNet + سلسلة التبريد الشمسية في نواذيبو لاقتناص فارق الأسعار قبل ذروة موسم التصدير." } } ], warnings: [ { id: "w1", text: { en: "Migration enforcement optics may trigger NGO pushback; align communications with humanitarian safeguards to reduce reputational risk.", fr: "La perception des contrôles migratoires peut susciter des réactions d’ONG ; aligner la communication avec des garanties humanitaires pour réduire le risque réputationnel.", ar: "قد تثير صورة إنفاذ الهجرة رد فعل المنظمات غير الحكومية؛ وحِّد الرسائل مع ضمانات إنسانية لتقليل المخاطر على السمعة." } }, { id: "w2", text: { en: "Dust and heatwaves can impair PV output; plan maintenance and panel‑cleaning logistics ahead of summer highs.", fr: "La poussière et les vagues de chaleur peuvent réduire la production PV ; planifier maintenance et nettoyage des panneaux avant les pics estivaux.", ar: "الغبار وموجات الحر قد يؤثران على إنتاج الألواح؛ خطِّط للصيانة وتنظيف الألواح قبل ذروة الصيف." } } ] };

// ----------------------------- // Helpers // ----------------------------- function classNames(...xs) { return xs.filter(Boolean).join(" "); }

function t(obj, lang) { if (obj == null) return ""; if (typeof obj === "string") return obj; // fallback return obj[lang] ?? obj.en ?? Object.values(obj)[0] ?? ""; }

function Badge({ label, active, onClick }) { return ( <button onClick={onClick} className={classNames( "px-3 py-1 rounded-full text-sm border transition", active ? "bg-black text-white border-black" : "bg-white text-gray-700 border-gray-300 hover:bg-gray-50" )} > {label} </button> ); }

function Stat({ label, value, hint }) { return ( <div className="rounded-2xl border p-4 shadow-sm bg-white"> <div className="text-xs uppercase tracking-wide text-gray-500">{label}</div> <div className="text-2xl font-semibold mt-1">{value}</div> {hint && <div className="text-xs mt-1 text-gray-500">{hint}</div>} </div> ); }

function Section({ title, children, right }) { return ( <section className="space-y-4"> <div className="flex items-center justify-between gap-2"> <h2 className="text-xl font-semibold">{title}</h2> {right} </div> {children} </section> ); }

function HeadlineCard({ item, lang }) { const url = item.docUrl?.[lang] || item.docUrl?.en || "#"; return ( <article className="border rounded-2xl p-4 bg-white shadow-sm hover:shadow-md transition"> <header className="flex items-start justify-between gap-4"> <h3 className="text-lg font-semibold leading-snug flex-1">{t(item.title, lang)}</h3> <div className="text-xs text-gray-500 whitespace-nowrap">{TODAY}</div> </header> <p className="mt-2 text-gray-700">{t(item.briefing, lang)}</p> <div className="mt-3 flex flex-wrap gap-2"> {item.tags.map((tg) => ( <span key={tg} className="text-xs px-2 py-1 rounded-full bg-gray-100 border text-gray-700">{tg}</span> ))} </div> <div className="mt-4 flex flex-wrap gap-2"> <a
className="inline-flex items-center justify-center px-4 py-2 rounded-xl bg-black text-white text-sm hover:opacity-90"
href={url}
target="_blank"
rel="noreferrer noopener"
> {lang === "fr" ? "Lire l’article complet (Google Doc)" : lang === "ar" ? "اقرأ المقال بالكامل (مستند Google)" : "Read Full Article (Google Doc)"} </a> <button className="inline-flex items-center justify-center px-3 py-2 rounded-xl border text-sm hover:bg-gray-50" onClick={() => navigator.clipboard.writeText(url)} > {lang === "fr" ? "Copier le lien" : lang === "ar" ? "نسخ الرابط" : "Copy Doc Link"} </button> </div> </article> ); }

function EditorialTicker({ title, items, variant = "neutral", lang }) { const color = variant === "warn" ? "bg-yellow-50 border-yellow-200" : variant === "pro" ? "bg-green-50 border-green-200" : "bg-blue-50 border-blue-200"; return ( <div className={classNames("rounded-2xl border p-4 space-y-3", color)}> <div className="text-sm font-semibold">{title}</div> <ul className="space-y-2"> {items.map((it) => ( <li key={it.id} className="text-sm leading-relaxed text-gray-800">{t(it.text, lang)}{it.confidence != null && (<span className="ml-2 text-xs text-gray-600">(Confidence: {(it.confidence * 100).toFixed(0)}%)</span>)}</li> ))} </ul> </div> ); }

export default function App() { const [query, setQuery] = useState(""); const [tag, setTag] = useState("All"); const [lang, setLang] = useState("en");

const filtered = useMemo(() => { const q = query.trim().toLowerCase(); return HEADLINES.filter((h) => { const matchesTag = tag === "All" || h.tags.includes(tag); const matchesQ = !q || t(h.title, lang).toLowerCase().includes(q) || t(h.briefing, lang).toLowerCase().includes(q) || h.tags.some((tg) => tg.toLowerCase().includes(q)); return matchesTag && matchesQ; }); }, [query, tag, lang]);

const langMeta = LANGS.find((l) => l.code === lang) || LANGS[0];

return ( <div className="min-h-screen bg-gray-50" dir={langMeta.dir}> {/* Header */} <header className="sticky top-0 z-50 backdrop-blur bg-white/80 border-b"> <div className="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between gap-3"> <div className="flex items-center gap-3"> <div className="w-9 h-9 rounded-xl bg-black text-white grid place-items-center font-bold">GIS</div> <div> <div className="text-sm font-semibold leading-tight">{lang === "fr" ? "Mauritanie Quotidien" : lang === "ar" ? "موريتانيا اليوم" : "Mauritania Daily"}</div> <div className="text-xs text-gray-500">{lang === "fr" ? "Titres • Brèves • Éditorial" : lang === "ar" ? "عناوين • موجز • افتتاحية" : "Headlines • Briefings • Editorial"}</div> </div> </div>

<div className="flex items-center gap-2">
        {/* Language switcher */}
        <div className="flex items-center gap-1 bg-gray-100 rounded-xl p-1 border">
          {LANGS.map((l) => (
            <button
              key={l.code}
              onClick={() => setLang(l.code)}
              className={classNames(
                "px-3 py-1 rounded-lg text-sm",
                lang === l.code ? "bg-white border shadow-sm" : "text-gray-700"
              )}
            >
              {l.label}
            </button>
          ))}
        </div>
        <input
          value={query}
          onChange={(e) => setQuery(e.target.value)}
          placeholder={lang === "fr" ? "Rechercher titres, tags…" : lang === "ar" ? "ابحث في العناوين والوسوم…" : "Search headlines, tags…"}
          className="w-full max-w-md px-3 py-2 rounded-xl border bg-white text-sm focus:outline-none focus:ring-2 focus:ring-black/20"
        />
      </div>
    </div>
  </header>

  {/* Main */}
  <main className="max-w-6xl mx-auto px-4 py-6 space-y-8">
    {/* Top Stats */}
    <div className="grid grid-cols-1 sm:grid-cols-3 gap-4">
      <Stat label={lang === "fr" ? "Date" : lang === "ar" ? "التاريخ" : "Date"} value={TODAY} />
      <Stat label={lang === "fr" ? "Articles du jour" : lang === "ar" ? "قصص اليوم" : "Stories Today"} value={HEADLINES.length} hint={lang === "fr" ? "Liés aux Google Docs" : lang === "ar" ? "مرتبطة بمستندات Google" : "Linked to Google Docs"} />
      <Stat label={lang === "fr" ? "Notes éditoriales" : lang === "ar" ? "ملاحظات افتتاحية" : "Editorial Notes"} value={EDITORIAL.predictions.length + EDITORIAL.advice.length + EDITORIAL.warnings.length} />
    </div>

    {/* Filters */}
    <Section
      title={lang === "fr" ? "Brève du jour" : lang === "ar" ? "الموجز اليومي" : "Daily Brief"}
      right={
        <div className="flex flex-wrap gap-2">
          {["All","Infrastructure","Water","Mining","Economy","Energy","Diplomacy","Migration","Culture"].map((t) => (
            <Badge key={t} label={t} active={t === tag} onClick={() => setTag(t)} />
          ))}
        </div>
      }
    >
      <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
        {filtered.map((h) => (
          <HeadlineCard key={h.id} item={h} lang={lang} />
        ))}
      </div>
      {filtered.length === 0 && (
        <div className="text-sm text-gray-600">{lang === "fr" ? "Aucun article ne correspond à vos filtres." : lang === "ar" ? "لا توجد مقالات مطابقة للمرشحات." : "No stories match your filters."}</div>
      )}
    </Section>

    {/* Editorial */}
    <Section title={lang === "fr" ? "Éditorial — Prédictions, Conseils, Alertes" : lang === "ar" ? "الافتتاحية — تنبؤات ونصائح وتحذيرات" : "Editorial — Predictions, Advice, Warnings"}>
      <div className="grid grid-cols-1 md:grid-cols-3 gap-4">
        <EditorialTicker title={lang === "fr" ? "Prédictions" : lang === "ar" ? "تنبؤات" : "Predictions"} items={EDITORIAL.predictions} variant="pro" lang={lang} />
        <EditorialTicker title={lang === "fr" ? "Conseils" : lang === "ar" ? "نصائح" : "Advice"} items={EDITORIAL.advice} variant="neutral" lang={lang} />
        <EditorialTicker title={lang === "fr" ? "Alertes" : lang === "ar" ? "تحذيرات" : "Warnings"} items={EDITORIAL.warnings} variant="warn" lang={lang} />
      </div>
    </Section>

    {/* Footer note */}
    <div className="text-xs text-gray-500 pt-4 border-t">
      © {new Date().getFullYear()} Gangary Intelligence Systems — {lang === "fr" ? "Pôle Mauritanie" : lang === "ar" ? "قسم موريتانيا" : "Mauritania Desk"}. {lang === "fr" ? "Le contenu éditorial combine des informations vérifiées et une analyse prospective." : lang === "ar" ? "المحتوى الافتتاحي يجمع بين تقارير موثوقة وتحليل استشرافي." : "Editorial content blends verified reporting with forward‑looking analysis."}
    </div>
  </main>
</div>

); }

