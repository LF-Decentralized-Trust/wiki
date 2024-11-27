1. [BootcampHK (archived)](index.html)
2. [BootCamp - Hong Kong](BootCamp---Hong-Kong_23102870.html)
3. [Bootcamp Results](Bootcamp-Results_23103386.html)

# BootcampHK (archived) : Eve of being technical ambassador -- David Liu

Created by david liu, last modified on May 02, 2019

Until the last minute to launch Hyperledger Bootcamp Hong Kong, I have been thinking about it.

During the preparatory stage, I had a lot of discussions with my friends in the Chinese community. Since the form of Bootcamp is the first attempt of Hyperledger, how the community response has always been a mystery. Questions includes:

1. how many developers are willing and able to participate in working hours
2. Compared to traditional hackfest that can bring direct market effect to the company. Do companies have enough motivation to support the BootCamp？
3. BootCamp does not adopt the format of lecturing or workshop, but emphasizes improvisation, free to join or leave, ad-hoc roundtable discussion, and the purpose is to eliminate people's fear in contribution project. It does not necessarily have the preset guide or course syllables.
4. Hyperledger's most famous framework projects, Hyperledger Fabric and Hyperledger Sawtooth, are mostly focused. Whether the enthusiasts have enough patience to learn and understand in just two days?
5. Due to the weakness of the software industry in Hong Kong over the years, will there be a shortage of participants.
6. General local travel problems in Hong Kong

Thanks to Dorothy of Hyperledger Marketing for providing us with local guidance. Thanks to the Hongkong community leader Edmund for giving us an open letter to company managers. As well as a lot of preparation and publicity work done by the Linux Foundation from behinds, problems 1, 2, 6, 7 have been roughly mitigated.

My daily work involves the development of fabric application and infrastructure. Last year, I also issued some suggestions and improvements for fabric-sdk-node, but after all, I am not a maintainer of Fabric, not even a core contributor. Therefore, I could have participate BootCamp as a audience and learner(and I was willing to). For example, it is a rare opportunity to take a single photo of all three co-chairs of the Hyperledger TWGC, F2F learn about the Fabric interop working group progress from Tong Li as well as discuss roadMap of Cello. For myself, I had only prepared a more relaxed session. But as the event time approached, I gradually felt the community need me to take more responsibility in BootCamp such as:

The FIRST Hyperledger BootCamp is held in Hong Kong and I am responsible for taking care guests as a host. 

But my worrying stood still for that no silver bullets to questions 3, 4, 5, and 6 which critical to BootCamp. We can only try our best.

# The eve

The afternoon before the event, I was doing some pre-arrangement for leave during the Bootcamp. When WeChat sounded, Baohua sent a picture in the group of participants. I realized that some friends arrived. Since the company is on the 5th floor above the venue, I sneaked on to see what I could help.

![](attachments/23103392/23103393.png?height=250)

When I first got out of the elevator, I saw Silona Bonewald. She looked serious and introduced me around the venue. Then I entered the main hall with her, witnessed the LF staffs were busy setting up the venue. Baohua is also among them. I even found out that the entire open source team of Huawei has arrived.

I looked at the Fabric table I would be using tomorrow. In my previous idea, I did not plan to engaged on March 7. Later, Dorothy hoped that I could help in the registration process on the morning of the 7th, and just a few days before the start of the event, Jay Guo, one of TWGC chairmans could not participate in person due to VISA issue. Once notified, I suggested and promised that Zhenhua Zhao and I can help him set up a remote session. So I must attend on the first day. Zhenhua Reminded me also that if I use the table, I might not have a big screen or a projector, so I had borrowed a monitor from the company in advance for the needs. The Fabric table is the first table close to ball area. Like all other tables, a power strip is prepared below.

# The first day

Unfortunately weather was bad, there was wind and rain. The Cyberport is far from downtown. But in the end it almost has no impact on the number and passion of attendees. At 8 o'clock in the morning, I went to the registration counter to help. At around 8:30, a large number of guests arrived almost at a moment to make a long queue, and the registration work was also carried out at the same time. I forgot the time and was still busy until the training camp started at 9:00, and our VP of Asia Pacific, Julian Gordon came out from the venue and notify me that the opening session had already begun and let me go in immediately

The timing also means that the Fabric remote session will start right away. In the gap between Silona's speech, I carried the screen from upstairs. At the beginning, I designed Jiannan to open a zoom conference with me only and I would share my screen. However, my monitor is too small compared to the roundtable, and the sound volume of my notebook is week for distant audience. As reminded by the participants, the layout was immediately changed to allow the listener to directly join the zoom conference, so that the volume and display problems were solved. I carefully checked each audience's computer to make sure everyone was ready. During the session, in order to prevent the network video traffic within this local area too large, I checked the audience's computer again and suggested that they temporarily turn off the microphone and camera.

