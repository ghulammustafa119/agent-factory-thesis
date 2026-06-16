# Markdown Andar, HTML Bahar — Questions & Answers

> Source: [Markdown Andar, HTML Bahar: Crash Course](https://agentfactory.panaversity.org/roman/docs/markdown-html-crash-course)

---

## Bunyadi Idea

**Q1. Is course ka core principle kya hai?**

**A:** Core principle yeh hai: **"AI ko Markdown mein likho, AI se output HTML mein lo."**

Yeh ek asymmetry (fark) hai:
- **Input (Insan → AI):** Markdown — kyunke structure machine ke liye ambiguity hatata hai
- **Output (AI → Insan):** HTML — kyunke rich formatting se insaan lambi cheezein padh leta hai
- **Agent-to-Agent:** Markdown — jab AI systems ek doosre ko specs aur context pass karte hain

**Ek sawaal jo sab decide karta hai:** "Yeh output aakhir mein kaun padhega?"
- Insan browser mein → **HTML**
- AI future session mein → **Markdown**
- Pata nahi → **Markdown** (safer default)

---

## Hissa 1: Do Zabanein

**Q2. Unstructured request aur structured request mein kya fark hota hai?**

**A:** Unstructured request mein AI ko priorities aur constraints khud andaza lagani parti hain — aur yeh andaza aksar galat hota hai. Structured request mein headings aur bullets constraints explicit aur visible banate hain.

**Misal:**

**Unstructured (Bura):**
> "Mujhe ek marketing plan chahiye 50,000 rupees mein next month ke liye."

**Structured (Acha):**
```
# Marketing Plan

## Goal
Next month social media par brand awareness badhana

## Hard Constraints
- Budget: PKR 50,000 — hard ceiling
- Timeline: 30 din
- Platform: Sirf Instagram aur Facebook

## Expected Output
Week-by-week breakdown table
```

Structured request dramatically behtar output deta hai.

---

## Hissa 2: Markdown Likhne Ka Tarika

**Q3. Markdown ke 5 core elements kya hain?**

**A:**

**1. Headings (`#`, `##`, `###`)**
- Information hierarchy dikhate hain
- Ek document mein ek hi title (`#`) hona chahiye
- Levels skip mat karo (# ke baad seedha ### mat likho)
- Heading ko claim banao, sirf label nahi:
  - **Weak:** `## Budget`
  - **Strong:** `## Budget: PKR 50,000 hard ceiling`

**2. Lists — Do Qismein**
- **Bullets (`-`):** Un cheezoon ke liye jahan order matter nahi karta
- **Numbers (`1.`):** Sequential steps ke liye jahan order zaroori hai
- AI dono ko alag treat karta hai — sahi choose karo

**3. Code Blocks (triple backticks + language)**
- Data, examples, error messages, quotes wrap karo
- AI ko signal karta hai: "analyze karo, execute mat karo"
- Sabse useful use: expected output format dikhana

**4. Links aur Images**
- Links se AI actual web page padh sakta hai, sirf summary nahi
- Image description brackets mein (`![description]`) — yahi AI padha hai

**5. Specification Skeleton**
```
# [Project Title] Specification

## Goal
(Ek paragraph — maqsad aur audience)

## Context
(Links, files, background facts)

## Requirements
(Checkable bullets — objectively verify ho sakein)

## Hard Constraints
(Jo kabhi violate nahi ho sakti: budget, timeline, platform)

## Out of Scope
(Yeh explicitly NAHI chahiye)

## Expected Output
(Example ya format description code block mein)
```

---

**Q4. "Spec ko 10 mein se grade karo" ka kya matlab hai?**

**A:** Har specification likhne ke baad khud evaluate karo teen criteria par:

| Criteria | Sawaal |
|---|---|
| **Clarity** | Kya AI bina pooche samajh sakta hai? |
| **Completeness** | Kya koi zaroori cheez miss hai? |
| **Checkability** | Kya output objectively verify ho sakta hai? |

**Rule:** Jab tak 9/10 score na mile, spec improve karte raho — phir AI ko dو.

Yeh "preliminary paperwork" nahi — **yeh asli kaam hai.** Acha spec = acha output.

---

## Hissa 3: HTML Output Strategy

**Q5. Kab HTML output maangni chahiye?**

**A:** HTML tab zaroori hai jab:

- **Output lamba ho** — plain text ki "diwar" insaan nahi padhta
- **Output visual ho** — tables, diagrams, color-coding, layout chahiye
- **Output share karna ho** — link messages mein, social media preview cards
- **Interactivity chahiye** — sliders, toggles, drag-and-drop

---

**Q6. HTML maangne ka sahi tarika kya hai? AI ko kya kya batana hota hai?**

**A:** Aap ne HTML likhna nahi — sirf AI ko 4 cheezein batani hain:

1. **Kaun padhega** — team lead, parents, client
2. **Kya shamil ho** — specific named components: diagram, table, summary strip
3. **Interactivity** — sirf padhna hai ya controls bhi chahiye (sliders, toggles)
4. **Reading pattern** — ek baar padhna hai, ya reference document, ya presentation

**Weak prompt:**
> "Mere sales data ka HTML report banao"

**Strong prompt:**
> "Attached CSV padho. Ek page mere co-founders ke liye jo ek baar laptop par padhenge: headline strip (3 key numbers, bade font mein), product-wise revenue chart, fastest-growing products table, aur next-steps section."

---

**Q7. HTML ke 5 practical patterns kaunse hain?**

**A:**

1. **Decision Grids:** Multiple approaches side-by-side comparison ke liye — jab options mein se choose karna ho
2. **Explainers:** Diagram + fact table + gotchas section — kisi concept ko clearly explain karne ke liye
3. **Code Reviews:** Annotated code with explanations aur flowcharts — code samajhne ke liye
4. **Design Prototypes:** Live sliders, color swatches, toggles — visual choices ke liye
5. **Throwaway Tools:** Drag-and-drop cards prioritization ke liye, phir text mein export

---

**Q8. Social media par HTML kaise kaam karta hai?**

**A:** Social media feeds (WhatsApp, LinkedIn, Facebook) formatting strip kar deti hain. Solution:

- **Post body:** Plain text likhو — koi formatting nahi chalti
- **Link preview cards:** HTML mein Open Graph meta tags shamil karo — designed preview milti hai
- **Images:** HTML mein design karo, phir PNG save karke attach karo

---

**Q9. HTML publish karne ke options kya hain — asaan se mushkil tak?**

**A:**

| Option | Kaise | Best For |
|---|---|---|
| **Claude.ai publish button** | Ek click, instant link | Quick sharing, no setup |
| **GitHub Gist** | Apni file, editable, version history | Permanent ownership |
| **GitHub Pages** | Free permanent web address | Lasting hosting |
| **Netlify** | Drag-and-drop, simple setup | Professional hosting |

---

**Q10. Output format kaise choose karein — PDF, Word, Excel, ya kuch aur?**

**A:** Jo kaam recipient karega, usi ke hisaab se format choose karo:

| Kaam | Format |
|---|---|
| Sign / print / file karna | **PDF** |
| Edit / comment karna | **Word (.docx)** |
| Present karna | **Slides (.pptx)** |
| Numbers pe kaam karna | **Excel (.xlsx)** |
| Tools ko feed karna | **CSV** |

**Pattern:** Content ek baar clean format mein likho (text ke liye Markdown, numbers ke liye plain data), phir recipient ki zaroorat ke hisaab se export karo.

---

## Hissa 4: Teen Tarike, Ek Skill

**Q11. AI ke saath kaam karne ke 3 "motions" kya hain?**

**A:**

**Motion 1 — Chat (Claude.ai, ChatGPT, Gemini)**
- Notes browser mein paste karo
- AI side panel mein artifact generate karta hai
- Instant preview, instant sharing
- **Best for:** Single specs, 1 minute se kam setup

**Motion 2 — Terminal (Claude Code, OpenCode)**
- AI folder ki sab files automatically padh leta hai
- Real files disk par create karta hai
- **Best for:** Jab notes kai files mein bikri hui hon

**Motion 3 — Desktop (Cowork, OpenWork)**
- Visual app jo files touch karne se pehle approval maangti hai
- Terminal jaisi workflow lekin UI ke saath
- **Best for:** Non-technical users, safety concerned log

Teeno mein same prompts use hote hain — sirf content deliver karne ka tarika badalta hai.

---

## Key Vocabulary

**Q12. Is course ke important terms kya hain?**

**A:**

| Term | Matlab |
|---|---|
| **Intent Layer** | Precisely likhi hui insaani niyyat jis par AI act kar sake |
| **Specification** | Asli kaam — preliminary paperwork nahi |
| **Artifact** | Woh live document jo AI browser side panel mein create karta hai |
| **Grade out of 10** | Har output evaluate karna: clarity, completeness, checkability |
| **Spec-driven development** | Pehle spec 9/10 tak behtar karo, phir build karo |

---

## Summary Table

| Concept | Core Rule |
|---|---|
| Input format | AI ko Markdown mein likho |
| Output format | Insaan ke liye HTML lo |
| Agent-to-agent | Markdown pass karo |
| Headings | Claim banao, label nahi |
| Lists | Bullets = set, Numbers = sequence |
| Code blocks | Data quote karo, execute nahi |
| Spec grading | 9/10 tak improve karo pehle |
| HTML maangna | 4 cheezein batao: reader, content, interactivity, pattern |
| Social media | Body plain text, preview Open Graph |
| Format choice | Recipient kya karega us se decide karo |

---

## Ek Line Mein

> **"Machines ke liye structured Markdown likhو; insanon ke liye rich, readable HTML maango."**
