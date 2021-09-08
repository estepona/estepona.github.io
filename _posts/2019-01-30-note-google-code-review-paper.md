---
title: "notes on paper \"Modern Code Review: A Case Study at Google\""
date: 2019-01-30
categories: dev

classes:
  - wide
---

I came across this paper this week and thought it very worth reading. The authors investigated the code review practice at Google and shared some insights.

Click [here](https://storage.googleapis.com/pub-tools-public-publication-data/pdf/80735342aebcbfc8af4878373f842c25323cb985.pdf) to read the original paper.

If you want to grasp the paper is one paragrah, the original paper's conclusion at the bottom provides a great summary.

## key notes
- code review at Google was introduced at the very beginning of the company, and is viewed as one of its core advantages;
- the main purpose of code review is __readability__, then comes education, maintaining norms, gatekeeping, and accident prevention;
- code review at Google is very lightweight: it uses an internal tool called CRITIQUE for basically everything;
- at Google, over 35% of the changes under consideration modify only a single file and about 90% modify fewer than 10 files. Over 10% of changes modify only a single line of code, and the median number of lines modifies is 24. The median change size is significantly lower than other companies such as AMD, Lucent, and Bing;
- at Google, fewer than 25% of changes have more than one reviewer, and over 99% have at most five reviewers with a median reviewer count of 1. Even very large changes on average require fewer than two reviewers;
- code review practice at Google is valued by most developers; 

## original paper's conclusion

Our Study found code review is an important aspect of the development workflow at Google. Developers in all roles see it as providing multiple benefits and a context where developers can teach each other about the codebase, maintain the integrity of their teams' codebases, and build, establish, and evolve norms that ensure readability and consistency of the codebase. Developers reported they were happy with the requirement to review code. The majority of changes are small, have one reviewer and no comments other than the authorization to commit. During the week, 70% of changes are committed less than 24 hours after they are mailed out for an initial review. There characteristics make code review at Google lighter weight than the other projects adopting a similar process. Moreover, we found that Google includes several research ideas in its practice, making the practical implications of current research trends visible.
