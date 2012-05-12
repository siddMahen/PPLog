# MYP Personal Project Process Journal 

### Topic:

The Web.

### Goal:

- Analyze the evolution of the Web, from it's inception to it's future

- Analyze a certain portion of the Web in great detail, such as *security*?

- Identify new/emerging technologies and their potential on the web

   - In security for example, homomorphic encryption, create my own encryption scheme that works well, analyze current encryption schemes that function well.

- I know! I should keep a kinda of little book, where I tally the awesomeness of my different ideas over a week or so and then I'll be sure that the idea I pick will be well vetted.

## Ideas:

- Real-Time Applications Idea

So recently, I was reading several ideas regarding bcrypt, RSA loopholes, DDOS prevention and general security stuff on the web… Seems very very, interesting! Perhaps I could focus on this? Create my own encryption algorithm? Analyze an existing one? Homomorphic encryption??

## 03/09/11

Hmmm I've looked into crypto a lot… It seems really, really interesting? I wonder how people did without it? Why it came about? Probably because of the War right? Engima cipher was used in the war by the Germans to encode messages. Not exactly computer crypto, because computers and encipher any kind of data so long as it's in binary; but it's still crypto.

I just realized I should date these journal entries. Oops. 

Anyway, I think I'm gonna go look into this topic a bit more, I have a meeting with my supervisor (Mr. Klomonen) Monday. Intrested to hear what he has to say, I'm kinda surprised he found my topic interesting considering he is a geography/history teacher.

If I end up doing crypto, then I'll probably learn some crypto analysis techniques, implement a few ciphers of different kinds, break them,  present that data and then make one that I'll challenge others to break? Or maybe make one good one and explain why it's good.

See bcrypt(), OpenSSL, SHA(1,2,3), RSA, DES, AES etc…

Don't forget that Amazon site where you were suppose to order the crypto books. (super cheap!!! $7!).

I should sign at the end of each post.

- Siddharth

## 05/09/11

Dammit! Just missed the meeting with Mr.K today!! He's gonna think I'm totally uninterested, and that I don't value his time. I'll write him up an apology and hopefully we can reschedule. Cryptography is looking to be an interesting subject! 

## 06/09/11

Set up a meeting for tomorrow that I will not miss. Doing some preparatory research.
Looking into some F-Secure stuff. Especially in light of the recent certificate signing breaches.

## 07/09/11

Getting the crypto books from HelMet libraries. One of them has a month long hold… But it's fine. First step, get a library card…


## 11/09/11

Just got my Algorithms book, hefty stuff. Brushing up on my higher level math skills too. Just learned derivatives and limits on my own. Calculus is next. The other books I want regarding cryptography are being held at the library. I'll get them next week I think. The algorithm book is really cool. Gets kinda complex at certain points but if I really get stuck I can ask Mr.Tyler for help.

## 12/09/11 

Finally figured out differentiation. You know, that wasn't really *that* difficult.
I mean, for the longest time, calculus was always something that was made out to be hyper daunting, but in reality, so long as you apply yourself, it's not that hard.

Reading through some of the first few pages of the Algorithms text book I just received. Still waiting on the crypto book from the HELKA library.


## 16/09/11

Spent yesterdays basketball meet up looking for crypto books at the HELKA library. Just starting to work up my plan for the next 6 months. Finally mastered implicit differentiation, it's pretty cool if you thing about what's going on. 

Finally found the introductory book to crypto that I absolutely needed. So far I have procured:

