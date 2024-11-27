1. [Hyperledger](index.html)
2. [LF Decentralized Trust](LF-Decentralized-Trust_19595266.html)
3. [Calendar of Public Meetings](Calendar-of-Public-Meetings_19595324.html)

# Hyperledger : Managing Zoom Meetings

Created by Tracy Kuhrt, last modified by David Boswell on Mar 26, 2024

This information is for community members who are hosting meetings.  Zoom is the main video communication platform for Hyperledger and is used to run community calls and virtual meetups.  A Zoom host needs to know the following information to deal with any issues that may happen during a meeting.  This could include issues such as a lot of background noise on the call because someone is unmuted or someone has joined the call and is trying to be disruptive.

- [Code of Conduct](#ManagingZoomMeetings-CodeofConduct)
- [Obtaining Host Access](#ManagingZoomMeetings-ObtainingHostAccess)
- [Claiming Host in a Meeting](#ManagingZoomMeetings-ClaimingHostinaMeeting)
- [Default Meeting Settings](#ManagingZoomMeetings-DefaultMeetingSettings)
- [Recording a Meeting](#ManagingZoomMeetings-RecordingaMeeting)
- [Moderating Meetings and Dealing with Disruptions](#ManagingZoomMeetings-ModeratingMeetingsandDealingwithDisruptions)
- [Screen sharing guidelines and recommendations](#ManagingZoomMeetings-Screensharingguidelinesandrecommendations)
- [Escalating and/Reporting a Problem](#ManagingZoomMeetings-Escalatingand/ReportingaProblem)
- [Audio/Video quality recommendations](#ManagingZoomMeetings-Audio/Videoqualityrecommendations)
  
  - [Recommended hardware to have](#ManagingZoomMeetings-Recommendedhardwaretohave)
  - [Hardware we don't recommend](#ManagingZoomMeetings-Hardwarewedon'trecommend)
- [Pro-tips](#ManagingZoomMeetings-Pro-tips)

## Code of Conduct

The Hyperledger project adheres to our [Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct) and all meeting attendees are expected to follow these guidelines.  As host, please read and familiarize yourself with the Code of Conduct details.

## Obtaining Host Access

If you are a project lead, Working Group or Special Interest Group lead, meetup organizer or another community who needs to host a Zoom meeting and you would like host access, please email [community-architects@hyperledger.org](mailto:community-architects@hyperledger.org).

## Claiming Host in a Meeting

When you join a meeting, you'll need to claim host in order to have host access. To claim host, follow these steps:

- Have the [latest version](https://zoom.us/download) of the Zoom client installed.
- Dial in to your call
- Use the [host key](https://support.zoom.us/hc/en-us/articles/205172555-Host-Key) to "[claim host](https://support.zoom.us/hc/en-us/articles/115001315866-Claiming-host-in-Zoom-Rooms-using-the-host-key)"

Here is a [video that shows the process of claiming host on Zoom](https://drive.google.com/open?id=1wBT7mTFlX3QefhMkqwPpqf9VlX1J-Jij).

## Default Meeting Settings

Be aware that our Zoom accounts have configured some default settings to prevent people from interfering with meetings.  As host, you should be aware of these so that you can help address and modify settings as needed.

- [Disabled “join before host”](https://support.zoom.us/hc/en-us/articles/202828525-Join-Before-Host)
- [Default to participants muted on join](https://support.zoom.us/hc/en-us/articles/115005759423-Managing-participants-in-a-meeting)
- [Disabled file transfer/sharing](https://support.zoom.us/hc/en-us/articles/209605493-In-meeting-file-transfer)
- [Disabled screen annotations for users](https://support.zoom.us/hc/en-us/articles/115005706806)

## Recording a Meeting

One of the main roles of a host is to record and share meetings after for anyone who missed the call.  Since we are a global community with people all over the world, there will be community members who are interested in your meeting that won't be able to attend because of time zone issues and other conflicts.  For most community calls you can handle recordings by following these instructions:

- Most Zoom calls are set to automatically record as soon as you start.  After claiming Zoom host you have the ability to pause or stop recording but we recommend that you don't.  Some hosts like to pause recordings for the first few minutes while people dial-in and before the meeting starts.  We've found though that sometimes hosts forget to unpause and then the calls aren't recorded, so we recommend not pausing or stopping recordings.
  
  - If you are the host of a Zoom call that isn't set to automatically record, you can claim host and start the recording and set it to record to the cloud.  Please also reach out to the Community Architects so we can update the settings for your call so recording will be automatic.
- When the meeting ends the recording will be moved over to the Hyperledger YouTube channel.  This process can sometimes take a day or two.  To find your video, you can look through the [recently uploaded videos on the channel](https://www.youtube.com/@Hyperledger/videos).  If you don't see it there feel free to ask one of the Community Architects and they'll be able to help you find your video.
- Once you have the link to the video, we recommend that you add it to the meeting page for the call so people can find the link there.  You can also share it with people on your Discord channel or any other community forums you use.  You can also coordinate with the Community Architects to get a playlist set up on the Hyperledger YouTube channel so all of your videos will be in one place.

## Moderating Meetings and Dealing with Disruptions

After the meeting has started you can make use of the following host features to moderate your meetings and deal with any bad actors:

- Prepare to mute people who are making unwanted noises – this will usually be people who don't realize that they are unmuted, but it could be people who are trying to make distracting noises.  As host, you can select specific participants and mute them.  Make sure you have the participant list view open while hosting a meeting and it will show you the mute/unmute status of everyone in the meeting.
- [Assign a co-host to help with moderation](https://support.zoom.us/hc/en-us/articles/206330935-Enabling-and-adding-a-co-host)
- [Turn **off** screen sharing for everyone and indicate only host](https://support.zoom.us/hc/en-us/articles/115005759423). If you have others that need to share their screen, the host can enable that on the fly. (via the `^` menu next to **Share Screen**). Be on the lookout for people that you don't know who are requesting to get screen access.
- [Put the troll or bad actor on **hold**](https://support.zoom.us/hc/en-us/articles/201362813-Attendee-on-hold). The participant will be put into a "[waiting room](https://support.zoom.us/hc/en-us/articles/115000332726-Waiting-Room)" and will not be able to participate in the call until the host removes the hold.
  
  - **NOTE:** Depending on your client version this will be called "**Put in Waiting Room**" instead of on **hold**.
- [Remove the participant](https://support.zoom.us/hc/en-us/articles/115005759423-Managing-participants-in-a-meeting). Please be cautious when testing or using this feature, as it is **permanent**. They will never be able to come back into that meeting ID on that particular device. Do **not** joke around with this feature; it's better to put the attendee on "hold" first and then remove.

**NOTE:** You can find these actions when clicking on the **more** or **"..."** options after scrolling over the participants name/information.

For more information about moderating meetings, check out the Zoom blog post: [How to Keep Uninvited Guests Out of Your Zoom Event](https://blog.zoom.us/wordpress/2020/03/20/keep-uninvited-guests-out-of-your-zoom-event/).

## Screen sharing guidelines and recommendations

Zoom has a [documentation on how to use their screen sharing feature](https://support.zoom.us/hc/en-us/articles/201362153-How-Do-I-Share-My-Screen):

Recommendations:

- Turn off notification to prevent any interference.
- Close all sensitive documents and unrelated programs before sharing the screen eg. Emails.
- Test your presentation before hand to make sure everything goes smoothly.
- Keep your desktop clean. Make sure there is no offensive or/and distracting background.

## Escalating and/Reporting a Problem

Issues that cannot be handle via normal moderation should be reported to the Community Architects.  Please email [community-architects@hyperledger.org](mailto:community-architects@hyperledger.org).

## Audio/Video quality recommendations

While video conferencing has been a real boon to productivity there are still [lots of things that can go wrong](https://www.youtube.com/watch?v=JMOOG7rWTPg) during a conference video call.

There are some things that are just plain out of your control, but there are some things that you can control. Here are some tips if you're just getting into remote meetings. Keep in mind that sometimes things just break. These are not hard rules, more of a set of loose guidelines on how to tip the odds in your favor.

### Recommended hardware to have

- **A dedicated microphone** - This is the number one upgrade you can do. Sound is one of those things that can immediately change the quality of your call. If you plan on being here for the long haul, something like a [Blue Yeti](https://www.bluedesigns.com/products/yeti/) will work great due to the simplicity of using USB audio and having a hardware mute button. Consider a [pop filter](https://en.wikipedia.org/wiki/Pop_filter) as well if necessary.
- **A Video Camera** - A bad image can be worked around if the audio is good. Certain models have noise cancelling dual-microphones, which are a great backup for a dedicated microphone or if you are travelling.
- **A decent set of headphones** - Personal preference, these cut down on the audio feedback when in larger meetings.

What about an integrated headset and microphone? This totally depends on the type. We recommend testing it with a friend or asking around for recommendations for which models work best.

### Hardware we don't recommend

- **Earbuds**. Generally speaking they are not ideal, and while they might sound fine to you when 50 people are on a call the ambient noise adds up. Some people join with earbuds and it sounds excellent, others join and it sounds terrible. Practicing with someone ahead of time can help you determine how well your earbuds work.

## Pro-tips

- [Join on muted audio and video](https://support.zoom.us/hc/en-us/articles/203024649-Video-Or-Microphone-Off-By-Attendee) in order to prevent noise to those already in a call.
- If you don't have anything to say at that moment, **MUTE**. This is a common problem. You can help out a teammate by mentioning it on Zoom chat or asking them to mute on the call itself. The meeting co-host can help with muting noisly attendees before it becomes too disruptive. Don't feel bad if this happens to you, it's a common occurrence.
- Try to find a quiet meeting place to join from; some coworking spaces and coffee shops have a ton of ambient noise that won't be obvious to you but will be to other people in the meeting. When presenting to large groups consider delegating to another person who is in a quieter environment.
- Using your computer's built in microphone and speakers might work in a pinch, but in general won't work as well as a dedicated headset/microphone.
- Consider using visual signals to agree to points so that you don't have to mute/unmute often during a call. This can be an especially useful technique when people are asking for lazy consensus. A simple thumbs up can go a long way!
- It is common for people to step on each other when there's an audio delay, and both parties are trying to communicate something. Don't worry, just remember to try and pause before speaking, or consider raising your hand (if your video is on) to help the host determine who should speak first.

*Thanks to the [Kubernetes Zoom Guidelines](https://github.com/kubernetes/community/blob/master/communication/zoom-guidelines.md) doc for the basis of much of this document.*

Document generated by Confluence on Nov 26, 2024 16:46

[Atlassian](http://www.atlassian.com/)
