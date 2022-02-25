# Midterm project individual submission - 02/24/2022

1. Describe your overall satisfaction level with your project results.

   - What went well and what did not?
     - The project went well overall. We started with stand up every day and I broke the user stories into several sub-tasks and put them on board and everyone picked a task they like. We used github project to manage our project so that we could track progress all the time.
       We wrote most of our unit tests after we complete MVP. We were supposed to write unit test as soon as a feature is done or before that.
   - How would you compare the outcome with your vision for the project?
     - We only included core feautres in our MVP so that we could complete it fast and then add more features. We accomplished MVP on Saturday and then we just kept adding more features and tests.

2. Briefly describe your group dynamic for the week.
   - Were there any problems that proved insoluble?
     - We communicated well and if someone was stuck, we always asked team member for help. We didn't get to ask help from TA or instructor during project.
   - Are there any team members you would call out for particular kudos?
     - Shout out to all team members for hard work.
3. Describe at least one difficulty you faced during project week and how you dealt with it. This difficulty could be technical in nature, or interpersonal.
   - One weird problem I faced was got 404 error when I tried to scrape historical stock price data. At first I thought I got wrong url but it was correct url. After research, I found out that yahoo finance website block the request for specific urls such as historical data. If I don't add parameter for header in the request, it assumes I am a bot and block the request. So I added a header parameter in the request and then I got the response that I needed.
4. Describe at least one surprising success or failure you experienced during the week.
   - There were many successes. One of the successes I want to mention is we accomplished our MVP very fast (on Saturday). We defined our MVP small but with core features. After we finished them, we added more features on the board and worked on them one by one.
5. Describe changes you would make to your personal or team process that you can incorporate into your next team effort.
   - One thing I want to do differently next time is to write unit tests and pass them before making a PR for the feature. This is industry standard and also a best practice to follow. I can either write unit tests right after I complete a feature or I can write unit tests first and then work on the feature (TDD).
