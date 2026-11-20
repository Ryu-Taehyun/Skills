---
name: "code-checker"
description: "Code Check and Github Upload Faster"
---

1. Thoroughly scan the project's `.env` files and other files for database credentials, keys, and other sensitive secrets. Report their locations without exposing their values.
2. Review the code for unnecessary functions and duplicate logic. Use test results to help identify unused or unnecessary code, and propose changes for any issues found.
3. Check that exception handling and asynchronous operations are correct and consistent. Propose changes for any issues found.
4. Do not modify files, commit, or push without the user's explicit approval.
5. This refers to a brief summary of the code, provided after the project review is complete but before committing the changes.
6. Following the rules outlined above, Claude Sonnet 5.5 should scan the project; if it determines there are no issues, it should—upon receiving the user's approval—proceed to create a GitHub repository, commit the changes, and push them, handling the entire process autonomously.
7. Once the project scan is complete, please provide an estimate—on a scale of 1 to 10—of how satisfied other users might be when they encounter this project in a public space and use it themselves.
8. Once the project review is complete, the project file structure and key files are organized into an ASCII-format roadmap. Additionally, the modules used in the code are categorized by programming language.
9. Indicate whether revisions are required at each check stage. Once the scan is complete, the system will ask whether you would like to commit and push the changes to GitHub; however, if any critical errors are found, this prompt will not be displayed.