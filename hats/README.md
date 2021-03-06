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

Related Work
============

 * [Security: Contextual Identity Project: Containers](https://wiki.mozilla.org/Security/Contextual_Identity_Project/Containers).  The Contextual Identity Project has been looking at ways to give users access to their different identities through the browser.  The Containers proposal suggests giving users task-specific browser windows, each running with its own identity information or profile.
 * [Profilist](https://addons.mozilla.org/en-US/firefox/addon/profilist/).  This addon lets you create, switch, and manage your profiles.  There's some support for things like [app icons](https://www.youtube.com/watch?v=fKw-BNWMyQM) as well.
 * [WebRT](https://wiki.mozilla.org/Apps/WebRT).  This is what allows you already to "install" Open Web Apps as stand-alone desktop apps.  Some of what it does might be applicable to "installing" Hats.
 * [SecureFox](https://etherpad.mozilla.org/securefox) is a vision for a more-secure Firefox, in ways that might cause too much breakage or be infeasible for a "normal" mode of Firefox.

Open Questions / Concerns
=========================

 * Do we start with general Firefox and suggest Hats, or do we market specific Hats directly?
 * Are we adding a cognitive load by giving people choice where before there was a single product?  Are we forcing people to ask burdensome questions like "should I be viewing this site in Firefox Focus or Firefox Secure?"
 * Is the engineering hard?  [Probably not as hard as it seems](https://github.com/Yoric/redreaming-firefox/blob/master/hats/details.md#implementation)
 * How many Hats can we expect one user to install?
 * What would be a good set of Hats to develop? (both are research topics)

Reasons Against
===============

 * Instead we should make Firefox the best Firefox it can be.  In other words, we should continue to focus on features and quality aspects that are universal.
 * We *should* focus on a niche or segment, but we should choose just one segment.
 * We lack the resources to do more than one thing (be it Firefox General, or Firefox focused on one niche).
 * Breaking up the Firefox brand into individual products will be confusing.
 
