# LoinWeb

> "LoinWeb was inspired by my personal blog called Lomen, and I spent a lot of time on this personal blog, including accessing materials, flipping through books, learning git language and so on. I once thought: Lomen is my place of creation and programming, then how if the entire Internet is added? This is how LoinWeb was born."

LoinWeb, is a comprehensive website dedicated to high-end geeks and programmers.The features of this website include the following :

1. LoinWeb's unique "World~ House" allows all users of the entire network to conduct a full-scale discussion. You can create a "Domain" in the World~ House and put this field on the "Layered" type it should be on. For example, if you want to build a discussion house about Cpp Editing, then you shall find the layered "C++Programming" in the World~ House, and then,  in this Layered, look again for the category that suits your discussion. The figure below is a good illustration of this.![Pic-WorldHouse](https://api.superbed.cn/pic/5c41c3799dc6d6a3f95943fa)

2. If you encounter a hit in the discussion room, you can also establish a Connection with him or her. The specific operations are described below. So what is the use of the connection?

   1. You will be able to have a separate real-time conversation with him/her like MSN or Facebook Messager, and all his conversations are confidential.

   2. LoinWeb​'s specific IDE: LoinWebber​ can support two-person compilation mode. You can enter LoinWebber​'s connection mode (Connecting~ Mode)​ to achieve two-person online coding after connection. That is to say, you can divide the code into two parts. Open but you can only compile your own, you can also achieve two people compile a piece of code at the same time! Of course, pay attention to the coordination of the two, so it is recommended to use Loin Talk, the built-in voice system of Loin Web.

   3. A powerful chat system. The text format of the chat system here is completely customizable! Inside, you can use the text you are used to, such as Markdown, Latex, etc., which is very convenient for spelling and emphasizing the formula. In addition, when using Markdown, you don't have to worry about the complexity of sending images, because when you use markdown to upload images on the network, you can still use the built-in system to send local images!

   4. Support a lot of small operations, such as remote desktop control, video chat, real-time code modification and so on. Below is Sublime, and the surface of LoinWebber is just like that.![Pic-CodeMode](https://api.superbed.cn/pic/5c41c8229dc6d6a3fa0c9690)

   5. This code below can help you connect to any online user of LoinWeb, of course, the  premise is that the other promises your request. Of course, if you don't know the other's LIP (LoinWeb Identification of Position), you can also use the following code to pass the other party's Name. Make a connection request.

      ```SLC
      LoinWeb Operation_ConnectRequest::user.name<Example>
      ```

      When you are invited, your SLC system will pop up a message stating that you have been invited to connect with... and will be accompanied by the username and LIP address of the other party.

      ```SLC
      ![New Message]!::"One want to connect with you![name<Jack>&LIP<Poster12345>]".Response with"Yes"or"Not".−−From System
      ```

3. Sometimes the connection is not the only way to communicate. For short messages, you can use the built-in Message of SLC in LoinWeb for information transmission. When you want to be interrupted for a period of time or to brew feelings, you can choose to use long information, that is, the content of the mail is sent to the other party, and the connection may not be connected, but the information you send us will Save to the other party to accept it! And the information transmission is to charge some fees, the long mail function is very powerful, so a long mail needs to charge 0.1LoinCoin

   ```SLC
   LoinWeb Operation_Message::New Message(Short)"Come to the library at 9:00!"To:user.name<Example>
   ```

   Like that, you send the Example user a short message with the content "Come to the library at 9:00!". For each short message, the system will calculate the number of characters minus your small amount of Loin Coin. When you receive the information, the system will prompt you to send out the short message to deduct a total of how much you have deducted from the coinage, and the total number of coins you have.

   ```SLC
   ![New Message]!::"The Message you send to <Example> has been received!A total of 0.04 Loin Coin will be deducted from this information,and you still have 1692.56 Loin Coin!"--From System
   ```

   If you want to edit a long article, the code is as follows:

   ```SLC
   LoinWeb  Operation_Message::New Message(Long)::@Start@ with Markdown
   ```

4. Multiplayer connection. After you have connected a user, you can still use the @System::Call Out@ command to call up the command console to connect to another user and then use @System::End@ to return to the connection.Just like that:

   ```SLC
   ==> LoinWeb Operation_ConnectRequest::user.name<Floser>
   ~ ![New  Message]!::"Successfully Connect Floser!." −−From System
   <==Floser :: Hello Mark !
   ==> @System::End@
   --- Message Box[Floser BOX]  ---
   Floser :: Hello Keinsz.S !
   You :: Yeah, Hello Floser.
   Floser :: You invited S.S ?
   You :: Not YET, wait...
   @System::CallOut@
   --- Message Box[Floser BOX]  ---
   ==> LoinWeb Operation_ConnectRequest::user.name<S.S> into [Floser BOX]
   ~ ![New  Message]!::"Successfully Connect S.S into Floser BOX!." −−From System
   ==> @System::End@ to [Floser BOX]
   --- Message Box[Floser BOX]  ---
   Floser :: Hello Keinsz.S !
   You :: Yeah, Hello Floser.
   Floser :: You invited S.S ?
   You :: Not YET, wait...
   S.S :: Hello!!
   
   ......ect.
   ```

5. LoinWeb's own LoinWebber compiler can support 90% of the languages that are still in use today, and has a powerful, comprehensive code modification, debugging, editing system, and LoinWebber settings are completely public, so if you think of LoinWebber's interface If you don't match your personality, you can modify Settings directly, and there is a plugin domain for LoinWebber on LoinWeb. You can download your favorite plugins directly from it.

6. LoinWeb has a Code Management Warehouse for all users. It is also known as the CMW library. All your code in LoinWebber, or any code in your locality can be saved to the CMW library. You can choose to These files are public, or hidden, and can even be passworded.

   ```SLC
   LoinWeb Operation_FileUpload::[C:/windows/A.cpp]=>=[Example:/CPPS]
   ```

   And you can also download CMW's file to your own computer.

   ```SLC
   LoinWeb Operation_FileDownload::[Example:/CPPS/A.cpp]=>=[C:/Windows/A.cpp] 
   ```

7. In fact, the CMW library can store more than just code. You can also use the CMW library to upload any software, images, videos, etc. in your local area. If you are willing to disclose the resources you have, then you can access the entire network. And download your resources! You can also find the software you want, etc. in the CMW Community (CMWC.com).

   ```SLC
   LoinWeb Operation_WebD::[https://CMWC.com/Floser/Example/CPPS/A/DownloadPage]=>=[F:/]
   ```

8. Question Set. LoinWeb has set up an in-house question bank, but the amount of questions in it will not affect your rankings or personal reputation, and you can also choose to hide information such as your amount of questions, because LoinWeb's question bank must have no other Websites dedicated to the question bank are more efficient. You can choose to do some topics of interest in the internal station. You can also upload questions that you find helpful.

   The following is the code to submit the code to the question set.

   ```SLC
   LoinWeb Operation_Submit::[C:/windows/A.cpp]=>=[Pinks01063]
   ```

9. Competition. LoinWeb will hold regular competitions. Users can also hold informal competitions after being reviewed by official officials. The official competitions organized by LoinWeb are divided into three types: 

   1. LPM: Loinweb Practice Match: Loin practice. This kind of competition is once a week. It doesn't affect the individual except the calculation of Loin Rating. It just exercises the exercises on the subject and adapts to the test. 
   2. LPC: LoinWeb Preparatory Competition: Loin Preliminaries. This kind of competition is once a month, lasts for three days, and there are a total of 9 questions. The P_Rating obtained in this game is more useful. He can decide whether you can be selected for the next game. Of course, this selection rule is a comparison. Strict, specific to the number of applicants in the next competition. Since there are very few people who can participate in the next competition, each time the LPC will also have a ranking, each of the top 10 will have 1000 500 worth of prizes. 
   3. LC: LoinWeb Championships, this kind of competition can be said to be global, and the cycle is one year. LC is not an ordinary examination system, and not all users can participate. Each LC will select the users that can be selected based on the P_Rating won by the 12 LPCs of the previous year. (Of course, for users who cheated, LoinWeb officially cancels all the powers of the game and will show the list for one month.) LC will select about 1,000 people in total, then group all the players and select the highest score of 200 people. For the knockout, yes, it’s the knockout. In the knockout round, 10 players will be played against each other. Later, the number will be reduced as appropriate. There are only two questions in each knockout, and the right ones will be promoted and the wrong ones will be lost. The final selection of the top 8 will be a unified venue competition, called the LCF (LoinWeb Championships Final), which is the finals. The final third-place champion will receive the gold and silver bronze medals made by LoinWeb and a large number of bonuses. LC is a big event for users of Loin.com, and users who can achieve excellent results on the LC list are also a glory. Loin will issue Rating to users on the LC list. Users who can enter the top 200, that is, the Big Melee, will be upgraded to Loin Vip. Of course, the personal information of the top eight players must be fully disclosed. The users who won the third place in the championship will be upgraded to the Principal Member and named "Crown of LoinWeb". The third place name is bronze, the runner-up is silver, and the champion is gold.

10. Vip system. Loin's Vip is divided into three types.

    1. Ordinary members: recharge. However, by recharging, only ordinary members can be obtained, while ordinary members have the least power, but are higher than ordinary users. And ordinary members do not have a grade, the recharge is 99 LoinCoin/Year
    2. Senior Member: The game is coming. The official will select the top 100 in each LPC competition and the top 200 in each LC list to issue senior members. The top 100 in the LPC competition will issue semi-annual senior members, and the top 200 in the LC competition will issue one-year senior members. Premium members have higher privileges than regular members and cannot be recharged.
    3. Principal Members: The coming of the game. Very demanding, only the top 16 of each year can qualify as a special member, with the highest authority and another authority: to enter the management. The stratified managers of the LoinWeb World House are basically selected by ordinary users. Those who have higher rankings in the three competitions have the opportunity to select management. Of course, it is necessary to ensure that they can spend a lot of time managing them. Layered. The Principal Members can be exempted from selection and directly enter the management team if they have the will. After entering management, you have the opportunity to get in touch with the deeper LoinWeb.

11. Team. LoinWeb can create team operations, and you can invite like-minded friends to join the team. The team's functions are as follows:

    1. Team Discussion. Each team has a discussion room built in. This discussion house supports code uploading. You can upload your code to the code module in the team's built-in discussion room. Please ask the whole team to help you modify it!
    2. Team Built-in Competition(TBC). Some built-in team games don't have to be known to the whole network, then you can build a game in the team!
    3. Team Exams. After the team test is started, the system will keep the PDF of the test topic interface and send it to each user's default PDF and open it, then call up the LoinWebber side. After that, LoinWeb will close all pages except PDF and LoinWebber and cut off the network. Connect until the completion of the transaction.
    4. Team Memo. You can apply for team management to add information to the team memo. This makes the whole group able to see your information that will not be forgotten.
       (5) Team Call. Send information jitter to the entire group of online users.
