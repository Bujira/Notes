Fill the open ( ) accordingly...<br>

# Backend Work Flow

### 1. Assign a task to yourself
Go to GitHub ZenHub extension and find an available task<br><br>

### 2. Pull latest code from GitHub
First time working on this project?<br>
_git clone ( ssh command line from GitHub )_<br><br>

Already working on the project and need the latest code?<br><br>
First, make sure you are at the develop branch:<br>
_git checkout develop_<br>
Then, pull latest version of the project code:<br>
_git pull origin develop_<br><br>

### 3. Work on given task
Create a new branch to work on:<br>
_git checkout -b ( (fix/feat/chore)/branch-name )_<br><br>
feat - working on a new feature <br>
fix - fixing an issue <br>
chore - working on something else<br><br>

No spaces allowed for the branch-name!<br><br>

Example:<br>
_git checkout -b feat/create-virtual-card_<br><br>

Try working on the task and ask for help if needed.<br><br>

### 4. Test current task
Use Postman or Insomnia, for example, to test your work.<br><br>

### 5. Commit current task
Choose the appropriate commit style: <br><br>
_git commit -m "feat: ( insert task name )"_ <br>
_git commit -m "fix: ( describe issue fixed )"_ <br>
_git commit -m "chore: ( describe current changes )"_ <br><br>
feat - if a new feature is being added <br>
fix - if a fix is beign added <br>
chore - if you are commiting something else<br><br>

Example:<br>
_git commit -m "feat: create virtual card"_<br><br>

Remember to commit along the way, keeping track of your work. Avoid one single commit!<br><br>

### 6. Push latest code to git hub
_git push origin ( branch name )_<br><br>

Example:<br>
_git push origin feat/create-virtual-card_<br><br>

### 7. Create Pull Request
Go to the Pull Request page on the GitHub repository and create a pull request.<br><br>
!!! Make sure DEVELOP branch is selected <br>
!!! Assign the pull request to yourself or team memebers working on the task <br>
!!! Link an existing issue to the Pull Request

### Docker & Prisma Projects
First make sure your .dotenv file is configured correctly, then...<br><br>

Download postgres image (if you don't have it already):
_docker run --name ( container name ) -e POSTGRES_PASSWORD=( mysecretpassword ) -d postgres_<br><br>

Download redis image (if you don't have it already):
_docker run --name some-redis -d redis_<br><br>

Download project db and sync db with db manager (DBeaver for example):
_yarn docker:up_<br><br>
_yarn prisma generate_<br><br>
_yarn prisma db push_
