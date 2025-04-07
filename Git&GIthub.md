# Git & GitHub- Complete Notes

## 1. Git Kya Hai?

Git ek distributed version control system hai jo developers ko apne code ke changes track karne, alag branches pe kaam karne, aur multiple developers ke sath collaboration mein help karta hai.

🔑 Version Control = Code ka purana ya naya version manage karna. 

-------------------------------------------------------------------------------------------------------------------

## 2. Git Kaam Kaise Karta Hai?

Git teen levels pe kaam karta hai:

1. Working Directory – Jahan hum actual code likhte hain.
   
2. Staging Area (Index) – Jahan selected changes ready kiye jaate hain commit karne ke liye.
   
3. Repository (Local) – Jahan final commit save hota hai (history ke sath).
   
-------------------------------------------------------------------------------------------------------------------

## 3. Git Installation & Setup

Install Git: https://git-scm.com/downloads

Configuration (First Time Only):

git config --global user.name "Your Name"

git config --global user.email "your@email.com"

-------------------------------------------------------------------------------------------------------------------

## 4. Basic Git Commands

git init – Nayi Git repository banata hai

git status – Changes aur repo ka status dikhata hai

git add <file> – File ko staging area mein daalta hai

git add . – Saari files ko stage karta hai

git commit -m "message" – Staged files ko repo mein commit karta hai

git log – Commit history show karta hai

git diff – Changes dikhata hai

git diff  <branch1>..<branch2> - do branch main changes dikhata hai

git diff  <commit#1>..<commit#2> -do specific commits  main changes dikhata hai

git config --list – Current config show karta hai

-------------------------------------------------------------------------------------------------------------------

## 5. Branching & Merging

Branch: Code ka separate line of development.

Merge: Ek branch ke changes ko doosri mein milana.


git branch – Branch list

git branch <name> – New branch

git checkout <name> –  Switch branch

git switch <name> ­ – Switch branch

git switch -c <name> – Create branch and Switch with newly created  branch

git merge <name> – Merge branch

git branch -m <old branch name> <new branch name> - rename branch

git branch -d <branch name> - delete branch

-------------------------------------------------------------------------------------------------------------------

## 6. Remote Repository (GitHub)

GitHub se connect karna:

git remote add origin <repo-url>

git push -u origin main


### Remote Commands: 

git clone <url> – Remote repo ko local mein lata hai

git remote -v – Remote repo ka URL dikhata hai

git pull – Remote se latest changes lata hai

git push – Local commits ko remote repo pe bhejta hai

-------------------------------------------------------------------------------------------------------------------

## 7. Undo Commands

git checkout -- <file> – File ko last commit wali state pe laata hai

git reset <file> – File ko staging se hata deta hai

git reset --soft HEAD~1 – Last commit remove karta hai (changes bache rehte hain)

/* head is cuurent directory*/

git reset --hard HEAD~1 – Last commit + changes dono hata deta hai (dangerous)


-------------------------------------------------------------------------------------------------------------------

## 8. .gitignore File

.gitignore file un files ko ignore karta hai jo hum Git repo mein nahi rakhna chahte (e.g., config files, logs, node_modules).

### Example:

node_modules/

.env

*.log

-------------------------------------------------------------------------------------------------------------------

## 9. Git Reflog

git reflog – Git ki hidden history. Kab kya branch ya commit checkout hua, sabka record.

git reflog <commit#> -specific commit ko 

-------------------------------------------------------------------------------------------------------------------

## 10. Git Tags

Tags ka use specific version ya release mark karne ke liye hota hai.

git tag v1.0

git tag – List tags

git show v1.0 – Show tag details

-------------------------------------------------------------------------------------------------------------------

## 11. Git Stash

Jab kaam beech mein ho aur switch karna ho bina commit kiye:

git stash – Save current changes

git stash pop - apply and drop  

git stash list – List all stashes

git stash apply – Wapas lana

git stash clear - stash clear 

git stash drop - drop stash

-------------------------------------------------------------------------------------------------------------------

## 12. Aliases (Shortcuts)

git config --global alias.s status

git config --global alias.ci commit

Ab git s likhke git status milega.

-------------------------------------------------------------------------------------------------------------------

## 13. Useful Tips

- Har commit ka short message likho (clear ho kya kiya).
 
