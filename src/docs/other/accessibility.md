---
layout: default
title: Accessibility
eleventyNavigation:
  key: Accessibility
  order: 0
  parent: Other
description: Best pracices for creating inclusive and accessible sites with swup
permalink: /accessibility/
---

# Accessibility

When developing AJAX-powered page transitions with a focus on accessibility, there are several potential pitfalls to watch for and best practices to follow. Here's a comprehensive list of issues to address and suggestions for improvements:

## Announce changes

- Use ARIA roles and properties to announce content changes to screen reader users.
- For instance, the `aria-live` attribute can be set to "polite" or "assertive" to notify users of content updates. When the content of an element with an `aria-live` attribute changes, the screen reader announces it.

## Maintain focus

- When new content is loaded, it's crucial to manage and set the keyboard focus accordingly. For example, when a new page section is loaded via AJAX, you might move the keyboard focus to the beginning of the new content.
- Ensure that when transitioning, the focus doesn't get lost or set to an unexpected location, making it difficult for keyboard-only users to navigate.

## Semantic HTML

- Ensure that the loaded content uses proper semantic elements (`<header>`, `<nav>`, `<main>`, `<article>`, etc.) so that screen readers can understand and narrate the content's context and structure.

## Keyboard navigation

- All interactive elements, including those loaded via AJAX, should be navigable using only the keyboard.
- Implement a visible focus indicator for all focusable elements.
- Ensure that the Tab order is logical and consistent.

## History management

- When using AJAX to change page content, the browser's back button might not behave as users expect. Consider using the `History` API to manage browser history and ensure that users can navigate back and forth without issues.
- Make sure that when a user navigates back, they're presented with the same state they left, ensuring consistency for all users.

## Avoid autoplay

- Don't automatically play videos, animations, or sounds when loading content through AJAX. It can be disorienting for users, especially those using screen readers.

## Provide skip links

- Offer "skip to main content" or "skip to navigation" links to allow screen reader and keyboard users to bypass repeated content, especially if you're only changing a portion of the page.

## Provide Loading Indicators

- When content is loading, provide visual and non-visual feedback (using ARIA roles and properties) so that all users are informed.

## Test with Real Devices and Users

- Use screen readers (e.g., NVDA, JAWS, VoiceOver) and other assistive technologies to test the AJAX transitions.
- Consider conducting usability tests with real users who rely on assistive technologies to identify any pain points and areas of improvement.

## Escape Mechanisms

- Provide a way for users to stop or escape any AJAX-driven animations or transitions. This can be essential for users who experience motion sickness or other adverse reactions to animations.

## Error Handling

- If there's an error while loading content (e.g., due to network issues), provide clear error messages and give users alternative ways to access the content.

In conclusion, focusing on the user experience for those using assistive technologies will not only make your AJAX-powered page transitions accessible but also improve the usability and enjoyment for all users. Continual testing and feedback are vital in this process.
