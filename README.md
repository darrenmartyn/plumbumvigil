# plumbumvigil
A "directory/file" fuzzer/buster that ate some lead paint. I bodged this together for content discovery in certain specific situations.

Basically, say you have a directory of webapp source code, like wordpress or whatever, and a site that runs probably that app.  
This basically takes the directory of stuff, walks over it, generates a list of paths, and does some path enumeration.  
Chucks out a CSV with response codes, response sizes, response-content md5, local file path, local file md5... etc. So you can compare static content too.  
This can be the basis for some pretty neat fingerprinting stuff, or maybe help you work out endpoints that do odd shit.

It by default proxies through burp, and is intended to be used alongside something like param-miner or parameth or similar.

It is also very slow because I wasn't fucked using threading, and am still coding in python2 in 2021 largely because I'm a dinosaur who dislikes putting brackets on my print statements.

Todo:  
Commit code to Github on Monday once I've fixed some stupid bugs.  
Wait for other people to find bugs I didn't.  
Promise to fix those bugs.  
Maybe fix those bugs, but probably won't.
Wait for a frustrated user to fix the bugs for me.
