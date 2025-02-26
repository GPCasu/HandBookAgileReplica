# How we use the guide every day

1. Most guidelines in this handbook are meant to help, and unless otherwise stated, are meant to help more than being absolute rules. Don't be afraid to do something because you don't know the entire handbook, nobody does. Be gentle when reminding people about these guidelines. For example say, "It is not a problem, but next time please consider the following guideline from the handbook."

2. If you ask a question and someone answers with a link to the handbook, they do this because they want to help by providing more information. They may also be proud that we have the answer documented. It doesn't mean that you should have read the entire handbook, nobody knows the entire handbook.

3. If you need to ask a team member for help, please realize that there is a good chance the majority of the community also doesn't know the answer. Be sure to document the answer to radiate this information to the whole community. After the question is answered, discuss where it should be documented and who will do it. You can remind other people of this request by asking "Who will document this?"

4. When you discuss something in chat always try to link to a URL where relevant. For example, the documentation you have a question about or the page that answered your question. You can remind other people of this by asking "Can you please link?"

5. Remember, the handbook is not what we hope to do, what we should formally do, or what we did months ago. It is what we do right now. Make sure you change the handbook in order to truly change a process. To propose a change to a process, make a merge request to change the handbook. Don't use another channel to propose a handbook change (email, Google Doc, etc.).

6. The handbook is the process. Any sections with names like 'process', 'policies', 'best practices', or 'standard operating procedures' are an indication of a deeper problem. This may indicate a duplication between a prose description of a process and a numbered list description of the same process that should be combined in one description of the process.

7. When communicating something always include a link to the relevant (and up-to-date) part of the handbook instead of including the text in the email/chat/etc. You can remind other people of this by asking "Can you please link to the relevant part of the handbook?"

8. Everyone should subscribe to the #handbook channel to stay up-to-date with changes to the handbook

9. All the information of the handbook are automatically valid also for all the consuntants, contractors and freelance, unless otherwise specified. Since we consider them just as part of the team and the company like any other "regular" employee. Obviously, we expect them to embrace AgileLab's values and processes

# How to change or define a process

1. To change a guideline or process, suggest an edit in the form of a merge request. When you hear about a good idea, you can remind other people of this by asking "Can you please send a merge request for the handbook?"

2. Keeping up with changes to the Handbook can be difficult, please follow the commit subject guidelines with a particular focus on your merge request's title, to ensure someone reading the Handbook Changelog can quickly understand the MR's content.

3. Communicate process changes by linking to the merged diff (a commit that shows the changes before and after). If you are communicating a change for the purpose of discussion and feedback, it is ok to link to an unmerged diff. Do not change the process first, and then view the documentation as a lower priority task. Planning to do the documentation later inevitably leads to duplicate work communicating the change and it leads to outdated documentation. You can remind other people of this by asking "Can you please update the handbook first?"

4. Like everything else, our processes are always in flux. Everything is always in draft, and the initial version should be in the handbook, too. If you are proposing a change to the handbook, whenever possible, skip the issue and submit a merge request. (Proposing a change via a merge request is preferred over an issue description). Mention the people that affected by the change in the merge request. In many cases, merge requests are easier to collaborate on since you can see the proposed changes.

5. If something is a limited test to a group of users, add it to the handbook and note as such. Then remove the note once the test is over and every case should use the new process.

6. If someone inside or outside AgileLab makes a good suggestion invite them to add it to the handbook. Send the person the URL of the relevant page and section and offer to do it for them if they can't. Having them make and send the suggestion will make the change and will reflect their knowledge.

7. When you submit a merge request, make sure that it gets merged quickly. Making single, small changes quickly will ensure your branch doesn't fall far behind master, creating merge conflicts. Aim to make and merge your update on the same day. Mention people in the merge request or reach them via Teams. If you get a suggestion for a large improvement on top of the existing one consider doing that separately. Create an issue, get the existing MR merged, then create a new merge request.

8. Try to add the why of a handbook process, what is the business goal, what is the inspiration for this section. Adding the why makes processes easier to change in the future since you can evaluate if the why changed.

# Style guide and information architecture

1. Single Source of Truth: think about the information architecture to eliminate repetition and have a Single Source of Truth (SSoT). Instead of repeating content cross-link it (each text has a hyperlink to the other piece). If you copy content please remove it at the origin place and replace it with a link to the new content. Duplicate content leads to having to update it in multiple changes, which is a lot of work and very easy to forget. If you forget one of the pieces of content is out of date.

2. Make sure to always cross-link items if there are related items (elsewhere in the handbook, in docs, or in issues).

3. Avoid unstructured content based on formats like FAQs, lists of links, resource pages, glossaries, courses, videos, tests, or how-to's. These are very hard to keep up-to-date and are not compatible with organization per function and result.

4. Instead, put the answer, link, definition, course, video, or test in the most relevant place. Use descriptive headers so that people can easily search for content 

# Management

It is each department and team member's responsibility to ensure the handbook stays current. People Operations Specialists will partner with a representative from each department (engineering, marketing, etc). For questions on who to submit a merge request to, or assistance with the handbook, please reach out on the `BigData/handbook` Teams channel.
If you need permissions to directly merge changes to the handbook, please submit a New Access Request issue and follow the process for access approval.
Any changes to the handbook as part of this review will be shared in the `BigData/handbook` Teams channel.

# Make it worthwhile

There are many occasions where something is documented in the knowledge base, but people don't know about it because they never bothered to read or search. Some people have a strong aversion against what they perceive as a 'wall of text'.
To ensure that people's time is well spent looking at the handbook we should follow the 'handbook guidelines' above, and also:
* Follow the writing style guide
* Have a great search function
* Test people on their knowledge during onboarding
* Give real examples
* Avoid corporate speak, describe things like you're talking to a friend

# Pay attention to privacy and confidentiality

Remember that the handbook is public and also merge requests are, then please do not share sensitive information like people's identity, financial data, etc.

# How to locally test a Merge Request

It could be useful to test the proposed changes on the Handbook before a MR is marked as "Ready to review". This is especially useful if the MR contains a complex Markdown structure that could not potentially be what you expect. 

It's pretty easy to setup your local environment. In this guide we will assume you are using Ubuntu.

Prerequisite: npm. If you do not have it, run `sudo apt install npm` or search the installation command for your OS.

```
# Setup the project environment. This should be done ONLY ONCE. It may require `sudo`
npm install

```

This will install all the dependencies and plugins used within the HonKit book.

Finally, locally start your Honkit instance:

```
# Exposes locally on http://localhost:4000 your gitbook
npm run serve
```

Everytime you make a change in your project, it will automatically refresh the web address with the new content.

# Plugins

## Holaspirit
When mentioning a company's role (e.g. Certification Coach) make sure you link it to the Holaspirit page of the role. 
To do that our Handbook uses our own Holaspirit plugin. Check the **usage** section of this [page](https://github.com/agile-lab-dev/honkit-plugin-holaspirit#readme) to know how to create a role mention.

There is no need to link every single role mention of the same role in the same page, just link the most significant one (usually at the bottom of the page). 
For instance: if I mention *Certification Coach* for 5 times inside the same page, I will create a Holaspirit link only once.


