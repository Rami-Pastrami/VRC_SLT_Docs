## Why?
I have played VRChat for a long time and I early on I have bumped into people who communicated in ASL to each other. They were all quite friendly but often side-lined from larger groups. I wanted to try to help and my engineer brain chose this path.

## What do you need to use this?
All you need is a human proportioned avatar (scale can vary quite a bit) with proper fingers, and a VR controller that supports finger tracking.
The maps framerate should also not drop below 20-25 otherwise there may be issues. _Note I am talking about game framerate here, not SteamVR interpolated frames!_

## Is this a map only system, can this be attached to a avatar directly?
This is something to add onto maps as it makes heavy use of Udonsharp. It may be _technically_ possible to port this work over to avatars but I wouldn't hold my breath.

## How much longer till a public release?
When its done™.
Keep an eye on this repository for updates, or at my blog [HERE](https://ramipastrami.engineering/)

## What languages are supported?
Currently just ASL -> English. I set up systems so more could be added later but I intend to make sure this works well first.

## Are you Deaf / hard of hearing?
I am not. Ironically I am new to ASL and still a beginner signer. This was actually a large reason why it took me so long to make this, because I would make bad assumptions and then have to rewrite things repeatedly to account for them.

![](https://imgs.xkcd.com/comics/here_to_help.png)

Please learn from my early arrogance kiddos.

I will expand on this topic on a future date, but I will say that not only have my technical programming / machine learning skills improved over the course of this project, but a general sense of Deaf culture as well (though I am not the right person to ask detailed questions about that).

That being said, now with my school and other responsibilities clearing up, I am taking the time to learn ASL properly, not just to better improve this system, but so I can better communicate to those I have met in the deaf community.

## Will this ever be able to translate full sentences / account for grammar?
No. 

Technical Explanation:

- English and Spanish texts are plentiful and thus there is plenty of training data available to AIs to use. Yet machine translation between written languages is still notoriously bad. Sign Language as a whole has far less training data resources available, so frankly I don't see why it would be better in the slightest. There's a reason why you see "Sign Language" Translator projects popup, get some fun press, then disappear 3 months later. 

Ethical Explanation:

- Deaf communities are rather close-knit and are rather offended by something attempting to "fix" their language and culture. I am not the person to go deeper on this but I do want to point out that general point of view. Given what I have learned and saw, I agree with it.

I am sure on a technical level with enough training data, time and effort, we could _maybe_ get to something closer to a conversational translator, but I am not interested in that due to the massive time sink required for something that I ultimately agree, is morally dubious.

## So what is the difference with this project then?

I am not targeting this as some replacement to sign language interpreters. My goal is to create an interface to allow map makers to make "games" and other things to teach vocabulary to people new to sign language.

## What is the stigma against machine signing translators?
I do not generally answer questions in regards to Deaf culture because, simply put, I am not Deaf and thus did not have the life experience of those who are. 

However this is a common question and I wish to be clear:  A vast majority of the Deaf people I interacted with have been great and open to new ideas, so from the outside it may seem strange that there is this hesitancy towards machine based translators. Simply put its because historically they have been pretty terrible. They were often designed by small teams with no awareness or care towards sign language or Deaf culture. A lot of attempts took the form of some unwieldy glove that barely worked, whos results were inaccurate, lacked important context (body/head posture, as well as facial expressions are important for sign language), and were often expensive. And ultimately, these devices were not for the Deaf, they were for **the hearing people who did not want to learn sign and just wanted some easy "fix" while the Deaf individual would be saddled with all the burden**.

But again, there are some steps / differences here:
- Cost is the same with hearing users as finger tracking controllers are common with everyone and VRC_SLT will remain free
- This system is not being aimed at translating sign, The limitation with grammar is to be advertised clearly. This system better for learning sign vocabulary (teaching non-signing students).

## How can I contribute?
This is a machine learning based system, which means it can learn by example. I will eventually need people to sign to this system for it to learn its vocabulary. There will also be other ways to contribute down the line. Please note for obvious reasons, I will be favoring suggestions from those who sign frequently.

## Will this be quest compatible?
The computation workload is only ran on the user signing, and the result is a string that can be synced over the network.
With the advent of quest finger tracking, it may be possible that this could be ran on a quest, but there may be performance / hardware limits. I do own a quest to test this but that would be at a later date.

## Will this be compatible with desktop mode?
Only if you explain to me how you plan on signing with a keyboard.

## What about words / letters that cannot be done on modern VR controllers?
Some words (and letters) cannot accurately be done on controllers, generally due to the lack of supporting finger crossing. The VR Deaf community has accounted for this generally by having alternate "VR" versions of affected words and phrases. Currently the plan is to add an asterisk or symbol of some kind to these alternate signs to make it clear they are different than standard IRL sign language. This however is very open to discussion.

## What if this fails to work in any meaningful way?
If so, then I will continue to document everything, why it didn't work out, etc. There will once again be people in the future who think translating ASL to English is as simple as throwing a neural network at the problem. If nothing else, I can hope that my attempt and documentation can be used as a warning for those that believe this is some trivial problem

## What about classifiers?
Currently there is no support for them but I have some ideas on how to approach this potentially. I would like to become better with ASL myself first however before truly tackling this major language component, but again my focus lays in vocabulary currently.

## Can this be used as a translator between signing and non-signing people, _anyways_?
_As a non-signer / hearing person_, even I have to express doubts on this when basic things like classifiers aren't implemented. It may *technically* work to a limited extent, but be restrictive to the person signing and still awkward to understand. _It would be something closer to a glorified tech demo_. The benefits to trying this anyways is it will allow more people to meet Deaf people, who in turn may become interested in learning sign language to better communicate with their new friends! I do see a risk though that people may start using this as a crutch to avoid actually learning sign language, which is not what I want to happen.

There is also the more fundamental issue about the loss of information when changing communication formats. Take spoken language for example. If you were to jokingly insult your friend, you'd probably use some sarcastic / funny tone of voice, not something deadpan and serious. Tone matters when speaking, and if converted to text, we lose that context (that's why we have things like "/s" to make up for it). We face the same dilemma when converting from sign to text, we lose that context. It is for this reason I stopped calling this software a "translator" and started calling it a "transcriber" because it is more accurate to its function. At this time, the only way to "translate" sign is to either know sign yourself so you can translate the meaning in your head, or have a human interpreter do it for you.

## Can I download a prefab to use into my map?
Prefabs / source will be made available once I believe the system is ready, though I plan to go through some closed testing / validation first.
Once it is available, please do follow the following rules:
- The disclaimer that VRC_SLT is not a replacement for knowing sign must be kept absolutely clear
- The disclaimer that the 1-1 mapping of sign words to written language is not grammatically accurate must also be kept clear

## Can this come to other games? (CVR/Resonite/STEAMVR plugin)?
Right now VRChat is my focus here, though once the source is released you are welcome to try!
Where ever you port it, please:
- Keep your software free and open source
- Make an effort to keep up to date with this repository, as we try new things we may switch algorithms / methods to transcribe sign that may be more appropriate.
- Please make clear systems like this is not a replacement for knowing sign!

