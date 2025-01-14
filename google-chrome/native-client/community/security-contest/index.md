---json {"title":"Security Contest Archive"} ---

{% include 'partials/nacl-warning.njk' %}

---

- <a href="#contest-overview" id="id2" class="reference internal">Contest overview</a>
- <a href="#contest-winners" id="id3" class="reference internal">Contest winners</a>
- <a href="#panel-of-judges" id="id4" class="reference internal">Panel of judges</a>

  - <a href="#chair" id="id5" class="reference internal">Chair</a>
  - <a href="#judges" id="id6" class="reference internal">Judges</a>

- <a href="#additional-information" id="id7" class="reference internal">Additional information</a>

The Native Client team at Google has gone to exceptional measures to make Native Client a secure system, including holding a public security contest. This page archives information from that contest, including the list of contest winners and the lineup of security experts who served as judges.

Although the security contest has ended, the Native Client team welcomes your continued involvement in the project. You can help by submitting bugs and participating in the Native Client discussion group.

## Contest overview

The Native Client team held a contest in 2009 to test the security of Native Client and help make the system more secure. Participants were invited to discover security bugs in Native Client technology in order to compete for cash prizes.

Here was the challenge put forth by the Native Client team:

Do you think it is impossible to safely run untrusted x86 code on the web? Do you want a chance to impress a panel of some of the top security experts in the world? Then submit an exploit to the Native Client Security contest and you could also win cash prizes, not to mention bragging rights.

The contest judges evaluated exploits designed to defeat Native Client security measures based on severity, scope, reliability, and style. The winning teams and entries are listed below.

## <span id="id1"></span>Contest winners

The Native Client team thanks everyone who participated in the contest for their contributions to improving the quality and security of the Native Client system. The judges reviewed the submitted exploits and identified the following teams as winners:

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><img src="/docs/native-client/images/medal-64_1st.png" alt="First place medal" class="first last" /></td><td><p><strong>Team</strong>: Beached As</p><p><strong>Members</strong>: Mark Dowd, Ben Hawkes</p><p><strong>Submitted issues</strong>: 50, 51, 52, 53, 55, 56, 57, 58, 59, 60, 62, 63</p><p>Mark Dowd and Ben Hawkes are application security specialists hailing from Australia and New Zealand, respectively. Mark works for IBM ISS X-Force R&amp;D, whereas Ben currently performs independent research while simultaneously pursuing a mathematics and computing science degree. Both have uncovered major security flaws in ubiquitous Internet software, in terms of both exploitable bugs and weaknesses in system protection mechanisms. Both have spoken at numerous security conferences in recent years, including BlackHat, Ruxcon, KiwiCon, and Cansec West.</p></td></tr><tr class="even"><td><img src="/docs/native-client/images/medal-64_2nd.png" alt="Second place medal" class="first last" /></td><td><p><strong>Team</strong>: CJETM</p><p><strong>Members</strong>: Jason Carpenter, Eric Monti, Chris Rohlf</p><p><strong>Submitted issues</strong>: 42, 44, 49, 70</p><p>Team CJETM is comprised of security vulnerability researchers Chris Rohlf, Jason Carpenter and Eric Monti. All three have abused software professionally for a long time.</p></td></tr><tr class="odd"><td><img src="/docs/native-client/images/medal-64_3rd.png" alt="Third place medal" class="first last" /></td><td><p><strong>Team</strong>: 0xdead</p><p><strong>Members</strong>: Gabriel Campana</p><p><strong>Submitted issues</strong>: 45</p><p>Gabriel Campana is a security researcher working at Sogeti ESEC R&amp;D labs. His research interests are mainly focused on vulnerability research, exploitation methods, and Linux kernel security. Lately he has been working on automated vulnerability research, especially fuzzing. In his spare time, he plays with embedded network devices.</p></td></tr><tr class="even"><td><img src="/docs/native-client/images/medal-64_4th.png" alt="Fourth place medal" class="first" /><p>(tie)</p></td><td><p><strong>Team</strong>: teamfkmr</p><p><strong>Members</strong>: Daiki Fukumori</p><p><strong>Submitted issues</strong>: 66, 67</p><p>Daiki Fukumori is a web security researcher. He has given talks at POC Korea and AVTokyo on Web 2.0 Hacking, and he introduced Native Client security at Shibuya.pm. He currently has an interest in cloud security.</p></td></tr><tr class="odd"><td><img src="/docs/native-client/images/medal-64_4th.png" alt="Fourth place medal" class="first" /><p>(tie)</p></td><td><p><strong>Team</strong>: Alex Rad</p><p><strong>Members</strong>: Alex Radocea</p><p><strong>Submitted issues</strong>: 81</p><p>Alex Radocea is a 20-year old student at Rensselaer Polytechnic Institute. In the realm of computer security he is really excited about proactively designed technology which can help wipe out entire bug classes. Currently he is helping improve Native Client through Google Summer of Code.</p></td></tr></tbody></table>

