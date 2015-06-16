
Workflow for casual users
=========================

1. On first install, start with a Vanilla Firefox ;
2. As the user browses, Firefox detects that the user is connecting to banking sites, to gaming sites, to dating sites, etc. At this stage, nothing happens, but Firefox is learning its Hats;
3. Once Firefox has learnt a bit about the user's behavior, a Suggested Tile offers to setup Firefox automatically:
  * « Firefox for Banking, by Mozilla »
    * Details: « You use Firefox to access your banking site. Firefox can configure itself to improve your security when you are browsing this site. This is entirely automatic and this does not affect your experience with other websites. »
  * « Firefox for Facebook, by Mozilla »
    * Details: « You use Facebook. Firefox can configure itself to improve your experience with Facebook, while better protecting your privacy. This is entirely automatic and this does not affect your experience with other websites. »
  * « Firefox for Gaming, by Mozilla »
    * Details: « You use Firefox for gaming. Firefox can configure itself to provide the best gaming experience. This is entirely automatic and this does not affect your experience with other websites. »
  * « Firefox for Privacy, by Mozilla »
    * Details: « You use Firefox for browsing a dating site. Firefox can configure itself to improve your privacy when you are browsing this site. This is entirely automatic and this does not affect your experience with other websites. »
  * ...
4. If a user accepts the suggestion of the Suggested Tile, this Tile becomes a Permanent Tile;
5. Clicking on either the Suggested Tile or the Permanent Tile switches to a *Firefox Hat*;
6. A *Firefox Hat* is basically an instance of Firefox window with its own visual theme and configured specifically for one website or a collection of websites;
7. As Firefox receives new features, some of the features may be hidden by default:
   * features that look complex (e.g. Developer Tools) or not directly related to browsing (e.g. Hello);
   * features that could break some websites or our revenue model (e.g. aggressive Privacy protection, auto-unloading tabs, https everywhere, ad-blocking, etc.);
   * features that are specifically designed to remain hidden by default (e.g. disabling add-ons);
   * features that are still considered somewhat experimental (e.g. Reading List, WebVR, ...)
8. Each Hat behaves as if it were upgraded semi-independently, with new features/settings that match specific needs:
  * As Firefox gains new Gaming-oriented features (e.g. ability to put other tabs on pause, or TeamSpeak Hello), these features are added to Gaming-oriented Hats, but not activated by default in other Hats;
  * As Firefox gains new aggressive privacy protection features, some of these features are turned on automatically on Privacy-oriented Hats;
  * Individual Hats can receive further features that are not turned on automatically but appear as Suggested Tiles;
  * ...
