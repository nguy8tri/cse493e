# What was your overall role in the final project? How do you feel about your contributions to the project?

I worked a lot on ideation, the backend, and some of the frontend. 
- I essentially designed parts of the technical flow of the website and the format of the rating system, specifically the categories.
- I made almost all of the backend, which works as a query-able multi-database for restaurants that saves its data in JSON. It also has a simple login mechanism which exchanges login information for tokens used to stand for the user. Its accessible via HTTP requests when the backend is active.
- I converted the initial pages of the frontend into react, and revised the frontend's code. I also made the "Leave a Review" page work, and I also made the login system and context work as well.

# For Accessible Document Creation, besides this document, what did you make accessible?

I think we tend to focus on the product in terms of accessibility. So, for the frontend, there were a few places in the frontend I pointed out or physically made accessible:
- Some href links had unhelpful descriptions (namely heading links), which when read by a screen reader is not very helpful, so I pointed that out when we were initially pointing out the frontend (I had to focus on other work at the time, so unfortunately, I myself did not fix it).
- For the "Leave a Review" page, I'm not sure if this counts, but we used to have a field for leaving the name of the person and the restaurant. However, anyone navigating the pages would not want to fill out those fields as they should be understood by the website. So, I fixed this problem, and that page automatically has context on the person and restaurant that pertains to the review, so that the user has less fields to fill out.

However, I'd like to point out that people with access needs are not just consumers, but also makers and developers as well. Although I myself am not aware of access needs among our team that interfered with the development process, I wanted to make the backend, which was a lot of what I worked on, easier to understand and interact with. I also wanted to make sure my teammates had an easy time understanding the physical code should they need to modify it. Thus:
1. I documented the code very thoroughly, but specifically all the endpoints, within the code itself. I clearly state how to use each endpoint, although I think I should've repeated this information within the [README.md](https://github.com/salmaaalyy/493E-final-project/tree/main/backend) for the backend.
2. I documented, in the [README.md](https://github.com/salmaaalyy/493E-final-project/tree/main/backend) for the backend, how to use the backend from an external perspective, also giving examples of how to access it from a frontend (in TS/JS). This documentation is in Markdown, which happens to be very nice in terms of accessibility.

# For Image Description, include any images you wrote alt text for in this report with their alt text

N/A

# For Plain Language Writing, did you help with the plain language? If so, which plain language writing principals should we use to assess your plain language summary? You don’t need to include the summary itself here, we will look at that on your project web page.

N/A

# Did you help with the disability justice analysis? If so, how?

I did, I revised the 3 analyses to be more specific to each topic.

# Did you help with the Positive Disability Principals analysis? If so, how?

N/A

# When writing the report, did you read and follow class guidelines on GAI use?

N/A