# Editor's Guide

The Journal of Open Source Education (JOSE) conducts all peer review and editorial processes in the open, on the GitHub issue tracker.

## Pre-review

Once a submission comes in, it will be in the queue for a quick check by the Editor-in-chief (EiC). From there, it moves to a PRE-REVIEW issue, where the EiC will assign a handling editor, and the author can suggest reviewers. Initial direction to the authors for improving the paper can already happen here, especially if the paper lacks some requested sections.

**If the paper is out-of-scope for JOSE, editors assess this and notify the author in the PRE-REVIEW issue.**

The EiC assigns an editor (or a volunteering editor self-assigns) with the command `@whedon assign @username as editor` in a comment. 

At that point, the handling editor's job is to identify reviewer(s). We'd like to have two reviewers per submission. If the editor is comfortable with their own assessment of the submission, one reviewer may be sufficient. If the editor feels particularly unsure of the submission, maybe a third reviewer can be recruited.

To recruit reviewers, the handling editor could first ping candidates on Twitter, or mention them in the PRE-REVIEW issue with their GitHub handle. After expressing initial interest, they may need a longer explanation via email. See sample reviewer invitation email, below.

Once a reviewer accepts, the handling editor issues the command `@whedon assign @username as reviewer` in the PRE-REVIEW issue.

Next, run the command `@whedon start review magic-word=bananas`. If you forget the magic word, `@whedon` will remind you. This will open the REVIEW issue, with a prepared review checklist, and instructions for reviewers. The editor should close the PRE-REVIEW issue, at this point, and move the conversation to the separate REVIEW issue. You can now close the PRE-REVIEW issue.

## Review

In the REVIEW issue, new reviewers can be added with the command `@whedon add @username as reviewer`. If a reviewer recants their commitment or is unresponsive, remove them with the command `@whedon remove @username as reviewer`.

The REVIEW issue contains some instructions, and a reviewer checklist. The reviewer(s) should check off items of the checklist one-by-one, until done. In the meantime, reviewers can engage the authors freely in a conversation aimed at improving the paper. 

Comments in the REVIEW issue should be kept brief, as mush as possible, with more lengthy suggestions or requests posted as separate issues, directly in the submission repository. A link-back to those issues in the REVIEW is helpful.

When the reviewers are satisfied with the improvements, we ask that they confirm a recommendation to accept the submission. 

## After acceptance

When a submission is accepted, we ask that the authors create an archive (on Zenodo, figshare, or other) and post the archive DOI in a the REVIEW issue. The editor should add the "accepted" label on the issue, run the command `@whedon set <archive doi> as archive`, and ping the EiC for final processing.

## Sample letter to invite reviewers

Dear Dr. Jekyll,

I found you following links from the page of The Super Project and/or on Twitter. This message is to ask if you can help us out with a submission to JOSE (The Journal of Open Source Education), where I’m editor.

JOSE publishes two types of articles, describing either:

* open educational software tools, or
* open-source learning modules

The submission I'd like you to review is titled:
*"great—how everyone learns"*

and the submission repository is at:
`https://github.com/< … >`

JOSE is a free, open-source, community driven and educator-friendly online journal (no publisher seeking to make revenue from the volunteer labor of researchers!). 

The review process at JOSE is unique: it is open and author-reviewer-editor conversations are encouraged.

JOSE reviews involve downloading and installing the artifacts, and inspecting the repository for key elements. See
http://joss.theoj.org/about#reviewer_guidelines

Editors and reviewers post comments on the REVIEW issue, and authors respond to the comments and improve their submission until acceptance (or withdrawal, if they feel unable to satisfy the review).

Would you be able to review the `great` submission for JOSE?
Or, if not, could you recommend someone from your team to help out?

Kind regards,

JOSE Editor.
