# Meetings

Public meeting agendas and memos in markdown, version controlled for consistency.

## Overview

This repository contains official meeting agendas and memos for the Buckeye Googlers organization. These documents help maintain a clear record of decisions, action items, and discussions for future reference.

## Contribution Guide

### Prerequisites

- Git installed on your computer ([Download Git](https://git-scm.com/downloads))
- Membership in the Buckeye Googlers GitHub organization with repo access

### Contributing a New Meeting Document

Follow these steps to contribute a new meeting agenda or memo:

1. **Clone the repository** (first-time setup)

    ```shell
    git clone https://github.com/buckeye-googlers/meetings.git
    cd meetings
    ```

2. **Update your local repository** (if already cloned)

    ```shell
    git switch main
    git pull
    ```

3. **Create a new docs branch**

    ```shell
    git switch -c docs/YYYY-MM-DD-meeting-[agenda|memo]/yourgithubusername
    git push -u origin docs/YYYY-MM-DD-meeting-[agenda|memo]/yourgithubusername
    ```

    Replace `YYYY-MM-DD` with the meeting date, choose either `agenda` or `memo`, and replace `yourgithubusername` with your GitHub username.

4. **Create a new meeting document**
   - Create the year directory if it doesn't exist (e.g., `2025/`)
   - Copy the appropriate template to create your new document:

      ```shell
      mkdir -p YYYY
      # For meeting agenda
      cp meeting-agenda-template.md YYYY/YYYY-MM-DD-meeting-agenda.md
      # OR for meeting memo
      cp meeting-memo-template.md YYYY/YYYY-MM-DD-meeting-memo.md
      ```

   - Edit the new file with the meeting details

5. **Add reference files (if any)**
   - Create the reference directory if it doesn't exist:

     ```shell
     mkdir -p YYYY/reference
     ```

   - Place any supporting documents, images, or external files in this directory
   - Name files clearly with the meeting date: `YYYY-MM-DD-description-of-file.ext`

6. **Commit your changes**

    ```shell
    git add YYYY/YYYY-MM-DD-meeting-[agenda|memo].md
    # If you have reference files
    git add YYYY/reference/*
    git commit -m "docs(YYYY/YYYY-MM-DD-meeting-[agenda|memo].md): add meeting [agenda|notes] for [brief description]"
    ```

   The commit message follows this format:
   - `docs`: The type of change (always use "docs" for this repository)
   - `(YYYY/YYYY-MM-DD-meeting-[agenda|memo].md)`: The file being changed
   - Description: Brief summary of what the meeting was about

7. **Push changes and create a pull request**

    ```shell
    git push
    ```

   - Go to the [repository on GitHub](https://github.com/buckeye-googlers/meetings)
   - Click "Compare & pull request" for your branch
   - Fill out the pull request details
   - Request review from an executive member
   - Pin the requested reviewer in Discord

8. **Make any requested changes**
   - Address feedback from reviewers
   - Make additional commits as needed
   - Push the changes to update the pull request

9. **Clean up after merge**

    After your pull request is merged:

    ```shell
    git switch main
    git pull
    git branch -d docs/YYYY-MM-DD-meeting-[agenda|memo].md/yourgithubusername
    ```

    The remote branch will be automatically deleted by GitHub.

### Directory Structure

Meeting documents are organized by year with a reference directory for supporting files, for example:

```text
meetings/
├── 2025/
│   ├── 2025-05-04-meeting-agenda.md
│   ├── 2025-05-04-meeting-memo.md
│   └── reference/
│       ├── 2025-05-04-presentation.pdf
│       └── 2025-05-04-diagram.png
├── meeting-agenda-template.md
├── meeting-memo-template.md
└── README.md
```

### Template Modifications

If you need to modify the standard templates for a specific document:

1. Note the modifications in your commit message
2. Explain the changes in your pull request description
3. Specifically mention the modifications when contacting the reviewer

## Questions?

If you have any questions about the process, contact the executive team through Discord or open an issue in this repository.
