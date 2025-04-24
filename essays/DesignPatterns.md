---
layout: essay  
type: essay  
title: "CI/CD: Design Patterns Behind the Scenes"  
date: 2025-04-24  
published: true  
labels:  
  - Personal Experience  
  - DevOps  
---

<img width="300px" class="rounded float-start pe-4" src="../img/single.jpg">  

## **Introduction**  

In our ICS 314 project *Club Organizers*, I didn’t touch much of the frontend. My main role was setting up backend infrastructure—mostly working with Vercel, Supabase, environment variables, and GitHub Actions.  

And honestly? I thought I was just “connecting stuff.” But as the project progressed, I noticed a pattern. Literally. Design patterns. The same kind we learn in theory, quietly showing up in practice—especially in CI/CD and deployment flow.

---

## **Singleton: .env Doesn’t Lie**  

One key lesson early on: **never repeat your secrets**. API keys and URLs were defined once in `.env.local`, then used everywhere. Vercel lets you define environment variables for each deployment stage (dev, preview, prod), but they all behave like a **Singleton**—only one version per environment, shared across the entire app.

Without this, we’d risk overwriting keys or leaking sensitive info. So yeah, not glamorous code—but design pattern? Absolutely.

---

## **Facade: GitHub Actions Is Just Built Different**  

GitHub Actions runs our CI/CD flow. One push to `main`, and like magic:  

- Playwright runs  
- ESLint checks  
- Build happens  
- Site is deployed  

What looks simple is hiding layers of complexity. This is **Facade pattern** in action. It gives us one clean entry point (`.yml` file), while quietly calling on all the tools behind the scenes.

---

## **Adapter: When Supabase Meets Next.js**  

Supabase is powerful—but it’s not tailored for Next.js out of the box. I had to wrap certain client features to work in server components, or inject environment variables properly for App Router use. That’s where **Adapter** comes in: bridging two systems that weren’t made for each other, so they work like they were.

---

## **Conclusion**  

I used to think design patterns only lived in frontend components or OOP-heavy Java apps. But now I realize—they’re everywhere. The tools I set up for our team worked smoothly not just because I wired them up, but because I unknowingly followed proven patterns. Singleton, Facade, Adapter—those weren't just buzzwords from class. They were how I built things to last.

---

## **AI Acknowledgment**  

I used ChatGPT to assist with formatting this essay and improving sentence clarity. All examples and content are based on my own development experience with the Club Organizers project in ICS 314. AI helped ensure my ideas were clearly structured and easy to follow.
