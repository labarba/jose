# Open Journals EiC guide

Open Journals live on GitHub, and carry out peer review using GitHub’s issue tracker. Our little bot, called @whedon, facilitates journal management. Associate Editors interact with @whedon directly on the review issues, entering commands right into a comment. The Editor-in-Chief has additional tasks to do with @whedon on the command line.

The EiC needs to clone the @whedon app —found at: https://github.com/openjournals/whedon —and install it. The next step is to create a `.env` file (starting from the example provided: `.env.text`). This configuration file will need to be edited with the journal’s name, URL, and repository locations. The EiC will need to add a GitHub token for authentication. 

The EiC also needs to clone the journal’s repository of published papers (e.g., `joss-papers`).

Command-line actions with @whedon are necessary after peer review is complete, and a paper is accepted. The steps are:

1. Add the “accepted” label on the REVIEW issue (if not already done by the handling editor).
2. Make sure to get the DOI for the revised submission from the author, then run the command `@whedon set <archive doi> as archive` 
3. Check the PDF of the article, automatically generated by @whedon.
4. In the local machine, use the `whedon download` command with the REVIEW issue number to clone the submission’s repository (it will go into a `tmp` directory). Example: `bundle exec whedon download 27`
5. Use the `whedon compile` command to create the paper PDF locally. Example: `bundle exec whedon compile 13` — Give it a check.
6. In the location of the local repository of papers (e.g., `joss-papers`), create a directory with the paper issue number: `mkdir joss.123`
7. Copy the files that whedon created with the `compile` command into this new directory
8. Add, commit and push the files to the papers repository
9. Run the commnand `whedon deposit xxx` to deposit the CrossRef metadata for the paper
10. Wait one or two minutes and check that the DOI correctly resolves.
11. Go to the REVIEW issue and leave a final nice comment, with thanks to all!
12. Close the REVIEW issue, and @whedon will post an automated message including the code snippet for the author to add the JOSS button to the submission repo. (Requires the "Accepted" label on the issue.)
