[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MMj2nZMu)
# Rsearch and Reflection Journal
Research and Reflection Journal for DGL 104 course

# Week 8 (Week of February 25)

## Lecture Topic: Functional User Requirements & User Stories

We were introduced to the concept of User Stories, short descriptions written from a user's perspective to inform software features. These user stories are then translated into Functional User Requirements, providing clear technical specifications for app development.

I found this method very practical, especially since I’ll be working on a project aimed at a specific user group. It ensures user needs stay front and center.

## Activities Completed

### Research a New Language: Haskell

What is Haskell used for?
Haskell is a purely functional programming language used in academia, finance, and data-intensive systems. It's known for its robustness and mathematical purity.

Who uses it?
Used mainly by academic institutions, fintech companies, and developers who prefer functional paradigms.

Useful resources:

Learn You a Haskell for Great Good! – beginner-friendly and humorous.

Haskell.org – official documentation.

Reddit’s r/haskell – active discussion community.

Why are they useful?
The tutorial makes it approachable for newcomers, while the official docs offer structured knowledge. Reddit helps stay updated with trends and common problems.

### Reflection on Slack Language Responses

I found it fascinating to learn about languages I hadn't considered before, like Lua (used in game development) and Processing (used for creative visuals). Reading other students’ posts gave me a broader understanding of language ecosystems and their real-world applications.

### Wrote a User Story

App Chosen: Spotify
Feature: Playlist Creation

User Stories:

"As a user, I can create a new playlist from the 'Your Library' tab."

"As a user, I can add songs to a playlist directly from the Now Playing screen."

"As a user, I can rename and delete playlists I’ve created."

Acceptance Criteria:

The 'Create Playlist' button is easily accessible.

User can add songs via 'Add to Playlist' option on all tracks.

Editing options include rename and delete.

### Chose a Programming Language

Experience: 1+ year of experience through personal projects and previous courses.
Why: JavaScript is highly relevant for both web and mobile development. I’m excited to learn more about frameworks like React or Vue as part of this course.

Posted my language selection and reasoning on Slack.

### Explored GitHub Topics and Repositories

I spent time on GitHub’s Explore tab:

Starred topics: frontend, mobile-app, user-interface, react, progressive-web-app

Starred repos: several React Native starter templates, open-source UI libraries, and mobile utility tools.

I was surprised by how active and collaborative the open-source community is. Most starred repos follow clean documentation standards and include beginner-friendly CONTRIBUTING.md files – a trend I found motivating.

### Reflection Question

Interesting learning from programming language research:

Haskell’s focus on immutability and pure functions intrigued me. It challenges conventional thinking and can lead to highly predictable code behavior, although it has a steeper learning curve.

Other languages I might consider:

TypeScript would be my second choice—it adds type safety to JavaScript and is widely adopted in large-scale applications.

GitHub exploration insights:

I noticed strong consistency in structure and documentation across popular repositories. Also, most trending projects had an active issue tracker and contributor section, which will help when I start contributing.

### References

Learn You a Haskell for Great Good. (n.d.). Retrieved from http://learnyouahaskell.com/

Haskell Documentation. (n.d.). Retrieved from https://www.haskell.org/documentation/

Spotify App. (n.d.). Features retrieved from user experience and platform usage.

# Week 9 (Week of March 4)

## Focus: Design Patterns & Open Source Contributions

This week, we shifted focus to design patterns and deepened our understanding of how we can contribute to open source projects as we continue building the foundation for our coding project. The lecture introduced reusable code solutions through design patterns, and we also explored GitHub’s open source contribution model to prepare us for real-world collaborative development.

## Lecture: Design Patterns

Design patterns provide a proven solution template to common programming problems. They don’t function as executable programs themselves but rather serve as best-practice strategies for implementing recurring solutions. This week’s video explored examples in Java and Kotlin, and introduced resources like Refactoring Guru and the JavaScript Design Patterns guide.

## Activities Completed

###  Research on Design Patterns

Here are four essential design patterns I explored:

Singleton Pattern

Purpose: Ensures a class has only one instance and provides a global access point.

Real-world example: Managing configuration settings or database connections.

Example (JavaScript):

``` js 
const Config = (function () {
  let instance;
  function createInstance() {
    return { setting: 'dark-mode' };
  }
  return {
    getInstance: function () {
      if (!instance) instance = createInstance();
      return instance;
    }
  };
})();

``` 

