# J.O.B-Training-Repo-1

If you are looking for the face to face guided training repository for CTS-IT Gitflow training then you are in the right spot. In this repository you will find instructions that will help you work with an instructor to learn the sequence of events for a successful gitflow workflow. This workflow is a simplified version of the process that happens on a bi-weekly basis at CTS-IT. 


1) Install gitflow which is a one-time operation
- With the laptop on click, go>utilities>terminal
- Type `brew install gitflow`

2) Browse to github.com and login
- Navigate to [github.com/ctsit](http://github.com/ctsit "CTS-IT Github Page").
- Locate the repository named [J.O.B.-Jump-On-Board](https://github.com/ctsit/J.O.B.-Jump-On-Board "CTS-IT Job Training")
- Click the fork button
- Select personal github account
- Click ‘clone or download’ button
- Copy URL into clipboard

3) Clone forked repository to local laptop
- Return to terminal window
- Type `git clone` and paste repository url in terminal and press enter

4) Initialize repository with gitflow
- Type `git flow init`
- Follow prompts and accept defaults by hitting enter

5) Create feature branch
- Type `git flow feature start helloworld`
- Review screen output

6) Make helloworld Python file
- Type `touch helloworld.py`
- Type `nano helloworld.py`
- In the nano editor on line 1 type `#This is my hello world program` on line 2 type `print ‘Hello World’`
- Press ctrl O
- Name the file helloworld.py and save

7) Run the helloworld.py program to verify it works
- Type `python helloworld.py`
- Review screen output

8) Close feature branch
- Type `git flow feature finish`

9) Go to github.com to create pull request from your forked repository branch to the develop branch of J.O.B-Training-Repo-1  
- Browse to github.com personal account
- Locate [J.O.B-Training-Repo-1](https://github.com/ctsit/J.O.B-Training-Repo-1) repository
- Click pull requests tab
- Click new pull request
- Click create pull request and use the personal fork to the develop branch of [J.O.B-Training-Repo-1]https://github.com/ctsit/J.O.B-Training-Repo-1
- Click create pull request again

10) Review pull request with instructor
- Review changes made with pull request using Github.com interface
- Click merge pull request
- Click confirm merge

10) Create release using gitflow
- Type `git checkout master && git pull && git checkout develop && git pull && git fetch --tags && git tag`
- Type `git tag`
- Type `git flow release start 0.0.1`
- Type `git chlog 0.0.1..HEAD`
- Type `git add CHANGELOG`
- Type `git commit –m “update CHANGELOG for release 0.0.1"`
- Type `git flow release finish 0.0.1`
- Type `git push && git checkout master && git push && git push --tags && git checkout develop`
