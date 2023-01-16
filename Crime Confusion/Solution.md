This is a 4 part challenge.


## CHALLENGE 1 - Crime Confusion 1: W as in WHERE

### PROBLEM
Someone has died unexpectedly. The police is on it, but between you and me, I cannot wait for the police. I am a private investigator and I need your help. Unfortunately, we might be tracked so I cannot give you the information directly. Start in a major social network. Certainly not a problem for the best hacker I know right...? Alright here goes a beautiful poem
```
  Some people in weird ways were connected
  Some were a triangle, some were less directed
  For one night they all met
  At doctor's Jonathan Abigdail the third they wept 
  Things were said, threats in the air
  A few days later someone is dead
  Who is that someone? That is for you to find,
  Also who is the killer, if you really don't mind.
```

### SOLUTION
Two things of note:
1. Start in a major social media site
2. Search for a doctor called "Jonathan Abigdail the third"

After trying both Facebook and Linkedin to no avail, I found ```@abigdail3djohn``` on instagram. There's nothing much of note in his bio, but he does have one instagram post, with a hashtag ```#TheEye12tothe3isthekeytoBEyousee?```.
This leads us to the next piece of the puzzle, as ```@hjthepainteng``` also used the exact same hashtag. We've found our victim (the someone from 'someone is dead' in the poem), Heather James! 

<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/Crime%20Confusion/1.png"  width="500" height="430">

From here we derive more clues
```
  1. Possible account: UThE_TS
  2. Possible Ebay account: great_paintball_portugal
 ```
A quick search on Ebay gives us the relevant account ```https://www.ebay.co.uk/usr/great_paintball_portugal``` 
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/Crime%20Confusion/2.png"  width="500" height="300">

This tells us we are searching for an "rip post" on the ```https://franparrefrancisco.wixsite.com/great-paintball-pt``` wix site, but it will not be directly provided on the site. I tried several avenues:

1. Inspect Element: I thought some information could be hidden in the website code --> fail
2. Search Bar: At this point i realised I was barking up the wrong tree. "RIP post" means I should be searching for a blog post. Since there's a search bar I figured I'd try my luck with searching "rip" and "post" --> fail
3. Suffix: Thought i'd just try my luck with searching for a /blog or /post subdomain --> success! 

```https://franparrefrancisco.wixsite.com/great-paintball-pt/blog``` leads us to the blog post ```https://franparrefrancisco.wixsite.com/great-paintball-pt/post/great-paintball-portugal-death-heather-james```

<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/Crime%20Confusion/3.png"  width="500" height="200">


The flag is: **idek{TGPP_WCIYD}**

**Thoughts**: This was fairly straightforward, just follow the breadcrumbs straight to the end. First blood :D  
&nbsp;  


## CHALLENGE 2 - Crime Confusion 2: W as in WEAPON

### PROBLEM
```
Now that you found where, can you help me find what was the weapon of the crime? It has something to do with a university of science.
```

### SOLUTION
Perfect! We have an unused clue from part 1: ```UThE_TS```. This is likely a social media handle, and sure enough we find the account we're looking for ```https://twitter.com/UThE_TS```.

<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/Crime%20Confusion/4.png"  width="370" height="500">

So, the school has released some information in the form of a website link. But where? One thing I learned from a previous CTF (idek2021, as a matter of fact), is to ALWAYS CHECK TWITTER LISTS. 
And sure enough at ```https://twitter.com/UThE_TS/lists``` we discover the following list:

<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/Crime%20Confusion/5.png"  width="500" height="200">


What we've been given is essentially a url suffix, and we know the prefix is related to ```german chaos pad```, whatever that means. Oh and did we struggle finding what it meant!
1. Googling "german chaos pad" brings up suggestions of "kaoss pad", an electronic music tool. Spoiler alert: this is a red herring.
2. The word "pad" and the sharing of varied information suggests we could be looking for an online notepad website. In fact, Googling the url suffix (in quotes) suggests its the typical format for the back half of etherpad servers.


We know we're looking for an etherpad. But how do we find it? We tried all sorts of typical formats for etherpad servers "german.chaospad.org/..." / "pad.chaos.de/..." / "german-chaos-pad.net/..." ...
5 hours deep in the rabbit (hell)hole to what turned out to indeed be chaos (though not particularly German), we asked the challenge writer for help and were told to focus on the "german" aspect. 
By sheer dumb luck we Googled ```"chaospad".de``` and would you look at that...

