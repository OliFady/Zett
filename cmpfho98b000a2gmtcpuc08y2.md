---
title: "When I realized Software Engineering isn’t about writing Code"
seoTitle: "When I realized SW Engineeri isn’t about writing Code"
seoDescription: "When I realized Software Engineering isn’t about writing Code"
datePublished: 2026-05-21T12:50:46.332Z
cuid: cmpfho98b000a2gmtcpuc08y2
slug: when-i-realized-software-engineering-isn-t-about-writing-code
cover: https://cdn.hashnode.com/uploads/covers/6954473169d85e73e2fdb07b/7b3202ce-4fab-429f-a470-eb4e854a2f88.png

---

Graduating from computer science made me imagine spending my future life solving bugs and implementing new features for myself and others. I never in any way imagined myself away from my text editor except for status update meetings or lunch. And then I landed my first engineering job. And boy was it an eye opening ride.

### Perfection meets Reality

I landed a job at a logistics and delivery company, A large domestic logistics company, and for a few months, I really got that hacker feeling for solving bugs, It was a great product too, one I saw through the lens of a junior dev as a perfect one.

Until one day, when the whole tech team was invited to a meeting where everyone was silent. Apparently, someone had dropped some tables from the database, and some of the delivery guys had stopped receiving orders info, so they were called back to the warehouses. Keep in mind that every undelivered order would cost us customers incentives. First thing that comes to mind is restoring the backups, right ? But what if i told you that the backups taken were 4 hours old. Meaning that the orders table still has some missing rows that we know nothing about.

Digging deeper, we found the only solution that would restore all rows. Tracking some relations from other tables, we could confidently guess the missing orders and restore them completely. Ready for the big gotcha ? We would need to restore those records manually. Yes by hand, one row after another. Talk about complex boring SQL queries and manual validation. You would ask how long it took me - yes i took that task partially alone - to restore them ? 15 straight hours !

I barely made it to the standup next day. And of course the company rewarded me with some applause and a voucher. But needless to say, this was my first time realizing two things:

1.  *Code alone won’t save you*.
    
2.  *Perfect systems fail imperfectly*
    

⠀

### One Man Army

When I decided to move to a fintech startup, I was hoping to wear a few hats that will help me grow. Little did I know that I would wear all the hats - no like literally all of them. The first project I got onboarded onto, I had the lucky chance to witness a process without a product manager, just me & the client. for a long time, I despised the job of the product manager. My assumption was, if we truly understood the Problem, then the product manager here only adds friction, as a Junior Engineer I just wanted to code man, leave me be.I was wrong twice here, and let me explain why. My manager used to say a wonderful quote

*common sense isn't that common, most people don't even have it.*

I used to laugh at that quote until I took on that Project alone, I thought the client would know exactly what he wants and I would go on coding that, win-win situation right ? Except it didn’t work that way in reality. As simple as a loan risk calculator app would sound, as much as the client didn’t have the slightest clue of what they want and when is the appropriate time to apply it. So I had to wear the hat of a product manager and act like I care for the product, until surprisingly, I got attached to it. You may say well, so we really don’t need product managers anyway. Well I’m intrigued to tell you that those few months before a product manager was onboarded on the project, were the worst few months of my life. Sleep was a luxury for me as I worked every hour between client meetings and writing the code. Even though we both spoke perfectly sound English, the communication barrier was always there. I’m not really here to debate the importance of a product manager, my point here is this, The more I worked with people, the more I realized that software engineering was never just about writing code. It was about translating ambiguity into something usable. And that ambiguity, more often than not, comes from people rather than machines.

And strangely enough, that’s what made me love engineering even more