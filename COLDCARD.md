# COLDCARD
This section will show you how to:

- Check the tamper-evident bag
- Setup a PIN
- Generate a seed phrase with some dice rolls
- Backup recommendations  

## Checking the tamper-evident bag:
Upon receiving your COLDCARD, ensure that the tamper-evident bag has not been compromised. If anything seems amiss or if you have any problems contact [support@coinkite.com](mailto:support@coinkite.com?subject=%5BContact%5D%20-%20). Visually inspect the surfaces and edges of the bag for indications of tampering, openings, or damage.

<p align="center">
  <img width="400" height="300" src="assets/Bag0.png">
  <img width="400" height="300" src="assets/Bag1.png">
</p>

<p align="center">
  <img width="400" height="300" src="assets/Bag2.png">
  <img width="400" height="300" src="assets/Bag3.png">
</p>

You will see the tamper-evident words "VOID" appear when the seal is opened. Inside you will find your new COLDCARD, the Wallet Recovery Backup Card, sticker(s), and an additional copy of the bag number which should match the bag number printed on the outside of the bag. 

<p align="center">
  <img width="388" height="208" src="assets/IMG_6079.JPG">
  <img width="399" height="277" src="assets/IMG_6080.JPG">
</p>

If everything looks good, then you are ready to power on your new COLDCARD and get it setup. 

Here is a diagram you can reference to learn the COLDCARD's navigation:

<p align="center">
  <img width="853" height="505" src="assets/Navigation.png">
</p>