Why I chose it: Useful for centralized app configuration

### Observer Pattern

Purpose: Allows objects to subscribe and react to events or data changes.

Real-world example: Event systems like addEventListener in JavaScript.

Example: React's state changes trigger re-renders — a form of observer logic.

Why I chose it: Great for real-time features and app state handling

### Factory Pattern

Purpose: Handles object creation without exposing the creation logic to the client.

Real-world example: UI component generators in frontend libraries.

Example (JavaScript):

``` js

function CarFactory(type) {
  if (type === 'electric') return { type: 'Tesla', speed: 150 };
  else return { type: 'Toyota', speed: 120 };
}

```
Why I chose it: Helpful in decoupling object creation logic.

### Strategy Pattern

Purpose: Enables selecting an algorithm’s behavior at runtime.

Real-world example: Payment systems that allow different methods (card, PayPal).

Why I chose it: Perfect for feature modularity and extensibility.

### Resources used:

https://refactoring.guru/design-patterns

https://addyosmani.com/resources/essentialjsdesignpatterns/book/

### Read the Application Development Coding Project Assignment

I revisited the coding project rubric on Brightspace. I now have a clearer understanding of the expectations around:

Code contributions

Collaboration

User stories and functional requirements

Timeline and scope

My group has formed, and our project repository is live and shared with the instructor.

### Read the Research and Reflection Journal Guide

The new guide provided helpful insight on how to make this journal valuable beyond a school project. It emphasized:

Writing with context

Incorporating research

Regular reflection

It’s helping me improve how I document not just what I did, but why it matters.

### ead “How to Contribute to Open Source” (GitHub Guide)

his guide broke down multiple ways to contribute beyond just writing code:

Reporting bugs

Improving documentation

Answering community questions

Helping triage issues

From Section 2, I liked how it defined contribution as anything that improves the project, not just coding.

From Section 4, I explored:

Up-for-grabs

First Timers Only

GitHub’s Trending tab for beginner-friendly repos

Reflection:
I’ve realized that I don’t have to be an expert to contribute meaningfully to open source. Even finding and fixing typos or testing issues can help projects grow. I’d like to start by contributing to documentation or beginner issues before moving into code contributions.

### Application Development Coding Project

Group Formed

GitHub Repo Created 

Initial Planning Meetings Held

We discussed initial project goals, set up our GitHub Kanban board, and assigned roles. I’m focusing on frontend logic and working with JavaScript. We're currently identifying core features and user stories.

### Slack Summary – “Identify Issues to Support”

Repository: https://github.com/public-apis/public-apis
Issue: https://github.com/public-apis/public-apis/issues/4200

Summary:
This repo lists public APIs. One issue requests detailed documentation for a new API that was added without proper usage details. I think it's a good fit since it focuses on writing/documentation and would help many new developers.

### Reflection Questions

1. Is my programming language still the right choice?
Yes! I’m confident about continuing with JavaScript. It’s versatile, and I’m using this opportunity to learn more about ES6+ features and frontend frameworks like React.

2. Application plan and timeline:
We’ve created a rough timeline:

Week 10–11: Complete feature breakdown, assign modules

Week 12: First iteration/prototype

Week 13: Polish and submit

Week 14: Presentation prep

### References

Refactoring Guru. (n.d.). Design Patterns. Retrieved from https://refactoring.guru/design-patterns

Osmani, A. (n.d.). Learning JavaScript Design Patterns. Retrieved from https://addyosmani.com/resources/essentialjsdesignpatterns/book/

GitHub Guides. (n.d.). How to Contribute to Open Source. Retrieved from https://opensource.guide/how-to-contribute/

# Week 10 (Week of March 11)

##  Focus: MV* Patterns & Community Contribution

This week centered around the MV* architectural patterns (like MVC and MVVM), and practical steps toward making an external open source contribution for the Community Code project. We also learned how to assess community guidelines and structure our contributions effectively using tools like forks, branches, and proper documentation.

## Lecture Recap: MV* Patterns (MVC & MVVM)

MV* patterns are architectural blueprints that dictate the structure of an application. Unlike design patterns (e.g., Singleton, Observer), which solve specific programming problems, MV* patterns guide how data flows and interfaces are built within the entire app.