## <span id="contest-judges"></span>Panel of judges

Google recruited the following group of distinguished security experts to serve as judges for the Native Client security contest:

### Chair

<table><tbody><tr class="odd"><td>Edward Felten</td></tr><tr class="even"><td>Princeton University</td></tr><tr class="odd"><td><a href="http://www.cs.princeton.edu/~felten/" class="reference external">http://www.cs.princeton.edu/~felten/</a></td></tr></tbody></table>

### Judges

<table><colgroup><col style="width: 33%" /><col style="width: 33%" /><col style="width: 33%" /></colgroup><tbody><tr class="odd"><td>Alex Halderman</td><td>Niels Provos</td><td>Bennet Yee</td></tr><tr class="even"><td>University of Michigan</td><td>Google</td><td>Google</td></tr><tr class="odd"><td><a href="http://www.cse.umich.edu/~jhalderm/" class="reference external">http://www.cse.umich.edu/~jhalderm/</a></td><td><a href="http://www.citi.umich.edu/u/provos/" class="reference external">http://www.citi.umich.edu/u/provos/</a></td><td><a href="http://www.bennetyee.org/" class="reference external">http://www.bennetyee.org/</a></td></tr><tr class="even"><td>Brad Karp</td><td>Stefan Savage</td><td>Nickolai Zeldovich</td></tr><tr class="odd"><td>University of College London</td><td>University of California San Diego</td><td>MIT</td></tr><tr class="even"><td><a href="http://www.cs.ucl.ac.uk/staff/B.Karp/" class="reference external">http://www.cs.ucl.ac.uk/staff/B.Karp/</a></td><td><a href="http://www.cs.ucsd.edu/~savage" class="reference external">http://www.cs.ucsd.edu/~savage</a></td><td><a href="http://people.csail.mit.edu/nickolai/" class="reference external">http://people.csail.mit.edu/nickolai/</a></td></tr><tr class="odd"><td>Greg Morrisett</td><td>Dan Wallach</td><td><div class="first last"> </div></td></tr><tr class="even"><td>Harvard University</td><td>Rice University</td><td><div class="first last"> </div></td></tr><tr class="odd"><td><a href="http://www.eecs.harvard.edu/~greg/" class="reference external">http://www.eecs.harvard.edu/~greg/</a></td><td><a href="http://www.cs.rice.edu/~dwallach/" class="reference external">http://www.cs.rice.edu/~dwallach/</a></td><td><div class="first last"> </div></td></tr></tbody></table>

## Additional information

For additional information about the Native Client security contest, see the archived <a href="/docs/native-client/community/security-contest/contest-announcement" class="reference internal"><em>Contest Announcement</em></a>, <a href="/docs/native-client/community/security-contest/contest-faq" class="reference internal"><em>FAQ</em></a> and <a href="/docs/native-client/community/security-contest/contest-terms" class="reference internal"><em>Terms &amp; Conditions</em></a>.

If you’d like to get involved with Native Client, you can:

- Use the <a href="/docs/native-client/sdk/download" class="reference external">Native Client SDK</a> to build Native Client web applications.
- Submit <a href="http://code.google.com/p/nativeclient/issues/list" class="reference external">bugs</a> and participate in the Native Client <a href="http://groups.google.com/group/native-client-discuss" class="reference external">discussion group</a>.
- Contribute to the <a href="http://code.google.com/p/nativeclient/" class="reference external">Native Client open-source project</a>.
