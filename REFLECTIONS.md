**1.** Your code lives in two places: your local repository (your laptop) and the remote repository (GitHub).

*Where changes exist:*

* After you save the file: Changes are in your working directory
* After `git add`: Changes are in the staging area
* After `git commit`: Changes are saved in your local repository
* After `git push`: Changes are in the remote repository (GitHub)
* After your partner runs `git pull`: Changes are in the remote repository and your partner's local repository

Your partner can see your work once you push your changes to GitHub.

**2.**

**Sanaa:** I predicted it would cause an issue.

**Elhadj:** I predicted that both changes would push.

Git rejected the push because the remote repository had a commit from Elhadj that Sanaa didn't have in her local repository yet. Git won't let you push until your local copy is up to date with the remote. Running `git pull` downloaded Elhadj's changes and tried to merge them with Sanaa's. Because we had both edited the same line, this created a merge conflict. Seeing both versions side by side allowed us to choose which code to keep and resolve the conflict, which the push alone could not do.

**3.** In Round 1, my partner and I chose to combine our titles because we both liked parts of each one. We confirmed the resolution was correct by running `python3 main.py` and seeing the combined title print correctly in the terminal before we pushed.

**4.** One moment something didn't work was when Sanaa tried to pull the first sentence Elhadj wrote. She had accidentally pressed `Enter` and added an empty line to the file before pulling, so Git printed an error: "Your local changes to the following files would be overwritten by merge. Please commit your changes or stash them before you merge." The error told her she needed to commit her changes before pulling. Instead, she deleted the extra line, which removed her local changes, and then she was able to pull Elhadj's changes.

**5.** Our most useful commit message was `resolve merge conflict in title` because it explained why the two previous commits had the same message. Our least useful messages were "first sentence," "second sentence," and so on, because they didn't say what the sentences were for. A better version would be `first sentence of the story`. If five people were working in this repo instead of two, clear commit messages and pulling before you start would matter even more for a smooth workflow. Clear commit messages help the team understand the changes made and why without opening every file, and pulling first makes sure everyone is working on the latest version, which reduces merge conflicts.