After the situation gradually stabilized, everyone was immersed in Jiannan’s speech, and I took the opportunity to look around other tables. At the end of the Session, I encourage everyone to talk about ideas and questions freely to enrich our interactions. Some listeners are interested in the source code of Fabric Orderer, and then Jiannan added a new wonderful and in-depth section correspondingly. At the closure, Jiannan said that he spared two entire days available to  continue and lead Fabric session. This is a very strong support, thus I intend to leave some private time for myself in the afternoon.

After lunch time, I went to the training room to listen to Tong's introduction to the Hyperledger Cello project. When coming to the configuration file parsing part, I received Mr. Pan's WeChat (it happened that he is also my university classmate and participant of BootCamp), and wondering whether there is arrangement in the afternoon. I felt guilty right after seeing this. I picked bags up and went back to the Fabric table. To my surprise, although I have stated that there is no special arrangement in the afternoon, the Fabric table is still fully surrounded by expectant audiences.

I have an idea in my mind. This extra time may be the best place to demonstrate Bootcamp.

I sit down and opened my coding environment. I first publicly asked if audiences were ready with LFID (Linux Foundation ID). The result was that everyone has already created it. It seems that the guidance this morning is fruitful and gave me confidence. Then I let them to speak out  any problems encountered when using Fabric. In the discussion, one audience mentioned that he did not know which java version is compatible to use fabric-chaincode-java. This is a wonderful question! I immediately decided, invite everyone collaborate to solve this question together this afternoon.

First, it is no written in ReadME. And no result after search key word in the github repository. Some participants said that we can try the integration test in fabric-sdk-java, which may have java-chaincode use case, and then run this use case. These tests are expected to call the local java, so you can test the compatibility by adjusting the version of the local java. Then I downloaded java sdk and found that it is still using the older maven build tool(compared to Gradle), then I have to prepare maven on this machine first. At this time, another participant suggested that it is better to check the gradle build configuration file in java-chaincode first.

Inside the configuration file, a statement is written showing code compatible with java 8

Ola, we find the short cut! Now is time to submit the patch.

I guide the participants to log in to the LFID, clone the code base from gerrit, modify the document in the way that they like, create a new local branch, fill in the commit information according to standards and push it out for review. In the meantime, a participant using macOS had some problems installing git review and struggled with it for a long time, but finally managed to submit the patch.

# The next day

The morning session of the Fabric table was hosted by Zhenhua. After I got up at 6 o'clock on the first day, I arrived the main hall almost at noon. In the afternoon session, I have a well-thought-out story. The title is "fabric-sdk-node: the romance of commits". I will cherry-pick dozens of important commits in the git history, and openly discuss function, patch, design inside and its success or failure. Listeners do not need to write code, and do not need to be proficient in fabric-sdk. My goal is to encourage software engineer to give feedback to me to collect, and I will later convey these voices to maintainers.

I prepared about 50+ such milestone commits like this. Unfortunately, the afternoon was very short to go through all of them. I have only 2.5 hours before wrap up, so it ended with Silona came over and reminded me that time was up when we reached 10+ commits. During the period, hot discussion focused on the error information return format of the proposal responses and the new client side signing feature. The level of passion is much higher than I expected, and I was benefited from high quality discussions.

Finally, the special award to me as Hyperledger Technical Ambassador is really unexpected. If I can know this information in advance, I will definitely put on a suit that day. When Zhenhua called me to the stage, I was still consulting and discussing with Ross Tang about the use case of new features of Hyperledger Fabric 1.4. He is old friend of me from Hyperledger HK community and extremely expertize on both technical and business side. The Fabric table is far from the main stage so I could not hear clearly what I needed to do when I was called. Thanks to Zhenhua told me to report on the session I hosted these two days. I am not prepared for it in English, so it is ad-hoc again. After my report of three sessions finished. Silona suddenly announced that I am the new Hyperledger Ambassador.

Until now, I feel I am not worthy of this title. I did not make much contribution to the community. Many proposals are also anticlimactic. Even more, there are many senior pioneer in front of me, such as Baohua. From a technical point of view, I am only giving some initial guidelines to new community members, and the code contribution quality and quantity is far inferior to Jay and other silent contributors. In this way, this award is more of a responsibility and trust assigned me, urging me to continue to work harder, so as not to be uncoordinated.

![](attachments/23103392/23103394.jpg?height=250)

The above picture shows other valuable gifts I got from BootCamp, the proof of role as community lead, souvenir from Hyperledger and a fresh signature from Baohua on his written book.

## Attachments:

![](images/icons/bullet_blue.gif) [unnamed.png](attachments/23103392/23103393.png) (image/png)  
![](images/icons/bullet_blue.gif) [unnamed.jpg](attachments/23103392/23103394.jpg) (image/jpeg)

Document generated by Confluence on Nov 26, 2024 13:03

[Atlassian](http://www.atlassian.com/)
