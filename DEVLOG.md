

<!-- **YYYY-MM-DD**: 
- [Project]: [What I did] 
- [Project]: [What I learned] 
- [Next]: [What's next]-->
**2026-04-02**
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
