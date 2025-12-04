---
layout: essay
type: essay
title: "Understanding Design Patterns in Our Final Project"
date: 2025-12-03
published: true
labels:
  - Design Patterns
  - Software Engineering
  - Next.js
---

## Introduction
When our group started building the Run-and-Route-Hub app, I wasn’t thinking about design patterns at all. I just wanted the website to work and for all the features to come together. But after finishing the project, I realized that we were actually using several common design patterns without even knowing it. These patterns showed up naturally because of the tools we used, like Next.js, React, and Prisma. Understanding them now helps me see why our project was structured the way it was, and how these patterns made the code more organized and easier to work with.

---

## MVC in Our Project
One pattern we followed without realizing it was **Model–View–Controller (MVC)**. It’s a simple idea: the data is the model, the logic that handles requests is the controller, and the user interface is the view. In our app, Prisma models acted as the **Model**, Next.js API routes worked as the **Controller**, and our React pages formed the **View**. Even though we never planned to use MVC, this pattern appeared naturally because that’s how Next.js applications are structured. Looking back, MVC made the project easier to manage by keeping the data, logic, and UI separated.

---

## Singleton with Prisma
Another pattern we used was the **Singleton Pattern**, which means only having one instance of something in the entire application. In our case, this was the Prisma client. Instead of creating multiple database connections, we used one shared client for everything. At the time, it just felt like the normal Prisma setup, but it prevented issues like connection overload and made the system more stable. Understanding that this was a design pattern helps me see why it’s the recommended approach.

---

## React Components as Factories
We also used the **Factory Pattern** through React components. Components are basically templates that create UI elements whenever we need them. For example, `<RunCard />` and `<FilterSection />` let us produce consistent pieces of UI without rewriting code. This pattern helped us keep the project clean and reusable. Whenever we needed a similar layout, we just reused the component instead of building everything from scratch.

---

## Strategy Through Filtering
The filtering feature in our app is a good example of the **Strategy Pattern**. Users can filter runs by difficulty, distance, or pace. Each filter is like a different strategy for deciding which runs to show. The backend just uses whichever strategy the user selects. This flexibility made the filtering system easier to adjust and expand. Even though we didn’t plan it this way, the Strategy Pattern fit naturally into how we built the filtering logic.

---

## Observer in React
Finally, React’s state system uses the **Observer Pattern**. Whenever the user changes something, like selecting a filter option, the UI updates automatically. This happens because components “observe” state changes and re-render when something changes. We used this constantly throughout the project. It made the app feel more responsive without us having to manually refresh anything.

---

## Reflection
Even though our team didn’t think about design patterns while building the Run-and-Route-Hub app, they were there the whole time. MVC organized our structure, the Singleton Pattern managed our database connection, the Factory Pattern helped us reuse UI components, the Strategy Pattern shaped our filtering system, and the Observer Pattern kept the interface reactive. Learning these patterns now helps me better understand how our project worked behind the scenes and gives me tools I can use in future assignments and real-world software development.

---

Used ChatGPT for formatting, and grammar
