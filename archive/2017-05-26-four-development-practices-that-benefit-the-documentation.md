---
layout: post
title: "Four agile development practices that benefit documentation"
date: 2017-05-26
categories: writing
---

I work with a team of **30+** developers and QA on a large platform. For the most part, I write the documentation by **reverse engineering** a feature and acting as its first **external consumer**. This is a good way of sanity checking design and architecture as well as learning how something works.

However:

-   Code does not always capture **intent**. Why something was designed a certain way -- especially if deadlines mean that you have to opt for a **minimum viable solution** -- makes a huge difference to the documentation.
-   Code tells you nothing about **business requirements** and the delineation between **features** is not always obvious.
-   Not all work results in code -- for example, scalability testing might results in a set of **recommended practices**.

Here are four development practices that can benefit the documentation. In our organisation, these are either enforced by the tools or the project manager.

## A task for everything, and for everything a task

![ to do list GIF](https://media3.giphy.com/media/cyMWMsUzpPn8s/giphy.gif)

Source: [Giphy](https://giphy.com/search/to-do-list)

Every piece of work must be captured as a product backlog item (PBI), task, or bug in the project tracking system (such as JIRA or Microsoft TFS).

-   The developers cannot start a piece of work until a task exists
-   All tasks are related to a specific feature area
-   All commits and pull request must be linked to a task -- this is enforced in the UI

This creates a comprehensive paper trail and links every code change to a task with a title and a description. The writer can use the task list as a starting point for the documentation and feel confident that it accurately reflects the work that was done.

## Detailed descriptions and acceptance criteria

![Beeld en Geluid Labs work office busy openbeelden GIF](https://media4.giphy.com/media/3Kp6sZlMqxphC/giphy.gif)

Source: [Giphy](https://giphy.com/gifs/benglabs-httpswwwopenbeeldennlmedia10811-3Kp6sZlMqxphC)

Acceptance criteria are used by QA to plan tests, and is usually a very detailed list of expected behaviour -- e.g. "If you try to save an object with a special character in the title, you will get a NoSpecialCharactersException".

The most useful descriptions contain business requirement and any key decisions that were made -- particularly if they were made during an offline meeting

Detailed descriptions and acceptance criteria tell you how a feature is expected to work and where the requirement came from. It is the best place to get business context for a task if you cannot speak to the developer or product owner.

## Unit and integration tests

![ test cooking american dad testing expected GIF](https://media0.giphy.com/media/7MZ0v9KynmiSA/giphy.gif)

Source: [Giphy](https://giphy.com/gifs/test-testing-expected-7MZ0v9KynmiSA)

Unit and integration tests are a great way to see the acceptance criteria in action, and are a virtual gold mine for code samples. Use tests to get a sense of how a feature or an API should be used.

Tip: If your team uses [SpecFlow](http://specflow.org/), test scenarios are defined in a very easy-to-read format.

## Tag breaking changes

![@SummerBreak food summer crush break GIF](https://media0.giphy.com/media/3oz8xLxnEcXHyVefQc/giphy.gif)

Source: [Giphy](https://giphy.com/gifs/summerbreak-summer-break-3oz8xLxnEcXHyVefQc)

This practice is particularly useful for release notes and for updating documentation that has already been written. Whenever a task or bug results in a breaking change to existing documentation, it gets a [breaking changes] tag.