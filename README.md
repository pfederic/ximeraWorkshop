Some [slides](https://osu.box.com/maa-ximera) provide an overview of the project.

The goal of these instructions are for you to set up your own Ximera page, modeled after [a basic example](http://ximera.osu.edu/course/kisonecat/ximeraWorkshop/master/activity).

# Check out Ximera

1. Create a [GitHub](https://github.com/) account.
2. View some sample content on [Ximera](http://go.osu.edu/ximerasample).
3. Click `Sign In` and choose Google.
4. Click on your name in the upper right hand corner, and click `Profile`
5. On your profile page, click `Connect GitHub` to connect your new GitHub account to your Ximera account.

# Build some content

1. Log into a GitHub account registered with Ximera (i.e., follow the instructions above).
2. Go to [https://github.com/kisonecat/ximeraWorkshop](the Ximera Workshop repository)
3. Click "Fork" in the upper right corner to create your own copy the `ximeraWorkshop` repository.
1. Create a [SageMathCloud](https://cloud.sagemath.com/) account.
2. Click on `New Project`.  Include your name in the project title.
4. Switch over to your forked GitHub repository, and copy the http URL from the right hand side.
5. Switch back to SageMathCloud (SMC).
3. Once in your new SMC project, click on `New`.
4. Under `Name your file, folder or paste in a link` paste in the link from GitHub.
5. Click `Download from Internet`
6. Open the folder `ximeraWorkshop`
7. Click `New` and create a terminal.
8. Enter `source setup.sh` into the terminal and press enter.
9. Tell git your name with the commands
```
git config user.email "you@example.com"
git config user.name "Your Name"
```
9. Close the terminal.
10. Navigate to `activity.tex` in the Sage Math Cloud file browser.
11. Try editing `activity.tex` to explore some of the printed possibilities of Ximera.

# Deploy your content

1. Go to GitHub.
1. In your own forked copy of the `ximeraWorkshop` repository, click on `Settings`
5. Choose `Webhooks and Services`
6. Click `Add webhook`
7. Confirm your password.
8. For the payload URL, enter `https://ximera.osu.edu/github`
9. Click `Disable SSL verification`
10. Confirm that you understand your webhooks may not be secure.
10. For the webhook secret, enter `8mi0tsrje9n3asPu86XC198G1XSdZj`
11. Click `Add webhook`

# After making edits, push them to GitHub

1. Go to SMC and enter the `ximeraWorkshop` folder.
2. Open a terminal.
3. If you changed `activity.tex` then run the command
```
git add activity.tex
```
to "stage" these changes.
4. Commit the change with `git commit -m "A description of your change."`
5. Push these changes to GitHub with `git push`
6. You will be asked for your GitHub credentials at this point.
7. Go to your GitHub repository to confirm that these changes are visible.

After the server processes your changes to `activity.tex`, you should be able to view them at `http://ximera.osu.edu/course/YOUR-GITHUB-USERNAME/ximeraWorkshop/master/activity`
