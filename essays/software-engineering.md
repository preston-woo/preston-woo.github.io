---
layout: essay
type: essay
title: "Seeing Design Patterns in Action in Our Project"
date: 2025-12-03
published: true
labels:
  - Software Engineering
  - Design Patterns
  - ICS 314
---

## Introduction
When our group started building the Run-and-Route Hub app, I wasn’t thinking about design patterns at all. I just wanted the website to work and for all the features to come together. But after finishing the project, I realized that we were actually using several common design patterns without even noticing. These patterns showed up naturally because of the tools we used, like Next.js, React, and Prisma. Understanding them now helps me see why our project was structured the way it was and how these patterns made the code more organized and easier to work with.

## MVC in Our Project
One pattern we followed without realizing it was Model–View–Controller (MVC). The data is the model, the logic that handles requests is the controller, and the user interface is the view.

In our app:
- **Model:** Prisma schemas  
- **Controller:** Next.js API routes  
- **View:** React pages  

We didn’t plan to use MVC, but this structure appeared naturally, and it helped keep the data, logic, and UI separated.

## Singleton with Prisma
We also used the Singleton Pattern through the Prisma client. Instead of creating multiple database connections, we used one shared instance across the whole application. At the time, it just felt like the normal Prisma setup, but it prevented connection issues and made our app more stable. Learning that this is a design pattern made me understand why it's recommended.

## React Components as Factories
React components also represent the Factory Pattern. Components act like templates that generate UI elements whenever needed. For example, `<RunCard />` and `<FilterSection />` allowed us to create consistent pieces of UI without rewriting the same structure. This made our code more reusable and easier to maintain.

## Strategy Through Filtering
The filtering feature in our app is an example of the Strategy Pattern. Users can filter runs by difficulty, distance, or pace. Each filter represents a different “strategy” for deciding what to show. The backend simply uses whichever strategy the user selects. This pattern made the filtering logic flexible and easy to update.

## Observer in React
React’s state system uses the Observer Pattern. When the user changes something—like selecting a filter option—the UI updates automatically. Components “observe” changes in state and re-render when needed. We used this constantly, and it helped make the app feel responsive without manual updates.

## Reflection
Even though our team didn’t think about design patterns while building Run-and-Route Hub, they were there the whole time. MVC organized our structure, the Singleton Pattern kept Prisma stable, the Factory Pattern helped us reuse UI components, the Strategy Pattern shaped our filtering system, and the Observer Pattern kept the interface reactive. Understanding these patterns now helps me see how our project worked behind the scenes and gives me tools I can use in future software development.

