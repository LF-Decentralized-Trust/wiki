1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [LFX Issues](LFX-Issues_21457312.html)

# Technical Oversight Committee : LFX Mentorship Platform Issues

Created by Victor Gridnevsky, last modified by Arun .S.M. on Jun 01, 2023

During the candidate selection for the Hyperledger Mentorship process, we faced a number of issues with the LFX Mentorship platform and have a proposal to improve them.

## Registration

The first and largest issue we have faced is the unclear registration process.

Currently, the platform's architecture leads to a lot of extra communication only to replace things that could be handled with manual effort using the platform.

### Mentor’s side

A mentor should see all the hints about his role and capabilities on the platform. The system should also provide hints to ensure everyone related has access to the CVs.

### Mentee’s side

When a mentee registers, they can upload their CV in two ways: one is in their profile, and the other is to submit it to a selected project.  
That leads to having CVs both in the mentorship program list and a mentee’s profile without a good reason.

Moreover, we believe the candidates themselves did not get reminders about uploading their CVs. Some of them provided their data right before the interview, some did not upload them at all.

### Recommended improvements

The LFX platform interface should provide a clear registration workflow for each user category. Instead of making a generic interface that has generic forms fitting both mentees and mentors, LFX should have a simple registration form and a wizard, and then display a message to guide each user category through a more suitable registration process.

If some step is not finished, the site should inform the new member about it. This applies both to access control measures and uploading the CV.

Moreover, the site can send email reminders. It should send daily emails pointing out a CV is missing or that a mentor didn’t fill some details needed to access the CVs.

## Roles

As far as I understand, there are only *Mentor* and *Mentee* roles supported, even though people with other roles might be involved into the process. I am a community manager and there are people besides me, who needed to see the CVs. Therefore, I needed to register as a mentor, which is incorrect.

### Recommended improvements

Ideally, mentors should be able to assign more roles for their colleagues.

## Buggy login system

We recorded the situation when we were logged in, and the tab in the interface that allows us to see the CVs was absent. The mentor user (me) could be displayed as “logged in”, but kind of not logged in in fact. It led to misunderstanding and believing that no one had applied. Specifically, this was the case with Google login, but it may apply to other methods.

### Recommended improvements

Please, fix the bug. The platform should be tested with more attention in order to avoid such a confusing situation.

## Buggy mentee view

When we open the mentorship page and start reviewing the candidates, often enough we see “No tasks currently assigned” while opening some candidate’s data. Page refreshing helps, but we didn’t notice it immediately and it remained as an inconvenience. The broken interface leads to wasted time while we wait for the data that is already there.

### Recommended improvements

Please, fix the bug. **If developers would need more information, we can provide a video.**

## UX: titles

Whatever mentorship project we open on the site, the page title (displayed as a browser tab’s title) is always “Mentorship”. It makes navigation between multiple tabs (and through the browser history) more difficult.

### Recommended improvements

Add a mentorship project name to the page title.

## UX: downloads

When we download a file with a candidate’s CV, it is always renamed to `id.ext` (e.g. `0c09f6ad-424c-4a9b-8de0-5f612c835115-.pdf` in some browsers or `task_file.ext` in others) instead of `candidate-project.ext`. It makes navigating through those CVs and cover letters confusing.

### Recommended improvements

It shouldn’t be hard to assign a more descriptive file name to a downloaded attachment.

## UX: CV links

We need to see CVs and cover letters and share them with colleagues. The easiest way to do so is to have a URL on the site in an accessible way. However, it might be not easy to share just an URL for security and privacy reasons. So, simply sharing files might be a good (but not very convenient) choice.

However, currently this mechanism is broken:

- We open CVs and cover letters as URLs by clicking on download icon buttons which open a new tab
- We cannot get an URL unless we click on the button. So, the URL is hidden behind some JavaScript, and we cannot get it in an *accessible* way when you have a `<a>` tag with the URL, and the browser can help you to work with the link. **It is a bad accessibility practice.**
- Some of URLs are internal (within the LFX platform) and require authentication for access.
- Some of URLs are external (out of LFX) and don’t require any authentication. These links are actually shareable, **but it is a security issue.**

So, we both don’t have URL accessibility and have URLs that sometimes are shareable (which leads to security problems) and sometimes are not.

### Recommended improvements

- Remove magic JavaScript if possible, make URL accessible on the page using `<a href="...">...</a>`
- Fix security issue with unauthenticated access to mentees’ data

## Conclusion

LFX mentorship platform has several major and minor technical and UX issues. Their fixing might make the interaction with the platform easier for mentees, mentors and other accomplices. Thus, it will most probably lead to a higher quality of further mentorship-related activities on the platform.

- Victor Gridnevsky
- Dmitry Balashov
- Aleksandr Petrosyan
- Marin Versic

Document generated by Confluence on Nov 26, 2024 11:24

[Atlassian](http://www.atlassian.com/)
