## Mohammed Khankan

Founder & CEO of **OFOQ Technical Solutions & Digitalization** and **RAFD**. Software engineer, based in Saudi Arabia.

I build SaaS products and internal business systems, and I stay with them after launch: onboarding the first customers, fixing what breaks under real use, and shipping the next version.

[Portfolio & case studies](https://mohammedkhankan.github.io/khankan-portfolio/en/) · [LinkedIn](https://www.linkedin.com/in/mohammed-tarek-533a2a214/) · [Email](mailto:engmohammedkhankan@gmail.com) · [WhatsApp](https://wa.me/966510371924)

---

### Products

| Product | What it is | Where it stands |
| --- | --- | --- |
| [**RUKN**](https://mohammedkhankan.github.io/khankan-portfolio/en/projects/rukn/) · ركن | Multi-merchant e-commerce SaaS. Each store gets its own isolated data. | 10 stores onboarded in the first launch |
| [**OFOQ Restaurant OS**](https://mohammedkhankan.github.io/khankan-portfolio/en/projects/ofoq/) · أفق | Tables, orders, waiters, cashier, kitchen stations and reservations in one system, with a [public digital menu](https://menu.ofoqsy.com/). | Running in 7 restaurants (trial) |
| [**MAAZEEM**](https://mohammedkhankan.github.io/khankan-portfolio/en/projects/maazeem/) · معازيم | Multi-tenant platform for invitations, guest lists, RSVP and QR check-in. | 52/52 tests on an isolated PostgreSQL · 10,000 guests imported in 1.84 s |
| [**RAFD**](https://rafd6.netlify.app/) · رفد | Supplementary learning platform for Syrian Virtual University students, plus the internal finance system behind it. | 2,000+ subscribers · 700+ videos |
| [**AL TAYF Architecture**](https://altayf-sa.com/) | Company website for an architecture firm in Saudi Arabia. | Live |

Product source code is private. The case studies cover the problem, the decisions, the test results and screenshots.

### A few things I've had to get right

- **Tenant isolation.** RUKN keys every store's data to its tenant, and the rule lives in the data-access layer instead of depending on each screen to remember it.
- **Concurrency at the door.** MAAZEEM check-in is a single conditional `UPDATE` backed by a `CHECK` constraint. In testing, 30 simultaneous scans on a 5-guest invitation admitted exactly 5.
- **Messy imports.** 10,000 guests from Excel in 1.84 s, handling Arabic-Indic digits and invisible characters, catching duplicates, and keeping plan limits under concurrent requests.
- **Roles that match the job.** OFOQ has separate views for owner, cashier, waiter and kitchen.

### Stack

Varies by product. Recent work:

- **RUKN:** ASP.NET Core (.NET 10), EF Core, React, TypeScript, PostgreSQL, Docker
- **OFOQ:** Next.js, React, TypeScript, Prisma, PostgreSQL, Supabase Auth, Docker
- **MAAZEEM:** Next.js, TypeScript, Drizzle ORM, PostgreSQL 17, Zod, Docker Compose

---

<div dir="rtl">

مؤسس ومدير تنفيذي لـ**شركة أفق للحلول التقنية والرقمنة** ولـ**منصة رفد التعليمية**. أبني منتجات SaaS وأنظمة أعمال داخلية، وأتابعها بعد الإطلاق مع العملاء الأوائل. دراسات الحالة بالعربي على [موقعي](https://mohammedkhankan.github.io/khankan-portfolio/ar/).

</div>
