# Following the Path: How Design Patterns Showed Up in Our Project

When we built the Run-and-Route-Hub app, I didn’t think much about design patterns. We were mainly focused on getting the features to work. But after finishing the project, I realized that we actually used a lot of common design patterns without even trying. It felt similar to walking on a hiking trail—you don’t notice the structure while you’re on it, but once you stop and look back, you see how everything fits together.

## MVC: The Basic Structure We Used Without Thinking

A hiking trail has the ground, the signs, and the views.  
MVC works the same way:

- **Model** = the data
- **Controller** = how requests are handled
- **View** = what the user sees

In our project:  
- Prisma models were our **Model**  
- Next.js API routes acted as the **Controller**  
- React pages were the **View**

We never said “let’s implement MVC,” but this structure naturally appeared because of how Next.js and Prisma are designed.

## Singleton Pattern: One Prisma Client for the Whole App

On a short hike, you don’t install multiple water stations—you rely on one.  
That’s basically the **Singleton Pattern**.

In our project, we used one shared Prisma client for all database operations. This prevents errors and keeps everything running smoothly. We followed this pattern simply by using Prisma’s recommended setup.

## Factory Pattern: React Components as Reusable Builders

React components work like small factories.  
You give them props, and they return UI pieces.

Examples in our app:

- `<RunCard />`
- `<FilterSection />`

These components use the **Factory Pattern** because they create reusable parts of the interface. This helped us keep our code clean and avoid repeating the same layout many times.

## Strategy Pattern: How Our Filtering System Works

On a hike, you can choose a steep path, a long path, or an easy path.  
Those are different “strategies.”

In our project, users can filter runs by:

- difficulty
- distance
- pace

Each one is a different strategy for filtering runs. Our system just uses whichever strategy the user selects. This made it easy to change or add new filters later.

## Observer Pattern: React Updating Automatically

When the weather changes, you notice right away.  
React works the same way with state.

Any time a user updates a filter or interacts with the page, React automatically re-renders the UI. This is the **Observer Pattern**, because components “observe” changes and react to them instantly. We used this constantly without realizing it.

## Final Thoughts

Building Run-and-Route-Hub helped me understand that design patterns are not complicated ideas you have to force into your project. They naturally appear when you use frameworks like Next.js, React, and Prisma. MVC organized our structure, Singleton handled our database connection, React components worked like factories, our filtering used the Strategy pattern, and React state updates followed the Observer pattern.

These patterns made our project cleaner, easier to maintain, and easier to understand—even before we knew what they were called.

---

ChatGPT uses for grammar and formatting

