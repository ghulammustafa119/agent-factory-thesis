# Skills & Connectors — Questions & Answers

> Source: [Skills & Connectors: Crash Course](https://agentfactory.panaversity.org/roman/docs/skills-connectors-crash-course)

---

## Bunyadi Idea

**Q1. "Vending Machine" model aur "Operating Layer" model mein kya fark hai?**

**A:** Yeh AI use karne ke do tarike hain:

| Vending Machine Model | Operating Layer Model |
|---|---|
| Har baar task explain karo | Ek baar likho, hamesha apply hota hai |
| AI kuch "yaad" nahi rakhta | AI aapka tarika seekh jaata hai |
| Repeat karte raho | Delegate karo aur verify karo |

Teen cheezein milkar "Operating Layer" banati hain:
- **Chat messages** — AI ko ek baar batao kya karna hai
- **Skills** — AI ko har baar kaise karna hai yeh sikhao
- **Connectors** — AI ko real apps aur data tak access do

---

## Key Definitions

**Q2. "Skill" kya hoti hai aur kaise kaam karti hai?**

**A:** Skill ek saved set of instructions hai — ek text file jise `SKILL.md` kehte hain. Yeh AI ko aapka specific methodology repeatable tasks ke liye sikhati hai.

**Skill kaise kaam karti hai — "kitchen wall par recipe card" ki tarah:**
- Instructions ek baar likhte ho
- AI unhe consistently apply karta hai
- Har baar dobara explain karne ki zaroorat nahi

`SKILL.md` file ke do hisse hote hain:

| Hissa | Content | Kab Load Hota Hai |
|---|---|---|
| **Frontmatter** | Name aur description | Hamesha — relevance matching ke liye |
| **Body** | Full instructions + optional files | Sirf jab request match kare |

---

**Q3. "Connector" kya hota hai?**

**A:** Connector ek safe link hai jo AI ko aapke real apps tak access deta hai — maslan Google Drive, Gmail, Slack, project trackers.

Key points:
- AI **aapki existing permissions inherit karta hai** — jo aap nahi dekh sakte, AI bhi nahi dekh sakta
- Aap choose karte ho: **read-only** ya **read-and-write** access
- Aap control karte ho: har conversation mein kaunse connectors active hain
- **Chhota scope = kam risk**

---

**Q4. "Fire/Trigger" aur "Scope" ka kya matlab hai?**

**A:**

- **Fire/Trigger:** Jab AI automatically ek skill activate karta hai kyunke aapki request uski description se match karti hai — aapko manually call nahi karna padta
- **Scope:** Aap kitna access dete ho — ek folder ya poora Google Drive? Chhota scope hamesha safer hota hai
- **Progressive Disclosure:** AI skill ki short summary hamesha load rakhta hai, lekin full instructions sirf tab kholata hai jab zaroorat ho — speed ke liye

---

## Skills Banana

**Q5. Skill ka "description" field itna important kyun hai?**

**A:** Description field decide karta hai ke skill **kab fire hogi**. Yahi "trigger" hai:

- **Vague description** → Skill sahi waqt par fire nahi hogi
- **Zyada broad description** → Galat waqt par fire hogi
- **Perfect description** → Sahi request par automatically activate hogi

**Misal:**
- **Weak:** `description: Writing help`
- **Strong:** `description: Jab bhi social media caption likhna ho brand voice ke saath — no exclamations, question-hook opening`

---

**Q6. Apni pehli Skill kaise banate hain?**

**A:** `skill-creator` (Anthropic ka built-in skill) use karke yeh process follow karo:

1. **Plain English mein describe karo** — "Main chahta hoon ke AI har client summary aise format kare..."
2. **AI `SKILL.md` file generate karta hai**
3. **Real examples se test karo** — kya sahi waqt par fire hoti hai?
4. **Failures par iterate karo** — description ya instructions improve karo
5. **"Save skill" click karo** — personal collection mein add ho jaati hai

**Test kaise karo:**
- Confirm karo skill relevant request par fire hoti hai
- Confirm karo unrelated request par trigger nahi hoti

---

**Q7. Claude.ai ki built-in capabilities kya hain jo bina skill ke kaam karti hain?**

**A:** Claude.ai mein code execution built-in hai jo automatically yeh files handle karta hai:

- Word documents (.docx)
- PowerPoint presentations (.pptx)
- Excel spreadsheets (.xlsx)
- PDFs

Koi slash command nahi chahiye — bas request karo aur AI khud activate kar leta hai.

---

## Skills aur Connectors Ka Sahi Use

**Q8. Kab skill use karein, kab connector, kab dono, aur kab kuch nahi?**

**A:**

| Situation | Kya Use Karein |
|---|---|
| Same instructions baar baar repeat karte ho (formatting, voice, methodology) | **Skill akela** |
| Kisi doosre app se data fetch karna hai, bina transformation ke | **Connector akela** |
| Real data bhi chahiye + apne tarike se format bhi | **Dono saath** |
| Ek baar ka sawaal, sirf acha prompt chahiye | **Kuch nahi** |

---

**Q9. Real-world workflow ki misalein kya hain?**

**A:**

**Accountant ka workflow:**
- **Skill:** "client-summary" — amounts reporting currency mein format karo, expense head se group karo, withholding items flag karo
- **Connector:** Google Drive se ledger fetch karo
- **Result:** Monthly close 2 ghante se 2 minute review mein aa gayi

**Marketer ka workflow:**
- **Skill:** "brand-voice" — koi exclamation marks nahi, question-hook opening
- **Connector:** Notion se content calendar pull karo
- **Result:** Captions brand rules dobara explain kiye bina on-brand draft hoti hain

---

## Safety

**Q10. Skills aur Connectors mein kya khataraat hain aur unse kaise bachein?**

**A:** Do main risks hain:

**Risk 1 — Malicious Skills:**
- Text files mein hidden instructions ho sakti hain (prompt injection, data exfiltration)
- **Bachne ka tarika:**
  - Sirf trusted sources se install karo
  - Enable karne se pehle skill file padho
  - Anjaan sources ki skills mat chalao

**Risk 2 — Over-broad Connector Access:**
- Zyada access dene se AI unintended changes kar sakta hai
- **Bachne ka tarika:**
  - Read-only access se shuru karo
  - Sirf zaroorat ki folders/apps scope mein rakho
  - Write permissions dene se pehle AI ka behavior test karo

---

## Portability

**Q11. Skills alag alag platforms par kaam karti hain?**

**A:** Haan — Skills **Agent Skills open standard** (December 2025 mein published) use karti hain. Ek hi `SKILL.md` file in sab par kaam karti hai:

| Platform | Type |
|---|---|
| **Claude.ai** (web/mobile) | Primary tool |
| **Cowork / OpenWork** | Desktop — non-coders ke liye |
| **Claude Code / OpenCode** | Terminal — developers ke liye |
| **OpenAI Codex CLI** | OpenAI ka terminal tool |
| **Google Gemini CLI** | Google ka terminal tool |

**Note:** ChatGPT ke "Custom GPTs" aur Gemini ke "Gems" vendor-specific alternatives hain — portable nahi hain, sirf usi platform par chalte hain.

---

## Troubleshooting

**Q12. Common masle aur unke hal kya hain?**

**A:**

| Masla | Wajah | Hal |
|---|---|---|
| Skill fire nahi ho rahi | Description zyada vague hai | Description zyada specific karo |
| Galat waqt par trigger ho rahi | Description zyada broad hai | Description narrow karo |
| Files nahi mil rahi | Connector enabled nahi ya permission issue | Connector check karo, permission verify karo |
| AI data ignore kar raha hai | Connector ka naam explicitly nahi diya | Prompt mein clearly likho "Drive connector se data lo" |

---

## Practical Projects

**Q13. Skill aur Connector seekhne ke liye 4 projects kaunse hain?**

**A:**

1. **Pehli Skill banana** (30-45 min) — koi ek repeating task lo, skill banao, test karo
2. **Read-only Connector connect karna** (20-30 min) — ek app connect karo, real data extract karo
3. **Skill + Connector wire karna** (45-60 min) — dono ko ek complete workflow mein join karo
4. **Skill share karna ya doosre platform par chalana** (30 min) — portability test karo

---

## Summary Table

| Concept | Core Rule |
|---|---|
| Skill | `SKILL.md` — ek baar likho, hamesha apply hota hai |
| Connector | Apps tak safe access — permissions inherit hoti hain |
| Description field | Trigger decide karta hai — jitna specific utna behtar |
| Scope | Chhota scope = safer |
| Safety | Trusted sources, read-only se shuru, pehle test karo |
| Portability | Agent Skills standard — sab platforms par chalti hain |
| Skill + Connector | Real data + aapka tarika = powerful workflow |

---

## Ek Line Mein

> **"Tasks ek baar describe karo, real tools connect karo, output verify karo — phir confidence se delegate karo."**
