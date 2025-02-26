# Courses
Internal courses are offered in a private corporate Learning Management System (LMS).

[Learning Management System (LMS)](#learning-management-system-lms)
1. [Access](#access)
2. [New courses](#new-courses)
3. [Existing courses](#existing-courses)
4. [Author Kit](#author-kit)



## Learning Management System (LMS)
The [LMS](https://agilelablms.talentlms.com/) is a private corporate platform for internal courses. 
When logging on the LMS, every employee can access modular, self-paced courses.

## Access
#### I can't access the LMS. How can I request access?
Access to the [LMS](https://agilelablms.talentlms.com/) is provided to every employee during the [Onboarding](Onboarding.md).

Please open an issue on the [LMS Gitlab repository](https://gitlab.com/AgileFactory/training/lms).
A {% role %}Training/LMS Course steward{% endrole %} will take care of your request and create a user with AgileLearner privileges. For more info, see the guidelines mentioned in the repository's [README](https://gitlab.com/AgileFactory/training/lms/-/blob/master/README.md).

#### How can I access the LMS on company laptop?
- Open a browser and access the LMS at [this](https://agilelablms.talentlms.com/) address.
- On the top right corner, click on the Login button.
- Choose to log in with SAML.

#### Can I access LMS on a personal mobile device (e.g. smartphone)?
- Enroll your personal device as described on [this page](https://handbook.agilelab.it/DeviceEnrollment.html). When prompted, provide Agile Lab office credentials.
This will create a new work partition on your personal device.
- On your personal device, in this newly created work partition,
    - download Edge,
    - open Edge and access the LMS at [this](https://agilelablms.talentlms.com/) address,
    - click on the Login button,
    - sign in with SAML.


### New courses
The [course offering](https://agilelablms.talentlms.com/dashboard/index/role:learner) is continuously updated with new titles.

#### How are new courses created?
Courses are sourced internally. Everybody can share their knowledge and curate content for new courses on [LMS](https://agilelablms.talentlms.com/).

You can:
- volunteer to create a new LMS course. We have time budget to create new courses. See the [Author Kit](#author-kit) section below for more info about creating for new courses, including how to spend time budget.
- request a topic for a new LMS course. You can optionally sponsor somebody else for creating LMS course contents about a topic. Please open an issue on the [LMS Gitlab repository](https://gitlab.com/AgileFactory/training/lms). For more info, see the guidelines in the repository's [README](https://gitlab.com/AgileFactory/training/lms/-/blob/master/README.md).

#### How do LMS Course stewards facilitate course creation?
A {% role %}Training/LMS Course steward{% endrole %} takes care of new course requests. {% role %}Training/LMS Course steward{% endrole %}s are Administrators of the LMS platform. They:
- will answer your questions during the creation of course content, directing you to documentation on this page and [official LMS platform documentation](https://help.talentlms.com/hc/en-us/categories/360001246253-Knowledge-Base),
- will enroll the needed learner group(s) after course content is created and published. More info [here](https://help.talentlms.com/hc/en-us/articles/360014657473-How-to-add-users-to-courses).

#### Are there any rules for course creation?
We have some rules to simplify and standardize the creation of new courses. Please see the [Author Kit](#author-kit) section below.


### Existing courses
The course offering is continuously updated and existing courses are maintained.

#### I have questions about an existing course. What can I do?
You may have issues with a course's content. For example:

- you find test questions confusing,
- in learning material, you don't find all needed information to successfully answer the test questions,
- the information you find in the learning material is outdated or not anymore valid.

If this is your case, please open an issue on the [LMS Gitlab repository](https://gitlab.com/AgileFactory/training/lms) with tags: `kind:hotfix`, `verb:understand`. 
A {% role %}Training/LMS Course steward{% endrole %} will facilitate of your request. For more info, see the guidelines in the repository's [README](https://gitlab.com/AgileFactory/training/lms/-/blob/master/README.md).


### Author Kit

- [Starting this journey](#starting-this-journey)
- [Creating an empty course](#creating-an-empty-course)
- [Adding content](#adding-content)
  - [Course layout essentials](#course-layout-essentials)
  - [Tests](#tests)
- [Reviewing the course](#reviewing-the-course)
    - [Review criteria: Topic](#review-criteria-topic)
    - [Review criteria: Self-paced training](#review-criteria-self-paced-training)
- [Releasing the course](#releasing-the-course)

#### Starting this journey
Welcome to this new journey of creating a new course!

We have time budget to create new courses. You can:
- use **8 hours** of company time to create a new course, 
- find how to track this time on the [Project Time Tracking](ProjectTimesheet.md) page.

Let's get your new course rolling:
Please try accessing "YOUR_COURSE_TOPIC course" on the [LMS Gitlab repository](https://gitlab.com/AgileFactory/training/lms/-/issues?sort=created_date&state=opened). 
- If you can access, please create a new issue with tags: `kind:feature`, `verb:act`, `granularity:work-item`. This will help {% role %}Training/LMS Course steward{% endrole %}s keeping track new course creations on [LMS](https://agilelablms.talentlms.com/). Please post all questions about course creation in this issue. A {% role %}Training/LMS Course steward{% endrole %} will provide support.
- If you can't access [this Gitlab repository](https://gitlab.com/AgileFactory/training/lms), please contact a {% role %}Training/LMS Course steward{% endrole %}s to initiate a conversation about creating a new course. The {% role %}Training/LMS Course steward{% endrole %} will create an issue for you on Gitlab to internally track support requests. 


#### Creating an empty course
Please follow the steps below to create an empty course that is not yet visible to learners:
- Read this [official documentation](https://help.talentlms.com/hc/en-us/articles/360017627173-How-to-create-a-new-course-) about creating a new course.
- Access the LMS in Instructor mode.
- From the LMS homepage, select `New course`.
- On the Add course page, fill in name, category, and description.
- On the Add course page, unflag `Active`. More info [here](https://help.talentlms.com/hc/en-us/articles/360017627173-How-to-create-a-new-course-).
- On the Add course page, flag `Hide courses from catalog`. More info [here](https://help.talentlms.com/hc/en-us/articles/360017627173-How-to-create-a-new-course-).
- On the blue button at the bottom of the page, click on the drop down menu and select `Save and add content`.

> **CAUTION**
>
> In a course page in Instructor mode > `...` , don't `Make the course public`. 
> All internal courses should not be open to the general public.

#### Adding content

##### Course layout essentials
In a nutshell, a course needs to:

- be split in sections. Each section should be self-contained and focus on a well-defined, short topic. This facilitates course consumption. Find out [how to create sections](https://help.talentlms.com/hc/en-us/articles/4405113196178-How-to-use-Sections-in-a-course) on LMS,
- have curated learning material. We have some material to help you get an idea about how to [create course resources](https://help.talentlms.com/hc/en-us/articles/360017465634-How-to-add-content-to-a-course) and [curate quality learning material](https://agilelablms.talentlms.com/unit/view/id:2550),
- have a test for every section. This helps self assessing learners' knowledge on the submodule topic. [Here](https://help.talentlms.com/hc/en-us/articles/360017465794-How-to-add-a-test) you can find how to create tests on LMS.

##### Tests
Tests should have the following configurations:
- the pass score is 70%,
- question and answer shuffle is enabled,
- test retries are always allowed,
- correct answers are shown only when the test scores a passing grade,
- given answers, correct/incorrect labels and score are always displayed after submitting a test,
- moving to next/previous question is enabled.

> **_NOTE_** 
> 
> These configurations are not set by default. 
> This means, you need to set these configurations for each new test you create.

The picture below has the configurations you need:

![TestOptions](images/training-lms-test-options.png)

#### Reviewing the course
Now that you've added curated tests and learning resources to your course, please communicate your course is ready for review to {% role %}Training/LMS Course steward{% endrole %}s. 

A {% role %}Training/LMS Course steward{% endrole %} will facilitate reviewing this course.

In the course review, we want to focus on improving the following:
- presenting the course **topic** clearly, so that the learner doesn't have false expectations,
- reproducing learner-teacher dialogue and close feedback loop with the capabilities of our LMS platform, so that we can achieve **self-paced training** that is both effective and enjoyable for the learner.

To achieve this, a {% role %}Training/LMS Course steward{% endrole %} will give you feedback and - if needed - propose clear actions for improving the course. Feedback will be based on the following review criteria.

##### Review criteria: Topic
- [ ] Learning takeaways are self-contained around a well defined core topic. 
- [ ] This topic is clearly identified in the title.
- [ ] This topic is clearly identified in the description.
- [ ] The topic scope defined in title and description matches the learning material (learning resources and quizzes).

##### Review criteria: Self-paced training
- [ ] Learning materials are modular and bite-sized to enable self-paced training.
- [ ] The course is structured in sections.
- [ ] Each section focuses on a sub-topic. This subtopic can be clearly identified.
- [ ] Each section has curated learning resources.
- [ ] A question is provided at the end of most learning resources (formative assessment).
- [ ] In each section, a quiz is provided in form of a test resource (summative assessment).
- [ ] Each quiz has at least 2 curated questions.
- [ ] Quiz questions cover all the key learnings in the given section.
- [ ] If the course has 2+ sections, a final quiz is provided (summative assessment).
- [ ] The final quiz has at least 1 question from each section.
- [ ] All test resource settings enable repetition, moving between questions, reasonable pass threshold. These setting need to be configured for all test resources (quizzes and final quiz). Find [here](#tests) a tutorial about how to achieve this.
- [ ] Assessments provide question feedback for [DOK 2 or higher](https://www.edutopia.org/article/how-use-norman-webb-depth-of-knowledge) (example: complex scenario-based questions) questions.


#### Releasing the course
A course is ready to release when the [review criteria](#reviewing-the-course) are met. 

A {% role %}Training/LMS Course steward{% endrole %} releases the course after the review is successfuly completed.

> Thanks for taking the time to share knowledge and contributing to the LMS!

##### Release checklist for the LMS Course Steward

> **CAUTION**
>
> In a course page in Instructor mode > `...` , don't `Make the course public`. 
> All internal courses should not be open to the general public.

Please follow the steps below:
1. add a resource to collect learner feedback using [this](https://gitlab.com/AgileFactory/training/lms/-/blob/master/lms-ops/learner-feedback-resource.md) template,
2. add the needed learner group(s) (see [here](https://help.talentlms.com/hc/en-us/articles/360014657473-How-to-add-users-to-courses)), 
3. make a course visible for the intended learners:
  - Access the LMS in Instructor mode.
  - In the course page > Edit Course > Course tab, flag `Active`. More info [here](https://help.talentlms.com/hc/en-us/articles/360017627173-How-to-create-a-new-course-).
  - In the course page > Edit Course > Course tab, unflag `Hide courses from catalog`. This will publish the course in the LMS homepage. More info [here](https://help.talentlms.com/hc/en-us/articles/360017627173-How-to-create-a-new-course-).
  - In a course page in Instructor mode > `...` , select `Lock course content`. More info [here](https://help.talentlms.com/hc/en-us/articles/360021501300-How-to-not-allow-the-content-to-be-edited-).
4. publish a message with the course link in the `BigData > training` channel on Teams.
