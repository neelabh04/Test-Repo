# Introduction
Self notes on how to get acquianted with git.

# Miscellaneous Steps
- Sabse pehle maine VS Code pe aake `ctrl + shift + p` kia
- fir git: clone command kari
    - waha se fir repository choose kari (yeh tab ka process hai jab already website pe repo banai hui thi)
- uske baad fir repository clone hogayi

# Commands their description
## Basics
### `clear`
- sab kuch clean kardeta hai yeh command prompt pe jo bhi aatank machaya jo hota hai
- linux command hai so sabhi jagah chalega

### `init`
- iss se folder humara git ki repository me initial hojata hai

```git
git init
```

### `status`
- iss se hume saare untracked/tracked changes pta chalte hai
- agar kuch changes nahi ho rakhe ho file me toh "working tree clean" ka aata hai msg command prompt pe
- varna jo files me changes kare hote hai unka dikhata hai

```git
git status
```

### `clone`
- Command prompt pe `git clone` fir http waali link paste karni hogi
- iss se hum github pe jo repository hoti hai usko clone karne ki koshish karte hai  

**try karke dekhna hai ki hoga ya nahi ?** 
```git
git clone https://github.com/Ashish-012/Whiteboard.git
```


### `add`

_What is staging area ?_

Temporary save ki tarah hota hai baas aur kuch nahi. Suppose tumne kuch kaam kara aur chahte ho ki ab woh save hojaye toh 
- iss command se hum jo _**untracked changes ko staging area**_ me le aate hai

Ab kuch chudaap kardia tumne aur chahte ho waapis aana toh revert ka function hota hai. Aage discuss karenge.

```git
git add (file name with extension)

git add . [This will add all the file which have changes to staging area]
```

### `commit`
- jab humne saare changes karliye hote hai aur staging area se finally apni working branch pe daalne hote hai tab iska use karte hai

```git
git commit -m "(Message Name)"
```

### `push`
- jo bhi changes kare hai abhi tak woh saare push kardo working branch me 

```git
git push
```

## Intermediate 
### `diff`
_Need to have more clarity on this_
- Iss command se hum yeh dekhte hai ki jis file me changes huye hai woh hai kya exactly
    - Red line -> original state
    - Green line -> New State(change hua hai)

```git
git diff (File Name)
```


### `show`
- iss se hume yeh pta chalta hai ki kya changes huye hai as per the comment

```git
git show (hash number)
```

### `log`
- iss se hum project ke saare logs dekh sakte hai

```git
git log (iss se saare logs dikhenge)
git log -5 (last 5 recently logged entries)
git log --oneline (shows only commit message)
```

### `branch`
 -  basically tells which branch are we on
 ```git
 git branch
 ```

### `checkout`
Suppose hume new feature laana ho aur current working product ko chhed na nahi hai. Toh hum branch nikalenge.

> Yeh tree ki tarah hogaya ki root main hai apna aur branch nikal ke new cheez pe kaam ho raha. Agar sab sahi raha toh root se merge hojayega

```git
git checkout -b thunderBolt [this will create a new branch named thunderBolt]
git checkout main [iss se hum main branch pe aajayenge]
```

This will create a new branch from the working tree. New branch's name would be thunderBolt.

Agar hum `git checkout (main branch)` kare toh hum seedha original root pe aajayenge. Yaani checkout basically branches pe travel karne ke liye hai

### `branch`
- branches pe hume kya operations karna hai uss hisaab se hai

```git
git branch -d (branch name) [Iss command se hum branch ko delete kar sakte hai]
```

**Jis branch pe kaam kar rhe hai usko delete nahi kar sakte hai.** Yaani jis daali pe ho usko nahi kaat sakte jab tak dusari daali pe naa chale jao

```git
git branch (new branch)
```

### `merge`
_Merge karne ke liye zaroori hai aap main branch pe ho_
- Jo changes kare hai kisi branch me agar woh main root branch ke saath merge karne ho toh yeh karte hai
- Jis branch me changes kare hai pehle unko aaram se "add, commit" karlo
- Fir main/root branch pe aao via `checkout` command
- uske baad command likho

```git
git merge (kaunsi branch merge karni hai uska naam)
```

### `restore`
Iska kaam dekhna hai ki kya karta hai

## Hard
### `pull`
- iss me dekhna hoga ki kya kaam hota hai

[Yaha se dekhna hai](https://youtu.be/uj4fy4kpaOA?t=1729)

### Mergin and conflict resolution
1. `git reset --hard HEAD^` 
	- yeh command humare **code changes and commit dono ko hata dega**
2. `git reset --soft (hash name)` 
	- iss se **sirf commit hatega** _code changes present rahenge._

### `amend`
Need to see about this properly. Commits ka naam change karne me help karta hai yeh sahi se. 
```git
git commit --amend 
```

Yaha pe username change kia hai via 
```
git config --global user.name "(new name)"
```
