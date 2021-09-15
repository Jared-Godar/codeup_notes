## DEFINITIONS

- GIT: Distributed version control system. 
    - Free. 
    - Open source. 
    - Small to large ptojects.
    - Distributed - lives on more than one computer
    - Version control (1.0, 2.0, etc) tracking changes to version
        - Crude: resume.pdf, resume1.pdf, resume2.pdf, redume_FINAL.pdf
        - More sophisticated: track changes in google doc
            - Which authors made what changes in what time
            0 lacking - why change was made and if new users need to know anything else


## VOCABULARY:

    - repository: directory managed by git; 
    - add: tell git which files we wish to look at for the nxt commit
    - commit: create a "save point" formal snapshot of a repositry.
    - push: copy state of a local repositry elsewhere; for our purposes, most commonly used to send

    - GIT 
        - Internally works like blockchain
        - Tracks all changes to any line of code / text in any file we are tracking
        - Permanent record with a timeline that has the ablilty to branch/- - navigate/merge parallel timelines

    - When git is enabled, we enable on entire folder/directory. Including subfolders and all files. In specific scenrios - like passwords or other sensative files - we can tell to ignore specific files.

## SO WHAT
    - Most interested in the permanent record part. Commits at good points - mess something up, can roll back.
    - Large trend in Data Science is adpoting methods, tools, and workflows that are extablished best practices in software engineering. 
    - DS practitionares uning SE workflows (new trent) a lot of your competition doesn't know / isnt using GIT, but employers are - competative edge
    - Tracking changes in analysis with hundreds/thousands of lines of code, much easier in git 

 ## NOW WHAT
    - Formal git curriculum
    - Turn regular directories into repositories
    - All repositories are foldwes, but not all forders are repositories
    - git runs on a computer (laptop, desktop, servers)
    - Doesn't automatically back up - our responsibility to back up. (GitHub makes this easy and cheap) - 
    - Codeup Git bill about $150 a month for all of codeup 
    - Push (upload) sends to GitHub in the cloud. Can use github as simple backup, or edit directly on github
    - Pull (download): brings most up to date github cloud back down to local (laptop) environment
    - Clone Copies the entire repository from cloud to local environment

## Some Concepts
- "Commits" are save points. Each commit is one or more changes to one or more files.
- repostiory: folder or directory managed by git
- add: file to git - tells which files we wish to look for at the next commit
- adding files/changes is like putting letters in an envelope
- making a commit is like SEALING that envelope with a timestamp (cryptographically) 
- pushing: upload process

## COMMANDS

- get init 
- Avoid initializing repositories within already initialized repositories
- git status: tells us which branch we are on; how many commits; list of untracked files

- Please enter the commit message for your changes. use good messages; 
- use 'git status' often. Make aware of state of repository. Initiially use git status btween every other git command you execute. (git init makes a hidden folder - deleting that turns a repositry back into a regular folder)

- Working on laptop. Made files and changes. Committed them. Laptop dies. Work gone. Need to push repositories to remote. using github puts the backup on their servers

## Remote Repository 

- Go to https://github.com/new Enter name and optional description.
- Make sure "initialize this repository with a README is NOT CHECKED
- Make sure the droopdowns for "Add .gitnore" and "Add a license" both say "none"
-(Should be default, but don't change)

- set public so far 
- GitHub will show instructions
- 1) Make sure configured to SSH not HTTPS - already set up SSH key
- Find line for remote git:  

git remote add origin git@github.com:YourUsername/your-repo-name.git

- Add remote repository called origin and poit it to a GitHub repository 
- Now that a remote is setup, we can push to and pull from that remote

- Push changes to remote
    - git push origin master

- Pull changes from remote
    - git pull origin master


-Push local repository to  

godarj/codeup_notes

## Workflow (Best practices)
- Make new repo locally (laptop) and remotely (on github) for each new porject
- Wisedom: one repo for project
- Daily Workflow:
    - Do work (creat file, edit file, delete)
    - 'git add .'
    - 'git commit' then type out a meaningful commit message to tell a story
    - 'git push'
- Make commits and push before before lunch / end of day / any time you close yout laptop
