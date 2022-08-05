# Ashley Design System Issues

This is a Repo for submitting issues or large changes to the Ashley Design System. This Repo is meant to capture all types of issues and changes from simple technical problems to design overhauls. 

## Links
- [Ashley Design System Storybook](https://storybook.dev.ashleyretail.com/)  *requires connection to the company firewall*
- [Ashley Design System Repo](https://dev.azure.com/ashleyfurniture/eComm%203/_git/MFE%20-%20Core)

## Requesting Access

If you need access to the Repository or Azure Boards please send an email to [Robert Bengtson](mailto:RBengtson@ashleyfurniture.com)

## Submitting Issues

When opening a new issue, always make sure to fill out the issue template. This step is very important! Not doing so may result in your issue not being managed in a timely fashion. Don't take this personally if this happens, and feel free to open a new issue once you've gathered all the information required by the template.

- One issue, one bug: Please report a single bug per issue.
- Provide reproduction steps: List all the steps necessary to reproduce the issue. The person reading your bug report should be able to follow these steps to reproduce your issue with minimal effort. If possible, use the REPL to create your reproduction.
- For small design issues, IE changing a color of one color token, or slighly rearanging a component. Please include information on why the change is necessary and, design mockups to illustrate your point.

## Submitting RFCs

RFCs are a place to discuss major changes to the Design System — where 'major' implies significant changes either to public interfaces or internal implementation details, particularly those that could be controversial or involve breaking changes.

An example of an RFC would be
- Completely changing the Design Tokens changing all the colors or renaming the tokens themselves.
- Redesigning the Header or Footer
- Removing a Component

Most changes don't need to go through the Request for Comments (RFC) process and can rely on issues.

A huge part of the value on an RFC is defining the problem clearly, collecting use cases, showing how others have solved a problem, etc. Coming up with a design is very iterative and only one part of the process. An RFC can provide tremendous value without the design described in it being accepted.

The is inspired by (which is to say shamelessly ripped off from) the RFC process adopted by React, Ember and others. The process itself is subject to change (or even abandonment!) as we gain experience with it.


## The process

* Fork the AshleyDesignSystem repo https://github.com/bertybot/AshleyDesignSystem
* Copy 0000-template.md to text/0000-my-feature.md (where 'my-feature' is descriptive. Don't assign an RFC number yet).
Fill in the RFC. Put care into the details: **RFCs that do not present convincing motivation, demonstrate understanding of the impact of the design, or are disingenuous about the drawbacks or alternatives tend to be poorly-received.**
* Submit a pull request. As a pull request the RFC will receive design feedback from the larger community, and the author should be prepared to revise it in response.
* Build consensus and integrate feedback. RFCs that have broad support are much more likely to make progress than those that don't receive any comments.
* Eventually, the team will decide whether the RFC is a candidate for inclusion in the Ashley Design System.
RFCs that are candidates for inclusion in the Design System will enter a "final comment period" lasting 3 calendar days. The beginning of this period will be signaled with a comment and tag on the RFCs pull request.
* An RFC can be modified based upon feedback from the team and community. Significant modifications may trigger a new final comment period.
An RFC may be rejected by the team after public discussion has settled and comments have been made summarizing the rationale for rejection. A member of the team should then close the RFCs associated pull request.
* An RFC may be accepted at the close of its final comment period. A team member will merge the RFCs associated pull request, at which point the RFC will become 'active'.


## The RFC life-cycle

Once an RFC becomes active, then authors may implement it and submit the feature as a pull request to the [Ashley Design System repo](https://dev.azure.com/ashleyfurniture/eComm%203/_git/MFE%20-%20Core). Becoming 'active' is not a rubber stamp, and in particular still does not mean the feature will ultimately be merged; it does mean that the core team has agreed to it in principle and are amenable to merging it.

Furthermore, the fact that a given RFC has been accepted and is 'active' implies nothing about what priority is assigned to its implementation, nor whether anybody is currently working on it.

Modifications to active RFCs can be done in followup PRs. We strive to write each RFC in a manner that it will reflect the final design of the feature; but the nature of the process means that we cannot expect every merged RFC to actually reflect what the end result will be at the time of the next major release; therefore we try to keep each RFC document somewhat in sync with the language feature as planned, tracking such changes via followup pull requests to the document.


## Implementing an RFC

The author of an RFC is not obligated to implement it. Of course, the RFC author (like any other developer) is welcome to post an implementation for review after the RFC has been accepted.

If you are interested in working on the implementation for an 'active' RFC, but cannot determine if someone else is already working on it, feel free to ask (e.g. by leaving a comment on the associated issue).


## Reviewing RFCs

We tend to do our thinking informally, in the open, when time allows. There are a large number of community members relative to a small number of a core contributors who have many responsibilities. You can help ensure your RFC is reviewed in a timely manner by putting in the time to think through the various details discussed in the template. It doesn't scale to push the thinking onto a small number of core contributors. If reviewers raise an issue, don't dismiss it as irrelevant, but take the time to provide examples or data explaining it and coming up with ways that the design might be changed in response. Sometimes answering a single question can be very time consuming (such as setting up a benchmark), but discussions tend to stall out if concerns don't get thoroughly addressed.