## Setting up a PIN
A great security feature of the COLDCARD is that it can be used completely air-gapped. Meaning that you never have to connect it to a computer, although that option is there if you choose to use it. You can use a standard USB outlet transformer or even a 9v battery with the COLDPOWER adaptor, which Coinkite offers [here](https://store.coinkite.com/store/cldpwr). To power on the COLDCARD simply connect a USB to micro-USB [cable](https://store.coinkite.com/store/category/accessories) to the port on top of the COLDCARD and the other end to the USB port on your COLDPOWER adaptor & 9v battery.

<p align="center">
  <img width="403" height="302" src="assets/IMG_5557.JPG">
  <img width="403" height="302" src="assets/IMG_5556.JPG">
</p>

Once powered on, first read and accept the terms of sale & use. Then you will be asked to confirm the bag number. If there are any discrepancies, contact [support@coinkite.com](mailto:support@coinkite.com?subject=%5BContact%5D%20-%20).

<p align="center">
  <img width="605" height="454" src="assets/BagNumber.jpg">
</p>

Make careful considerations with your PIN number. You don't want to use one that is easy to guess. Your PIN will have two parts, a prefix and suffix. The way the PIN works after you set it all up is that once you enter the prefix, you will be presented with two anti-phishing words. If the words are the same as the original words presented to you at initial setup, then you know that your COLDCARD has not been tampered with since the last time you accessed it. After confirming the anti-phishing words, you then enter the PIN suffix and if all is correct you will be permitted access to the COLDCARD. 


First, select `Choose PIN Code`, then you will see a brief description of how the PIN code works. Each part of your PIN code can be between 2 and 6 digits. There is absolutely no way to access a forgotten or lost PIN. Also, if you enter a PIN incorrectly too many times, it will brick your COLDCARD as a security feature.

<p align="center">
  <img width="605" height="454" src="assets/Choose PIN.jpg">
</p>

After hitting <kbd>OK</kbd> you will get one more warning about the risk of losing or forgetting your PIN. After reading that, you can enter your PIN prefix. Use the included notecard to write down your PIN prefix then hit <kbd>OK</kbd>. 

<p align="center">
  <img width="454" height="341" src="assets/EnterPreFix.jpg">
  <img width="454" height="341" src="assets/EnterPreFix2.jpg">
</p>

Next you will be presented with your two anti-phishing words. Write these down on your notecard.

<p align="center">
  <img width="605" height="454" src="assets/AntiPhishingWords.jpg">
</p>

Next, enter your PIN suffix, then write it down on the notecard and hit <kbd>OK</kbd>.

<p align="center">
  <img width="454" height="341" src="assets/EnterSuffix.jpg">
  <img width="454" height="341" src="assets/EnterSuffix2.jpg">
</p>

Then you will be asked to re-enter your PIN prefix, confirm the two anti-phishing words, and enter your PIN suffix. The COLDCARD will save that information and then open up the wallet where you can generate your seed phrase.

## Generating a seed phrase
There are a couple considerations you may want to make when creating a seed phrase. For example, COLDCARD will generate a seed phrase for you by default, as shown in the [Ultra Quick guide](https://github.com/econoalchemist/ColdCard-UltraQuick). However, maybe you don't trust the True Random Number Generator (TRNG) in your COLDCARD, you can introduce some of your own randomness using a six sided dice and combine that with the COLDCARD's TRNG entropy. If you still don't trust the COLDCARD is doing what it purports to be doing then you can generate additional entropy with dice rolls and even verify the dice roll math as shown in the [Paranoid guide](https://github.com/econoalchemist/ColdCard-Paranoid).

In the steps below you will see how to add some of your own entropy using a six sided dice combined with the TRNG entropy from the COLDCARD to generate your seed phrase. After setting up the PIN, you should be at the COLDCARD main menu. Select `New Wallet` and after a moment you will be presented with 24 words. However, to add some of your own dice roll randomness, scroll down to the bottom of the word list and select <kbd>4</kbd> to add some dice rolls.

<p align="center">
  <img width="454" height="341" src="assets/NewWallet.jpg">
  <img width="454" height="341" src="assets/AddEntropy.jpg">
</p>

Each 6-sided dice roll gives you 2.58 bits of additional entropy `(log2(6))`. For reference, it would take the world's most powerful supercomputer trillions of years to brute force a 256 bit key. The COLDCARD's TRNG has already picked 256 random bits at this point, but when you roll more, each time you are adding 2.58 bits of entropy on top of those bits. So roll the dice and enter the corresponding number for each roll. Repeat this process as much as you want. If you roll less than 50 times then the COLDCARD will add the remaining necessary entropy with the TRNG. Then hit <kbd>OK</kbd>.

<p align="center">
  <img width="804" height="605" src="assets/ZeroRolls.jpg">
</p>  

Now you will be presented with a new list of 24-words. Write these words down in order on your notecard. Then double check your work. 

<p align="center">
  <img width="454" height="341" src="assets/SaveWords1.jpg">
  <img width="454" height="341" src="assets/SaveWords2.jpg">
</p>

Next, you will be asked to take a test to prove you wrote the words down correctly. 

<p align="center">
  <img width="806" height="605" src="assets/Test.jpg">
</p>  

After passing the test, you will be at the COLDCARD's main menu. Best practice is to test your backup information before depositing any bitcoin. The basic idea is to use only your written backup information in an attempt to restore your wallet. If all of your backup information is correct and you successfully restore your wallet then you know that you can recover any bitcoin deposited to that wallet with that backup information. First you need a way to identify your wallet. Your newly generated wallet has a unique fingerprint which you can find from the main menu by navigating to `Advanced` > `View Identity`. You will find a unique 8-character fingerprint such as `99E870EF`. Write that fingerprint down. Now you can destroy the seed on your COLDCARD by again navigating to `Advanced` then `Danger Zone` > `Seed Functions` > `Destroy Seed`. Then you will be presented with a couple of warnings, after confirming, your seed will be destroyed and you will be brought back to the login page where you enter your PIN. Log back into your COLDCARD and from the main menu navigate to `Import Existing` > `24 words` and then start entering your seed words in order from your backup card. Start by scrolling down until you see the first letter of your word, then scroll down to the next nearest part of the word, and keep narrowing down the search until you arrive at the word you need. For example, `t` > `th` > `thr` > `throw` then hit <kbd>OK</kbd> and repeat the process for the next word. If you make a mistake, you can hit <kbd>Cancel</kbd> to go back and reselect a word. After you enter the 23rd word, COLDCARD will compute a list of 8 possible options for your 24th word. Select your 24th word from that list. If you do not see your 24th word on that list then you either made a mistake entering the first 23-words or you wrote down your backup information incorrectly. After selecting the 24th word and hitting <kbd>OK</kbd> the seed will be applied and then you can navigate back to `Advanced` > `View Identity` and confirm the fingerprint is correct. 

Your COLDCARD is ready to start receiving deposits, next we'll set it up as a "watch-only" wallet in Sparrow Wallet and demonstrate how to transact in an air-gapped fashion. If you are interested in adding the additional security of a passphrase to your COLDCARD wallet, then check out the [Paranoid guide](https://github.com/econoalchemist/ColdCard-Paranoid).

## Backup recommendations
Careful considerations should be made in regards to how the wallet backup information will be stored. The information required for a proper backup varies depending on how the wallet was setup. These requirements may be only 24-words for a simple wallet or the requirements can include 24-words, a passphrase, master fingerprint, derivation path, and more. There are several options when it comes to picking a storage medium, each has its own set of tradeoffs. Writing the 24-words on paper is a good start and helps mitigate the risks associated with having a digital copy of the backup information. With the backup information written down on paper, an adversary would need physical access to the paper in order to retrieve the information. Where as a photo, text file, or other digital medium can be copied and replicated and shared quickly. 

The trade off with paper backups is that they do not withstand fire or flooding very well. This is where steel backups come into play. Robust backups made from stainless steel can withstand fire temperatures beyond the range of a typical house fire, up to 1,500°C. Also stainless steel backups can withstand being submerged in water for extended periods of time. There is a wide range of steel backups available. Coinkite offers the [SEEDPLATE](http://bitcoinseedbackup.com/) which gives users a robust backup option that is resistant to fire and flooding as well as easy to conceal.   

<p align="center">
  <img width="950" height="529" src="assets/IMG_6687.JPG">
  <img width="950" height="713" src="assets/IMG_6688.JPG">
</p>

These stainless steel plates are etched with a grid on both sides. The grid contains the alphabet along the Y-axis and 48-columns along the X-axis. The 48-columns are split into 12 groups of 4-columns. Each of the 12-groups has enough room for 4-letters. Only the first 4-letters of each BIP39 seed word is required in order to restore the wallet as no two words on the BIP39 word list share the same sequence of the first 4-letters. 

Use a marker to indicate the first 4-letters of the first 12-words on one side of the plate and then flip the plate over and repeat the process for the 13th through 24th words. Double check your work then use a spring-loaded punch to stamp the plate on each mark.

<p align="center">
  <img width="950" height="713" src="assets/IMG_6689.JPG">
  <img width="950" height="713" src="assets/IMG_6692.JPG">
</p>

Now you have a robust stainless steel backup that can withstand fire and flood. This backup plate is easy to conceal measuring in at 127mm X 76mm x 1.5mm so that it can be hidden in a variety of places and environments. 

