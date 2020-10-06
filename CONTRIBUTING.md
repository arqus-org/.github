# Contributing to KooQit!
We want to make contributing to this project as easy and transparent as possible, whether it's:

- Reporting a bug
- Discussing the current state of the code
- Submitting a fix
- Proposing new features

We encourage and appreciate your contributions and will be more than happy to integrate them in the project. 🚀

## Table of Contents
- [Contributing to KooQit!](#contributing-to-kooqit)
  - [Table of Contents](#table-of-contents)
  - [Project Management](#project-management)
  - [Workflow](#workflow)
    - [Quick Reference](#quick-reference)
    - [General Guidelines](#general-guidelines)
    - [Issues](#issues)
    - [Commits](#commits)
    - [Pull/Merge requests](#pullmerge-requests)
    - [Branch Naming](#branch-naming)
    - [Example Workflows](#example-workflows)
      - [Propose a new feature](#propose-a-new-feature)
      - [Fix an existing bug (i.e. GitHub issue #12)](#fix-an-existing-bug-ie-github-issue-12)
  - [References](#references)

## Project Management
KooQit! organisation uses GitHub to host code, track issues and handle feature requests, as well as accept pull requests.

SCRUM methodology principles are followed applying the following mapping between Agile Concepts and GitHub: 

<table>
  <thead>
    <tr>
      <th>SCRUM Agile Concept</th>
      <th>GitHub Concept</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Sprint</td>
      <td>Milestone</td>
    </tr>
    <tr>
      <td>User Stories</td>
      <td>Issues</td>
    </tr>
    <tr>
      <td>Epics</td>
      <td>Projects</td>
    </tr>
    <tr>
      <td>Product Backlog</td>
      <td>Issues without Milestone</td>
    </tr>
    <tr>
      <td>Sprint Backlog</td>
      <td>Issues with Milestone</td>
    </tr>
  </tbody>
</table> 


## Workflow

### Quick Reference

<table>
  <thead>
    <tr>
      <th>Instance</th>
      <th>Branch</th>
      <th>Description, Instructions, Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Stable Product</td>
      <td>`main`</td>
      <td>Accepts merges from `topic/*` and `fix/*`</td>
    </tr>
    <tr>
      <td>General Enhancement</td>
      <td>`topic/*`</td>
      <td>Always branch off latest version of `main`</td>
    </tr>
    <tr>
      <td>Patches / Fixes</td>
      <td>`fix/*`</td>
      <td>Always branch off latest version of `main`</td>
    </tr>
  </tbody>
</table>

### General Guidelines

[GitHub Flow](https://guides.github.com/introduction/flow/) serves as reference for the branching workflow applied for this project.

Pull requests should be used to propose changes to the codebase.

Any significant change to the code should start with an issue that describes the goal. Having a reason for every code change helps to inform the rest of the team and to keep the scope of a feature branch small.

The issue title should describe the desired state of the system. For example, the issue title “As an administrator, I want to remove users without receiving an error” is better than “Admin can’t remove users.” 

### Issues
Please apply the following rules when opening an issue :

* Check for duplicate
* Each bug or feature request should be documented in its own issue.
* If applicable, use templates (i.e. New Feature, Bug report, ...)
* Use a short but specific title (i.e `Search errors on 50-character submit` instead of `Search input causes error when you type over 50 characters and press enter`)
* Tag your issue with appropriate `theme` and `type` tags if available


### Commits

A commit message should reflect your intention, not just the contents of the commit. It is easy to see the changes in a commit, so the commit message should explain why you made those changes. An example of a good commit message is: `Combine templates to reduce duplicate code in the user views.` The words "change," "improve," "fix," and "refactor" don’t add much information to a commit message. For example, `Improve XML generation` could be better written as `Properly escape special characters in XML generation.`

Please, if applicable, __reference issues__ related to your commits.

### Pull/Merge requests
The following points are to be considered before/when opening a merge request:

__Document / test all the things__

Please make sure to document and comment your work before submitting a merge request.

If applicable, your code should be tested as well.

Merge requests containing __undocumented work will unfortunately be rejected__.

__Link to issues__

Everything in the title. Please make sure to link any issue solved buy the pull requests.


__If not ready, tag it as "Work In Progress"__

If you open a merge request but do not assign it to anyone, it is a "Work In Progress" merge request. These are used to discuss the proposed implementation but are not ready for inclusion in the `main` branch yet. Start the title of the merge request with `[WIP]`: to prevent it from being merged before it’s ready. 

### Branch Naming
The accepted branch name convention is the following : `<token-prefix>/<short-description>`
<table>
  <thead>
    <tr>
      <th>Token Prefix</th>
      <th>Use case</th>
      <th>Examples</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>`topic`</td>
      <td>Propose a new feature, refactoring and/or cleaning work</td>
      <td>`topic/oauth-integration` `topic/mysupertool-scans-import` `topic/clean-root-readme` `topic/refactor-users-service`</td>
    </tr>
    <tr>
      <td>`fix`</td>
      <td>Patches, and security issues (Both bug and hot fixes)</td>
      <td>`fix/root-readme-typos` `fix/fix-csrf`</td>
    </tr>
  </tbody>
</table> 

### Example Workflows

#### Propose a new feature

1. [Create an issue](https://github.com/vulnlabs-org/vulnlabs/issues/new) in the repository
2. Fork the repo and create your branch (i.e. `topic/oauth-integration`) from `main`
  
  `git checkout main && git checkout -b topic/branch-topic`

3. Code
4. If you've added code that should be tested, add tests
5. Ensure your work is documented
6. Ensure the test suite passes
7. Make sure your code lints
8. Commit your work (Make sure to reference any related issue in the commit message)
9.  Issue a pull request against `main`
   
#### Fix an existing bug (i.e. GitHub issue #12)
1. [Create an issue](https://github.com/vulnlabs-org/vulnlabs/issues/new) in the repository
2. Fork the repo and create your branch (`fix/issue-12`) from `main`
    
    `git checkout main && git checkout -b topic/branch-topic`

3. Code
4. If you've added code that should be tested, add tests
5. Ensure your work is documented
6. Ensure the test suite passes
7. Make sure your code lints
8. Commit your work (Make sure to reference issue #12 in the commit message)
9. Issue a pull request against `main`

## References 
* [Understanding the GitHub Flow - GitHub Docs](https://guides.github.com/introduction/flow/)
* [About collaborative development models - GitHub Docs](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-collaborative-development-models)
* [Merging VS Rebasing - Atlassian](https://www.atlassian.com/git/tutorials/merging-vs-rebasing)
* [Managing Work on GitHub > Copying a project board - GitHub Docs](https://docs.github.com/en/github/managing-your-work-on-github/copying-a-project-board)