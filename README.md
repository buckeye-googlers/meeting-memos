# Meeting Memos

Public meeting memos in markdown, version controlled for consistency.

## Overview

This repository contains official meeting memos for the Buckeye Googlers organization. These documents help maintain a clear record of decisions, action items, and discussions for future reference.

## Contribution Guide

### Prerequisites

- Git installed on your computer ([Download Git](https://git-scm.com/downloads))
- Membership in the Buckeye Googlers GitHub organization with repo access

### Contributing a New Meeting Memo

Follow these steps to contribute a new meeting memo:

1. **Clone the repository** (first-time setup)

    ```shell
    git clone https://github.com/buckeye-googlers/meeting-memos.git
    cd meeting-memos
    ```

2. **Update your local repository** (if already cloned)

    ```shell
    git switch main
    git pull
    ```

3. **Create a new docs branch**

    ```shell
    git switch -c docs/YYYY-MM-DD-meeting-memo/yourgithubusername
    git push -u origin docs/YYYY-MM-DD-meeting-memo/yourgithubusername
    ```

    Replace `YYYY-MM-DD` with the meeting date and `yourgithubusername` with your GitHub username.

4. **Create a new meeting memo**
   - Create the year directory if it doesn't exist (e.g., `2025/`)
   - Copy the template to create your new memo:

      ```shell
      mkdir -p YYYY
      cp memo-template.md YYYY/YYYY-MM-DD-meeting-memo.md
      ```

   - Edit the new file with the meeting details

5. **Commit your changes**

    ```shell
    git add YYYY/YYYY-MM-DD-meeting-memo.md
    git commit -m "docs(YYYY/YYYY-MM-DD-meeting-memo.md): add meeting notes for [brief description]"
    ```

   The commit message follows this format:
   - `docs`: The type of change (always use "docs" for this repository)
   - `(YYYY/YYYY-MM-DD-meeting-memo.md)`: The file being changed
   - Description: Brief summary of what the meeting was about

6. **Push changes and create a pull request**

    ```shell
    git push
    ```

   - Go to the [repository on GitHub](https://github.com/buckeye-googlers/meeting-memos)
   - Click "Compare & pull request" for your branch
   - Fill out the pull request details
   - Request review from an executive member
   - Pin the requested reviewer in Discord

7. **Make any requested changes**
   - Address feedback from reviewers
   - Make additional commits as needed
   - Push the changes to update the pull request

8. **Clean up after merge**

    After your pull request is merged:

    ```shell
    git switch main
    git pull
    git branch -d docs/YYYY-MM-DD-meeting-memo/yourgithubusername
    ```

    The remote branch will be automatically deleted by GitHub.

### Directory Structure

Meeting memos are organized by year:

```text
meeting-memos/
├── 2025/
│   └── 2025-05-04-kickoff-meeting-memo.md
├── memo-template.md
└── README.md
```

### Template Modifications

If you need to modify the standard template for a specific memo:

1. Note the modifications in your commit message
2. Explain the changes in your pull request description
3. Specifically mention the modifications when contacting the reviewer

## Questions?

If you have any questions about the process, contact the executive team through Discord or open an issue in this repository.
