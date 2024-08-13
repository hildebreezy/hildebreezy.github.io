---
layout: post
title: Personal online security quick start,  a beginner's guide
splash: Hello world
author: Tanner
excerpt_separator: <!--more-->
---

Many parts of our lives have been increasingly turned over to management by various online services: banking, email, news and entertainment. Online applications also typically ask for large amounts of identifying information and manage important, sometimes necessary, parts of our lives. Alongside the convenience online services offer, criminal and fraudulent industries have arisen to exploit our dependence on them, making ordinary people like you and me an incidental target of convenience when larger organizations are targeted. 

It is important to have a minimum baseline of security and privacy to protect against exploitation, so that when a service you depend on fails to protect your information (or actively sells it), you can feel confident that you won't be significantly harmed.

Here, we'll explore several simple security and privacy steps that will protect you when other systems fail.

<!--more-->

## TL;DR

1. [Lie](#step-one) - wherever practical (and legal) provide information for a made up identity, rather than your own personal identifying information when registering for services.
2. [Enable MFA](#step-two) - SMS or email will suffice, MFA apps are OK, but security keys (e.g. Yubikey) are best (by a lot).
3. [Use a password manager](#step-three) - use an app that can generate unique, strong passwords for all your different services and that can encrypt your password database with a single, strong, easy to remember password.

[Jump to a set of examples of tools to help you accomplish these tasks.](#examples)

## Step Zero - Understanding the threat

Most privacy and security posts would start by telling you to assess your threat model and develop a security plan based on that. Almost all of us share a similar baseline threat that I'm going to address here that is reasonably easy to address for everyone:

1. We are NOT a deliberate target. That is to say, we are not a high-profile person who fraudsters would target because of our importance or wealth. We are a target of conveniance because a larger service leaked our personal information making it trivial for someone to try and exploit us.
2. We are dependent on a complex array of independant services, many of which we rarely think about or monitor and which we do not have a good inventory of. Because of this we cannot possibly keep track of where our information is or how it is moving across the internet.
3. Scammers can be incredibly clever and it can be difficult even for the most vigilant of us to identify scams and fraud in real time. Scammers will often cast a wide net and, similar to point #1, don't usually target us deliberately but hope to catch us with some other bait.

## Step One - Lie
{: #step-one }

The first and easiest defense mechanism while online is to lie wherever possible. Occaisionally it will be important to provide accurate identifying information, such as for financial and banking system applications where providing false information would be illegal, but in other cases it can prevent your real information from leaking into the wrong hands. 

[See some ideas for tools to get your started.](#tools-one)

For mundane and routine cases such as registering an email address or signing up for one of the millions of apps in the App Store, creating an imaginary identity to use when filling in birthdates, middle names (or full names if it doesn't matter), pet names, etc. can create a false trail that turns you from a trivial target of convenience to an inconvenient invenstment to exploit.

In the worst case, when accurate identifying information is leaked, your identity can be correlated to social security numbers and your identity stolen. A more common case, that could be equally as devestating, would be this information being used to access your existing accounts and wreak all kinds of havoc in your life, potentially locking you out of your own services.

### Basic protection

Create a false identity for yourself with the typical identifying information applications will often ask for to correlate your identity.

For example:

- Name
- Birthday
- Middle name
- Mother's maiden name
- Pet's name
- City of birth
- First car

When filling out applications that have no legitimate need for your accurate identifying information, provide the fabricated answers to these questions instead.

*Important* don't forget this information - some services require it to correlate your identity if you need to reset a password later on.

### Advanced Protection

Create and manage independant identities for each service your sign up for. In the past this would have been a nearly impossible task to manage alone, however services such as Proton Pass have started adding Identity management that lets you easily create and manage multiple identities for all of your services.

## Step Two - Understand and use Multi-factor authentication
{: #step-two }

Passwords are notoriously weak protection for your accounts for a variety of reasons. For one, using the same password for multiple accounts means that if one service improperly protects your password, all of your other accounts are vulnerable. For another, a good, strong password can make the password difficult to remember.

[See some ideas for tools to get your started.](#tools-two)

I'll address passwords more in the next section, but there is a more important step you can take to reduce the short comings of passwords: enabling multifactor authentication (MFA).

For our purposes, this means adding an additional verification step to account access that doesn't rely on a remembered password, but is instead dependant on a physical object that you control. This can come in a lot of forms: email address, phone number (via text message, e.g.), an app installed on your phone, or a physical security token.

Not all of these options offer the same level of protection, but no matter what multi-factor authentication should be enabled on all services that support it. 

Enabling multi-factor authentication means that your accounts cannot be compromised by passive exploitation - that is, if your password is stolen or if an attacker is just trying to brute force passwords on known account IDs, they won't be able to get in without your participation. For many cases will make exploiting your account too much of an effort for attackers.

### Basic protection

Enable SMS or email multi-factor authentication. SMS and email probably do not require any additional setup on your part - no additional apps, no additional secrets to protect, and little worrying about losing access.

If you lose your phone, likely your carrier can restore your phone number to you ensuring that you never lose access to your MFA. 

Email multi-factor authentication can be a bit touchy, as it is possible to lock yourself out of this MFA capability which would put you in a deadlock for all of your other accounts. It is better than nothing, but risky.

Both SMS and email are susceptible to compromise via phishing or scamming given a persistent and clever scammer. There are well developed scams for tricking you into revealing your MFA code and to create an illicit session into one of your accounts. Again, it is better than nothing but you will need to be warry of scam attempts to access your account and NEVER provide your multi-factor code to any unauthenticated source.

### Intermediate protection

The next option for multi-factor authentication is to use a dedicated multi-factor authentication app.

Some popular options: 
- Microsoft Authenticator
- Google Authenticator
- Aegis
- Raivo

These apps use a special secret token generated for EACH internet service you use in order to create a special code that changes every few seconds to authenticate you into the service.

This is a popular option and somewhat more recommended for your privacy since you do not need to give up your phone number or email address to the service provider.

One of the main downsides is that you will want a way to securely back up the secrets stored in the app. Each app has its own way to do this - many popular ones like Microsoft Authenticator use your existing cloud accounts to safely back them up so you can recover the codes when you log in on a new device. It is also important to note that these secret codes will often not automatically migrate if you get a new device, you will need to make sure you re-initialize your MFA app when you set up a new device.

If are willing to put in the extra work, I would typically recommend using an app that lets you manually export an encrypted version of the secret codes that you can use to restore later, just in case. Aegis (Android) and Raivo (iOS) can do this. They are not compatible across platforms, however, and you will need to manage the cloud back up yourself. If that is a bridge to far, apps that synchronize your codes to the cloud is your best bet. Just be sure you can get back into the account if you lose the device with your MFA on it.

Some services like Yahoo and Microsoft have a multi-factor authentication mechanism built in to their apps that let you provide approval for each login directly from the app in real time, rather than using an additional secret time code.

### Advanced protection

Your best option for services that support the capability is to use a security token.

A security key is a physical device, usually in the form of a USB, that needs to be plugged in to the device you are accessing your account from in order to access the service. 

The advantage, I think, is a bit obvious here. When an account is protected by a security key, no one can access the account without having physical access to the key that you control. 

The technology underlying physical security keys is fairly advanced and very robust. The protocols and negotiations that go on between your device and the server go through multiple steps that ensures both that your key is legitimate and the server is who they say they are - that is, a middle man can't make the request on your behalf and steal the session.

There is a downside - if you lose your security key, you can be locked out of your accounts. For this reason it is generally recommended you have at least two keys configured for each account, with one kept in a safe location.


## Step Three - Manage your passwords
{: #step-three }

There are two big vulnerabilities that are common in password management that we have already alluded to in step 2:

- weak passwords
- password reuse

Password manager applications can help solve both of these problems, and there is no shortage of available products to do this for you.

[See some ideas for tools to get your started.](#tools-three)

A password manager generates a strong, very secure password using a long string of random characters and saves the information into an ecrypted database.

There are multiple ways to unlock these password databases, the simplest mechanism is with another password - if you choose the password method, you should choose a password that is long, strong, but easy to remember. 

[Some tips on generating a strong password.](https://www.isaca.org/resources/isaca-journal/issues/2019/volume-1/nists-new-password-rule-book-updated-guidelines-offer-benefits-and-risk)

Another option for some databases is to use biometrics or physical security keys to unlock your password database.

Whatever method you choose to use to manage passwords, it is good practice to commit to one method for all of your passwords, and avoid spreading them across multiple services as it can become difficult to track down the appropriate account information if you are constantly switching between softwares.

### Basic Protection

The easiest mechanisms to keep your passwords strong and organized are the password managers built into the tools that you already use. 

If you are an Apple device user, such as iPhone, iPad, or Mac, a good option is the iCloud Keychain. iCloud Keychain can automatically save your logon information, generate and save strong passwords, and back it all up to the cloud to be accessed on all of your Apple devices. The capability is built in to every Apple device and so is available everywhere you use Apple and your passwords can be unlocked using your AppleID and/or biometrics stored on your devices making access to your passwords easy and unobtrusive. The draw back is that if you leave the Apple ecosystem, migrating your passwords will be more difficult.

All major web browsers also support password management on your behalf, and the big name browsers also offer a cloud service to backup the passwords as well. One of the drawbacks is that these browsers aren't good about sharing saved passwords between eachother and other browsers, so you may be dependant on a single browser or end up managing multiple sets of password databases.

With browsers, the password database is typically protected by your device account credentials, such as your Windows logon. The drawback here, is that if you are already logged in your passwords are potentially useable. In the worst case if you device pin is cracked, all of your passwords are exposed.

### Advanced Protection

There are several services which provide dedicated cloud password management such as [Proton Pass](https://proton.me/pass) and [Bitwarden](https://bitwarden.com). Microsoft Authenticator, the MFA app discussed above, also has the ability to do password management. These applications have the advantage of being cross platform, working on all of your devices, and offering cloud back up services. Most are paid, however, so these are typically a better option when bundled with another service you intend to use.

A good online password manager encrypts your passwords on their server side using your user password or other unique qualifier so that the cloud passwords are never revealed over the network, and are only unlocked on your device. If the service does not, your credentials could be susceptible to compromise if the online service is hacked. Not all cloud based services are created equal - you should be sure you trust and potentially understand how an online password manager protects your credentials before you trust it with your login information.

The most versatile option for password management is an offline encrypted database like [Keepass](https://keepass.info). With an offline database, cloud back up is up to you, as there is no built in service to save the passwords to the cloud but this is easy enough to accomplish with a cloud service you already use, such as iCloud, OneDrive, Google Drive, or [Proton Drive](https://proton.me/drive). Offline databases are simply encrypted files saved to the filesystem that you unlock with your strong password, biometrics, or security key. Functionally they work the same as the other options, with a couple of advantages. 

Because it uses an open standard for password encryption, offline password management has a robust ecosystem of applications that can manage them, so you can pick and choose the best and most comfortable app to use for your device - there are multiple app options for each platform.

Furthermore, you do not have to have any inherent trust in your cloud provider with this option. Because the files are encrypted and decrypted locally, even if your cloud account is compromised the passwords cannot be extracted without the decryption key protected by your strong password.

### Optional Protection

Passwordless authentication is an option offered by some services that can be beneficial for some use cases. As the name suggests, with passwordless authentication set up account logon no longer uses a password and is instead dependent on your multi-factor authentication solution to authorize account access, most commonly using an app produced by the service provider or a physical security key.

For example Microsoft accounts can be configured to have passwordless logon where the user with the Microsoft Authentication app installed accepts a notification request on their phone to logon instead of a password.

The upside is that no attacker can ever use brute force to access your account, and your password could never be leaked. A potential downside is the dependence on a physical object that could be lost or stolen, thus leaving you digitally stranded.

## Examples of quality tools that can help enable your personal online security
{: #examples }

I'm not sponsored by any of these applications but I've used all of them in one format or another and can attest to the sufficiency to do the task recommended and nothing more. Some of these products do not offer privacy guarantees, which is not part of the scope of this article.

1. Lie <a id="tools-one" />
    - [Proton Pass](https://proton.me/pass) - Online password manager with Identities manager feature (intermediate, free)
2. Enable MFA <a id="tools-two" />
    - [Yubikey](https://www.yubico.com/) - A very popular physical security key with a lot of support (intermediate, purchase)
    - [Microsoft Authenticator](https://www.microsoft.com/en-us/security/mobile-authenticator-app) - A very popular multi-factor authentication app with cloud backup (easy, free)
    - [Aegis](https://getaegis.app/) - a great opensource MFA app for Android, you will need to manage cloud backup yourself (intermediate, free / open source, Android)
    - [Raivo OTP](https://raivo-otp.com/) - a great open source MFA app for iOS, you will need to manage cloud backup yourself (intermediate, free / open source, Apple)
3. Use a password manager <a id="tools-three" />
    - [Keepass](https://keepass.info) (advanced, free / open source)
    - [Proton Pass](https://proton.me/pass) (intermediate, free)
    - iCloud Keychain (very easy, free, Apple Only)
    - Browser (Chrome / Firefox) password managers (easy, free)

## Summary

In order to protect yourself online, a beginner should consider three basic steps.

1. Lie as often as is practical and legal when filling in online applications and forms. You do not need to give up your identifying information to service that have no legitimate need for it.
2. Use multi-factor authentication. Multi-factor authentication is a phenomenal first line defense against hackers and scammers who are playing a numbers game; if they need to spend any additional effort to scam or socially engineer you to compromise your account, they are likely to either move on, or they will be required to involve you to access the account.
3. Use a password manager. Using password managers allows you to use different passwords for all of the services you use, meaning that a website that leaks your password for one service will not compromise any others. It also helps keep your passwords strong without you needing to memorize multiple complicated passwords.

Basic online security doesn't have to be terribly hard. Hopefully this helped some people get started without neeing to parse a bunch of complicated discourse on the topic. 

Most of us have a simple threat model; that is fraudsters and scammers explointing easy to access credentials and we are unlikely to be deliberately targeted. 

These three steps should lock down your digital life enough to move confidently about the internet and enjoy what it has to offer, rather than constantly worrying about damage control.