---json {"title":"Publications and Presentations"} ---

{% include 'partials/nacl-warning.njk' %}

---

This page lists Native Client and Portable Native Client talks, demos, and publications from various conferences and academic symposiums.

## Recent talks and demos

<table><thead><tr class="header"><th>Date</th><th>Event</th><th>Talk</th></tr></thead><tbody><tr class="odd"><td>2013/05/16</td><td><a href="https://developers.google.com/events/io/2013" class="reference external">Google I/O 2013</a></td><td><a href="https://www.youtube.com/watch?v=5RFjOec-TI0" class="reference external">Introduction to Portable Native Client</a></td></tr><tr class="even"><td>2012/12/11</td><td><a href="https://developers.google.com/live/" class="reference external">Google Developers Live</a></td><td><a href="https://developers.google.com/live/shows/7320022-5002/" class="reference external">Native Client Acceleration Modules</a> Learn how to use Native Client to deliver performance where it counts (<a href="https://github.com/johnmccutchan/NaClAMBase/" class="reference external">source code</a>)</td></tr><tr class="odd"><td>2012/07/26</td><td><a href="http://casualconnect.org/seattle/content.html" class="reference external">Casual Connect Seattle 2012</a></td><td><a href="https://www.youtube.com/watch?v=RV7SMC3IJNo" class="reference external">Take your C++ To the Web with Native Client</a> Includes an overview of Native Client technology, porting legacy applications from the Windows desktop, and current third-party use of Native Client in middleware and games</td></tr><tr class="even"><td>2012/06/28</td><td><a href="https://developers.google.com/events/io/2012" class="reference external">Google I/O 2012</a></td><td><a href="https://www.youtube.com/watch?v=1zvhs5FR0X8" class="reference external">Native Client Live</a> Demonstrates how to port an existing C application to Native Client using a Visual Studio add-in that lets developers debug their code as a trusted Chrome plugin</td></tr><tr class="odd"><td>2012/06/28</td><td><a href="https://developers.google.com/events/io/2012" class="reference external">Google I/O 2012</a></td><td><a href="https://www.youtube.com/watch?v=KOsJIhmeXoc" class="reference external">The Life of a Native Client Instruction</a> (<a href="https://nacl-instruction-io12.appspot.com" class="reference external">slides</a>)</td></tr><tr class="even"><td>2012/03/05</td><td><a href="http://www.gdcvault.com/free/gdc-12" class="reference external">GDC 2012</a></td><td><a href="https://www.youtube.com/watch?v=R281PhQufHo" class="reference external">Get Your Port On</a> Porting Your C++ Game to Native Client</td></tr><tr class="odd"><td>2011/08/12</td><td>—</td><td><a href="https://www.youtube.com/watch?v=g3aBfkFbPWk" class="reference external">Native Client Update and Showcase</a></td></tr><tr class="even"><td>2010/11/04</td><td><a href="http://llvm.org/devmtg/2010-11/" class="reference external">2010 LLVM Developers’ Meeting</a></td><td><a href="http://llvm.org/devmtg/2010-11/videos/Sehr_NativeClient-desktop.mp4" class="reference external">Portable Native Client</a></td></tr></tbody></table>

## Publications