MVC (Model-View-Controller):

Common in frameworks like Ruby on Rails.

Splits concerns across:

Model – Handles data/business logic

View – UI presentation

Controller – Manages interaction between Model and View

MVVM (Model-View-ViewModel):

Used in modern frameworks like SwiftUI (iOS) and Jetpack Compose (Android).

ViewModel handles logic and state binding between the UI (View) and the Model, enhancing separation and scalability.

Understanding this architecture will help inform the structure of our coding project and future contributions.

## Activities Completed

### Assessed External Community Contribution Guidelines

Target Repository: https://github.com/public-apis/public-apis
Issue Chosen: Missing documentation for a newly added API

After reviewing the repo, here’s what I found:

README.md: Clear overview of the project and its structure.

CONTRIBUTING.md: Includes guidelines for adding new APIs and updating existing entries.

CODE_OF_CONDUCT.md: Outlines community behavior and inclusivity policies.

Process Requirements:

Fork repo

Work on a separate branch

Format additions with proper headers

Follow alphabetical ordering

Submit PR with meaningful title and description

🔍 Reflection:
The contributing process is well-documented. It’s designed to be beginner-friendly with many open issues tagged as “good first issue.” I feel confident about working on a documentation-related contribution.

### Slack Summary of Contribution Guide

Shared a summary of the contribution process in the Slack thread. Highlighted that the repo provides strong support for new contributors and how its well-maintained docs help reduce ambiguity.

### Began External Contribution

epository Forked: 

Local Clone + New Branch Created: 

Issue Identified: Add detailed documentation for the “Art Institute of Chicago” public API

Why This Issue?:

It’s an approved but undocumented entry

My contribution will make this API more accessible for developers

Improves usability and adds value to the overall list

Documented this progress in a new CONTRIBUTING.md file inside my Research & Reflection repo.

Contribution Plan Summary (from CONTRIBUTING.md):

``` markdown 
### Contribution Plan

**External Project:** [Public APIs GitHub Repo](https://github.com/public-apis/public-apis)

**Issue:** API added without documentation

**Goal:** Add missing usage details, endpoint examples, and authentication info

**Reason for Contribution:** 
This API entry exists but lacks helpful metadata that devs typically use to evaluate if an API is suitable for their app. My contribution will help increase adoption and improve clarity for future users.

**Documentation Found:**
- https://api.artic.edu/docs/
- GitHub issue thread confirming missing doc request: [#4200](https://github.com/public-apis/public-apis/issues/4200)

**Plan:**
- Update API description
- Add example usage URLs
- Specify authentication requirements

```

### Reflection Questions

What was the hardest thing I had to do this week?
The most challenging part was making sure I thoroughly understood the contribution guidelines for the external repository. It was easy to assume I knew the process from prior GitHub use, but each repo has its own expectations. I overcame this by carefully reading all the contributing files and documenting everything step-by-step to avoid any mistakes.


### References

GitHub – https://github.com/public-apis/public-apis

GitHub Guides – How to Contribute to Open Source: https://opensource.guide/how-to-contribute/

MVVM & MVC Overview – Lecture & in-class video walk-through

# Week 11 (Week of March 18)

## Object-Oriented Programming (OOP) & Finalizing External Contributions

This week’s focus was on deepening our understanding of the Object-Oriented Programming paradigm, examining its key principles, and exploring how it can be integrated into our group coding project. We also continued work on our Community Code contribution, with an emphasis on engagement and progress tracking.


## Lecture Recap: OOP Principles

Object-Oriented Programming (OOP) is a major programming paradigm that organizes code around objects rather than actions. It emphasizes modularity, encapsulation, inheritance, abstraction, and polymorphism. These features help build scalable, secure, and maintainable software.

## Activities Completed

### OOP Summary & Application to Group Project

For our group project, we’re using JavaScript, which fully supports OOP through ES6 classes and object prototypes.

We plan to implement OOP concepts as follows:

Encapsulation:
We'll wrap critical logic (e.g. user authentication, data validation) inside classes/modules to avoid exposing raw data or logic.

````js

class AuthService {
  constructor() {
    this.loggedInUser = null;
  }

  login(username, password) {
    // validation & login logic here
  }

  getCurrentUser() {
    return this.loggedInUser;
  }
}


