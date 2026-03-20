

<!-- **YYYY-MM-DD**: 
- [Project]: [What I did] 
- [Project]: [What I learned] 
- [Next]: [What's next]-->
**2026-03-20** 
* Levenhuk: still working on OrderContext class and its functions, in relation to select_delivery and select_payment. Looks like it gets unnecessary complicated, but I'll evaluate after it starts working 
* Ermenrich: started refactoring DE order, currently not working (wrong selector, "finds no items")
* Overall: hectic day as I got my laptop repaired
* 
**2026-03-19**  
Created DEVLOG
* Levenhuk: fixing errors in EU, DE V2 on pause - data for fill_order_form() is too messy. Started implementing OrderContext in IT (= the most complicated script). Classes seems difficult and foreign.
* Both: autotests actually made me notice different price formats (delimiters) across our websites. Got approval to unify it to "1 023.95" for US/EU and "1 023,95" for all other websites. Edited scripts accordingly.
