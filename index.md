# Technology Tips for Protesters

In today's United States, attending a peaceful protest can make you a target of law enforcement. It's now common practice for police departments to record photos and videos of everyone attending a protest for review later. Their tools for electronic surveilance are anything but targeted; in fact they carelessly ignore the privacy of thousands of people while conducting surveilance. This guide is designed to help you reduce the impact of invasive surveilance techniques that are deployed en masse against everyone attending a protest.

## Phone Unlock

If you end up in custody, the police may try to compel you to unlock your phone so they can read your messages and calls. The legality of this is very much in question: a court in New Jersey [ruled](https://njcourts.gov/attorneys/assets/opinions/supreme/a_72_18.pdf) that the state can compel you to enter a passphrase on your phone, a decision supported by earlier cases in [Vermont (2009)](https://arstechnica.com/tech-policy/2009/03/court-self-incrimination-privilege-stops-with-passwords/), [Colorado (2012)](https://arstechnica.com/tech-policy/2012/01/judge-fifth-amendment-doesnt-protect-encrypted-hard-drives/), and [Massachusetts in 2014](https://assets.documentcloud.org/documents/1209519/commonwealth-vs-gelfgatt.txt). However, opposing rulings have happened in [Florida](https://arstechnica.com/tech-policy/2018/10/court-teens-driving-killed-someone-but-he-cant-be-forced-to-give-up-passcode/), [Wisconsin](https://arstechnica.com/tech-policy/2013/04/fifth-amendment-shields-child-porn-suspect-from-decrypting-hard-drives/), and [Pennsylvania](https://arstechnica.com/tech-policy/2015/09/forcing-suspects-to-reveal-phone-passwords-is-unconstitutional-court-says).

A court in Virginia [ruled in 2014](https://arstechnica.com/tech-policy/2014/10/virginia-judge-police-can-demand-a-suspect-unlock-a-phone-with-a-fingerprint/) that you can be compelled to give up biometric information, but not a passphrase. In California last year, a US District Court [ruled](https://assets.documentcloud.org/documents/5684083/Judge-Says-Facial-Recognition-Unlocks-Not.pdf) that compelling a suspect to unlock their phone with biometrics is a violation of Fifth amendment rights.

We probably won't see a consistent ruling on this until a case reaches the Supreme Court, so for the time being look to legal precedent in your state. If you are detained and you're concerned about police trying to access your phone, consider these general points of advice:

- "Swipe to unlock" and "draw a pattern" unlocks are considered biometrics in some of these court cases.
- Police can physically force you into a position that unlocks your phone via biometrics- placing your face in front of the camera or putting your thumb on the phone.
- Police cannot physically force you to divulge a password or PIN to your phone. Even if your state has ruled that you can be forced to divulge your PIN, they still need a warrant to do so.

## IMSI Catchers

[IMSI catchers](https://en.wikipedia.org/wiki/IMSI-catcher) are the most common technology deployed by police and [federal agencies like ICE](https://www.aclu.org/blog/privacy-technology/surveillance-technologies/ice-using-powerful-stingray-surveillance-devices) to deanonymize people who carry cell phones. You might also hear these devices called "StingRay", which is the the most common brand name. They are small enough to be carried in a car and handheld models are also available. You can think of these devices as fake cell phone towers. Normally, your cell phone sends out a signal to find the nearest cell phone tower, the one closest says "hi I'm a cell phone tower!" and then your phone says "oh great, you're pretty close to me so let's talk about cell phone stuff." An IMSI catcher pretends to be the closest cell tower to wherever it's deployed, by broadcasting a really strong signal saying that it's a cell phone tower. Your phone thinks nothing is wrong and that it's connecting to a legit part of the cell network, but the IMSI catcher is now the only gateway from your phone to other phones and the internet. The really wild part is that this happens for _everyone in range of the device_, which usually ends up being thousands of people in the vicinity of a police deployment.

We won't go into the technical operation of these devices in this guide, there are [many good resources](https://theintercept.com/2020/07/31/protests-surveillance-stingrays-dirtboxes-phone-tracking/) around the Internet that can explain it well. Instead, let's talk about practically what can happen if your cell phone is targeted by one of these devices.

At minimum, the IMSI catcher can do the following with your phone:
- Collect details about what calls were placed and what SMS messages were sent while connected to the catcher
- Force your phone to drop 4G/5G encryption from all calls by swapping to a 2G connection
- Read a special subscriber number (this is the "IMSI") - which we'll talk about in a second

That's all pretty scary. To make it worse, with a warrant or court order the police can combine the IMSI number with information from phone companies to identify the person who bought the cell plan. This technique has been used to open the door for further surveilance of the person who owns the phone. If the police have already identified your IMSI number from a previous trawl, they can tell whether you're present at an event with one of these devices.

Beyond court orders and warrants, more advanced versions of these devices have the capability to do much more:
- Record the full contents of [phone calls](https://www.wired.com/2015/10/stingray-government-spy-tools-can-record-calls-new-documents-confirm/) and [text messages](https://www.wsj.com/articles/americans-cellphones-targeted-in-secret-u-s-spy-program-1415917533).
- Create a copy of all mobile data used while connected to the catcher.
- Send text messages and calls which masquerade as a different mobile number, impersonating people you know
- Read information about other cell towers your phone has connected to, revealing places you've visited recently
- Inject malware into your phone which can turn it into a recording device
- [Jam communication](https://www.kgw.com/article/news/nd-pipeline-protesters-question-aircraft-surveillance-jamming/283-345780315) coming from your phone

From [what we know](https://theintercept.com/2020/07/31/protests-surveillance-stingrays-dirtboxes-phone-tracking/), these advanced versions of IMSI catchers have been used by the military for at least a decade. With the ongoing transfer of equipment from the military to police departments, it's very likely that military-grade IMSI catchers are now in use by police departments- so it's worth considering the risk.

What can you do against these devices? Well, it's all about trade-offs. Your phone is an incredibly useful tool to use at a protest- you can record video and photos of what's going on, coordinate with other protesters, and show the Internet what is happening near you. The approach that you take has to do with what protection you need.

A few methods provide some protection, but with drawbacks:
- Turn your cell phone off. This is *the simplest and most effective method for denying IMSI catchers*, but it has obvious drawbacks- you can't communicate with other people or use your phone's camera during an action.
- Turn your phone to airplane mode. This will prevent it from connecting to an IMSI catcher while allowing you to use your phone for recording photos and videos. However, it means you won't be able to communicate with anyone during the protest.

If you want to communicate during a protest, you must use a platform that can't be broken by the police. Text messaging (SMS) and phone calls can be read by a police department with an IMSI catcher. However, end-to-end encrypted communications over platforms like Signal, Telegram, and Matrix cannot be broken by police. The important bit here is "end-to-end", which means that your messages are encrypted on your phone and aren't decrypted until they reach your friends' phones. Even if they manage to record all the data sent by your phone, they would need an encryption key from one _end_ to get into the contents of the communication. The one exception here is if your phone is physically taken by the police, unlocked, and one of those apps is running- then one end is compromised and the messages can be read.

To protect yourself from IMSI catchers while still communicating with other people, try using an encrypted app:
- Talk with your group before attending an action and decide on an encrypted app like Signal, Telegram, or Matrix for communication. DO NOT trust a platform owned by a large tech company like Facebook Messager, Instagram, WhatsApp, Google Talk, etc. Even though these apps use end-to-end encryption, the companies who run them have a history of cooperating with the police and federal authorities under regulatory pressure. They could be compelled to hand over metadata about your communications.
- Have everyone download the app and practice talking with it a few times before attending the action. Try out the disappearing messages feature of Signal if you're using it, to make sure all your communications disappear after some time.
- While at the action, do not trust any text messages or phone calls that don't come through the encrypted app. They might be a police officer trying to identify you.

If you have an Android phone, you can also set your phone to never connect to insecure networks like 2G. This is hugely inconvenient if you're traveling to an area with bad service, so you might want to revert these settings after attending an action.
- Go to the "Settings" app and click on the "Network & internet" category
- Click on your mobile data connection to go into its settings
- Click "Preferred network type" (you might have to expand "Advanced Settings" to get here)
- Set to "LTE / CDMA". 2G networks are also known as GSM, so you want to avoid any setting that includes GSM.

With these settings in place, an IMSI catcher can't force your phone to drop encryption from your data, which makes things a tiny bit safer. I'm not sure if the same settings exist on iOS, but [this Apple help page](https://support.apple.com/guide/iphone/view-or-change-cellular-settings-iph3dd5f213/ios) is a good place to start. Side note, apps that claim to detect IMSI catchers aren't a silver bullet. Even [reputable apps in this space](https://github.com/CellularPrivacy/Android-IMSI-Catcher-Detector) acknowledge that their methods are flawed and incomplete.

## Photography and Video recording

There are good reasons to record video at protests, chief among them documenting the activity of police officers who believe they can act with impunity. However, we've seen that photos and videos taken at protests are used to deanonymize protesters after the fact. If you take any pictures or record video of other protesters, do not post it on social media. I want to repeat that again for the people who are thinking about their clout: **DO NOT post recordings of protesters on social media**. Even with the best intentions, these photos and videos can be used to target other people who attended the action. Consider the fact that posting information on social media is trading someone else's safety for your curated experience of "being a protester".

As mentioned earlier, police departments commonly record video of protests for later analysis, hoping to find individuals who attended. This mass video surveilance is often [combined with digital data](https://www.theatlantic.com/technology/archive/2019/07/three-states-granted-ice-access-dmv-photos/593509/) in order to identify people who attended. In Philadelphia, for example, a woman was arrested after [footage from protests was combined with her Etsy, Poshmark, and Instagram profiles](https://www.inquirer.com/news/philly-protests-arrests-fbi-lore-elisabeth-blumenthal-george-floyd-20200617.html). I bring this up not to discuss the ethics what she did at the protest, just to provide evidence that law enforcement uses techniques that tie together digital information in this way. Expect that any public information about you on the Internet can be used against you, and make a plan that makes you harder to identify given that information.

There are a lot of good tips around the Internet on how to dress during a protest, which I can't cover well here. Definitely do further research to supplement this information. In general, consider buying a generic dark-colored hoodie and a baseball cap, so you can hide your face and hair if you notice that a camera is pointed in your direction. If you have tattoos, wear clothing to cover or obscure them.

## Miscellaneous Tracking

Disable your Bluetooth connection before attending a protest. Bluetooth is a "noisy" way of communicating, in that it's constantly sending messages asking if there are any Bluetooth devices nearby. These messages can be recorded by anyone in range, making it possible for interested parties to correlate your Bluetooth data with other data sources. I can't find any documented instances of Bluetooth traffic being used by police departments, but it's a common method of attack in the computer security world.

On a similar note, turn off your WiFi before attending a protest. If your phone isn't connected to a WiFi network but the WiFi is on, your phone will be constantly searching for a known network to connect to. Imagine that your phone is constantly shouting "IS THE NETWORK HOME-12345 IN RANGE NOW? NO? WELL HOW ABOUT Starbucks-Wifi?" over and over again for every network it knows about. If your phone has connected to a lot of wifi networks, or if your name/address are in any of those network names, this can be used to deanonymize you. Furthermore, a police tech could set up an open network named "Starbucks-Wifi" (or whatever) and get your phone to connect to it. This is like an IMSI catcher, but for your wifi. Fun!

## tl;dr

- Use a password or PIN to unlock your phone, but research court cases in your state.
- Download and use an encrypted messaging app like Signal, Telegram, or Matrix and do not trust any calls / text messages you get outside of that app.
- If you don't need to communicate at the action, put your phone in airplane mode.
- Don't post any photos or video on social media after an action.
- Cover identifying marks on yourself and wear generic clothing.
- Disable WiFi & Bluetooth while you're at an action.

## Why should I trust this guide?

I won't pretend that this guide is comprehensive, rather it tries to communicate what you should know quickly and simply so you can follow up with your own research. This must be supplemented by research and careful planning, as everyone's situation and risks are different. All this tries to accomplish is arming you with the right knowledge to start to protect yourself from invasive surveilance.

Also, this guide is [open source](https://github.com/protestprivate/protestprivate.github.io), so you can fix any inaccuracies you find in here.
