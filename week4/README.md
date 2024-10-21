Accessibility Implementation
==============

# What website/app and task were you testing? 
I chose to modify the (CSE 493 E website)[courses.cs.washington.edu/courses/cse493e/24au/] for this quarter.
![A portion of the cover for CSE 493E website. On the top left is the UW Paul G Allen School logo, and on the top left are 5 navigation buttons. Towards the top of the page is a banner that introduces this page as the syllabus, and also introducing this course as a course to learn how to use accessibility in Computer Science. The content, which is towards the bottom is the beginning of the Syllabus. There are 5 skip links towards the top of the content, then a section that explains why to take this class, and 2 expansion buttons that introduce the course.](website.png "CSE 493 E Website")

# What Accessible Technologies did you use?
## Windows Narrator
- What is it?

It is a screen reader for Windows
- What disabilities does it support?

It supports vision impaired persons
- What are its strengths and/or weaknesses?

It follows conventional keys to navigate a screen on Windows (like tab, down arrow,etc.), but some actions are not very obvious. For instance, when I was trying to figure out how to navigate the slides on the Accessibility Website, I could not figure out how, and no screen reader element told me how.
- What happened when you tried it?

It took a little bit to learn, but I started getting the hang of it. After a bit, I was able to use it to mostly navigate around the CSE 493 E website. I was a bit bummed though that holding down any navigation key (like tab) did not quickly go through everything.
## Windows Magnifier
- What is it?

It is a magnifier for Windows
- What disabilities does it support?

It supports vision impaired persons who are still able to see, but not to a great extent.
- What are its strengths and/or weaknesses?

It is very easy to start up and use. However, trying to zoom in more in the screen might be a problem. To first time users, you have to go to the tiny window it occupies on the screen and press the +/- button to change the zoom. If you hover over the keys, you figure out there are shortcuts for it, but that might not be obvious to everyone.
- What happened when you tried it?
It was very easy to use, I didn't really experience much inconvenience with it. I used it to inspect some images on the CSE 493 E website.
# Summarize the problems you found with the original website/app
The website in general did not have many problems, and neither were they super alarming. I was very impressed by how accessible the website is. But, I found a few small issues:
1. All assignment pages were missing a skip link
2. Low contrast on one of the quote items within the Syllabus FAQ
3. Blurry Image describing Competency-Based Grading, along with an incomplete alt text for it
# Describe what you did to fix them
I will describe my fixes in the order I declared above:
1. I fixed the assignment pages by adding a skip link to all of them. This was simple, since all of them depend on one HTML that defines this skip link
2. I fixed this by shifting that quote item to use the quote block style that all the others used. The difference is that the quote block that had poor contrast now has a much blacker text.
3. I replaced the image with a written description and example of competency-based grading, which also makes it more robust.
# What did you learn when completing this assignment?
I learned a few things:
1. Even when you are experienced at accessible design, you can still make mistakes. I personally have made many mistakes over the assignments concerning accessibility, so I'm happy to see that it truly is a constant learning process.
2. Non-accessible elements can be hard to find. I used my ATs to search through the whole website, and it did take some time to find some of the issues I've identified. I suppose this is why many employers think that accessibility is such a cumbersome task that they end up de-prioritizing.
3. Making an accessible service takes careful work. I was really impressed by how little inaccessible things are in this website. Personally, I would have made a large amount of mistakes, which goes to show that it takes time and care to do things like good alt text, and accessible interactivity.

# Use of GAI
I used GAI to help figure out which WCAG Guidelines I should be targeting for my UARs, but I think that ultimately, I used the good-ol' web for that.

# UARs

## UAR #1: Missing Skip Links
### ID: **SR-Windows Narrator-1**

*(AT=Automatic Tool, SR = Screen Reader, SW=Switch)*

---

### Brief Description:
All Assignment Pages (pages that described each assignment) lacked skip links

