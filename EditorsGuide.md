# Editor's Guide

The Journal of Open Source Education (JOSE) conducts all peer review and editorial processes in the open, on the GitHub issue tracker.

Editors will manage the review workflow with the help of our bot, `@whedon`.
The bot is summoned with commands typed directly as comments in the GitHub issues.
For a list of commands, type: `@whedon commands` (Also listed below.)

## Pre-review

Once a submission comes in, it will be in the queue for a quick check by the Editor-in-chief (EiC). From there, it moves to a PRE-REVIEW issue, where the EiC will assign a handling editor, and the author can suggest reviewers. Initial direction to the authors for improving the paper can already happen here, especially if the paper lacks some requested sections.

**If the paper is out-of-scope for JOSE, editors assess this and notify the author in the PRE-REVIEW issue.**

The EiC assigns an editor (or a volunteering editor self-assigns) with the command `@whedon assign @username as editor` in a comment. 

At that point, the handling editor's job is to identify reviewer(s). We'd like to have two reviewers per submission. If the editor is comfortable with their own assessment of the submission, one reviewer may be sufficient. If the editor feels particularly unsure of the submission, maybe a third reviewer can be recruited.

To recruit reviewers, the handling editor could first ping candidates on Twitter, or mention them in the PRE-REVIEW issue with their GitHub handle. After expressing initial interest, candidate reviewers may need a longer explanation via email. See sample reviewer invitation email, below.

Once a reviewer accepts, the handling editor runs the command `@whedon assign @username as reviewer` in the PRE-REVIEW issue.
Add more reviewers with the command `@whedon add @username as reviewer`. 

Next, run the command `@whedon start review magic-word=bananas`. If you forget the magic word, `@whedon` will remind you. This will open the REVIEW issue, with prepared review checklists for each reviewer, and instructions. The editor should close the PRE-REVIEW issue, at this point, and move the conversation to the separate REVIEW issue.

## Review

The REVIEW issue contains some instructions, and reviewer checklists. The reviewer(s) should check off items of the checklist one-by-one, until done. In the meantime, reviewers can engage the authors freely in a conversation aimed at improving the paper. 

If a reviewer recants their commitment or is unresponsive, editors can remove them with the command `@whedon remove @username as reviewer`.
You can also add new reviewers in the REVIEW issue, but in this case, you need to manually add a review checklist for them.

Comments in the REVIEW issue should be kept brief, as mush as possible, with more lengthy suggestions or requests posted as separate issues, directly in the submission repository. A link-back to those issues in the REVIEW is helpful.

When the reviewers are satisfied with the improvements, we ask that they confirm their recommendation to accept the submission. 

## After acceptance

When a submission is accepted, we ask that the authors create an archive (on Zenodo, figshare, or other) and post the archive DOI in the REVIEW issue. The editor should add the "accepted" label on the issue, run the command `@whedon set <archive doi> as archive`, and ping the EiC for final processing.

## Sample letter to invite reviewers

Dear Dr. Jekyll,

I found you following links from the page of The Super Project and/or on Twitter. This message is to ask if you can help us out with a submission to JOSE (The Journal of Open Source Education), where I’m an editor.

JOSE publishes two types of articles, describing either:

* open educational software tools, or
* open-source learning modules

The submission I'd like you to review is titled:
*"great—how everyone learns"*

and the submission repository is at:
`https://github.com/< … >`

JOSE is a free, open-source, community driven and educator-friendly online journal (no publisher is seeking to raise revenue from the volunteer labor of researchers!). 

The review process at JOSE is unique: it is open and author-reviewer-editor conversations are encouraged.

JOSE reviews involve downloading and installing the artifacts, and inspecting the repository and submitted paper for key elements. See
http://joss.theoj.org/about#reviewer_guidelines

Editors and reviewers post comments on the Review issue, and authors respond to the comments and improve their submission until acceptance (or withdrawal, if they feel unable to satisfy the review).

Would you be able to review this submission for JOSE?
If not, could you recommend someone from your team to help out?

Kind regards,

JOSE Editor.


## Editor workflow

1. An author submits a paper. They can select or not select an editor. The EiC starts the workflow, which opens the PRE-REVIEW issue.

2. If you are selected as an editor you get @-mentioned in the PRE-REVIEW issue. 
This doesn’t mean that you’re the editor, just that you’ve been suggested by the author. The EiC can assign another handling editor, if you're unable to serve.

3. Submissions without an editor will show up in the weekly 
digest email under the category ‘Papers currently without an editor.’ Please review this weekly email and volunteer to edit papers. 
If you choose to be an editor, run the command `@whedon assign @yourusername as editor` in the submission's PRE-REVIEW issue.

4. Once you are the editor, find the link to the submission's repository in the PRE-REVIEW issue. Inspect the materials submitted and check if
    * the materials are described in a README file
    * the materials are within scope for the journal
    * they are openly licensed: OSI-approved license for code, Creative Commons license for other content
    * the paper includes the requested content

6. Post a response to the author saying that things look in line (or not) and start search for reviewer(s).

    * use the list of reviewers in the Google [spreadsheet](https://bit.ly/jose-reviewers);  to chose reviewer(s) from list, you can @-mention them on the issue and ask them to serve;
    * or solicit reviewers outside the list: use Twitter, and/or send an email to people describing JOSE and asking if they would be interested in reviewing.

8. Assign reviewer(s) with `@whedon assign @username as reviewer` and `@whedon add @username as reviewer`.

9. Create the REVIEW issue with `@whedon start review` (it gets automatically populated with one checklist per reviewer).
    
10. Close the pre-review issue.

11. Review: The reviewer has a conversation with the author to improve the submission, and requests changes as necessary. 
The editor lurks on this conversation and participates as needed for questions (or CoC issues).
The author makes changes to the submission and reports. Everyone agrees it’s ready.

12. The author makes an archive of the submitted materials and posts the archive DOI.

13. Editor runs `@whedon assign <doi> as archive` and pings the EiC (@labarba) to get the paper published.

13. Celebrate publication! Tweet! Thank reviewers! Say thank you on the issue!


**Whedon commands**

```# List all of Whedon's capabilities
@whedon commands

# Assign a GitHub user as the reviewer of this submission
@whedon assign @username as reviewer

# List the GitHub usernames of the JOSS editors
@whedon list editors

# List of JOSS reviewers together with programming language preferences and domain expertise
@whedon list reviewers

# Change editorial assignment
@whedon assign @username as editor

# Set the software archive DOI at the top of the issue e.g.
@whedon set 10.0000/zenodo.00000 as archive

# Open the review issue
@whedon start review
```