```
We find https://pads.ccc.de/ and from there https://pads.ccc.de/ep/pad/view/ro.lvGC01KAJWI/rev.354
```
The flag is: **idek{HSTM_X!#$}.**

**Thoughts**: later it was revealed that if you searched "german chaos pad" using the duckduckgo search engine, it would immediately output the website we were searching for. It's definitely something I'll bear in mind in future CTFs so as not to waste 5hours stuck in german chaos hell.  
&nbsp;  


## CHALLENGE 3 - Crime Confusion 3: W as in WHO

### PROBLEM
```
I feel the killer might be dangerous so I have some info to give you but I don't want to disclose my email just like that. 
So find my review from the image below and send me an email asking for info. Be creative with the signature so I know its you. 
It is time to find Who is the killer.
```
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/Crime%20Confusion/6.jpeg"  width="280" height="400">


### SOLUTION
Imagine my horror at having to do this alongside 17 images for the geoguessr OSINT Challenge. Done? Good.

The image shows two shops, one called ```Cabeleireiros``` and the other ```Alfaiate D'Interiores```. We know we're searching for a review of one of these two places.
We pick the latter to begin with, and compare the images of the Google Maps search results with the storefront in the image to find the correct store. It's```Alfaiate D'interiores - Foz do Porto``` by the way, if anyone's in the market for a Portuguese interior designer.

<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/Crime%20Confusion/7.png"  width="300" height="300">

Send an email to the email address and we get a reply:
```
So... I got some stuff to tell you. I think the killer is probably watching us. The killer used a weird weapon as you have found out. L
ook, the info I have is that weirdly enough the university page of Heather tweeted something that might lead you to the killer. 
They deleted it though. Luckily these days you can just walk back in time! Ah, the tweet was 1612383535549059076. When you have the info look in github!
```

Our first step is to use waybackmachine on the ```@UThE_TS``` twitter account from part 2 with the tweet id attached. 
Basically ```https://twitter.com/UThE_TS/status/1612383535549059076```. Note that you could also find this by using wayback machine on the Twitter main page and navigating to "URLs".
The deleted tweet is:

<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/Crime%20Confusion/8.png"  width="500" height="70">


Now on to our next step: finding the github: ```https://github.com/potatoes-eating-camels``` Where we are treated to this delightful red herring:

<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/Crime%20Confusion/9.png"  width="500" height="300">

(Don't bother with the morse it's just YOUREALLYDOTHINKIWOULDGIVE) We checked commit history and were about to start searching for a wikipedia page but then realised that "wiki" could refer to the github repository wiki!

<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/Crime%20Confusion/10.png"  width="500" height="500">


The flag is: **idek{JULIANA_APOSIDM723489}**

**Thoughts**: learned two new things to add to the list of basic checks to make when using waybackmachine and github  
&nbsp;  


## CHALLENGE 4 - Crime Confusion 4: W as in WHY

### PROBLEM
```
You did it! You found the killer!!! But whyy oh why did she do it?

Apparently she was obsessed with stamps, but was it real or not?

Well, I found this image on her computer, maybe it can help you.

Also a nice poem:

``` A man of peace, a collector too
His name, Johan Jørgen, forever true
A network vast, across the land
His passion, stamps, with Olympic brand

A stamp of Seoul, in '88
Issued to commemorate, the games we all love
A rare find, this stamp of Olympic dream
But where, oh where, can it be seen?

A man of peace, his legacy lives on
In stamps and memories, forever strong
But where to find, this elusive prize
A mystery yet, to the collector's eyes.
```
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/Crime%20Confusion/11.png"  width="280" height="400">

### SOLUTION
TLDR; we have a photo of two stamps (circa Seoul Olympics) and we need to find these somewhere on the internet. I tried the following:
1. Basic Image check: properties, exifTool, etc.
2. Reverse Image search: Tineye.com and Yandex.com.
3. Waste Time: I then accidentally started doing research on Johan Jorgen and the 1988 Seoul Olympics... idk how I thought that would be relevant.

Eventually I thought perhaps I was overthinking it, and as it turns out all that was required was a simple google dork...
```
Both ' "xxiv olympiske sommerleker" johan jorgen' and ' "xxiv olympiske sommerleker" stamps' will give us the final result
```
```https://digitaltmuseum.no/021027988861/frimerke``` provides us with our final flag.

The flag is: **idek{OLM-08741}**

**Thoughts**: I still think it's always good to do the standard image-related checks when being provided with a photo like that, though it was the wrong path in this specific case.