9. Several Hats can be active at once. To switch between Hats, the user may use:
  * the Permanent Tile;
  * the Window menu (even if the Hat hasn't been loaded yet);
  * a keyboard shortcut;
  * the OS's process-switching mechanism (e.g. Ctrl-Tab, the Dock, etc.);
  * the icon in the Start Menu, the Applications Folder, etc;
  * a built-in page `about:hats`;
11. Also, following a link, opening a bookmark, typing a URL for a websites that is associated to a Hat switches to that Hat, while following a link/bookmark/URL for a website that is not associated switches back to the Vanilla Hat;
12. Tabs can be moved between Hats with drag/drop or by right-clicking on a tab and selecting `Send To...`. Menu `Send To...` contains the list of all Hats that have been created, as well as a submenu `New...` offering specific templates (e.g. Gaming, Banking, Blank) for manually creating Hats. Bookmarks can be moved between Hats using essentially the same mechanism;

Variant workflow
================

1. User visits getfirefox.com and picks a Hat in the collection of Hats.
2. Hat is installed (along existing Firefox, if any).
3. Proceed as above.

Variant workflow (Power Users)
==============================

1. User starts with Vanilla Firefox;
2. User moves a Tab or a Bookmark to a new Hat by right-clicking and selecting `Send To... > New Hat... > Blank`;
3. User sets up new Hat as she wants, using add-ons, themes, ...;
4. At some point, user picks a name for the Hat;
5. Hats may be managed through a built-in page `about:hats`;

Technical aspects
=================
What is NOT shared between Hats
-------------------------------
 * **Cookies**, as this would hurt privacy and security protection of this proposal;
 * **Cache**, as this would hurt privacy and security protection of this proposal;
 * **Plug-in instances and data**, as this would hurt privacy and security protection of this proposal;
 * **Identities and Sessions**,  as this would hurt privacy and security protection of this proposal;
 * **History**, as this would hurt privacy of this proposal;
 * **Preferences**, as we wish to use Hats-specific Preferences for customization purposes;
 * **Add-ons**, as we wish to use Hats-specific add-ons for customization purposes;
 * **Desktop Icon**, as we wish to make it easy for users to launch specific Hats;
 * **Task Manager Icon**/**Task Switcher Icon**, as we wish to make it easy for user to switch to specific Hats;


What is shared between Hats
---------------------------
 * **Firefox Core**, which is used to run all Hats (so, Firefox Developer Edition could be reimagined as a Hat that can apply to Firefox Release, Firefox Beta, Firefox Aurora or Firefox Nightly);
 * **Bookmarks**, which also have the side-effect of switching the user to the appropriate Hat when they are used;
 * **Site-to-Hat association**, which let Firefox switch the user to the appropriate Hat when browsing to given site;
 * **Password Manager**, so it's easy to choose to use the same identity across multiple Hats (but you opt-in to identities through the login process);


What is shared between devices
------------------------------
 * Each Hat is Synced individually across devices;

Open questions
==============

**Q** How can we make sure that users who have been switched automatically to a Hat know how to switch back to the previous Hat? With tabs, it is simple, because they are still visible, but since Hats are in distinct windows, they are harder to find for casual users with limited knowledge of windows.

**Q** How are we going to use Facebook, Google, etc. to login to a website?

**Q** Is this going to break the `like` button?

Implementation
==============

Each Hat is technically simple:

  1. A Hat is a separate profile.  We set up Sync in some fashion to copy information between profiles.
  2. A Hat is Firefox Core plus a number of addons.
  3. A Hat also gets its own launcher and icon.  It looks like its own program.
  4. At least one of the addons in a Hat should change the browser visually.  Maybe simply a theme.  It should be obvious which kind of Firefox you have open when you look at the window.
  5. The lightest sort of addons need only override default settings.
  6. A team dedicated to a specific Hat curates and develops the addons and partnerships.  Partnerships also take the form of addons.
  7. A power user can recreate or curate the experience through managing the addons.  Though in some Hats addon management may be disabled (such as Firefox Simple – don't install the AddonManagementDisabler addon if you don't want this ;)

  The platform changes required for this proposal would primarily be in keeping the Hats in sync (to the degree we wish to), and features to move sites between Hats (explicitly or automatically).  And of course we'll be leaning heavily on addons, so they have to work well.

Precedence
----------

Firefox already has a way to install applications that look independent, [WebRT](https://wiki.mozilla.org/Apps/WebRT).

The basic technique it uses:

  1. As part of the build process it builds a stub installer ([Mac](https://github.com/mozilla/gecko-dev/tree/master/webapprt/mac), [Windows](https://github.com/mozilla/gecko-dev/tree/master/webapprt/win), [GTK](https://github.com/mozilla/gecko-dev/tree/master/webapprt/gtk))
  2. There is code to [copy the installers](https://github.com/mozilla/gecko-dev/tree/master/toolkit/webapps), invoked by [some UI](https://github.com/mozilla/gecko-dev/blob/master/browser/modules/WebappManager.jsm)
  3. After the stub is copied, its icon is changed (platform specific), it is renamed, and the webapp ID is saved alongside the stub
  4. When you launch the stub, it finds Firefox and launches libxul, which does most of the work
  5. The stub also decides on an app-specific profile path.  This profile gets created by libxul if necessary.  You can't control the profile when using WebRT launchers.
  6. The [Firefox launcher](https://github.com/mozilla/gecko-dev/blob/master/browser/app/nsBrowserApp.cpp) does a bit more, maybe related to crash stats and such, not sure.  WebRT's launcher is an independent implementation.
  7. The stub then asks libxul to load [webapp.xul](https://github.com/mozilla/gecko-dev/tree/master/webapprt/content), as opposed to browser.xul.  Maybe pointing to browser.xul would be all its taks to turn it back into a normal browser?
  8. There may be code (maybe in webapp.js) that on first run sets up the profile.  I can't locate this code however.
  9. Currently there's no data sharing between WebRT apps and any other profiles.  The WebRT team has talked about it some.