### Evidence:
Taking one page as an example, the [AT Around Us](https://courses.cs.washington.edu/courses/cse493e/24au/assignments/finding-accessibility.html) assignment description did not have a skip link.

### Explanation:
This violates [WCAG 2.4.1](https://www.w3.org/WAI/WCAG21/Understanding/bypass-blocks), which states that a there must be a way to get to the main content of a page when starting to navigate it.

---

### Severity Rating (from an accessibility perspective):
2. Minor: Low Priority

### Justification (Frequency, Impact, Persistence):

#### Frequency – Is Problem common or rare? For which types of users?
This problem is common to all assignment description pages. This is a problem for vision-impaired persons that require the use of a screen reader.

#### Impact – Is it hard or easy to overcome this?
It is easy to fix this issue simply by adding a skip link to the HTML for these pages.

#### Persistence – Is there a way to work around this problem? 
It is easy to overcome this, as the user simply needs to tab down to the main content.

### Fix
I fixed this issue by adding a skip link to all the assignment pages. The skip link is now the second element that a screen reader encounters when reading assignment description pages

### Relationships to other problems reported (if relevant):
N/A

## UAR #2: Quote Low Contrast
### ID: **AT-WAVE-2**

---

### Brief Description:
There was low contrast for the following element found in the [Syllabus page](https://courses.cs.washington.edu/courses/cse493e/24au/):
![A block quote found in the Syllabus page of the CSE 493 E website. The content talks about the usefulness of COVID-19 masks. The color of the quote is gray, while the background of the quote is light gray. There is a light gray bar on the left, with a dark gray quote icon also on the left.](quote-before.png)

### Evidence:
*The contrast of 3.09:1 for the text in comparison to the background*

### Explanation:
This violates [WCAG 1.4.3](https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum.html), which stipulates that the contrast must be a ratio of at least 4.5:1.

---

### Severity Rating (from an accessibility perspective): 
2. Minor: Low Priority

### Justification (Frequency, Impact, Persistence):

#### Frequency – Is Problem common or rare? For which types of users?
This problem only occurs here (as far as I could tell). Other block quotes strangely do not suffer from this issue, and appear to have more contrasting text color. This is a problem for color blind users, or for vision-impaired and persons who are not using a screen reader.

#### Impact – Is it hard or easy to overcome this?
It is easy to overcome this, all we need to do is to either change the color of the text directly, or make that block quote the same as the others on the website.

#### Persistence – Is there a way to work around this problem? 
There is. Right above this block quote is a link to an article that contains this exact text. This text is near the top of that article too.

### Fix
I fixed this by changing the block quote style to match the others in this website. It now looks like this:
![A block quote found in the Syllabus page of the CSE 493 E website. The content talks about the usefulness of COVID-19 masks. The color of the quote is a dark gray, while the background of the quote is light gray. There is a light gray bar on the left, with a dark gray quote icon also on the left.](quote-before.png)

### Relationships to other problems reported (if relevant):
N/A

## UAR #3: Problematic Image
### ID: **MAG/SR-Windows Magnifier/Narrator-3**

---

### Brief Description:
An image about competency-based grading has scaling and alt-text issues, and has text in the image.

### Evidence:
The image below does not scale well. There is also text in the image. Finally, the alt text associated with it only reads out the the text on the right hand side of it.
![Describes competency grading. Towards the top left is a visual of a normal grading system, where assignments each fall under some category, and all assignments contribute to the overall grade. On the bottom left is a visual of competency grading, where all assignments are merely evidence of certain competencies. On the right is an explanation of what was just explained, and how competency-based grading shifts the focus to improvement over time, and changes how teachers deal with assignments](compentency-grading.png)

### Explanation:
This violates the following guidelines:
1. [WCAG 1.4.4](https://www.w3.org/WAI/WCAG21/Understanding/resize-text.html), which states that images must be scaled to 200% without loss of functionality.
2. [WCAG 1.4.5](https://www.w3.org/WAI/WCAG21/Understanding/images-of-text), which states that text must be a substitute for images with text if it is better at conveying information.
3. [WCAG 1.1.1](https://www.w3.org/WAI/WCAG22/Understanding/non-text-content.html), which states that images must have an alt-text description that serves the same purpose. Although this is debatable, the example that they have inside the image in my opinion was crucial to my understanding of competency-based grading. I don't think it would be the same if I read only the right hand side.
---

### Severity Rating (from an accessibility perspective):
2. Minor: Low Priority

### Justification (Frequency, Impact, Persistence):

#### Frequency – Is Problem common or rare? For which types of users?
This problem is only present for this image. This is a problem for vision-impaired persons using screen readers.

#### Impact – Is it hard or easy to overcome this?
It will take some work. I was not able to find a better image, and so one would have to make another image, or replace it with actual text.

#### Persistence – Is there a way to work around this problem? 
There is. Above this image is a short description of competency based grading, with a link to an explanation of it in depth.

### Fix
I fixed this by replacing the image with the following text:

---
In a traditional grading scheme, a grade is determined by categories
like Homework, Quizzes, Tests, and such. Any assignment in a class then
falls into these categories. Each category has a weight that contributes
to the overall grade, and so does each assignment. This means that each
assignment impacts your total grade. Below is an example:

|Homework (15%)|Quiz (5%)|Test (80%)|
|--------------|---------|----------|
|HW #1|Quiz #1|Test #1|
|HW #2|Quiz #2|Test #2|
|.......|.......|.......|

But in competency-based grading, your grade is determined by learning goals,
or competency that are set for the class. Any 1 assignment can fall under
multiple competencies. Additionally, only the competencies are used to determine
your final grade (except for participation). Since many assignments fall under a competency
you get multiple chances to prove your skill in a competency. An example of this
system is shown below:

|Competency #1|Competency #2|Competency #3|
|-------------|-------------|-------------|
|Assignment #1|Assignment #1|Assignment #2|
|Assignment #4|Assignment #2|Assignment #3|
|.......|.......|.......|

Let's be more explicit and talk about an example. Consider the following competency and
its corresponding assignments:

Competency #1: For-Loops
- Assignment #1: For-Loops Introduction
- Assignment #2: Quiz on Loops
- Assignment #3: ASCII Art with For-Loops

In the first assignment, you might be rated as "not competent". Let's say though that
you study a bit, and by the second assignment, you are rated as "competent", and then
in the third, you are rated as "excellent". At the end of the quarter, this competency
will be rated as "excellent", and it won't matter that your first assignment was "not
competent" in this competent.

Competency-based grading is thus growth oriented, and teaches that its okay to not
understand a competency in the first assignment, just as long as you can improve in
the next few assignments under that same competency. A beautiful philosophy!

---

### Relationships to other problems reported (if relevant):
N/A

# Appendix

1. Gitlab Repository: [https://gitlab.cs.washington.edu/nguy8tri/undergrad-accessibility-website](https://gitlab.cs.washington.edu/nguy8tri/undergrad-accessibility-website)