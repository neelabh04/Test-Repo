# Initial Steps
- Sabse pehle maine VS Code pe aake `ctrl + shift + p` kia
- fir git: clone command kari 
    - waha se fir repository choose kari (yeh tab ka process hai jab already website pe repo banai hui thi)
- uske baad fir repository clone hogayi 
# Commands their description
## `clear`
- sab kuch clean kardeta hai yeh command prompt pe jo bhi aatank machaya jo hota hai
- linux command hai so sabhi jagah chalega

## `git init` 
- iss se folder humara git ki repository me initial hojata hai

## `git status` 
- iss se hume saare untracked/tracked changes pta chalte hai 
- agar kuch changes nahi ho rakhe ho file me toh "working tree clean" ka aata hai msg command prompt pe
- varna jo files me changes kare hote hai unka dikhata hai

## `git clone`
- Command prompt pe `git clone` fir http waali link paste karni hogi 
- iss se hum github pe jo repository hoti hai usko clone karne ki koshish karte hai 

**try karke dekhna hai ki hoga ya nahi ?** 

```git
git clone https://github.com/Ashish-012/Whiteboard.git
```

## `git diff`
Thodi iski clarity paani hogi 

- Iss command se hum yeh dekhte hai ki jis file me changes huye hai woh hai kya exactly
    - **red line** me jo aayega yaani woh hata hai (original state)
    - _Green line_ me jo aayega yaani woh change hua hai

```git
git diff (File Name)
```

## `git add`
What is staging area ?

Temporary save ki tarah hota hai baas aur kuch nahi. Suppose tumne kuch kaam kara aur chahte ho ki ab woh save hojaye toh 

- iss command se hum jo _**untracked changes ko staging area**_ me le aate hai 

Ab kuch chudaap kardia tumne aur chahte ho waapis aana toh revert ka function hota hai. Aage discuss karenge.

```git
 git add (file name with extension)
```

## `git show`
- iss se hume yeh pta chalta hai ki kya changes huye hai as per the comment 

```git
git show (hash number)
```

## `git commit`
- jab humne saare changes karliye hote hai aur staging area se finally apni working branch pe daalne hote hai tab iska use karte hai

```git
git commit -m "(Message Name)"
```

## `git log`
- iss se hum project ke saare logs dekh sakte hai

```git
git log (iss se saare logs dikhenge)
git log -5 (last 5 recently logged entries)
```

## `git branch` 
 -  basically tells which branch are we on
 ```git
    git branch 
 ```
## `git checkout` 
Suppose hume new feature laana ho aur current working product ko chhed na nahi hai. Toh hum branch nikalenge. 

> Yeh tree ki tarah hogaya ki root main hai apna aur branch nikal ke new cheez pe kaam ho raha. Agar sab sahi raha toh root se merge hojayega

```git
git checkout -b thunderBolt
```
This will create a new branch from the working tree. New branch's name would be `thunderBolt`

Agar hum `git checkout (main branch)` kare toh hum seedha original root pe aajayenge.

Yaani checkout basically branches pe travel karne ke liye hai

## `git branch`
- branches pe hume kya operations karna hai uss hisaab se hai

```git
git branch -d (branch name)
```
Iss command se hum branch ko delete kar sakte hai 

> **Jis branch pe kaam kar rhe hai usko delete nahi kar sakte hai**

Yaani jis daali pe ho usko nahi kaat sakte jab tak dusari daali pe naa chale jao

```git
git branch (new branch)
```
aise bhi hum new branch create kar sakte hai

_"Storm-breaker branch pe hunn me aur changes laa raha."_

## `git merge`
- Jo changes kare hai kisi branch me agar woh main root branch ke saath merge karne ho toh yeh karte hai
- Jis branch me changes kare hai pehle unko aaram se "add, commit" karlo
- Fir main/root branch pe aao via `checkout` command
- uske baad command likho

```git 
git merge (kaunsi branch merge karni hai uska naam)
```
**Merge karne ke liye zaroori hai aap main branch pe ho**

# Mergin and conflict resolution
1. `git reset --hard HEAD^` yeh command humare **code changes and commit dono ko hata dega**
2. `git reset --soft (hash name)` iss se **sirf commit hatega** _code changes present rahenge_ 