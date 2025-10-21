<center><p1>تمبلت بسيط لمشاريع التخرج باستعمال اوبسيديان, صدقة عني وعن والداي وعن كل من كان له الفضل عليّ</p1></center>
<center><p1>بالتوفيق بإذن الله</p1></center>

---

# Example : SLAM Drone Documentation
Obsidian vault for documenting a drone graudation project. use it as a template for your own project!
## 🗂️ Current Vault Structure
```
├── 📁 Documentation/
├── 📁 Images/
├── 📁 Meeting Notes/
       ├── Profs
       ├── Mentors
│── 📁 Modules/
   ├── 1 - SLAM
   ├── 2 - Recon
   └── 3 - Controller
          └──📁 Notes/
          │   ├── Custom Gazebo Model.md
          │   ├── Custom PMA Model.md
          │   ├── MMPOS.md
          │   ├── Toolchain setup.md
        │── Controller.md
    └── 4 - Vehicle
├── 📁 Papers/
├── 📁 Tasks/
├── 📁 Templates/
└── 📄 Main.md
```
### 📝 How to Maintain This Vault
1. 📁Documentation
	- draft of the documentation, or any other useful document
2. 📁Meeting Notes
	- write inside a dated folder with all the meeting notes, either discussion points during the meeting or presentations for the meetings
3. 📁Modules Notes Organization
	- Keep the current module-based structure, Follow What's Done in Controller Module
	a folder for different module sub-notes and a main markdown file to explain the flow of the module and general module info.
	- Don't Leave files hanging, notes stay in notes folder and images in their respective folders too
	- Maintain Notes/ for development documentation
4. 📁Tasks
	- contains the task sheet for every module, add a task by simply going to the module you want and type `- [ ] `, or use the button in [[GPS Denied Indoor SLAM Drone#Task Board]], make sure to add the task to the correct task sheet!

# **HOW TO GIT GUD**
[Git Cheat-sheet](https://git-scm.com/cheat-sheet)
Check out how to get a pass token below #-git-login-problem
```bash
# 1. Clone the repository
git clone https://github.com/alyayman921/Project-Obsidian-Vault.git
cd Indoor-SLAM-Drone-Docs

# 2. Configure their identity
git config user.name "Name"
git config user.email "email@example.com"

# 3. Verify remote
git remote -v
# Should show: origin  https://github.com/alyayman921/Project-Obsidian-Vault.git 
```
### Always start with pulling latest changes:
```bash
# 1. Get latest changes from main
git pull origin main

# 2. Create a new branch for your work
# if you own the repo, skip this step
git checkout -b your_name(ie.aly)
```
### Commit your changes
```bash
# 3. Make your changes to files
# 4. Stage changes
git add .

# 5. Commit with descriptive message
git commit -m "docs: add XYZ implementation notes
- Link to relevant hardware specs"
```

```bash
# 6. Push the branch to origin
git push -u origin module_name
```
then make a pull request to merge with main branch 

## 🔐 git Login Problem
```

**GitHub no longer accepts passwords** for Git operations since 2021. When you see:
```text
Username for 'https://github.com': yourusername
Password for 'https://yourusername@github.com': 
remote: Invalid username or token. Password authentication is not supported for Git operations.
```

> [!info]- The Solution
> ## 🎯  Personal Access Tokens (PAT)
> ### What is a PAT?- A **token-based password substitute** generated from your GitHub account
> - Acts as your **authentication credential** for Git operations
> - **Required instead of your GitHub password**
>  ## 🚀 How to Get a PAT
>  ### Step 1: Generate Token
> 1. Go to **[GitHub.com](https://github.com/) → Settings → Developer settings → Personal access tokens → Tokens (classic)**    
> 2. Click **"Generate new token" → "Generate new token (classic)"**
> 3. **Required scopes:** ✅ **repo** (full control of private repositories)
>4. Set expiration (90 days recommended)    
>5. Click **"Generate token"**
>6. **⚠️ COPY THE TOKEN IMMEDIATELY** - you won't see it again!
> ### Step 2: Use the PAT
When Git asks for credentials:
> - **Username:** your GitHub usernam    
>- **Password:** **paste your PAT** (not your GitHub password!)
> ## 💾 Make It Permanent
>```bash
># Store credentials so you don't have to enter them every time
>git config --global credential.helper store
># Then do one push with PAT, it will be saved
>git push origin main
>```


# Install git on windows

in an adminstrator powershell, install chocolatey
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
then 
```powershell
choco install git
```
now go back to the top and follow GIT steps to push updates to the vault!