- Introduction to Algorithms (M.I.T)
- An Introduction to the Theory of Numbers (However, this book is really, really dense and I'm having trouble reading through it. Unlike the MIT book, the proofs are not very intuitively explained and the books moves from theorem to theorem very quickly, probably gonna ditch this).
- An Introduction to Mathematical Cryptograpy (This looks pretty awesome)

I've also put a hold on An Introduction to the Theory of Computation, but it seems as though every second ICT student in Helsinki wants a copy. 

Mrs. Tammivuori talked to us yesterday about a variety of sources for our information. So far I'm using the following:

- Khan Academy (Calculus)
- The books I mentioned above

I think I need more internet source, despite the quality of my printed reference material. I should probably have my first basic crypto cipher by next week, depending on how easy of a read my new books are. 


## 17/09/11

Reading through An Introduction to Mathematical Cryptography right now, this is a goldmine of information, especially the bibliography, seeing as it included prof. selected texts and lots of relevant background information.

> Your opponent always uses her best strategy to defeat you, not the strategy that you want her to use. Thus the secu- rity of an encryption system depends on the best known method to break it. As new and improved methods are developed, the level of security can only get worse, never better.
> - Joseph H. Silverman

## 24/09/11

Yikes! Haven't filled out an entry in quite a while… Things have been quite hectic regarding my school life and my personal project. In a terrible turn of events, Mr. Komonen's been hospitalized and I therefore have no personal project supervisor in the foreseeable future. 

On a happier note, I am trudging along my Introduction to Cryptography book, however it's getting pretty complicated, so I've scheduled a meeting on Tuesday with Mr.Tyler to make sure I understand everything that I'm reading. 

Oh yeah, and I just received my Applied Cryptography book from the Iso Omena Library, which looks pretty awesome. This book is a lot more in my element because it forgoes the mathematical explanation of all of the concepts for coded examples, which I find far easier to understand. Due the importance of maths in my project, I'm gonna ask Mr. Tyler if he could be my interim supervisor and if he's too busy maybe Mrs. Baranwal.

## 26/09/11

My deadline for this month is fast approaching and I still don't know if Mr. Komonen is all right. I really hope he's doing well. I'm gonna shoot him an email tomorrow if he still hasn't showed up to school. On an unrelated note, our S.S. classes are really taking a hit. 

I think I will reschedule my meeting with Mr. Tyler from tomorrow to Wednesday or Thursday so I can complete some of the questions and ask something interesting. If Mr. Komonen is not back by Friday, I'm gonna ask if Mr. Tyler could be my supervisor.

## 01/10/11

Mr. Tyler is now my supervisor. I just realized I should probably include some of my findings from my research stage in this journal, not just my ideas and planning. This is a little difficult because my notes are more technically oriented, therefore, I think I will begin writing my technical findings in a separate journal. I'm currently working on a bunch of stuff including (but not limited to):

* Primality testing
* Modulo
* Divisibility
* Fundamental theory of numbers
* Symmetric and Asymmetric systems

And much, much more!!!

## 05/10/11

Today I was reading a very interesting article which was not really related to my personal project, but wholly related to computer science and software engineering. The author of node.js (a popular server-sider javascript framework), Ryan Dahl, wrote a provocative article[1] about the way UNIX systems were poorly structured to scale as technology improves. 

[1]:(https://plus.google.com/115094562986465477143/posts/Di6RwCNKCrf)

He states that due to this poor design, problems are soon to follow both in our programs and in our hardware. Which will eventually slow down our advances in the field of C.S. because we will eventually need to rebuild a lot of software and hardware from scratch. He states that eventually, due to poor coding practice, poor design, poor hardware and poor software implementations, the complexity of the solutions that computers provide us are going to exceed the complexity of the problems we set out to solve; at which point computing becomes obsolete.

I was disheartened to find out that the fundamental architecture of computer is wrong. For the longest time, I have know that it is far easier to write bad code than good code, but I never realized that the fundamental architecture of computing was doomed to failure. From this day forth, whenever I code I'll make sure to do what I can to reduce the complexity of my programs and increase efficiency. 

> In the past year I think I have finally come to understand the ideals of Unix: file descriptors and processes orchestrated with C. It's a beautiful idea. This is not however what we interact with. The complexity was not contained. Instead I deal with DBus and /usr/lib and Boost and ioctls and SMF and signals and volatile variables and prototypal inheritance and _C99_FEATURES_ and dpkg and autoconf.

> There will come a point where the accumulated complexity of our existing systems is greater than the complexity of creating a new one. When that happens all of this sh*t will be trashed. We can flush boost and glib and autoconf down the toilet and never think of them again.
> - Ryan Dahl

## 08/10/11

October break has started and I plan to use this time to get through a large portion of the cryptography book and make sure I have complete notes for my essay.

Renewing library books and stuff.

Also just finished writing a complete and final version of my basic `shifcipher` which can be found on github [here][1].

[1]:(https://github.com/siddMahen/shiftcipher)

It was relatively simple, and I think that the next sub-project will be several times more interesting. Mr. Komonen has yet to reply to my email, and he is still not at school. I sincerely hope he gets well.

>We can learn from ourselves and go beyond our original programming. - Zack Morris

Can we?

## 13/10/11

**Really** getting in to the theoretical and mathematical side of this now. I think I have a pretty solid understanding of the first chapter of An Introduction to Cryptography (mind you, there are only 8 chapters in total).

I'm finishing up the questions in the first chapter while beginning to read the second chapter. I've also filled out all of my notes for the first chapter, which took me quite a long time to do, but really helped cement my understanding of the topic.

I'm also gonna start reading a more computer scienceish book on cryptography, which is pretty cool because I find it much easier to analyze computer implementations of cryptographic work than their mathematical proofs.

## 22/10/11

Still reading, however, my book list has expanded and I'm looking into a bunch of other interesting things including:

* Random bit generation using cellular automata

* The Application of Cryptography book with examples in C

* Public key systems for encryption along with Diffie-Hellman key exchange

* Perfect secrecy and perfect forward secrecy

Mr. Komonen's is gonna be back by next week, so that's good. 

Just learning, thinking and absorbing all of the information that's there. I think I will lessen the detail in my notes, because as of this point, they will become far to large to allow me to keep them feasibly. Perhaps a short paragraph on each subtopic with the necessary equations written down, nothing more.

[Rule 30 - Crypto](http://www.stephenwolfram.com/publications/articles/ca/85-cryptography/1/text.html)

## 01/11/11

Haven't done any PP work in a while, should really update my log soon. Mr. Komonen is back, so that's good, but I think I'll continue to see Mr. Tyler once in a while to help with the mathematics.

I should start devoting more of my weekends to this…

## 09/11/11

In the process of building the block cipher for stage two of my project. Applied Cryptography is an amazing resource. I have sorta moved away from the very mathematical side of cryptography and into the more computer-ish side. Currently reading several different chapters in the book, gonna be making another Notes entry pretty soon to cover what I have learned. Basically, looking at examples of block cipher algorithms that were implemented and seeing how I could implement my own (DES, GOST, Blowfish, IDEA).

Also thinking of ideas for my final cipher. Really interested in integrating Rule 30 with a probabilistic encryption algorithm, similar to Manual Blum and Goldwasser algorithm (see page 553, and sec. 17.9), expect using Rule 30. Depending on how much entropy there is when choosing initial configurations of Rule 30. If the initial configuration becomes a problem, I think I can implement a rule proven to be very sensitive to initial config, such as Rule 101, and then XOR that on a random bit from 30 with a set initial config.

## 27/11/11

Literally just uploaded the (close to) final copy of my block cipher on Github[1]. That was very, very, very interesting. Gonna see if I can book a personal project meeting with Mr. Tyler and Mr. Komonen to have them check out my project. Once again, this requires another entry into Notes to fully explain. 

Quickly thought, the algorithm is a combination of GOST, IDEA and a few of my own ideas. It is an 8 round iterative algorithm which takes a 64 bit block and a 256 bit key as input and outputs a 64 bit encrypted block. The algorithm uses 8 S-boxes extracted from GOST and a "mangling" algorithm similar to the one found in IDEA, except with a few modifications.

As I said before, I have yet to test my algorithm on speed and memory usage, but as a rough indicator, my algorithm stores 256 bits in the key and another 128 bits in the S-boxes, to a total of 384 bits or 48 bytes.

[1]:(https://github.com/siddMahen/blockcipher)

## 27/12/11

It's been over a month since I last updated my log. I haven't done a ton of coding work related to my personal project, mostly due to the (winter) break, however, I have been thinking a lot about the final cipher I will be creating as well as the essay I will have to write. Lots of ideas seem interesting, and I'm having a lot of trouble finding something that is both graspable, implementable as well as mathematically provable (for me). Here are some of the topics I have been looking at:

1. Expander graph based ciphers [1]:

Iffy because there hasn't been much symmetric/asymmetric + PKS, mostly used for hashes, so it's not the "kind" of work I'm looking for.

2. Probabilistic encryption schemes [2]:

Although this field is sort of washed out, but still cool.

3. Elliptic curve cryptosystems [3]:

This is my most promising field. I think it is mathematically challenging enough, yet graspable (if only on a superficial level). It is covered later in Introduction to Cryptography, around chapter 6, so I still have quite a bit of reading to do.

[1]:(http://research.microsoft.com/en-us/um/people/klauter/HashMarch13%202007.pdf)

[2]:(http://en.wikipedia.org/wiki/Blum%E2%80%93Goldwasser_cryptosystem)

[3]:(http://en.wikipedia.org/wiki/Elliptic_curve_cryptography)

## 09/01/12

Lots of reading, looking at RFC1750 on randomness… [1]

[1]:(http://www.ietf.org/rfc/rfc1750.txt)

## 18/01/12

Just lots of reading, lots of research. Finishing chapters 4 and 5 of Introduction to Cryptography. School work is beginning to pile up at this point, so my personal project work time is taking the toll. However, I try to read as much as I can.

I read a little bit about Markov Models and Hidden Markov models too. Those seem very, very cool for random number generation and testing the security of random functions and such. 

But I digress. 

I think my final algorithm will be some sort of ECC algorithm. The math is going down okay at this point; the ECDLP seems to be identical to the DLP except with a new elliptic group twist. I have also picked up a few very cool cryptanalytic tools such as Pollards rho method and it's extension into the elliptic field. Things are going well.

As I said before, lots of reading...

## 18/02/12

Ski break is starting. My school work has finally subsided and I plan to complete my implementation of ECC. Finally understand all of the math behind it. This should not be that difficult.

ECC presents itself as a very interesting and efficient alternative to normal DLP-based ciphers. Check out these stats from 
the NSA. They state that to maintain a security level equivalent to that of a 3072 bit key in RSA (read strong DLP) you only need 256 bit key in ECDLP! Thats 10x less space cost! Furthermore, this decrease in space cost increases as the security bits are increased!

---------------------|-----------------------
Security Level(bits) | Ratio of Cost: DC - EC
---------------------|-----------------------
			80					  				3:1
---------------------|-----------------------
			112				  				6:1
---------------------|-----------------------
			128				  				10:1
---------------------|-----------------------
			192				  				32:1
---------------------|-----------------------
			256				  				64:1
---------------------|-----------------------

Freaking amazing stuff. Obviously, however, there is a slight calculation over head as computation over the EC can get expensive.

[1]:(http://www.nsa.gov/business/programs/elliptic_curve.shtml)

## 27/02/12

I booked a meeting with Mr. Tyler and we ironed out the details about the structure of my essay and what kinds of stuff I should talk about. That meeting went pretty well.
He said that I'm doing well so far, but then again, he had to fail the last student he 
mentored, so I guess the bar is pretty low.

You can find a working draft of my structure 
draft here:

[1]:(https://docs.google.com/document/d/13SH2R-HuMUG-odswxvmecWfGY3Q3vyzUfDxAoepxCJo/edit)

## 17/03/12

Finally finished the first draft of the personal project reflection essay. I'm really buckling down this weekend and getting this stuff done. I finished the goal and the selection of sources portions, in about 820 words. I thinks that's pretty good, because the minimum in 1500, and I haven't even gotten to the meat and potatoes of my essay yet. Next week, it's every night working on the crypto essay…

Emailing them to my supervisors now.
Mr. Komonen, from what I have heard, has left yesterday for something or the other, therefore I'll be looking to Mr. Tyler for
support. However, I should email it to him out of courtesy any who.

On another note, I was looking up some secret NSA stuff and this popped up in google. It would be very cool to work there:

[1]:(http://cryptome.org/nsa-nse/nsa-nse-01.htm)

## 20/03/12

Since I'm writing my report and my reflection using LaTeX, I've had to learn a little bit of it.

Here are some websites I've been using:

[1]:(http://www.tex.ac.uk/tex-archive/info/symbols/comprehensive/symbols-a4.pdf)

[2]:(ftp://ftp.funet.fi/pub/TeX/CTAN/macros/latex/contrib/tocloft/tocloft.pdf)

[3]:(http://en.wikibooks.org/wiki/LaTeX/Document_Structure)

The first is a comprehensive guide to symbols and their representation in LaTeX.

The second is a manual for a module I'm using to style certain elements in my paper.

The last link is the Wikibook I used to become familiar with TeX. It was pretty easy to learn, but the book helped guide me towards figuring out some of the finer points.

Very cool stuff.. Very useful as well.

## 14/04/12

Just finishing up the second section of my product, which was probably the most difficult one.

Was discussing linear cryptanalytical methods of breaking block ciphers in my product, and therefore had to expand this linear expression of an S-box. Normally, I would have written a program to do so, however, I just couldn't get it to work out in the amount of time that I had. So I had to do it by hand. 

It was an immense pain.

Aside from understanding some of the more mathematical content of this project, such as ECC, this was the most painful to do.

I think my project is running a little latter than it should.

I should have done more work regarding the essay and the product at an earlier stage, despite the fact that I hadn't finished all of my research. Although now, I am certain that what I'm doing it really reflective of what I have learned.

Actually, scratch that, the product isn't really a true reflection of all of what I learned. A lot of what I learned isn't visible in the product. A lot of what I taught myself is completely off the books. A lot of what I taught myself isn't even directly related to my actual project.

I should stop myself here, and save it for the project essay though…

Just want to say, to who ever is marking this, that you will probably not know how much effort and time I invested in learning things which didn't even make it into my final project, either because of their sheer complexity, or because I did not have enough time to really truly profoundly understand them.

Oh btw, the latest version of my project can be found [here](https://github.com/siddMahen/PPReport/raw/master/LaTeX/doc.pdf).

## 28/04/12

Finally finished up the greater part of my project, now
I just need to clear up some minor things like copy/paste
the code examples in from my github repos and make sure I don't have any stupid hbox overflows in my draft.

I got feedback from Mr. Tyler as well, during our last meeting, which was very helpful. He took a look at both my reflection essay draft and my product draft and marked em up for me. Glad he did, because I make so many stupid mistakes. While I'm talking about drafts, I might as well
mention that I finally figured out a way to do spellcheck
in VIM!!!!! This is awesome because previously, I would
copy my entire PP essays into Pages and then try to spell check it, but Pages being dumb, doesn't recognize simple things such as dashes marking long words ("cryptography"). What a relief!

I really think that I should have planned this whole report writing thing better. I mean, sure now its done, but I don't think all of the down to the minute stress was worth it. When I do my EE next year I'm gonna be sure
to finish it a whole damned month before it's due, so I can rewrite it k times and be free of this crushing stress…

Well, I'm gonna need to turn this markdown into a format my supervisor is going to read, because I doubt he has the program I built to type this up installed on his computer.

So this is goodbye.

As a final note, I want to say that the personal project
wasn't really as bad as people make it out to be, and I think I had a lot of fun. Sure reflecting isn't on my bucket list but I didn't die, and I don't think my essay is half bad.

Oh maybe I should talk about how I solved the ECC problem, as I think I've only kept it in my head since now.. What messed up order, you can tell it's late can't you…

I used a variation of the Shank's Baby Step Giant step algorithm for DLP. It was much less effective than the rho, but I didn't want to explain the whole orbit business and the ideas behind Shank's were simpler so I just adapted that. They both take `O(sqrt p)` time anyway. I also didn't mention the speedup for rho, but that gets even more complex.

As I said before, gotta wrap this up. It's been good.  