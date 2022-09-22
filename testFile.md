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

## `git add`
- iss command se hum jo _**untracked changes ko staging area**_ me le aate hai 

What is staging area ?

Temporary save ki tarah hota hai baas aur kuch nahi. Suppose tumne kuch kaam kara aur chahte ho ki ab woh save hojaye toh 

> `git add` (file name with extension)

Ab kuch chudaap kardia tumne aur chahte ho waapis aana toh revert ka function hota hai. Aage discuss karenge.