- Har naye feature ke liye alag branch banao.
 
- Push karne se pehle pull zaroor karo.
 
- .gitignore file zaroor banao.
 
-------------------------------------------------------------------------------------------------------------------


# GitHub - 

-------------------------------------------------------------------------------------------------------------------

## 1. GitHub Kya Hai?

GitHub ek online platform hai jahan developers apna code Git ke through host karte hain. Ye collaboration, version control aur code sharing ke liye use hota hai.

### 🔗 GitHub = Git + Cloud Hosting

-------------------------------------------------------------------------------------------------------------------

## 2. GitHub Account Setup

1. https://github.com par jaake account banao
   
2. Profile setup karo
   
3. Naya repository create karo
   
-------------------------------------------------------------------------------------------------------------------

## 3. Repository Create Karna

- GitHub dashboard pe 'New' button par click karo
  
- Repository ka naam do (e.g., my-project)
  
- Public/Private choose karo
  
- ReadMe file add kar sakte ho
  
- 'Create Repository' button dabao
  
-------------------------------------------------------------------------------------------------------------------

## 4. GitHub Repository Clone Karna

Local machine pe kaam karne ke liye repo ko clone karte hain:

git clone <repo-url>

Example:

git clone https://github.com/username/repo.git

-------------------------------------------------------------------------------------------------------------------

## 5. GitHub Pe Code Upload Karna

1. Code likho apne local system par
   
2. Use Git commands se commit karo:

   git add .
   
   git commit -m "message"
   
3. Fir GitHub pe push karo:

   git push origin main
   
-------------------------------------------------------------------------------------------------------------------

## 6. GitHub Pull Request (PR)

Pull Request ka use hota hai jab tum kisi repository mein changes suggest karte ho:

- New branch banao aur usme kaam karo
  
- Commit & push karo
  
- GitHub pe jaake 'Compare & Pull Request' dabao
  
- PR review hone ke baad merge hota hai
  
-------------------------------------------------------------------------------------------------------------------

## 7. Fork vs Clone

- **Fork**: Kisi aur ke repo ka copy apne GitHub account mein banana.
  
- **Clone**: Kisi repo ka copy local system mein lana.
  
-------------------------------------------------------------------------------------------------------------------

## 8. GitHub Pages

GitHub Pages se tum apne static websites (HTML, CSS, JS) ko free mein host kar sakte ho.

Steps:

1. Repo banao (e.g., portfolio)
   
2. Code upload karo
   
3. Settings > Pages > Deploy karo
   
-------------------------------------------------------------------------------------------------------------------

## 9. Collaborators Add Karna

- Repository > Settings > Collaborators
  
- Username enter karo jise access dena hai
  
- Invite button dabao
 
-------------------------------------------------------------------------------------------------------------------

## 10. GitHub Actions (Basics)

GitHub Actions ek CI/CD tool hai jo automation ke liye use hota hai.

- Example: Test chalana, build karna, deploy karna jab bhi code push ho
  
- `.github/workflows` folder mein YAML file bana ke workflows define karte hain
  
-------------------------------------------------------------------------------------------------------------------

## 11. Issues & Discussions

- **Issues**: Bugs, feature requests ya tasks track karne ke liye

- **Discussions**: Community interaction aur feedback ke liye
  
-------------------------------------------------------------------------------------------------------------------

## 12. README.md File

- Har repo ke root mein ek README.md file hoti hai jo project ka overview deti hai

- Markdown syntax ka use hota hai (e.g., # Heading, **bold**, - list)
  
-------------------------------------------------------------------------------------------------------------------

## 13. License Add Karna

- License se log samajh paate hain ki wo code kaise use kar sakte hain
  
- Common licenses: MIT, GPL, Apache 2.0
  
- Repo banate waqt ya baad mein LICENSE file add kar sakte ho
  
-------------------------------------------------------------------------------------------------------------------

## 14. Star, Watch, Fork

- **Star**: Repo pasand aane par bookmark jaisa
  
- **Watch**: Notifications ke liye
  
- **Fork**: Copy repo to your account to customize or contribute
  
-------------------------------------------------------------------------------------------------------------------

## 15. GitHub Desktop

GitHub Desktop ek GUI tool hai jo beginners ke liye Git aur GitHub ko use karna asaan banata hai

Download: https://desktop.github.com/

