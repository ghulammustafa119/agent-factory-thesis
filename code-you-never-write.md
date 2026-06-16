# Code Jo Aap Kabhi Nahi Likhte — Questions & Answers

> Source: [Code Jo Aap Kabhi Nahi Likhte: Crash Course](https://agentfactory.panaversity.org/roman/docs/code-you-never-write-crash-course)

---

## Bunyadi Idea

**Q1. Is course ka core shift kya hai?**

**A:** Purana sawaal tha: "Kya main yeh build kar sakta hoon?" — nayi soch hai: **"Kya main yeh describe kar sakta hoon?"**

AI ab code likhta bhi hai aur chalata bhi hai — aapko:
- Koi installation nahi karni
- Koi syntax nahi seekhni
- Koi code nahi copy-paste karna

Sirf apna masla clearly describe karo — AI code likhega, chalayega, aur result dega. Non-programmers bhi real data problems hal kar sakte hain.

---

**Q2. AI code kaise run karta hai — Python aur JavaScript mein fark kya hai?**

**A:** AI do languages mein code run karta hai:

| Language | Kab Use Hoti Hai |
|---|---|
| **Python** | Data analysis, files process karna, spreadsheets, calculations |
| **JavaScript** | Interactive tools, browser-based apps, visual interfaces |

Aapko in languages ka kuch pata hona zaroori nahi — yeh decide AI karta hai. Aap sirf result describe karo.

---

## Hissa 1: Nayi Haqeeqat Samajhna

**Q3. "VPRF Test" kya hai — kaise pata chalega ke problem coding problem hai?**

**A:** VPRF test se pata chalta hai ke koi problem "code problem" hai ya "answer problem":

| Signal | Matlab | Misal |
|---|---|---|
| **V — Volume** | Data itna zyada hai ke haath se nahi hoga | 5,000 rows ki spreadsheet |
| **P — Precision** | Exact calculation chahiye, andaza nahi | Tax calculation, interest |
| **R — Repetition** | Same kaam baar baar karna hai | Har month same report |
| **F — Files** | Multiple files process karni hain | 10 Excel files merge karna |

Agar in mein se koi bhi ek signal hai — **code problem hai.** Sirf reasoning chahiye toh answer problem hai, code ki zaroorat nahi.

---

**Q4. AI se code "force" karke run karwane ka tarika kya hai?**

**A:** AI kabhi kabhi code chalane ki jagah sirf andaza deta hai — isse rokne ke liye yeh **"Three-Sentence Incantation"** use karo:

> **"Write and run code to answer this. Show me the code you ran. Before analyzing, tell me exact row count, column names, date range."**

Roman Urdu mein:
> "Is sawaal ka jawab dene ke liye code likho aur chalao. Jo code chalaya woh dikhao. Analysis se pehle mujhe exact row count, column names, aur date range batao."

Yeh teen cheezein force karti hain:
1. AI code likhe (guess nahi kare)
2. Code visible kare (transparency)
3. Basic facts pehle confirm kare (verification)

---

## Hissa 2: Code Commission Karna

**Q5. "Five-Part Brief" kya hai — code commission karne ka sahi tarika?**

**A:** Coding knowledge ki jagah yeh 5 sections use karo:

| Section | Sawaal | Misal |
|---|---|---|
| **Goal** | Kya masla hal karna hai? | "Dono spreadsheets mein mismatch dhundne hain" |
| **Input** | Kaunsa data de raha hoon? | "Attached CSV — student names aur fees" |
| **Output** | Exactly kya chahiye wapas? | "Ek table: unmatched rows, reason ke saath" |
| **Rules** | Kya constraints obvious nahi honge? | "Name matching case-insensitive ho" |
| **Edge Cases** | Ganda data kaise handle ho? | "Blank rows ignore karo, duplicates flag karo" |

Yeh 5 sections ek bhi programming language jaane bina AI ko poori baat samjha dete hain.

---

**Q6. AI ka output verify kaise karein — code padhe bina?**

**A:** "Verification Ladder" — 5 steps mein verify karo:

1. **Known-Answer Test:** Data ka ek chhota hissa lo jiska jawab aapko pehle se pata hai — wahi answer aana chahiye
2. **Reality Questions:** Row counts aur totals sense karte hain? "5 million sales ek din mein?" — yeh galat lagta hai
3. **Plain-English Replay:** AI se poocho: "Apne code ne exactly kya kiya — simple Urdu mein batao"
4. **Adversarial Pass:** Khud khojna — "Is result mein kya galat ho sakta hai?"
5. **Cross-Model Check:** Same brief doosre AI (ChatGPT, Gemini) par chalao aur results compare karo

**Key principle:** Code ka logic padhna zaroori nahi — results ko independently verify karo.

---

**Q7. Error aane par kya karna chahiye?**

**A:** Error text analyze karne ki koshish mat karo — yeh karo:

**Galat tarika:** Error message khud samajhne ki koshish karna

**Sahi tarika — Symptoms report karo:**
> "Yeh kaam nahi kiya — yeh error aaya: [error paste karo]. Main chahta tha ke [apna goal likho]. Data aisa tha: [data describe karo]."

AI error text se khud samajh jaata hai — aapka kaam sirf:
1. Error message copy-paste karna
2. Apna original goal dobara explain karna
3. Data ki condition describe karna

---

**Q8. Scripts (code) long-term kaise save karein?**

**A:** Ek baar kaam karne wala code ek reusable asset hai — aise save karo:

- **Script save karo** — file mein rakh do
- **Brief bhi saath rakh do** — woh 5-part description jo tune di thi
- **Sample data bhi** — chhota example dataset jo test ke liye use hua
- **Documentation** — ek line likho: "Yeh kya karta hai aur kab use karna hai"

**Agla baar:** Single sentence se trigger hoga — "Pichli baar wali fees reconciliation script chalao is month ke data par."

---

## Hissa 3: Paanch Surfaces (Kahan Code Chalta Hai)

**Q9. Code run karne ke 5 "surfaces" kaunse hain?**

**A:**

**1. Claude.ai / ChatGPT / Gemini (Browser)**
- Browser sandbox — zero risk
- Files upload karo, code chalao, result lo
- Koi persistence nahi (session khatam = script gone)
- **Best for:** One-off jobs, pehli baar try karna

**2. Claude Code / OpenCode (Terminal)**
- Aapke computer ke folders direct access
- Scripts disk par save rehti hain (persistent)
- Errors khud theek kar leta hai
- **Best for:** Repeating tasks, permanent scripts

**3. Cowork / OpenWork (Desktop App)**
- Visual interface — files touch karne se pehle plan dikhata hai
- Approval step — aap OK karo tabhi action hota hai
- **Best for:** Non-technical users, cautious log

---

## Hissa 4: Safety Aur Limits

**Q10. Jab code real files touch kare toh kya احتیاط karni chahiye?**

**A:** Real files ke saath yeh 4 rules hamesha follow karo:

1. **Backup par kaam karo:** Original file kabhi directly mat do — pehle copy banao
2. **Dry run maango:** "Pehle batao kya karega — actually karo mat" — phir approve karo
3. **Chhota scope:** Poori hard drive nahi — sirf specific folder do
4. **New files mein output:** "Results original file mein mat likhna — nayi file banao"

**Wajah:** Galti hone par original data safe rehta hai.

---

**Q11. AI-generated code ki kya limits hain — kab engineer chahiye?**

**A:** Yeh 4 situations mein AI code kafi nahi — real engineer chahiye:

| Situation | Kyun AI Kafi Nahi |
|---|---|
| **Multi-user software** | Multiple logon ke liye apps banana complex hai |
| **Unattended automation** | Bina supervision ke chalne wale systems risky hain |
| **Irreversible actions** | Galti ho toh undo nahi ho sakta |
| **Judgment calls** | Jahan domain expertise aur decisions zaroori hain |

Yeh course ek insaan ke kaam ke liye hai — production systems aur scalable software ke liye proper engineering team chahiye.

---

## Practical Workflow

**Q12. Ek poori "code problem" solve karne ka workflow kya hai?**

**A:** 7 steps mein:

1. **Recognize:** VPRF test — Volume, Precision, Repetition, ya Files? Haan toh code problem hai
2. **Describe:** Five-part brief likho — Goal, Input, Output, Rules, Edge Cases
3. **Commission:** Three-sentence incantation se force karo computation
4. **Verify:** Verification ladder — known answers, reality check, plain English replay
5. **Iterate:** Issues mile toh symptoms report karo, conversation mein fix karwao
6. **Save:** Script + brief + sample data save karo
7. **Reuse:** Agla period — single sentence se trigger karo

---

## Real-World Misalein

**Q13. Yeh practically kise help karta hai?**

**A:** Real log, real masle:

| Insan | Purana Tarika | Nayi Tarika |
|---|---|---|
| **Clinic Manager** | Raat bhar do spreadsheets mein discrepancies dhundta | 5 minute mein AI code se mismatch report |
| **School Admin** | 200 student submissions haath se roster se match karta | Ek brief — AI instant results deta hai |
| **Marketer** | 4 platform exports haath se manually reformat karta | Code merge karta hai, format set karta hai |

Kaam khatam nahi hota — **sirf 5 minute ka process ban jaata hai** documented code ke saath.

---

**Q14. Shuru kaise karein — pehla qadam kya ho?**

**A:** Seedha simple start karo:

1. **Claude.ai free account** banao — browser mein, koi installation nahi
2. **Apna real data** lo — koi spreadsheet ya CSV jo actually use karte ho
3. **Brief-Commission-Verify loop** practice karo:
   - Five-part brief likho
   - Three-sentence incantation se commission karo
   - Verification ladder se check karo
4. **Claude Code par jao** jab file upload karna annoying lage

Skills ek baar seekhi toh sab surfaces par same kaam karti hain.

---

## Summary Table

| Concept | Core Rule |
|---|---|
| Core Shift | "Describe kar sakta hoon?" — "Build kar sakta hoon?" nahi |
| VPRF Test | Volume, Precision, Repetition, Files = Code Problem |
| Incantation | "Write and run code. Show code. Row count first." |
| Five-Part Brief | Goal, Input, Output, Rules, Edge Cases |
| Verification | Known answers, reality check, plain English, adversarial, cross-model |
| Errors | Symptoms report karo, code analyze mat karo |
| Safety | Backup, dry run, small scope, new output files |
| Limits | Multi-user, unattended, irreversible, judgment = engineer chahiye |
| Start | Claude.ai free → brief → commission → verify |
