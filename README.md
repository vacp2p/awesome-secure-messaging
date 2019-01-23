# Awesome Secure Messaging

*A curated collection of links for secure messaging. Part of the ["Awesome X" series](https://github.com/sindresorhus/awesome).*

The list is periodically updated with new links. Click "Watch" in the right top corner to follow.

Your [contributions](contributing.md) are welcomed.

## Table of Contents

- [Fundamentals](#fundamentals)
- [Messaging](#messaging)
- [Anonymity](#anonymity)
- [Censorship Resistance](#censorship-resistance)
- [Coercion Resistance](#coercion-resistance)
- [Attacks](#attack)
- [Applications](#applications)

## Fundamentals

- [SoK: Secure Messaging](http://cacr.uwaterloo.ca/techreports/2015/cacr2015-02.pdf) - evaluation of current secure messaging solutions based on security, usability and adoption

- [Viewing Privacy as a Security Property](http://www0.cs.ucl.ac.uk/staff/G.Danezis/talks/privacy-as-security.pdf) - presentation by George Danezis that tells the story of privacy as security, informational self-determination

## Messaging

- [Double Ratchet](https://signal.org/docs/specifications/doubleratchet/) - two-party protocol to exchange encrypted messages based on shared key

- [Bramble Transport Protocol](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) - transport layer security protocol for delay-tolerant networks, provides secure channel between two endpoints

- [Bramble Synchronisation Protocol](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BSP.md) - data synchronisation protocol for delay-tolerant networks


## Trust establishment
- [X3DH](https://signal.org/docs/specifications/x3dh/) - two-party asynchronous key agreement protocol

- [Bramble QR Code Protocol](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BQP.md) - in-person key agreement protocol to establish a shared secret


## Session management

- [Sesame](https://signal.org/docs/specifications/sesame/) - session management for async and-multi device setting

## Anonymity

- [The Differences Between Onion Routing and Mix Networks](https://crypto.is/blog/mix_and_onion_networks) - brief comparison

- [Anonymity Trilemma: Strong Anonymity, Low Bandwidth Overhead, Low Latency—Choose Two](https://eprint.iacr.org/2017/954.pdf) - on fundamental tradeoff for anonymous communication protocols

- [Selected Papers in Anonymity](https://www.freehaven.net/anonbib/) - meta-list of selected papers in anonymity since 1977

- [Sphinx: A Compact and Provably Secure Mix Format](http://www.cypherpunks.ca/~iang/pubs/Sphinx_Oakland09.pdf) - paper on secure and compact message format for mix networks

- [Sphinx Mix Network Cryptographic Packet Format Specification](https://katzenpost.mixnetworks.org/docs/specs/sphinx.html) - specification for Sphinx mix network packet format

- [Introducing Anonymous Communications slides](http://www0.cs.ucl.ac.uk/staff/G.Danezis/talks/AnonTalk.pdf) - notes by George Danezis on properties, threat models, systems & attacks

- [Anonymous Communications slides at CCC](https://events.ccc.de/congress/2004/fahrplan/files/355-anonymous-communication-slides.pdf) - another overview of anonymous communication systems by George Danezis

- [What is a Remailer?](https://crypto.is/blog/what_is_a_remailer) - anonyomus remailers tutorial building up from basics

- [Cwtch: Privacy Preserving Infrastructure for Asynchronous,Decentralized, Multi-Party and Metadata Resistant Applications](https://cwtch.im/cwtch.pdf) - extension of the Ricochet protocol that provides asynchronous, offline and multi-party metadata resistant messaging

## Censorship Resistance

- [Pluggable Transport](https://www.pluggabletransports.info/) - specification initiative to allow applications being used as transports to make network traffic harder to distinguish and block, origins in Tor

- [Selected Research Papers in Internet Censorship](https://censorbib.nymity.ch/) - meta-list of papers on censorship and resistance thereof

## Cocercion Resistance

- [Coercion-Resistance and Receipt-Freeness in Electronic Voting](http://people.irisa.fr/Stephanie.Delaune/PUBLICATIONS/DKR-csfw06.pdf) - academic paper that outlines ways to provide coercion-resistance for electronic voting

- [Coercion-Resistant Electronic Elections](https://eprint.iacr.org/2002/165.pdf) - paper on coercion resistance and trusted setup requirement

- [On-Chain Vote Buying and the Rise of Dark DAOs](http://hackingdistributed.com/2018/07/02/on-chain-vote-buying/) - on problems of user generated keys and electronic voting


## Attacks

- [The Sybil Attack](https://www.freehaven.net/anonbib/cache/sybil.pdf) - attack on p2p systems from cheap identity generation, requiring some form of logically centralized authority

- [Tagging Attacks](https://crypto.is/blog/tagging_attacks) - adversary recognizing traffic by modfiying it in acceptable fashion

## Applications

- [Briar](https://briarproject.org/) - messaging app employing several censorship-resitance techniques, like direct device-to-device comms (bluetooth, wifi), Tor routing

- [Signal](https://signal.org/) - widely used security-based messaging app with intermediate server and phone based registration, includes voice calls