<table><thead><tr class="header"><th>Title</th><th>Authors</th><th>Published in</th></tr></thead><tbody><tr class="odd"><td><a href="http://research.google.com/pubs/archive/37204.pdf" class="reference external">Language-Independent Sandboxing of Just-In-Time Compilation and Self-Modifying Code</a></td><td>Jason Ansel, Petr Marchenko, <a href="http://research.google.com/pubs/ulfar.html" class="reference external">Úlfar Erlingsson</a>, Elijah Taylor, <a href="http://research.google.com/pubs/author37895.html" class="reference external">Brad Chen</a>, Derek Schuff, David Sehr, <a href="http://research.google.com/pubs/author38542.html" class="reference external">Cliff L. Biffle</a>, Bennet S. Yee</td><td>ACM SIGPLAN Conference on Programming Language Design and Implementation (PLDI), 2011</td></tr><tr class="even"><td><a href="http://research.google.com/pubs/pub35649.html" class="reference external">Adapting Software Fault Isolation to Contemporary CPU Architectures</a></td><td>David Sehr, Robert Muth, <a href="http://research.google.com/pubs/author38542.html" class="reference external">Cliff L. Biffle</a>, Victor Khimenko, Egor Pasko, Bennet S. Yee, Karl Schimpf, <a href="http://research.google.com/pubs/author37895.html" class="reference external">Brad Chen</a></td><td>19th USENIX Security Symposium, 2010, pp. 1-11</td></tr><tr class="odd"><td><a href="http://research.google.com/pubs/pub34913.html" class="reference external">Native Client: A Sandbox for Portable, Untrusted x86 Native Code</a></td><td>Bennet S. Yee, David Sehr, Greg Dardyk, <a href="http://research.google.com/pubs/author37895.html" class="reference external">Brad Chen</a>, Robert Muth, Tavis Ormandy, Shiki Okasaka, Neha Narula, Nicholas Fullagar</td><td>IEEE Symposium on Security and Privacy (Oakland ‘09), 2009</td></tr><tr class="even"><td><a href="http://nativeclient.googlecode.com/svn/data/site/pnacl.pdf" class="reference external">PNaCl: Portable Native Client Executables</a></td><td>Alan Donovan, Robert Muth, Brad Chen, David Sehr</td><td>February 2010</td></tr></tbody></table>

## External Publications

In these articles outside developers and Google engineers describe their experience porting libraries and applications to Native Client and Portable Native Client. They share their insights and provide some tips and instructions for how to port your own code.

### Porting Nebula3 to Portable Native Client

Andre Weissflog ported his Nebula3 engine to Portable Native Client (see <a href="http://www.flohofwoe.net/demos.html" class="reference external">his demos</a>). He discusses <a href="http://flohofwoe.blogspot.de/2013/08/emscripten-and-pnacl-build-systems.html" class="reference external">build systems</a> and <a href="http://flohofwoe.blogspot.de/2013/09/emscripten-and-pnacl-app-entry-in-pnacl.html" class="reference external">app entry</a>.

### Porting Go Home Dinosaurs

<a href="http://firehosegames.com" class="reference external">Fire Hose Games</a> developed a new webgame <a href="https://chrome.google.com/webstore/detail/icefnknicgejiphafapflechfoeelbeo" class="reference external">Go Home Dinosaurs</a>. It features tower defense, dinosaurs, and good old fashioned BBQ. This article explains their experiences developing for Native Client including useful lessons learned to help you get started.

<a href="http://www.gamasutra.com/view/feature/175210/the_ins_and_outs_of_native_client.php" class="reference external">Read more</a>

### Porting Zombie Track Meat

<a href="http://www.fuzzycubesoftware.com" class="reference external">Fuzzycube Software</a>, traditionally a mobile game development studio, talks about their adventure into the web, porting the undead decathlon <a href="https://chrome.google.com/webstore/detail/jmfhnfnjfdoplkgbkmibfkdjolnemfdk/reviews" class="reference external">Zombie Track Meat</a> from Objective C to Native Client.

<a href="http://fuzzycube.blogspot.com/2012/04/zombie-track-meat-post-mortem.html" class="reference external">Read more</a>

### Porting AirMech

<a href="http://carbongames.com/" class="reference external">Carbon Games</a> chose Native Client as a solution for cross-platform delivery of their PC game <a href="https://chrome.google.com/webstore/detail/hdahlabpinmfcemhcbcfoijcpoalfgdn" class="reference external">AirMech</a> to Linux and Macintosh in lieu of native ports. They describe the porting process on their blog.

<a href="http://carbongames.com/2012/01/Native-Client" class="reference external">Read more</a>
