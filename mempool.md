*Uncurated list - to be curated, categorized and described*.

## Secure Ethereum messaging study compendium
[TOC]

## Starting point
https://medium.com/message/everything-is-broken-81e5f33a24e1

## Comparisons
* [Crazy list of messengers and features](https://docs.google.com/spreadsheets/d/1-UlA4-tslROBDS9IqHalWVztqZo7uxlCeKPQ-8uoFOU/edit#gid=0) - lots of messengers and lots of features!

* [SoK: Secure Messaging](http://cacr.uwaterloo.ca/techreports/2015/cacr2015-02.pdf) - overview of security properties across various schemas

## Whisper

### Talks and specs

In general, some of the links are dated 2015 whereas the protocol has moved to version 6 by now..

* [EIP-627](http://eips.ethereum.org/EIPS/eip-627) - Vlad Gluhovsky's proposal to document the protocol. There's some interesting discussion in the [PR thread](https://github.com/ethereum/EIPs/pull/627#discussion_r124582523) about supporting multiple topics per message - now a parity extension (`psh`)
* [Whisper PoC Protocol spec](https://github.com/ethereum/wiki/wiki/Whisper-PoC-2-Protocol-Spec) - this looks like one of the most detailed accounts of the thinking that went into whisper
* [Whisper Proposal - Ethereum Wiki](https://github.com/ethereum/wiki/wiki/Whisper) - some high-level overview and background discussion
* [Whisper Overview - Ethereum Wiki](https://github.com/ethereum/wiki/wiki/Whisper-Overview) - Useful section on use cases describing the effect of supplying different combinations of keys and encryption
* [DEVCON1: Shh! Whisper - Gavin Wood](https://www.youtube.com/watch?v=U_nPoBVLPiw)
* [DEVCON3: Whisper: Achieving Darkness - Vlad Gluhovsky, Guillaume Ballet](https://youtu.be/vXVcuWvR5Z0?t=10)
* [Scuttlebutt talks](https://www.scuttlebutt.nz/talks)

### Status notes and usages
* [Call notes, Vlad/Status](https://docs.google.com/document/d/1RfGIYpZ8xOJKBD0w1F-DtwCKTA43O4zyWhxFtLtdLNc/edit) 
* [Status whisper research](https://wiki.status.im/Research_Whisper_Status) - V5-V6 difference, status implementation notes and what status needs the procotocol for
* [Open issues brainstorming](https://docs.google.com/document/d/1Cw3LA1r6ItLDp8bMFvIxQMxYjnzEVOcHuZJz8gRa7HE/edit#) - round-table on what whisper pain points are held with our Whisper devs (2018-04-18)
* [Messsage spec, clojure](https://github.com/status-im/status-react/blob/develop/src/status_im/transport/message/transit.cljs)
* [Protocol background work doc](https://docs.google.com/document/d/1Qh2h07T_qepzEJ7IytmxwIdQAOsGHrvhXwZxuZtbwgc/edit)
* [Status wiki whisper docs, including V5/V6 comparison](https://wiki.status.im/index.php?title=Research_Whisper_Status)
* [How-status-uses-whisper thread](https://status-im.slack.com/archives/C8QP8S5UH/p1523495849000201)
* [Mail-server topic-vs-bloom discussion](https://status-im.slack.com/archives/C8QP8S5UH/p1523256511000120)
* [JS usage example](https://gist.github.com/noman-land/410fbfd632b61d29e78120b2475e9955) - how to post a message to the chat

### Push notification
* [Push notifications v2](https://github.com/status-im/ideas/blob/master/ideas/086-push-notif-v2/README.md) - idea for the next iteration of PN
* [Whisper push notifications](https://github.com/status-im/status-go/wiki/Whisper-Push-Notifications) - this looks like the most recent one (?)
* [Push notification market](https://wiki.status.im/Decentralized_Push_Notification_Market)
* [Where we are at](https://wiki.status.im/Push_notifications_-_Where_we_are_at)
* [Original proposal](https://docs.google.com/document/d/1OgjnY8ps8lVA4dIohwkfGK9HVt0nZxEWbuNdb7BX5-o/edit#heading=h.kjam5hcc2nif)

## PSS - postal service over swarm
* [Swarm PSS](https://github.com/ethersphere/go-ethereum/blob/a12c003114ab702a820428c2c6ef3d950e1e0a55/swarm/pss/ARCHITECTURE.md) - architectural notes, crucial quote: `Optionally routing can be turned off, forcing the message to be sent to all peers, similar to the behavior of the whisper protocol.`
[PSS = bzz whispered](https://gist.github.com/zelig/d52dab6a4509125f842bbd0dce1e9440) - initial PSS idea description
[PSS hacking](https://hackmd.io/dDvTNlSWS6601GQ9LbEY8Q#) - Group chat using mutable resources from Mainframe / PSS

## Related ETH projects
* [Mainframe](https://mainframe.com/) - Swarm/PSS user?
* [Bloom](https://blog.hellobloom.io/introducing-bloom-payment-channels-enabled-by-ethereum-whisper-1fec8ba10a03) - whisper use-cases
* [Origin](https://medium.com/originprotocol/introducing-origin-messaging-decentralized-secure-and-auditable-13c16fe0f13e) - distributed log-based messenger, as well as an IPFS-based replicated log database

## Secure messaging - Non-ethereum
* [Building a secure messenger - EFF](https://www.eff.org/deeplinks/2018/03/building-secure-messenger)
* [Tox](https://wiki.tox.chat/users/techfaq) - distributed secure chat, DHT-based P2P lookup with lots of clients
* [Briar](https://briarproject.org/how-it-works.html) - messaging app employing several censorship-resitance techniques, like direct device-to-device comms (bluetooth, wifi), tor routing,
* [FireChat](https://www.opengarden.com/firechat.html) - mesh comms, closed source
* [Wire](https://wire.com/en/security/) - Open source messenger with lots of transparency around security
* [Vuvuzela](https://vuvuzela.io/) - metadata-leak-resistant chat protocol / application, also alpenhorn that takes care of contact setup / key exchange
* [cwtch](https://cwtch.im/) - extension of the Ricochet protocol that provides asynchronous, offline and multi-party metadata resistant messaging
* [Scuttlebutt](https://www.scuttlebutt.nz) - open source, p2p replicated ledgers. 3 year old ecosystem, in active use. Offline friendly. Recent Android app (runs peer instance) https://manyver.se

## Security / encryption
* [X3DH](https://signal.org/docs/specifications/x3dh/) - key exchange protocol for async comms with an intermediary server involved
* [On Ends-to-Ends Encryption: Asynchronous Group Messaging with Strong Security Guarantees](https://eprint.iacr.org/2017/666.pdf) - Continuation of Signal Double Ratchet
* [Megolm](https://git.matrix.org/git/olm/about/docs/megolm.rst) - An AES-based cryptographic ratchet intended for group communications

## Alternate protocol
* [Salsify](https://snr.stanford.edu/salsify/) - real-time Internet video that jointly controls a video codec and a network transport protocol

## PSS Open issues
* Mutable resources, how to find last message? binary search?
* Key exchange
* Payload format

###### tags: `messaging` `whisper` `study`



## Laundry list

Papers and resources related to protocol work. Holy mix of field of vague awareness. Some read in detail, some skimmed, some barey looked at.

Solid overview / categorization as a starting point:
- http://cacr.uwaterloo.ca/techreports/2015/cacr2015-02.pdf

Anonymity:
- The Differences Between Onion Routing and Mix Networks
 https://crypto.is/blog/mix_and_onion_networks
- Introduction to Mix Networks and Anonymous Communication Networks: https://leastauthority.com/blog/mixnet-intro/
- Dissent accountable anonymous group communication: (DC-net based): http://dedis.cs.yale.edu/dissent/
- Anon system overview: https://www.youtube.com/watch?v=fhqabqmzpqE
- I2P Jack Grigg - I2P: Open Research Questions about I2P (2017) [video]: https://www.youtube.com/watch?v=BHpEELiHBwM
- Mixnetworks and dummy traffic to increase anonymity https://www.freehaven.net/anonbib/cache/taxonomy-dummy.pdf

Tor:
- Tor: The Second-Generation Onion Router, 2004 [Dingledine04]: https://svn.torproject.org/svn/projects/design-paper/tor-design.html
- Anonymity and the Tor Network:
https://www.schneier.com/blog/archives/2007/09/anonymity_and_t_1.html
- Tor: Hidden Services and Deanonymisation:
https://media.ccc.de/v/31c3_-_6112_-_en_-_saal_2_-_201412301715_-_tor_hidden_services_and_deanonymisation_-_dr_gareth_owen

Mixmaster and mixminion (high latency):
- Mixmaster high latency: https://raw.githubusercontent.com/cryptodotis/mixfaster/master/mixmaster-spec.txt
- Mixminion Type 3 anon remailer high latency https://nymity.ch/tor-dns/pdf/Danezis2003a.pdf

"New gen" mixnetworks with lower latency [unclear if this is real classification]:
- USENIX Security '17 - The Loopix Anonymity System [video] (2017): https://www.youtube.com/watch?v=R-yEqLX_UvI
- Loopix slides: https://www.usenix.org/sites/default/files/conference/protected-files/usenixsecurity17_slides_piotrowska.pdf
- The Loopix Anonymity System (mixnetwork, low latency vs fake traffic) https://arxiv.org/pdf/1703.00536.pdf
- https://davidlazar.org/papers/karaoke.pdf

Delay-tolerant networking:
- Briar designed for, related to censorship-resistance and transport-invariance
- https://en.wikipedia.org/wiki/Delay-tolerant_networking
- https://web.archive.org/web/20050209141050/http://www.dtnrg.org/

Classic RFCs:
- TCP - talks about layers and reliability over unreliable: https://tools.ietf.org/html/rfc793
- TLS 1.0 https://www.ietf.org/rfc/rfc2246.txt
- BEP DHT: http://bittorrent.org/beps/bep_0005.html

Misc:
- Moral character of crypto: http://web.cs.ucdavis.edu/~rogaway/papers/moral-fn.pdf

Misc projects:
- SSB
- Hopper (Validity Labs)
- PSS and Whisper
- https://katzenpost.mixnetworks.org/ (Loopix)
- Briar
- I2P
- http://dedis.cs.yale.edu/dissent/
- https://katzenpost.mixnetworks.org/_static/slides/2017-12-modern-mixnets.pdf

Seminal Chaum papers:
- Chaum: Unctraceable Electronic Mail, Return Addresses, and Digital Pseudonyms (1981) [Chaum81]: https://www.freehaven.net/anonbib/cache/chaum-mix.pdf
- Chaum blind signatures: http://www.hit.bme.hu/~buttyan/courses/BMEVIHIM219/2009/Chaum.BlindSigForPayment.1982.PDF
- Chaum DC-Net: http://www.cs.cornell.edu/people/egs/herbivore/dcnets.html

P2P Overlay etc:
- https://blog.nucypher.com/why-were-rolling-our-own-intra-planetary-node-discovery-at-nucypher-beeb53018b0
- DHT fail anon https://www-users.cs.umn.edu/~hoppernj/hashing_it_out.pdf

Briar specs:
- BQP key exchange: https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BQP.md
- Introduction model: https://code.briarproject.org/briar/briar/wikis/Introduction-Client
- BTP and BSP also interesting, siblings above

References:
- Internetworking with TCP/IP, Douglas Comer, (1987) [Comer87]: *cough*
- Buford: P2P, [Buford00]: *cough*
- Sharp: Principles of Protocol Design (2008): *cough*

Lists of papers:
- Selected Papers in Anonymity https://www.freehaven.net/anonbib/
- Selected Research Papers in Internet Censorship: https://censorbib.nymity.ch/

Protocol design meta:
- Layering pitfalls:
- Wrong layering? E.g. see trade-off here. Postel (https://tools.ietf.org/html/rfc817) terrible formating, useful to read
- Layering Are they correspoding or fake ones? e.g. us tied to whisper (litmus test and assumptions~)
- Meta considerations: upgradability, language agnostic, compatible etc, machine readable orthogonal. Enable building of human protocols what primitive needed whitepaper.

## Messier

Mixminion
https://www.mixminion.net/minion-design.pdf
Spec https://www.mixminion.net/minion-spec.txt

Anonymity loves company.
https://www.freehaven.net/doc/wupss04/usability.pdf

https://mlswg.github.io/ and https://github.com/mlswg/mls-architecture/blob/master/draft-ietf-mls-architecture.md

https://datatracker.ietf.org/meeting/103/materials/slides-103-pearg-otrv4-slides-01


----

Katzenpost Mix Network Public Key Infrastructure Specification
https://katzenpost.mixnetworks.org/docs/specs/pki.html#pki

Impact of Network Topology on Anonymity and Overhead in Low-Latency Anonymity Networks
https://www.esat.kuleuven.be/cosic/publications/article-1230.pdf

Sphinx Mix Network Cryptographic Packet Format Specification
https://katzenpost.mixnetworks.org/docs/specs/sphinx.html

Paying for Privacy Preserving Messaging by Robert Kiel & Jeff Burdges at Web3 Summit 2018
Source: https://www.youtube.com/watch?v=Dd7Zfm7iU1s

Jack Grigg - I2P: Open Research Questions about I2P (2017) [video]
Source: https://www.youtube.com/watch?v=BHpEELiHBwM

---

What about Dispersy?
https://github.com/Tribler/dispersy

"Stateless sync using Bloomfilters"?
https://dispersy.readthedocs.io/en/devel/system_overview.html?highlight=bundle

What about Swarm Feeds?
https://www.epiclabs.io/wp-content/uploads/2018/11/Swarm-Feeds.Devcon4-jpeletier.pdf

Dispersy Bundle Synchronization (Zeilemaker 2013)

Refers http://bitsavers.trailing-edge.com/pdf/xerox/parc/techReports/CSL-89-1_Epidemic_Algorithms_for_Replicated_Database_Maintenance.pdf

---

https://github.com/burdges/lake/blob/master/Xolotl/papers/Xolotl-1-intro.tex
https://github.com/burdges/lake/blob/master/Xolotl/papers/Xolotl-3-mailboxes.tex

---

DHT on mobile? Battery life, considerations, etc:
https://github.com/ipfs/notes/issues/68
-- also LES and ULC design considerations? vs DHT
http://cse.aalto.fi/en/midcom-serveattachmentguid-1e3875898c3d482875811e388eb558ff26bbefebefe/optimizing-energy-consumption-of-mobile-nodes-in-heterogeneous-kademlia-based-distributed-hash-tables-ngmast08.pdf
http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.411.7926&rep=rep1&type=pdf

---

http://www.cs.umd.edu/projects/p5/p5-talk.pdf

https://www.usenix.org/system/files/conference/foci13/foci13-zamani.pdf

https://web.stanford.edu/class/cs259/WWW04/lectures/06-Protocols%20for%20Anonymity.pdf

https://en.wikipedia.org/wiki/Degree_of_anonymity

http://www0.cs.ucl.ac.uk/staff/G.Danezis/papers/set.pdf

anon trilemma https://eprint.iacr.org/2017/954.pdf

https://dspace.mit.edu/handle/1721.1/99859

https://freedom.cs.purdue.edu/projects/anonymity/trilemma/

https://freedom.cs.purdue.edu/projects/anonymity/trilemma/index.html

https://panoramix-project.eu/wp-content/uploads/2017/06/AnonHUJ.pdf

Really good overview by:
https://panoramix-project.eu/wp-content/uploads/2017/06/AnonHUJ.pdf
-- also loopix design considerations

Sphinx Mix Format - provable secure mix header format:
https://cypherpunks.ca/~iang/pubs/Sphinx_Oakland09.pdf

https://petsymposium.org/award/winners.php

Ian Goldberg thesis https://cypherpunks.ca/~iang/pubs/thesis-final.pdf
https://cypherpunks.ca/~iang/pubs/asymmetry-popets18.pdf

https://www.csail.mit.edu/research/new-way-handling-all-all-broadcast

http://www.cs.umd.edu/projects/p5/p5-talk.pdf

really interesting, broadcast bw vs comm eff, bitmask
http://www.cs.umd.edu/projects/p5/p5.pdf
vs xor tree no per user setting

http://ecee.colorado.edu/~ekeller/classes/fall2013_advsec/papers/tarzan_ccs02.pdf


https://github.com/Katzenpost/docs specs etc

https://www.freehaven.net/anonbib/cache/terminology.pdf

Paul Syverson low latency anon
Tor http://www.sti.uniurb.it/events/fosad10/slides/syverson-fosad10-2.pdf

https://svn.torproject.org/svn/projects/design-paper/challenges.pdf

--

https://www.youtube.com/watch?v=OgGTJIgNewE

https://www.esat.kuleuven.be/cosic/publications/article-1335.pdf


routing anon protocols
https://arxiv.org/pdf/1608.05538.pdf

signal censor
https://signal.org/blog/looking-back-on-the-front/


Video 90m, George privacy master class
Privacy technologies masterclass: Professor George Danezis, UCL
https://www.youtube.com/watch?v=VltNcmGvEVo

The Transport Layer Security (TLS) Protocol Version 1.2 (and v1)
https://www.rfc-editor.org/rfc/rfc5246.txt

Orchid: Enabling Decentralized Network Formation and
Probabilistic Micro-Payments
https://www.orchid.com/whitepaper.pdf

towards info theoretic metric anonymity set george
http://www0.cs.ucl.ac.uk/staff/G.Danezis/papers/set.pdf

---


From a Trickle to a Flood: Active Attacks on
Several Mix Types
https://www.freehaven.net/doc/batching-taxonomy/taxonomy.pdf

---

(https://tools.ietf.org/html/rfc793)

-

Mixminion?
TLS: https://www.mixminion.net/minion-spec.txt

---

Then you have DHT and stuff here: http://bittorrent.org/beps/bep_0005.html

---

Support QUIC and WebRTC etc as transports, not just TCP. OK.

https://hackmd.io/FcSt28PHTq6xw24BpRiduw?both

Reliable delivery on top of best-effort delivery. E.g. TCP/IP.

---

https://tools.ietf.org/html/rfc1122 nice layers

Idea - should have rough similar structure to RFC, with pointers to e.g. Whisper and PSS possibly

(~defacto now?) write req etc stuff

https://www.rfc-editor.org/rfc/rfc817.txt

https://www.brianstorti.com/tcp-flow-control/

https://ieeexplore.ieee.org/document/7163029/references#references

sok https://m.youtube.com/watch?v=oLwilFUH790

---

USENIX Security '17 - The Loopix Anonymity System [video] (2017)
Source: https://www.youtube.com/watch?v=R-yEqLX_UvI

Mixminion design and spec
Source: https://www.mixminion.net/minion-design.pdf

---

https://github.com/fjl/p2p-drafts

Secure messaging compare https://docs.google.com/spreadsheets/d/1-UlA4-tslROBDS9IqHalWVztqZo7uxlCeKPQ-8uoFOU/edit#gid=0

Also secure messaging sheet

https://discuss.status.im/t/can-whisper-support-a-public-chat-room/695/4

https://discuss.status.im/t/visibilty-stake-for-public-chat-room-governance/133/21

https://petsymposium.org/faq.php

libp2p

eclipse attack: https://eprint.iacr.org/2015/263.pdf

https://ieeexplore.ieee.org/document/7163029/references#references

https://github.com/isislovecruft/library--/tree/master/anonymity%20%26%20circumvention

https://censorbib.nymity.ch/

https://github.com/isislovecruft/library--/blob/master/anonymity%20%26%20circumvention/Hashing%20it%20out%20in%20public:%20Common%20failure%20modes%20of%20DHT-based%20anonymity%20schemes%20(2008)%20-%20Tran%2C%20Hopper%2C%20Kim.pdf

Paper draft submitt https://petsymposium.org/

http://web.cs.ucdavis.edu/~rogaway/papers/moral-fn.pdf - pond sup?

https://arxiv.org/pdf/1404.4818.pdf

Reading Chaum, 1981. https://www.freehaven.net/anonbib/cache/chaum-mix.pdf

---

Internetworking with TCP/IP, Douglas Comer, (1987)
Tanenbaum 1981. What is it?
Reading: P2P, Buford, 2000
Freenet
Tribler
OverlayWeaver viz?
