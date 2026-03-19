

<!-- **YYYY-MM-DD**: 
- [Project]: [What I did] 
- [Project]: [What I learned] 
- [Next]: [What's next]-->

2026-03-19  
Created DEVLOG
- Levenhuk: fixing errors in EU, DE V2 on pause - data for fill_order_form() is too messy. Working on implementing OrderContext class, but I started it in IT because it's the most complicated script (will be easy to remove or simplify on EU, DE than add later for IT). Still learning classes, seems super complicated/messy for now.
- Both: autotest actually made me notice that we have different price format (delimiters) across websites. Got approval to unify it to "1 023.95" for US/EU and "1 023,95" for all other websites. Edited scripts accordingly.
