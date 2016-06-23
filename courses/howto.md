---
title: How to Create a Course
layout: default
---

## How to create a new course listing

To create a new course page, you will need to fork the GitHub repository at [github.com/byu-cs/byu-cs.github.io](https://github.com/byu-cs/byu-cs.github.io). Following the instructions on the README there will have you installing the required tools and the source code.

Once that is completed, copy the following template as a new file within the `_courses` directory, with the name following this pattern: `cs"$COURSE-NUMBER".md`. For example, if I wanted to create a course for CS 142, I would name the file `cs142.md`. Then fill out the template as necessary, save your work, commit to your forked repository, and then create a pull request on GitHub. You will be notified if it has been accepted, or someone will leave notes on things that should be improved or changed.

---

## Template

```
---
title:  CS $COURSE_NUMBER       // Example: CS 142
name:   $COURSE_NAME            // Example: Intro to Programming
layout: default                 // Leave this one be
---

# {{ page.title }} - {{ page.name }}

## General Information

| Semesters Taught | <!-- Add F,W,Sp,Su or some combo here --> |
| Typical number of sections | <!-- How many sections are there ususally? --> |
| Technologies Used | <!-- What do you use in this course? --> |

## Work Load

### Learning Outcomes

What do you learn in the class?

### Homework

What are the homework-type assignments like?

### Projects

What are the projects like?

If applicable, fill out a table like so:

| Project Number | Name | Description |
| 1 | Hello World / Lab Tutorial | Basic Intro at the lab |

## Reviews

Not sure if we want these, but we could use something like the following:

| Name | John Smith |
| Semester Taken | Fall 2015 | 

Leave remarks here...

Something for people to do? Won't allow for anonymous reviews, but those could be submitted to repo owners for submission...or they could use a throwaway account.

```