````

Abstraction:
We’ll expose clean interfaces for external modules while hiding complex data operations internally.

Inheritance:
If we implement multiple content types (e.g. BlogPost, GalleryItem), they can inherit from a common ContentItem class.

Polymorphism:
Functions like render() can behave differently based on the object being passed (blog post, user profile, etc.)

This structure will help keep our project modular and easier to extend in the future.


### Connect with External Community

his week, I explored how active the Public APIs GitHub community is. Although the repo doesn’t use Discord/Slack for discussion, it has an active GitHub Issues section. I commented on a related issue thread explaining my intended contribution and mentioned I’m working on it as part of a class project.

No reply yet, but the documentation already allows for clear solo contributions, so I will proceed unless I hear otherwise.

### Continued Work on Coding Project (Group)

Our team had a productive sprint:

Finalized UI wireframes and architecture plan

Began implementing the dashboard structure using component-based design

Added basic routing and authentication flow

Began testing integration of JavaScript modules with Firebase (for data)

We’re dividing the work based on modules: I’m focusing on user profile management and content rendering logic.

### Reflection Questions

Is your chosen programming language OOP capable?
Yes. We are using JavaScript, which:

Fully supports OOP using class syntax introduced in ES6.

Also supports functional programming, making it a multi-paradigm language.

Gives us flexibility to blend both paradigms depending on what works best for each part of the project.

I appreciate how JavaScript enables hybrid development—sometimes a class-based approach is best, and other times, simple functions or hooks (e.g., in React) make more sense.

# Week 12 (Week of March 25)


## Functional Programming & Project Finalization

This week served as the final push toward completion of the Community Code Project and the ongoing development of our group coding project. In lecture, we explored the Functional Programming paradigm, focusing particularly on functional tools and APIs like map(), filter(), and reduce()—powerful alternatives to imperative loops.


## Functional Programming

Functional Programming (FP) emphasizes pure functions, immutability, and stateless operations. While FP languages like Haskell or Elm are built entirely around these principles, most modern languages (JavaScript, Kotlin, Swift, etc.) incorporate functional features through APIs.

Key Functional Concepts:

Immutability: Variables don't change after they're set.

Pure Functions: Output depends only on input (no side effects).

First-Class Functions: Functions are treated as variables and passed around.

Examples in JavaScript:

```js

const numbers = [1, 2, 3, 4, 5];

// map: double the values
const doubled = numbers.map(n => n * 2);

// filter: get even numbers
const evens = numbers.filter(n => n % 2 === 0);

// reduce: sum the array
const sum = numbers.reduce((total, n) => total + n, 0);

```

Reflection:
I’ve used map() and filter() before but didn’t realize they were part of the functional paradigm. Using them more intentionally will help reduce side effects and keep our code cleaner.

## Activities Completed

### Work on Coding Project (Group)

This was a busy and productive week! Our group focused on:

Final integration of components (authentication, dashboard, UI)

Cleaning up and modularizing code

Implementing form validation using functional utilities

Replacing some for and while loops with functional methods like map() and filter() for a cleaner codebase

Adding helpful comments and finalizing README documentation

Examples of Functional Tools Used:

```js

const users = [ ... ]; // sample data

const activeUsers = users
  .filter(user => user.status === 'active')
  .map(user => ({
    name: user.name,
    email: user.email
  }));

```

### Community Code Project Submission

We submitted our external contribution to the Public APIs repo by March 30 at 11:59pm PST. Here’s a quick recap of the work:

Forked and cloned the repo

Worked on an issue related to missing documentation

Added a detailed API entry for the Art Institute of Chicago, including:

Title, link, description

Usage notes and endpoint example

Auth information

Our PR was submitted and is pending review.

### Reflection & Insights

Functional Programming Takeaways:

Functional tools like map() and reduce() make my code more expressive and readable

Code is more predictable since side effects are minimized

I now understand why developers and instructors emphasize avoiding mutation

Project Status Update:

We are in the final sprint! The app is fully functional and undergoing testing.

Next step: Polish UI/UX, add accessibility features, and finalize documentation for Week 13 submission.

### References

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array

Blacquiere, A. (2025). Functional Programming Video Lecture

Public APIs GitHub Repository – https://github.com/public-apis/public-apis




















