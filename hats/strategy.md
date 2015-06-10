## Strategy

What does this to do help Mozilla-the-organization?

### De-commodify the browser

We aren't at risk of browsers becoming a commodity: we're already there.  The basic feature set of browsers is identical.  The extended feature set of browsers is almost identical.  The distinguishing features of browsers are largely unused.  In a commoditized market the competition takes place along only a few parameters: speed, reliability, (perceived) security, platform and cross-platform integration.  Firefox has to hustle just to keep up.

We explain browsers as completely general-purpose.  One browser can do everything: it can load your pages, save your data, host your extensions, debug your code.  As a result we ourselves treat our browser as a commodity.

We could distinguish commodity features as *quantitative*: improvements that exist along already-identified lines in the browser space.  De-commodifying features could be see as *qualitative*: they change the experience of using a browser.  We are very shy about qualitative changes.  And probably we're right to be.  We have a large and diverse user base that has chosen Firefox based on its current functionality.  Any change we introduce is likely to upset many of those users if they recognize there was any change at all – and as we make more subtle changes, users who would find value in those changes are unable to find them or understand the change's positive impact.

Because of the diversity of our users we can *understand* our users, but we can't do much *with* that understanding.

Multiple editions (Hats) for Firefox gives us ways to introduce qualitative changes without expecting that all users will find the feature useful or even understandable.  In the context of a particular kind of behavior the user has decided to make (and that we know the user has decided to make, due to their use of a specific edition), we can posit much more about a user than we can with a completely aggregated user base.

As features are tested in specific contexts, we can still consider introducing those features more widely across editions.

### Create an avenue for disruptive innovation

In _The Innovator's Dilemma_ Clayton Christensen describes some of the problem of introducing innovation as an established player:

> The last element of the failure framework, the conclusion by established companies that investing aggressively in disruptive technologies is not a rational financial decision for them to make, has three bases.  First, disruptive products are simpler and cheaper; they generally promise lower margins, not greater profits.  Second, disruptive technologies typically are first commercialized in emerging or insignificant markets.  And third, leading firms' most profitable customers generally don't want, and indeed can't initially use, products based on disruptive technologies.  By and large, a disruptive technology is initially embraced by the least profitable customers in the market.  Hence, most companies with a practiced discipline of listening to their best customers and identifying new products that promise greater profitability and growth are rarely able to build a case for investing in disruptive technologies until it is too late.

Rational decision making will naturally lead us in the direction of what Christensen calls "sustaining technologies" – ideas that improve on our product given the identified competitive landscape.  This does not represent a flawed decision making process.  But it is the natural result of our current product scope:

* It's very hard for a differentiating feature to show a marginal benefit that registers with the large scale of customers we have; a feature may be very exciting to some small group of people, but that's hard to see amidst the volume of users we have.
* Current customers are not excited about the features we add.  For example, the vocal reaction to Pocket.  Generally we don't have a way to distinguish features for *retention* from *acquisition*.  If we can acquire users through a new Hat, those users are bought into the vision of that Hat.  We avoid splitting our attention between users that are already happy with Firefox and want More Of The Same (who are perfectly good people who we want to satisfy), and users who are open to new experiences (and may represent the vanguard of a new perspective on browsers).

### Improve access to the browser by contributors

Contributors to Firefox do not have the agency or impact they have in other open source projects.  We ask that everything we do be good enough for everyone.  We have addons, but we don't have a path to add addons to general Firefox.  Even if we accept addons as part of the Firefox installation as part of Go Faster, it is very unlikely we will accept contributed addons.

Agency is much easier to offer with a segmented set of browsers.  The contributors can concentrate on an audience they understand, and we have a very sticky shared understanding of that audience via the segmentation.  If you contribute something to Firefox for Kids, then no one is going to forget that the intended audience is kids; it'll be stuck right on the Bugzilla ticket.

### Give a context to explain our work internally and externally

Who wants to think about browsers?  Not many people.  But they do think about things they want to do, and they think about their online experience.  We get to talk about "gaming" or "security" or "privacy" *and then*: we have the browser for you.

Current it's hard for us to explain a feature to individuals.  We don't know *why* a person uses Firefox, we don't know what that person is trying to achieve, so we only have generic language to explain our product.  "Bloat" is a common complaint, which can mean anything, but maybe most generally is a complaint of "there are parts of the product that aren't meaningful to me."  Pocket for instance does not affect the performance, as the button just sits there dumbly until you use it.  But it adds to a sense of Bloat.

When a new feature appears a user will want to know: is this feature for me?  The person may like or not like the feature, but before they explore the feature they want to know if they are even the intended audience.  Is the feature worth exploring or learning?  When using a use-case-specific browser, they'll know that any feature Firefox adds or shows them is a feature someone thinks this person specifically might like: a feature this user personally may find valuable.  That's not something we can claim right now with our features.

Internally we can do the same thing: with segmentation we will know how to sort features, and we understand much more about the utility criteria, because we know what the user expects from a *specific* product.  Firefox for Research invites very specific tools.  And when we deploy a feature, we'll know if it satisfies that use case, without the data being confounded with a large unsegmented population.

### Allows us to be bold

Aggressive tracking protection is an implemented feature, we just have to turn the switch on.  But we can't, or don't let ourselves.  We could hide it in a little pref.  We could try to explain it.  If we push it more strongly we'll get pushback from sites that feel we are breaking a contract of the web.

With a segmented product some of these choices will be easy.  Firefox Private would turn this feature on without a doubt.  We would not wring our hands.  The people involved would see their contribution put to use.  Site owners would have a hard time complaining, as it would clearly follow from user intent: the intent the user clearly indicated when they chose to use Firefox Private.

Maybe Firefox Private would be the launching point for delivering these features more widely across these products.  If we do so, we can do so feeling more confident about the impact of and reaction to the feature.

The same is true for integrations with proprietary services.  Some of these may make very clear sense in specific contexts, but receive stiff pushback from our community that has many implicit assumptions about the purpose of Firefox.

### Acquisition funnel

The acquisition funnel might look something like this:

![Funnel](http://1g1uem2nc4jy1gzhn943ro0gz50.wpengine.netdna-cdn.com/wp-content/uploads/2015/05/Screenshot-2015-05-31-19.50.54.png)

*From [
The Next Feature Fallacy: The fallacy that the next new feature will suddenly make people use your product](http://andrewchen.co/the-next-feature-fallacy-the-fallacy-that-the-next-new-feature-will-suddenly-make-people-use-your-product/).  Replace "signup" with "download".  Some comments [here](https://via.hypothes.is/http://andrewchen.co/the-next-feature-fallacy-the-fallacy-that-the-next-new-feature-will-suddenly-make-people-use-your-product/)*

We might ask, what tools do we have to decrease our attrition at each of these stages?  A user is more likely to continue through these steps if we can provide compelling value, which may include explaining that value.  What does this user want as he or she enters the funnel?  We don't know very much right now about a specific user, and *anything we know* will be wiped out at the point of download. Only by customizing the downloads to the funnel entry point can we continue to offer specific value targeted at a user's desires or expectations.  This proposal *is* that customization of the download.

Note that while we talk about "Firefox Core" being common among all *Hats*, the download doesn't have to map 1-to-1 to our current approach.  Assuming we use a stub installer, we can detect if Firefox Core is already installed and reuse that, and downloading a specific edition could be equivalent to indicating through a Firefox tool that you want to use a different Hat.  Downloads are just the most familiar entry point to a new program, and a "program" is how we expect people to understand the separate launchers, profiles, and visual identities of the Hats.
