
Workflow for casual users
=========================

1. On first install, start with a Vanilla Firefox (except for power users who wish to customize this manually) ;
2. As the user browses, Firefox detects that the user is connecting to banking sites, to gaming sites, to dating sites, etc. At this stage, nothing happens, but Firefox is learning its Hats;
3. Soon, Firefox starts using Suggested Tiles to offer suggestions: 
  * « For security purposes, do you wish me to setup Firefox to deactivate non-essential add-ons while you are browsing on your bank's website? Here's what you can gain. [Yes/Not Now/Never]» (which is probably implemented by spawning an entire profile for this Hat);
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
  
  Technical aspects
  =================
  What is NOT shared between Hats
  -------------------------------
    * **Cookies**, as this would hurt privacy and security protection of this proposal;
    * **Cache**, as this would hurt privacy and security protection of this proposal;
    * **Plug-in instances and data**, as this would hurt privacy and security protection of this proposal;
    * **Passwords and Identities**,  as this would hurt privacy and security protection of this proposal;
    * **History**, as this would hurt privacy of this proposal;
    * **Preferences**, as we wish to use Hats-specific Preferences for customization purposes;
    * **Add-ons**, as we wish to  Hats-specific add-ons for customization purposes;
    * **Desktop Icon**, as we wish to make it easy for users to launch specific Hats;
    * **Task Manager Icon**/**Task Switcher Icon**, as we wish to make it easy for user to switch to specific Hats;
    

  What is shared between Hats
  ---------------------------
    * **Firefox Core**, which is used to run all Hats;
    * **Bookmarks**, which also have the side-effect of switching the user to the appropriate Hat when they are used;
    * **Site-to-Hat association**, which let Firefox switch the user to the appropriate Hat when browsing to given site;


  What is shared between devices
  ------------------------------
    * Each Hat is Synced individually across devices;
