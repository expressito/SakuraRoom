# SakuraRoom
SakuraRoom on TryHackMe write-up by express

![Screenshot_2021-04-13 TryHackMe Sakura Room](https://user-images.githubusercontent.com/64150407/114520410-b2b5d380-9c41-11eb-883f-f8a701bb9d3c.png)

So first see if there is something in the image :

![Screenshot_2021-04-13_04-20-20](https://user-images.githubusercontent.com/64150407/114530214-05e05400-9c4b-11eb-86ab-92fef803ab2f.png)

And yes we see a username : SakuraSnowAngelAiko !
__________________________________________________________

![Screenshot_2021-04-13 TryHackMe Sakura Room(1)](https://user-images.githubusercontent.com/64150407/114521006-4c7d8080-9c42-11eb-9102-e81fe5570219.png)

So let's find out if the user have a social media with Sherlock.py :

![sher](https://user-images.githubusercontent.com/64150407/114530425-33c59880-9c4b-11eb-8015-b7171c7ff4b8.png)

So with it we see the attacker have a GitHub account, let's check it out !
We see a PGP key and we can find find the email address thanks to this key (https://pgp.help):

![Screenshot_2021-04-13 pgp help - Modern javascript client-side PGP encryption and decryption tool](https://user-images.githubusercontent.com/64150407/114528091-f6600b80-9c48-11eb-94be-ed259ee54867.png)

__________________________________________________________
![Screenshot_2021-04-13 TryHackMe Sakura Room(2)](https://user-images.githubusercontent.com/64150407/114522878-0de8c580-9c44-11eb-8582-0d7a47475a58.png)

If we Google the username we find a LinkedIn account :

![Screenshot_2021-04-13 (2) Aiko Abe LinkedIn](https://user-images.githubusercontent.com/64150407/114528321-31623f00-9c49-11eb-944d-42168189fe0a.png)

So now we got a name and a GitHub account.

__________________________________________________________
![Screenshot_2021-04-13 TryHackMe Sakura Room(3)](https://user-images.githubusercontent.com/64150407/114523335-7e8fe200-9c44-11eb-954a-a748d3f92715.png)

So we see a crypto : E******

![Screenshot_2021-04-13 TryHackMe Sakura Room(4)](https://user-images.githubusercontent.com/64150407/114523472-99625680-9c44-11eb-9661-e068f3c6a5cd.png)

We can go to the ETH repository and see changes in time and we see more information about the wallet :

![Screenshot_2021-04-13 sakurasnowangelaiko ETH](https://user-images.githubusercontent.com/64150407/114528528-653d6480-9c49-11eb-8eed-eee92169f323.png)

So now that we have this we can find the solution for other questions.

![Screenshot_2021-04-13 TryHackMe Sakura Room(5)](https://user-images.githubusercontent.com/64150407/114523737-daf30180-9c44-11eb-83ba-7b5151412315.png)

Answer : E********

![Screenshot_2021-04-13 TryHackMe Sakura Room(6)](https://user-images.githubusercontent.com/64150407/114523778-e6462d00-9c44-11eb-8daa-a4d0211ae9eb.png)

We can see on the etherchain that he made a T***** transfer :

![Screenshot_2021-04-13 Account 0xa102397dbeebefd8cd2f73a89122fcdb53abb6ef - etherchain org - 2021](https://user-images.githubusercontent.com/64150407/114528881-b3eafe80-9c49-11eb-9ee0-230c34eb6eb1.png)

 Answer : T*****
 ____________________________________________________________
 
 ![Screenshot_2021-04-13 TryHackMe Sakura Room(7)](https://user-images.githubusercontent.com/64150407/114524135-3de49880-9c45-11eb-9481-20a09775e83e.png)
 
 So we got this screenshot and we see the username @AikoAbe3 and with a search on Twitter we find the updated username which is @Sakura********* :
 
 ![taunt](https://user-images.githubusercontent.com/64150407/114524249-58b70d00-9c45-11eb-9c5f-4216ab505485.png)
 
 ![Screenshot_2021-04-13 Aiko ( SakuraLoverAiko) Twitter](https://user-images.githubusercontent.com/64150407/114529090-e5fc6080-9c49-11eb-97c8-acc9911e2ade.png)

 ![Screenshot_2021-04-13 TryHackMe Sakura Room(8)](https://user-images.githubusercontent.com/64150407/114524562-9d42a880-9c45-11eb-9fcf-ece742b3a028.png)

They give us a hint with a screenshot of the page :

![sakura-17r](https://user-images.githubusercontent.com/64150407/114524735-c105ee80-9c45-11eb-93ff-95b64e9246ec.png)

We can see the beginning of the URL and we see a md5 parameter and we can guess it's the md5 that is display on the screen.

So the final URL is : http://depastedihrn3jtw.onion/show.php?md5=*******************************

![Screenshot_2021-04-13 TryHackMe Sakura Room(9)](https://user-images.githubusercontent.com/64150407/114524996-01656c80-9c46-11eb-80fb-340e11f5240c.png)

So we got the home SSID, we go on wigle.net and we can guess the attacker is Japanese so we check the latitude and longitude of Japan and we query for SSID=DK1F-G:

![Screenshot_2021-04-13 WiGLE Wireless Network Mapping](https://user-images.githubusercontent.com/64150407/114525562-7df84b00-9c46-11eb-8aaa-dcae60b49a47.png)

![Screenshot_2021-04-13 WiGLE Wireless Network Mapping(1)](https://user-images.githubusercontent.com/64150407/114529416-35db2780-9c4a-11eb-8b2f-8bf5e6e8468b.png)

Nice ! We found one BSSID : 84:AF:**:**:**:**

_____________________________________________________________

![Screenshot_2021-04-13 TryHackMe Sakura Room(10)](https://user-images.githubusercontent.com/64150407/114525743-a54f1800-9c46-11eb-9172-8ac9b2b9057c.png)

![Esh-uTvUcAc-sXC](https://user-images.githubusercontent.com/64150407/114526046-ec3d0d80-9c46-11eb-8794-4576f25757c5.jpg)

So we can see on the picture an obelisk and cherry blossoms, we check on Google Maps the closest airport from Washington Monument and we found R***** Airport with code D**.

![Screenshot_2021-04-13 TryHackMe Sakura Room(11)](https://user-images.githubusercontent.com/64150407/114526139-fced8380-9c46-11eb-873f-54c5d5aab0ec.png)

![EsiM12KVoAEhAsI](https://user-images.githubusercontent.com/64150407/114526155-0119a100-9c47-11eb-8c1e-61d3c820fc17.png)

So we see on the picture "First Class Lounge Sakura Lounge" and simply by googling we found that the H***** Airport have it. Code : ***

![Screenshot_2021-04-13 TryHackMe Sakura Room(12)](https://user-images.githubusercontent.com/64150407/114526447-48079680-9c47-11eb-8ecf-35b30f70c57d.png)

We check the lake on Google Maps and we find the name of the lake : L** I*********

![Screenshot_2021-04-13 TryHackMe Sakura Room(13)](https://user-images.githubusercontent.com/64150407/114526675-7f764300-9c47-11eb-8e66-2943059893f4.png)

![Screenshot_2021-04-13 WiGLE Wireless Network Mapping(2)](https://user-images.githubusercontent.com/64150407/114526805-99b02100-9c47-11eb-9296-8b264fdd3174.png)

Thanks to the BSSID we can see that the attacker lives in H*******

Thank you to have read this writeup :) My THM profile : https://tryhackme.com/p/express
