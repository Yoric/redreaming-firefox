Codename
========

*A browser for every hat you wear*

140 Chars Pitch
===============

You are many persons, and you do many things. Firefox can adapt to all of them, automatically

Synopsis
========

Today's Firefox can be deeply customized thanks to the use of preferences, lightweight themes and add-ons. However, it has two big limitations:
 * much of this customization is reserved to power users;
 * users can only customize Firefox globally, while much customization is actually specific to what the user is currently doing.

We have observed that people naturally use more than one browser, with different browsers specialized to different kinds of behavior.  We want to embrace that by offering different Firefox experiences using the metaphor of multiple browsers that users are familiar with.

This proposal reverses the flow, as follows:
 * Firefox observes and learns usage patterns (e.g. gaming, banking, social networking, web development, etc.);
 * Firefox spawns usage-specific instances (a.k.a. **Hats** or, of course, Personas);
 * Using Suggested Tiles, Firefox offers task-tailored customizations (e.g. elevated privacy settings, activating gaming-specific add-ons or experimental flags, neutralizing all non-essential add-ons for gaming for performance purposes, neutralizing all non-essential add-ons for banking for security purposes, ...)

Power Users can keep the old flow or combine both.

Objectives
==========

 * Tailor Firefox to the needs of users;
 * Improve security;
 * Improve privacy;
 * Improve task-specific user experience;
 * Understand our users' goals;
 * Create a venue for experimentation;

Open Questions / Concerns
=========================

 * Do we start with general Firefox and suggest Hats, or do we market specific Hats directly?
 * Are we adding a cognitive load by giving people choice where before there was a single product?  Are we forcing people to ask burdensome questions like "should I be viewing this site in Firefox Focus or Firefox Secure?"
 * Is the engineering hard?  [Probably not as hard as it seems](https://github.com/Yoric/redreaming-firefox/blob/master/hats/details.md#implementation)
 * How many Hats can we expect one user to install?
 * What would be a good set of Hats to develop? (both are research topics)
