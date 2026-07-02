<!-- **YYYY-MM-DD**: 
- [Project]: [What I did] 
- [Project]: [What I learned] 
- [Next]: [What's next]-->
**2026-02-07**
* ERM/LVH: these stubborn express deliveries are just a nightmare - every time I think I've fixed it, the errors appear again. Annoyingly, they are not consistent so I may test it a few times and it works fine - until it doesn't. Still working on these and also a few minor fixes across LVH/ERM
* Cyberleto is over, so I will plan to make the folder public
  
**2026-30-06**
* ERM/LVH: I'm still working on this tricky new express delivery. The button only appears after the full address, and my scripts keep clicking payment before the page is rendered again. I'm trying a new solution, a helper function that compares the list of button ids (the expected payments for this delivery) to the ids on the page, but it's still not working properly
  
**2026-06-26**
* Admin: because of the huge promo we're running and other reasons, I've not been as consistent with the devlog as I'd like. I've been working on promo scripts that were mostly a success. The scripts are in the currently closed repo, but I'm planning to open it once the promo is over.
* ERM/LVH: beside promo scripts, I've been working on editing the delivery logic for CZ and IT websites. They now have an express delivery (completely new for CZ; was on IT before, but different) that is processed through 3rd party API. The main problem is with timing: the express delivery button only appears when full and valid address is typed in and it takes some time to render. My scripts were trying to select payment option once the express buton was not fully loaded and when it did, it overrode the payment choice making it a default. That's what I've been trying to fix. Got really frustrated with DeepSeek not giving me proper advice until I figured out that IT website just changed an express delivery selector - that was my shameful "duh!" moment.
  
**2026-06-22**
* Summer promo: I've done a working file reader + scrapper + runner on 4GLAZA and tested it on a stage website. It worked but it mostly shows errors (because stage has a different catalog with older prices - most checks fail). The promo goes live later during the week so I decided to include RU LVH in this as well. The plan is to have the same reader but different checkers and runners for each website and also put common helper functions in a separate file (to be imported).
* Small fix on TR LVH where the price class 0 is practically dying - my script showed a bug with shipping fee being different than expected, but only because the price of the item increased. For now, the lists of item are hardcoded, but I may want to add some functionality to avoid these false negatives in the future. 

**2026-06-15**
* Summer promo: created more or less stable xls file reader, now working on a web scrapper and comparison. It's simpler than my other scripts, but more options to do things so the difficulty is seeing these options and picking the right one
**2026-06-11**
* LVH: tested discount verification a bit more (seems stable) and added a function to make an order as a legal entity. It's a separate tab on order page with a dedicated URL, and it has all the delivery options available in the region, just 1 payment option (for legal entities) and 1 more Dadata point where you type in TIN and the company name and address fields are automatically populated
* Summer Promo: started a new repo (currently private) to test the discounts on our available summer promo. Will open the repo after the promo is over

**2026-06-10**
* LVH: worked on verifying discount feature on RU ERM (5% discount for regional orders paid with a credit card). Doesn't sound complicated but it took some work and debugging. Verification involves 2 steps: checking whether we have a discount section with discount % and calculating the price with the discount. The discounted price is calculated in an unusual way - the discount is applied to the item's price (or the total cost of all items) but it is displayed in a total sum. To verify it, we need to calculate the price of the item with the discount applied (price - price*0,05), add the delivery/payment fee and round the kopecks
  
**2026-06-09**
* Admin: not much work today, just a little fix for IT ERM, IT LVH. But I think I made an important realization: the demotivation I've been feeling about my work lately and my struggle to focus are related to ill-defined goals and tasks. If I define my tasks in more specific term and rebuild my vision for this project, I think I'll be more excited to work on these scripts again.
**2026-06-08**
* LVH: today I took some time to just slowly go through my BG LVH random script and make sure I understand everything and also remove redundant comments or even code. This work kinda scares me because I'm afraid to find out I'm completely out of touch of what's going on in my code. But I believe it's super important, so I'm just going slow and taking my time. The most work should be done with one script and then I can just "trim" the others based on that, only investigating the local features with particular attention. 

**2026-06-05**
* Admin: this week, I haven't done much, and I feel pretty demotivated. The connection to websites, especially European/US is so bad my scripts are failing constantly. There is not much sense in fixing a script if you can't even make it open the home page. The reason for bad connection is apparenly some RKN blocking although our sysadmins are doing their best. I hope the next week the work will be more bearable, otherwise I'll need to switch to another project or something.

**2026-06-02**
* Admin: I took a little break from scripts reverse-engineering some of our APIs - plus we have some issues with a catalog on a few language websites (which I wouldn't have noticed without the errors in script!). My plans are to keep refactoring scripts and add legal entity order for RU websites as well as add some kind of fallback in case the item is not found (as now I only have a fallback for the item that is found but unavailable)

**2026-06-01**
* LVH: I took BG LVH random and started refactoring it. I created a checklist for the ponts to check and update in other scripts (there are a lot of scripts, and changes can get messy, so I'm all in for a more "surgical" approach here). As a few examples, the updates include fixing small errors (like missing "f" before an f-string), adding a few new order variables ("displays_cents", "free delivery" phrase etc), adding a new function (formatting price) and making sure it's integrated with no errors. The plan is to clean up BG LVH and then use it as a template to add the same changes to all the other scripts that need them

**2026-05-29**
* Tier 3: these websites are tested with 1 random order only, so I took random scripts for ERM and LVH Tier 3 websites with minor updates and also updated Tier 3 runner (no need to track emails that thoroughly)
* Admin: I'm feeling like this project is getting close to the end, so I'm already considering the possible next ones - I have a few exciting ideas

**2026-05-28**
* Tier 1 4GL: completed test plan, the script is relatively stable. May need some more finetuning still, will monitor
* Tier 3: started working on Tier 3. The check for Tier 3 websites is just a random order, so all I really need to do is just assemble my random scripts in a sequence with a runner. Just the LVH and ERM random runners won't work, because Tier 3 has both LVH and ERM scripts and it's more convenient to run them in one go.
  
**2026-05-27**
* Tier 1: edited RU 4GL script up until a working order, but I'm still working on a test plan (every delivery option, 6 + every payment option, 7)

**2026-05-26**
* Tier 1: started working on 4glaza, got up to the basket so far (working slowly and practicing finding the selectors myself instead of asking AI). I'm still amazed at how helpful the class structure has been as it took me very little effort to edit it. Chances are, the working version will be ready tomorrow - and I'm already thinking what my next big projects can be. 

**2026-05-25**
* Tier 1: there are only 2 b2c websites - CZ LVH and 4glaza (a Russian website with no EU counterpart), and today I wrote a CZ LVH tier1 script (adapted from CZ LVH random and CZ ERM tier 2) and edited a runner - it was all pretty fast. CZ LVH tier1 seems to work, but I'll monitor it just in case. Next big task is writing a script for 4glaza completely from scratch, including the test plan generation logic (I expect it to be complicated as there are many parameters - region, delivery/payment, discount - and not everything work with everything)

**2026-05-22**
* LVH: I didn't want to rush into 4glaza just yet, and I thought about 2 problems that annoyed me. First, most websites have cents (or their equivalent), but a few don't and they don't need to display prices in floats, but rather integers. Second, while verifying shipping/payment costs, some websites have an annoying 'TBD' option that can't be converted into a number - hence some sites verify numbers while other strings. Both these things should ideally be language-agnostic, and there should be a function that could count that based on the details provided in OrderContext (likes "self.displays_cents = True"). I have some ideas for solution and may work on implementing it next week.
  
**2026-05-21**
* RU LVH random and Tier 2: achieved a relatively stable version for both, will monitor in the upcoming days. I now have full suite of B2C websites across EU and Russian websites for random LVH, random ERM and Tier 2 🎉! Tier 3 is basically already in my pocket (will be 1 random order per website, the majority of these I already have, so just need to edit the runner). And my next challenge will be 4glaza (a unique Russian website, doesn't have EU version) and Tier 1 where we test every delivery and payment option.
* EU ERM: fixed some small errors, like verification error on DE ERM

**2026-05-20**
* RU ERM: my insight today was - not everything that seems to work actually works. RU ERM seemed pretty fine until I discovered a big obvious bug - the delivery selection completely missed the region!
* RU LVH: keep working on it, but script is not stable yet. It starts to run, but doesn't close the cookie popup and can't move to order yet

**2026-05-19**
* Admin: this day, I did something different for a change - I added some basic documentation on my scripts in case some of my colleagues want to run it. I added 2 .bat files - install_dependencies and a runner for each series that you can just by double-clicking. Would be great to get some feedback from real users on that, but I'm not sure anybody would be interested.
* RU LVH: started RU LVH random (should have started with the more difficult one, Tier 2, but alas) and plan to work on it tomorrow.
  
**2026-05-18**
* Tier 2 RU: turns out, last FRI I was just 1 step away from having RU ERM Tier 2 running! Fixed it, fixed a few more errors, and now I have a seemingly stable script. Already incorporated it in a normal runner (not a dedicated RU runner for test), and it seems to work. Will see for the next few days.
* ERM RU: it also took me not that much effort to edit it to be a RU ERM random script (choosing a delivery and a payment option randomly). I think it's because Tier 2 scripts are a bit more complicated, so I was editing by simplifying, plus the classes helped a ton.
* Plans: I'm pretty excited to start working on RU LVH script, and I have a feeling it should be relatively easy. I've already figured out the most difficult parts (whole setup for LVH websites + Russian payment/delivery system similar across all RU websites), so the challenge is to combine them to work smoothly without messing up anything in the process.

**2026-05-15**
* Tier 2 RU: today I was pretty excited to work on this project because I feel like I've almost got it! I'm currently stuck on order page, wrestling with Dadata-hinted address input (the same thing that made me abandon the script for some time). The theory is that JS doesn't work for it so we have to use real keystrokes. I have a hunch that, once I figure it out, I pretty much get the whole script - and then editing it for Tier 2 RU LVH would be easy peasy. 

**2026-05-14**
* Tier 2 RU: finally some meaningful progress - I managed to run the script up until the order form where it failed with the error. Most notably, I created a simple, clear concept for test plan, although it does involve a little hardcoding. Since we only have 1 3rd-party payment option (worsk with everything) and 3 3rd-party delivery options, the test plan will just pair the payment with any of the deliveries and find 2 random payments for other deliveries. No fancy combination needed. (I was worried about the perspective of using this structure on 4glaza, where we will test ALL the options, but let's solve the problem as they come). 

**2026-05-13**
* Tier 2: fixed some errors, incl. PL ERM where the script failed to confirm the shop after shop pickup (not an insignificant error!). Added currency feature to DE LVH and PL ERM (I added it to the scripts where I fix other issues, so it may seem random - but I do keep a track)
* Tier 2 RU: kept working on test plan function
  
**2026-05-12**
* Tier 2: I decided to finally add a variable for currency since fixing it manually has been a nightmare - it needs consistency. Added it on HU LVH only, will transfer to other scripts.
* Tier 2 RU: some progress with RU script - updated it up to the test plan creation (the scariest part). Also created a test runner for RU specifically so as to not mess with the real runner.
  
**2026-05-08**
* Tier 2 RU: work on RU ERM is really slow, I'm getting overwhelmed and feel strong resistance, but today I was able to finish organizing data (for now) and move to functions, up to delivery selection. It needs to revise some logic as the options are more complicated. The great thing is that both shop pickups and SDEK pickup points are identical so we're able to group them together.

**2026-05-07**
* Tier 2: not much done on the RU ERM today, but it's the first time I ran all my Tier 2 scripts for a real Tier 2 website check - and it went pretty well, no errors and no crashes. Feels good to be reminded why I'm doing all this :)
* ERM/LVH: fixed a few small errors like fee verification fails and removing my old temporal data rewriting real data for test purposes

**2026-05-06**
* Tier 2 - RU: still working on RU ERM script with a very slow progress. It seems very overwhelming because, although the structure is similar, the approach must be different. A simple example: while in EU scripts we added "compatible_with" to payments (set a delivery > scan payments' 'compatible_with' to find said delivery > choose payment), for RU, we have to add 'compatible with' to deliveries because they depend on the region (Moscow, St.Pete, regions) and the payments are shown after the delivery is chosen
* 
**2026-05-04**
* Tier 2 / LVH: added fix for the city field error (script fails, because it can't find city field after country selection), added wrong selectors by error, fixed them, too. Also added a fix for Tier 2 that correctly counts and uses test emails for the whole suite (currently 2 for LVH, 2 for ERM, with IT ERM variability of either 2 or 3 orders). Fixed HU LVH and HU ERM fee verification error.
* Tier 2 - RU: I got a little bored and needed another challenge so I decided to start working on RU ERM (previously, I couldn't make progress with our RU websites). The RU ERM layout is the same, but it has many more payment and delivery options with its own pretty complicated logic. Also, it uses Dadata API to get hints of the user's location (I couldn't find a way to give this field the correct input before). Now with a bit more expreience, I hope that I'll be able to solve these issues eventually. 

**2026-04-30**
* Tier 2: still fine-tuning LVH and ERM scripts. Updated them with the consistent delivery/payment option spelling (now it must be consistent across ALL scripts) and added function enabling to use several emails per country, but it doesn't work as expected yet (has 1 email for PL ERM, but thinks it has no emails). Will keep working on it.
* Admins: I have a list of errors that appears inconsistently and will monitor it

**2026-04-29**
* Admin: I spent my efforts today on ensuring the delivery and payment options are spelled correctly on ERM and LVH scripts (haven't done Tier 2 yet). It's boring and unsexy, but I was tired of this little mistakes where, say, it has "courier" on LVH and "Courier delivery" on ERM, and I need to remember that or it'll throw an error that is hard to trace. Also, a few minor fixes for Tier 2 websites.

**2026-04-28**
* Tier 2: mainly worked on the issue where a script needs 2 emails (e.g. IT ERM) and has to change email mid-script. It required some tweaks to the runner and the individual scripts as well. Implied and tested on ERMs only, will add to LVH later
  
**2026-04-27**
* Tier 2: finished all Tier 2 ERM scripts, now all LVH and ERM websites are covered for Tier 2 (but I haven't started working on our RU websites or B2B)
* Tier 2: IT ERM has unpredictable number of orders (2 or 3) because it's the only case so far where not every 3rd party payment option is compatible with 3rd party delivery options (no Credit card for Express delivery)

**2026-04-23**
* Tier 2: fixed up some errors and ensure consistency across BG, EU, HU and PL LVH, but there is still a problem with InPost (PL) that needs to be fixed
* Admin: I started to keep a .txt file on my desktop where I put all the little annoying details or errors in script (like too many ticks that are just distracting when I scan logs or IT "unavailable indicators" in HU scripts) - and I work on them calmly first thing in my workday. So far I really like this process and it's also efficient. 
  
**2026-04-23**
* Tier 2: edited the runner and all 4 Tier2 Levenhuk websites (BG, EU, HU, PL). It's working, but need to clean it up a bit. Hope to contunue editing all Tier2 ERMs in the following days. The logic of the runner is different and the main functions of the scripts also have the different structure, but once figured out, individual changes in the scripts are pretty small.

**2026-04-22**
* Admin: I forgot to keep my devlog again, but now I'm back. I reconsidered my goals and decided to write a test suite based on Tiers (groups of websites based on importance, 3 Tiers total) instead of brands + random/choice. That way, I can just run the suite runner and execute all orders needed for the Tier. It sounds pretty obvious, but I didn't think of it before. The only difficult moment is that it needs a dedicated function to create a test plan to contain all combos to test (Tier 1 = all delivery/payment optiions at least once, Tier 2 = all 3rd party delivery/payment options at least once, Tier 3 - 1 random order per site, for which my existing random scripts can be used)
* I already wrote a dedicated runner for Tier 2, edited a script for HU LVH and tested them together (seems to work). Will add more scripts in the next days.
  
**2026-04-16**
* Admin: forgot to post here AND forgot to push my commits yesterday. Gotta be more disciplined with that
* Ermenrich: our devs fixed PL ERM error, and I fixed my script so it's working now. Also, found and fixed a fee verification error on HU ERM and LVH
* Levenhuk: started to work on IT LVH script that lets the user choose delivery and payment options - still stuck on 'stale reference' for express + paypal. I call these scripts "choice" as opposed to "random".  This is the next step towards complete test suite - it will let me selectively test each possible flow on every website

**2026-04-13**
* Ermenrich: I was still working on InPost-non-default payment flow when I realized it worked the same way in PL LVH script (that previously worked fine). And with the manual order! Turned out, it's not my bad code, it's more global issue - even if it's just due to a slow network. Will investiage tomorrow
* Ermenrich and Levenhuk: in the process of fixing 2 small errors - space in HU delivery/payment fee prevents the correct comparison ("2 000 Ft" != "2000 Ft") and changed business logic on IT (no more payment fees)

**2026-04-10**
* Admin: my mishaps keep coming - now my work PC had some problem, and D disk was gone...
* Ermenrich: still working on PL script with not much progress. Consulted with DeepSeek, but its suggested edits and debugs just bloated code without solving the issue. I gave up and decided to copy and paste this section from old VO version with thoroughly checking and editing it (still in progress).
* 
**2026-04-09**
* Admin: missed yesterday again for logging. Some network issues (everything runs super slow) plus a lot of manual testing
* Ermenrich: Still working on PL ERM (InPost + non-default payment flow) which takes annoyingly long. The problem seems to be that the required fields takes long to populate and when payment is selected, the data is not there yet which throws an error

**2026-04-07**
* Ermenrich: updated EU and HU ERM scripts adding OrderContext class. It really helped me update ERM scripts quickly, but as I copy and paste scripts from one country as a draft from another, there are still a few errors here and there (e.g. Italian delivery gets lost and reproduces for HU and EU).
* Both: now that I only have PL ERM to update, I'm thinking of the next step which will be updating and creating a series of orders where the user selects delivery and payment option - that will allow me to test any combination of delivery/payment specifically or all of them.
  
**2026-04-06**
* Levenhuk: fixed order fee verification error for ES LVH, updated payment logic. Thanks to my autotests, it was discovered that COD doesn't work for orders 120+ EU as expected and managers decided to hide COD payment option for such orders
* Ermenrich: updates ES ERM based on DE ERM and ES LVH, with the new payment logic
  
**2026-04-03**
* Ermenrich: fixed shop pickup flow on PL ERM. It's weird how sometimes things that were super simple once turned into a real obstacle somewhere else. On LVH it was a default option with nothing to click and required no action. But on PL ERM it had a complex flow that unfolds interactively so it took some tinkering.

**2026-04-01 and 2026-04-02**
* Admin: wow, I somehow missed yesterday - just didn't notice. This entry will be for today and yesterday then
* Ermenrich: I started refactoring my ERM scripts, adding ParentContext/OrderContext classes. ERM differs from LVH in some details (e.g. need to confirm shop pickup), but the classes are still pretty universal and a huge help. Currently working on CZ
* Levenhuk: doing some minor edits in case I find something suspicious in the respective ERM script

**2026-03-31**
* Levenhuk: last day of March, and what a day - I finished all my random LVH scripts! 🎉 Added OrderContext class to US script and wrote BG and HU from scratch - thanks to the new class structure, it was easy and fast.
* Ermenrich: these will be probably my next goal. They are a messy lot. Some still sloppy, others in variable degrees of update, a few still throwing small errors - yet all work. But it's pretty annoying to work with these compared to new LVH scripts so I'm thinking this is my next step.

**2026-03-30**
* Levenhuk: debugged PL InPost flow - turned out more complicated than CZ PPL, but seems stable now. Also added TR script (no TR ERM), tested once, will check up thoroughly tomorrow.
* Plans: seems like I'll be done with LVH random scripts within this week. Next step is either to work on LVH choice scripts (will probs take longer as I suspect significant change in OrderContext class) or polish up ERM scripts, still not decided

**2026-03-26**
* Admin: some network/connection issues hindering my scripts. I got API call error that I've never got before. Turned off work VPN - ERM scripts were practically flying...
* Levenhuk: started ES LVH but turns out there is some unclear payment logic (orders over 120 EU paid in cash - TBD?). Left as is, worked on PL LVH (the most difficult script) - but can't test properly due to network issues at the time. 


**2026-03-26**
* Levenhuk: OrderContext already pays off - was able to write LVH CZ (one of the most complicated on LVH!) in < 1 workday, seems stable. Pretty happy with this class
* Ermenrich: also was able to fix the annoying summary error in ERM DE, added OrderClass (first ERM to have it) and cleaned up some more. May leave a few errors still, will check tomorrow

**2026-03-25**
* Admin: getting used to VS Code - it's really more convenient to edit, search, compare etc. Need to learn more about its cool functions
* Levenhuk: seems to finish pilot IT with OrderContext class, added it to DE and EU. Started to see the benefits of better structure/organization! We'll see how it works in other countries with different flows/logic.

**2026-03-24**
* Admin: swtiched to VS Code - search/copy-paste in IDLE works like half of the time
* Levenhuk: still working on IT script and fixing errors (mainly in "express delivery" flow). Not used to working with/debugging scripts that long - good that VS Code lets you open same script in different parts to track the references. Also tried to edit DE V2, but working with 2 long scripts is super overwhelming.

**2026-03-23**
* Levenhuk: finally finished adding OrderContext to IT LVH, it's working. HUGE class, but does look more organized. Will use it as a template for other LVH and ERM scripts.
* Ermenrich: finished cleaning up DE ERM - my sloppy previous edit actually made it harder to fix. Summary throws an error, but I let it be for now (until adding OrderContext)


**2026-03-20** 
* Levenhuk: still working on OrderContext class and its functions, in relation to select_delivery and select_payment. Looks like it gets unnecessary complicated, but I'll evaluate after it starts working 
* Ermenrich: started refactoring DE order, currently not working (wrong selector, "finds no items")
* Admin: hectic day as I got my laptop repaired
  
**2026-03-19**  
* Admin: Created DEVLOG
* Levenhuk: fixing errors in EU, DE V2 on pause - data for fill_order_form() is too messy. Started implementing OrderContext in IT (= the most complicated script). Classes seems difficult and foreign.
* Both: autotests actually made me notice different price formats (delimiters) across our websites. Got approval to unify it to "1 023.95" for US/EU and "1 023,95" for all other websites. Edited scripts accordingly.
