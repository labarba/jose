# Author Guidelines

#### Preparing your JOSE submission should be a simple task, once you have a complete software or learning module you wish to publish.

## The two submission types

JOSE accepts two types of submissions: (1) computational learning modules, created as open educational resources (OER), and (2) open-source software, created as educational technology or infrastructure.

### Submission requirements

JOSE submissions must be fully open, under the [Open Definition](http://opendefinition.org). This means that any text content or graphical objects should be under a Creative Commons license (ideally CC-BY) and code components should be under an [OSI-approved license](https://opensource.org/licenses).

Computational learning modules should be complete and immediately usable for self-learning or adoption by other instructors. They should make a clear contribution to teaching and learning of any subject, supported by computing. JOSE is not focused in OER for "learning to code" as much as "coding to learn."

Software submissions should make a clear contribution to the available open-source software that supports teaching and learning, or makes an educational process better (e.g., faster, easier, simpler). Examples include software to auto-grade student work, learning management systems, and student collaboration frameworks. Software should be feature-complete (no half-baked solutions).

### What about novelty?

Authors make the case for their submission's contribution in the paper, under the heading "Statement of Need." The criterion is less one of novelty, than _need_: submissions targeting subjects or applications already addressed by other resources _are eligible_, if the authors make a case for why they might be adopted by learners or other instructors.

### How to prepare a software submission?

Before starting your submission, you should:

* Have the software available in an open repository (GitHub, Bitbucket etc.) under an [OSI-approved license](https://opensource.org/licenses).
* Write a short Markdown file titled `article.md`  with title, author names and affiliations, containing a description of the software, statement of need, and key references. 
* Ideally, also create a metadata file and include it in your repository. We provide a [script](https://gist.github.com/arfon/478b2ed49e11f984d6fb) that generates the metadata automatically.

Once you have those items in place, [submit](http://jose.theoj.org) via the JOSE web app.

### How to prepare a learning-module submission?

Before starting your submission, you should:

* Have the content in an open repository, under a Creative Commons license (ideally CC-BY), and any code components under an OSI-approved license.
* Write a short Markdown file titled `article.md`  with title, author names and affiliations, containing a description of the module, statement of need, and key references. 
* Ideally, also create a metadata file and include it in your repository. We provide a [script](https://gist.github.com/arfon/478b2ed49e11f984d6fb) that generates the metadata automatically.

Once you have those items in place, [submit](http://jose.theoj.org) via the JOSE web app.

### What to include in the paper?

JOSE papers should:

* List all authors and affiliations.
* For software submissions, describe the functionality of the software, usage and recent experience of use in teaching and learning situations. For learning modules, describe the learning objectives, instructional design, and experience of use in teaching and learning situations.
* Include a statement of need, explaining the contribution made by the submitted artifacts to computationally enabled teaching and learning, and describing how they might be adopted by others.
* List key references including a link to the open archive of the sofware or the learning module.

JOSE papers contain a limited set of metadata (see header in the [sample article file]()), plus Summary & Reference sections. We explicitly do not publish long-form articles, because the scholarship represented by a JOSE article is contained in the software or learning modules themselves. Expected length less than 1000 words.


## How will the review proceed?

You should read the [reviewer guidelines]() to help you understand what our reviewers will be looking for. Provided you have followed our pre-submission steps and meet our submission requirements then you should expect the review to proceed at a quick pace.

Review workflow:

* You submit via the JOSE web app.
* A "Pre-review" issue is created in the JOSE reviews repository on GitHub.
* An editor will be assigned by the EiC or will self-assign to your submission. You will suggest an editor in the submission form.
* Editors may enter comments in the "Pre-review" issue while determining that the submission is in-scope for the journal.
* The handling editor will assign one or more JOSE reviewers and create the "Review" issue in our GitHub repository. (At this point, the "Pre-review" issue will be closed.)
* Reviewers will enter comments about the submission in the "Review issue," and authors respond to the comments at will. Reviewers may also open specific issues in the external issue-tracker of the submitted software or content.
* Authors make changes or improvements to the submission, as needed.
* Reviewers will check off each item of the JOSE Review Checklist.
* When the review completes, you will be asked to deposit a full archive of your (updated) repository with a data-archiving service such as Zenodo or figshare. You will update the review issue thread with the DOI for this archive.
* After assignment of a DOI (for the JOSE article), your paper metadata will be deposited in CrossRef, and the published article will be listed on the JOSE website.
