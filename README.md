# Khanfused Social Deduction Game

## About The Game

KHANFUSED is a social deduction game for 6-18 players, similar to Werewolf or Mafia, where social interaction and bluffing are key. The game is designed to be quick, with a typical 10-player match lasting about 15 minutes.

The core conflict revolves around resource management and hidden identities. Players are secretly assigned one of three roles:

* **Khans (Traitors):** A hidden minority who aim to starve the Kingdom by pillaging the Lords' lands in the winter.
* **Lords (Innocents):** The majority who must keep the Kingdom from starving. They face a critical choice each summer: either farm to produce grain or scout to identify the Khans.
* **The King:** A single player who is the only one with the power to banish suspected Khans. However, the King is uninformed and must rely on the Lords for information to make the right decision.

The game progresses through a cycle of four seasons, with phases for discussion and action. Players must balance the need to produce food with the urgency of finding and banishing the traitors before the Kingdom's resources run out.

---
## Quick Start Guide
### 1. Clone the repository
Use your Git client of choice, or if you don't know any of them, do it my way:
- Open Command Prompt.
- `git clone https://github.com/homeworkace/khanfused`
  - If your computer can't find `git`, download Git.

### 2. Run the server
- Open Command Prompt.
- `cd` to your working directory (the directory where this README is).
- `cd server` brings your Command Prompt to the server folder.
- Check your Python version with `py -3.12`. If your computer can't find it, download Python 3.12.
- The server runs on a virtual environment made just for it. `pipenv` maintains that environment. `py -3.12 -m pip install pipenv`
- `pipenv install` to install all the dependencies written in the provided `Pip.lock` file into the environment.
  - Periodically run this command as more dependencies are added to the project.
- `pipenv shell` to enter this virtual environment.
  - `exit` to leave.
- When in the environment, `python server.py` to start the server.
  - Ctrl+C to stop.

### 3. Run the frontend
#### The CLI way
When there are dependencies to install/update, you must use this.
- Open another Command Prompt.
- `cd ..` to go up one level.
- `cd khanfused` to go down the frontend folder.
- `npm install` to install all the dependencies written in the provided `package.json` file into the directory.
  - If your computer can't find `npm`, download React.
  - Periodically run this command as more dependencies are added to the project.
- When the server is running, `npm start` to start the React framework.
  - Ctrl+C to stop.
 
#### The batch script way:
When you wish to run multiple instances, you must use this.
- Open Notepad as administrator.
  - Find Notepad from the Start Menu.
  - Right-click, and click "Run as administrator".
- In Notepad, open `C:\\Windows\\System32\\drivers\\etc\\hosts`.
  - Click on "File", then "Open...".
  - Paste `C:\\Windows\\System32\\drivers\\etc` in the URL bar.
  - Find the dropdown menu that says "Text Documents (\*.txt)", and replace it with "All Files (\*.\*)".
  - Open `hosts`.
- At the bottom of the file, paste the following and save:
  ```  
  127.0.0.1 app3000
  127.0.0.1 app3001
  127.0.0.1 app3002
  127.0.0.1 app3003
  127.0.0.1 app3004
  127.0.0.1 app3005
  127.0.0.1 app3006
  127.0.0.1 app3007
  127.0.0.1 app3008
  127.0.0.1 app3009
  ```
- In File Explorer, go to the directory where the frontend is (`\\khanfused`).
- Double click on `start_instance.bat` to start one instance.
  - Repeat for up to 10 times for 10 instances.
  - If you need more, add more lines into `hosts`.
 
### 4. Receive and make changes
- `git pull` updates your local copy of the repository with new changes from the one on GitHub (remote).
- `git add *` stages all your changes.
  - If for some reason you want to control which files go to GitHub, use `git add ` followed by the relative path of your file/folder.
- `git commit` makes... a commit based on your staged changes.
  - It's good courtesy to pace your commits around the completion of each feature, and to make sure your project actually runs before you commit.
  - Commits need messages: a description of what you did. Add this with `git commit -m "Your message"`, because if you don't, you get thrown into a Vim interface just to write that message, which is very hard to get out of. Kind of like detention for not doing your homework (commit message)...
- `git push` to send your changes to GitHub.
  - You must always commit, then pull, before you push.
  - When pulling, Git automatically merges your changes (from your commit) with all the changes that are introduced with the pull. This typically happens without issue, unless two of you edit the same line of code... then you get a _merge conflict_. Resolving them is an art form which I CBA to write about here,
- `git branch` to switch to a different branch of development.
