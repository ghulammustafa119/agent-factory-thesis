# AI Ke Daur Mein Sochna — Questions & Answers

> Source: [AI ke Daur Mein Sochna: Working Day Crash Course](https://agentfactory.panaversity.org/roman/docs/how-to-think-ai-era)

---

## Bunyadi Idea

**Q1. Is course ka core principle kya hai?**

**A:** Core principle yeh hai: **"Deliverable thinking ka documented evidence hai."**

Iska matlab yeh hai ke deliverable (kaam ka output) sirf polished jawab nahi hota — balke yeh aapki soch ka documented saboot hota hai. AI ke zamanay mein asli value yeh nahi ke aap ne kya likha, balke yeh hai ke aap ne kaise socha, kya decide kiya, aur kyun. Jo log sirf AI ka jawab copy karte hain woh apni soch ka koi trail nahi chorte — aur isi wajah se woh long-term mein peeche reh jaate hain.

---

## Hissa 1: Bunyad (Posture)

**Q2. "Prediction Lock" discipline kya hai aur yeh kyun zaroori hai?**

**A:** Prediction Lock ek technique hai jisme aap koi bhi AI tool kholne se PEHLE char lines likh kar apni position commit karte ho:

1. **Actual decision:** Jo decision leni hai woh seedha likho
2. **Ek specific fact:** Woh ek fact jo is decision ko settle kar sakta hai
3. **Aapka decision + wajah:** Apna jawab aur reasoning likho
4. **Confidence level:** Kitna sure ho aur kya cheez aapko flip kar sakti hai

**Kyun zaroori hai:** Jab AI pehle confident jawab de deta hai, toh woh "anchor" ban jaata hai aur aap subconsciously usi ke hisaab se sochne lagte ho — yeh "anchoring bias" hai. Prediction lock se aap pehle apna judgment anchor karte ho, AI ka nahi. Is tarah AI ka jawab aapki soch nahi ban paata.

---

**Q3. "Reasoning Receipt" kya hai aur isse kaise use karte hain?**

**A:** Reasoning Receipt ek tracking system hai jisme aap AI ke har suggestion ko teen columns mein record karte ho:

| Column 1 | Column 2 | Column 3 |
|---|---|---|
| AI ne kya suggest kiya | Aapka action | Kyun |
| (AI ka suggestion) | ACCEPT / REJECT / MODIFY / SURFACED / MISSED | (Aapki wajah) |

**Kaise kaam karta hai:**
- **ACCEPT:** AI sahi tha, mana liya
- **REJECT:** AI galat tha, nahi mana
- **MODIFY:** AI ka idea thoda badal kar use kiya
- **SURFACED:** AI ne ek angle dikhaya jo khud nahi socha tha
- **MISSED:** AI ne koi zaroori cheez miss kar di

**Faida:** Yeh passive consumption ko active evaluation mein badal deta hai. Aapke decisions ka audit trail banta hai — baad mein explain kar sakte ho ke kyun kya kiya.

---

## Hissa 2: Errors Dhundna (Detection)

**Q4. AI output mein kaunse 6 qisam ke errors ho sakte hain?**

**A:** Error Taxonomy mein 6 specific error types hain jo scan karne chahiye:

1. **Factual Errors:** Galat numbers, dates, names — jo facts AI ne cite kiye woh actually galat hain
2. **Logical Gaps:** Conclusion hai lekin evidence nahi — "isliye" ke baad ka logic kamzor hai
3. **False Confidence:** Jab AI kisi cheez ko "fact" ki tarah state kare bina qualification ke, jab actually yeh uncertain ho
4. **Missing Context:** Zaroori details jo AI ne chhod di — incomplete picture
5. **Fabricated Sources:** Citations jo exist hi nahi karti — AI ne reference invent kar liya
6. **Stale Facts:** Purani information jo ab outdated ho chuki hai

**Kyun named scanning behtar hai:** General proofreading ("yeh check karo") se zyada effective hai specific names le kar dhundna, kyunke yeh deliberate checking force karta hai.

---

**Q5. "Thinking in Systems" kya hai aur "cascade map" kaise banate hain?**

**A:** Thinking in Systems ka matlab hai ke kisi bhi decision ke sirf direct effects nahi, balke 3 layers deep consequences track karo.

**Cascade Map banana ka tarika:**
1. Apna decision likho
2. Poocho: "Aur phir kya hoga?" — Layer 1
3. Us jawab par phir poocho: "Aur phir kya hoga?" — Layer 2
4. Phir se poocho: "Aur phir kya hoga?" — Layer 3
5. **Feedback loops dhundho:** Kya Layer 3 ka effect wapas original decision ko undermine karta hai?

**Example:** Agar cost kam karo → customers khush hon → demand badhe → production cost badhe → wapas price badhana pade. Yeh feedback loop hai jo original faida ulta kar deta hai.

**Kyun zaroori hai:** Direct effects aksar feedback loops chhupa dete hain jo baad mein aapke original decision ko reverse kar dete hain.

---

## Hissa 3: Original Soch (Origination)

**Q6. "First Principles" thinking kya hoti hai aur AI se yeh kyu alag hai?**

**A:** First Principles thinking woh kaam hai jo AI nahi kar sakta — yeh aapki original soch hai. Iska matlab:
- Kisi problem ko uske bunyadi elements mein todna
- Assumptions ko challenge karna — "yeh hamesha aise kyun kiya jaata hai?"
- Scratch se naya solution banana, existing patterns copy karne ki jagah
- Woh sawaal poochna jo pehle kisi ne nahi poocha

**AI se fark:** AI training data ke patterns se generate karta hai — woh average of existing thinking hai. First principles thinking naya angle create karta hai jo training data mein exist hi nahi karta tha.

---

**Q7. AI ke saath "sahi tarike se" kaam karna kya hota hai?**

**A:** AI ke saath sahi kaam karne ka matlab sirf use karna nahi — balke apni soch ko preserve karte hue use karna hai:

**Galat tarika (Person B):**
- AI ka pehla jawab le lo
- Copy kar do
- Defend nahi kar sakte baad mein

**Sahi tarika (Person A):**
- Pehle khud socho (Prediction Lock)
- AI se consult karo
- Carefully compare karo
- Disagreements document karo (Reasoning Receipt)
- Apna final decision explain kar sako

Same tools, same AI — lekin thinking discipline ka fark vastly different outcomes deta hai.

---

## Research Foundations

**Q8. "Premortem Technique" kya hai aur yeh kaise kaam karta hai?**

**A:** Premortem technique mein aap event hone se PEHLE prediction likhte ho — baad mein nahi. Research kehti hai ke aisa karne se accuracy 30% behtar hoti hai.

**Kaise use karein:**
- Koi project shuru karne se pehle likho: "Yeh project 6 mahine mein fail hoga kyunke..."
- Decision lene se pehle likho: "Yeh decision galat sabit hoga kyunke..."
- Phir actual outcome se compare karo

**Kyun kaam karta hai:** Baad mein likhne par hum subconsciously apni prediction jo hua us se match kara lete hain — yeh "hindsight bias" hai. Pehle likhna isko rokta hai.

---

**Q9. "Forecasting Calibration" kya hai?**

**A:** Forecasting calibration ka matlab hai ke aap apna confidence percentage record karo PEHLE outcome jaanne se — phir track karo ke aap kitne accurate the.

**Process:**
- "Main 70% confident hoon ke yeh kaam karega"
- Outcome note karo
- Track karo: Jab 70% bol rahe the tab kitni baar sahi the?

**Faida:** Waqt ke saath aap apni judgment calibrate kar sakte ho — pata chalta hai ke aap overconfident ho ya underconfident, aur kis tarah ke decisions mein.

---

**Q10. "Anchoring Bias" aur "Processing Fluency" kya hain — AI use karte waqt yeh kaise affect karte hain?**

**A:** Do cognitive biases jo AI use mein khaas tor par khatarnak hain:

**Anchoring Bias:**
- Pehla confident jawab jo dikhta hai woh reference point ban jaata hai
- Baad ki sari soch usi "anchor" ke around hoti hai
- AI ka pehla jawab aksar yeh anchor ban jaata hai
- **Solution:** Prediction Lock — pehle khud anchor karo

**Processing Fluency:**
- Smooth, acha likha hua text automatically zyada trustworthy lagta hai
- AI bohut fluently likhta hai — isliye galat baat bhi sahi lagti hai
- Yeh feeling accuracy ka proof nahi hai
- **Solution:** Error Taxonomy use karo — fluency se distract mat ho, content check karo

---

## Summary Table

| Discipline | Kya Hai | Kab Use Karein |
|---|---|---|
| Prediction Lock | AI se pehle 4 lines mein apni position commit karo | Har bade decision se pehle |
| Reasoning Receipt | AI suggestions ko 3 columns mein track karo | Jab bhi AI advice le rahe ho |
| Error Taxonomy | 6 specific errors scan karo | Har AI output review karte waqt |
| Thinking in Systems | 3 layers deep "aur phir kya?" poocho | Complex decisions mein |
| First Principles | Scratch se original soch — AI nahi kar sakta | Naye problems par |
| Working WITH AI | Soch preserve karo, sirf tool use karo | Hamesha |

---

## Person A vs Person B

| | Person A (Sahi Tarika) | Person B (Galat Tarika) |
|---|---|---|
| Pehla qadam | Khud predict karta hai | AI ka jawab seedha leta hai |
| Comparison | Carefully compare karta hai | Directly accept karta hai |
| Documentation | Disagreements note karta hai | Kuch record nahi |
| Baad mein | Apna decision explain kar sakta hai | Defend nahi kar sakta |
| Long-term | Judgment behtar hoti hai | AI dependent rehta hai |
