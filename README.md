# Sen-a · Space Detective Agency

**Is that "historic" heatwave or flood a real trend, or just a bad year?**
Sen-a is a web app where anyone can learn to answer that question with real NASA data.

Guided by **Sen**, a young sentinel who watches over Earth from a space station, you complete short missions: explore a climate signal, read its trend, and decide whether it is a **★ confirmed case** or just a **☆ clue**. Every finding becomes a star in your own constellation, and you learn to review other people's research, catching mistakes like confusing correlation with causation.

🔗 **Live demo:** [sen-a.vercel.app](https://sen-a.vercel.app)
🚀 Built for the **NASA Space Apps Challenge 2026**, challenge *Be an Earth System Trend Detective*.

> The demo starts with the guided tutorial (Mission 00 · Valencia). Finish it to unlock the rest of the app.

## The data

All the numbers come from NASA, downloaded through [Giovanni (NASA GES DISC)](https://giovanni.gsfc.nasa.gov/) for **2001–2024**, around Valencia (Spain) and the Poyo river basin, where the 2024 DANA flood hit hardest:

| Signal | Dataset |
|---|---|
| Rainfall (monthly and daily) | GPM IMERG v07 (`GPM_3IMERGM`, `GPM_3IMERGDF`) |
| Sea temperature | MERRA-2 (`M2TMNXOCN`, `TSKINWTR`) |

Trends were calculated with the **Mann-Kendall test** and **Sen's slope**, and relationships between signals with **Spearman correlation**. Inside the app we keep one simple rule: **p < 0.05 → confirmed case**, anything else stays a clue.

## Run it locally

```bash
npm install
npm run dev
```

Then open [http://localhost:3000](http://localhost:3000).

Built with Next.js, React, TypeScript, Tailwind CSS, Framer Motion and Three.js. Progress is saved in your browser; there are no accounts yet.

## What's next

- Live data straight from NASA Earthdata instead of pre-computed results
- Accounts and real peer review between users
- More places, more signals, more missions

---

*You don't need to be a renowned scientist to take part in science.*
