
Workflow for casual users
=========================

1. On first install, start with a Vanilla Firefox (except for power users who wish to customize this manually) ;
2. As the user browses, Firefox detects that the user is connecting to banking sites, to gaming sites, to dating sites, etc. At this stage, nothing happens, but Firefox is learning its Hats;
3. Soon, Firefox starts using Suggested Tiles to offer suggestions:
  * « For security purposes, do you wish me to setup Firefox to deactivate non-essential add-ons while you are browsing on your bank's website? Here's what you can gain. [Yes/Not Now/Never]» (which is probably implemented by spawning an entire profile for this Hat);
  * « Do you want to setup a theme for gaming? »
  * « In the future, for performance reasons, do you wish me setup Firefox to pause all other webpages while you're playing? Here's what you can gain.»;
  * « In the future, for privacy reasons, do you wish me to setup Firefox to prevent Facebook from tracking you around the web using your connection data? Here's what you can gain. »;
  * « In the future, for privacy reasons, do you wish me to automatically turn on Privacy mode when you are browsing this dating site? »
  * ...
4. At this stage, we have a multi-headed Firefox, each head wearing a different Hat. Firefox learns how websites need to be opened with specific Hats;
5. Each Hat behaves as if it were upgraded semi-independently, with new features/settings that match specific needs:
  * As Firefox gains new WebVR features, Gaming-oriented Hats receive a Suggested Tile that offers users the ability to turn on experimental features;
  * As Firefox gains new privacy protection features, Hats that already have some Privacy settings on turn have these features turned on automatically;
  * Some new privacy protection features are developped as add-ons, which appear as Suggested Tiles for Privacy-aware hats;
  * ...
6. To switch between Hats, the user may use the Window menu, or a shortcut. Additionally, opening a tab using a bookmark, or the search bar, or typing a url, causes the appropriate Hat to be picked;
   _(or the current Hat if no Hat can be determined? Or should that be the Vanilla Hat?)_
7. Tabs can be moved between Hats with drag/drop or by right-clicking on a tab and selecting `Send To...`. Menu `Send To...` contains the list of all Hats that have been created, as well as a submenu `New...` offering specific templates (e.g. Gaming, Banking, Blank) for manually creating Hats;


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
    * **Firefox Core**, which is used to run all Hats (so, Firefox Developer Edition, as it currently exists, is *not* a Hat of Firefox Stable);
    * **Bookmarks**, which also have the side-effect of switching the user to the appropriate Hat when they are used;
    * **Site-to-Hat association**, which let Firefox switch the user to the appropriate Hat when browsing to given site;
    * **Password Manager**, so it's easy to choose to use the same identity across multiple Hats (but you opt-in to identities through the login process);


  What is shared between devices
  ------------------------------
    * Each Hat is Synced individually across devices;

  Implementation
  ==============

  Each Hat is technically simple:

  1. A Hat is a separate profile.  We set up Sync in some fashion to copy information between profiles.
  2. A Hat is Firefox Core plus a number of addons.
  3. A Hat also gets its own launcher and icon.  It looks like its own program.
  4. At least one of the addons in a Hat should change the browser visually.  Maybe simply a theme.  It should be obvious which kind of Firefox you have open when you look at the window.
  5. The lightest sort of addons need only override default settings.
  6. A team dedicated to a specific Hat curates and develops the addons and partnerships.  Partnerships also take the form of addons.
  7. A power user can recreate or curate the experience through managing the addons.  Though in some Hats addon management may be disabled (such as Firefox Simple – don't install the AddonManagementDisabler addon if you don't want this ;)

  The platform changes required for this proposal would primarily be in keeping the Hats in sync (to the degree we wish to), and features to move sites between Hats (explicitly or automatically).  And of course we'll be leaning heavily on addons, so they have to work well.
