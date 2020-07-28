# Agora Flutter Documentation

Agora delivers easy to embed Real-Time Engagement APIs which includes all the development tools and cloud infrastructure needed for mobile, web, and desktop applications.
Use this guide to quickly start a basic video call with the Agora Video SDK for Flutter.


# Prerequisites
- Flutter SDK
- Agora [Flutter SDK](https://pub.dev/packages/agora_rtc_engine)
- Android Studio 3.0+ / VS Code
- A mobile device running Android 4.1 or later
- A valid Agora account ([Sign up](https://console.agora.io/) for free)

## Set up the development environment
- Step 1: Sign up using a valid account on agora dashboard
- Step 2: Go to 'Project Management' tab and click on ' Create'
-  Step 3: Give name to your project and procure an APP ID from there.
-  Step 4: Create a new Flutter project by running the below command in your terminal. 
	> flutter create agoraDemoApp  

- Step 5: Open 'agoraDemoApp' in VS Code or Android Studio.
-  Step 6: Integrate the Agora Flutter SDK in your pubspec.yaml file

```
dependencies:
	flutter:
		sdk: flutter
	agora_rtc_engine: 1.0.5
```
# Agora API Reference for Flutter Development

Agora provides ensured quality of experience (QoE) for worldwide Internet-based voice and video communications through a virtual global network optimized for real-time web and mobile-to-mobile applications.

- [AgoraRtcEngine]() class provides the main methods that can be invoked by your application.
- [addAgoraEventHandlers]() class enables callbacks to your application.
- [channel]() class provides methods that enable real-time communications in a specified channel. 
- [EventChannel]() class provides callbacks that report events and statistics of a specified channel.


## AgoraRtcEngine

You can rename the current file by clicking the file name in the navigation bar or by clicking the **Rename** button in the file explorer.



### Public Member Functions  
Public Function calls

|	Return Type  	|Function	|
|----	|---|	
|abstract int   	|   	[setChannelProfile](#setChannelProfile) (int profile)|
|abstract int   	|   	[setClientRole](#setClientRole) (int role)|
|abstract int   	|   	[joinChannel](#joinChannel) (String token, String channelId, String optionalInfo, int optionalUid)|
|abstract int   	|   	[switchChannel](switchChannel) (String token, String channelId)|
|abstract int   	|   	[leaveChannel](#leaveChannel) ()|
|abstract int   	|   	[renewToken]() (String token)|
|abstract int   	|   	[registerLocalUserAccount](#registerLocalUserAccount)(String appId, String userAccount)|
|abstract int   	|   	[joinChannelByUserAccount](#joinChannelByUserAccount) (String userAccount, String token, String channelId, )|
|abstract int   	|   	[getUserInfoByUserAccount](#getUserInfoByUserAccount)(String userAccount)|
|abstract int   	|   	[getUserInfoByUid](#getUserInfoByUid) (int uid)|
|abstract int   	|   	[enableWebSdkInteroperability](#enableWebSdkInteroperability) (bool enabled)|
|abstract int   	|   	[getConnectionState](#getConnectionState) ()|
|abstract int   	|   	[enableAudio](#enableAudio)()|
|abstract int   	|   	[disableAudio](#disableAudio)()|
|abstract int   	|   	[setAudioProfile](#setAudioProfile)(int profile, int scenario)|
|abstract int   	|   	[adjustRecordingSignalVolume](#adjustRecordingSignalVolume)(int volume)|
|abstract int   	|   	[adjustPlaybackSignalVolume](#adjustPlaybackSignalVolume) (int volume)|
|abstract int   	|   	[enableAudioVolumeIndication](#enableAudioVolumeIndication)(int interval, int smooth, bool vad)|
|abstract int   	|   	[enableLocalAudio](#enableLocalAudio)(bool enabled)|
|abstract int   	|   	[muteLocalAudioStream](#muteLocalAudioStream)(bool muted)|
|abstract int   	|   	[muteRemoteAudioStream](#muteRemoteAudioStream)(int uid, bool muted)|
|abstract int   	|   	[muteAllRemoteAudioStreams](#muteAllRemoteAudioStreams)(bool muted)|
|abstract int   	|   	[setDefaultMuteAllRemoteAudioStreams](#setDefaultMuteAllRemoteAudioStreams())(bool muted)|
|abstract int   	|   	[enableVideo](#enableVideo)()|
|abstract int   	|   	[disableVideo](#disableVideo)()|
|abstract int   	|   	[setVideoEncoderConfiguration](#setVideoEncoderConfiguration)(VideoEncoderConfiguration config)|
|abstract int   	|   	[createNativeView](#createNativeView)(Function(int viewId) created, {Key key})|
|abstract int   	|   	[removeNativeView](#removeNativeView)(int viewId)|
|abstract int   	|   	[setupLocalVideo](#setupLocalVideo)(int viewId, VideoRenderMode renderMode)|
|abstract int   	|   	[setupRemoteVideo](#setupRemoteVideo)(int viewId, VideoRenderMode renderMode, int uid)|
|abstract int   	|   	[setLocalRenderMode](#setLocalRenderMode)(VideoRenderMode renderMode)|
|abstract int   	|   	[setRemoteRenderMode](#setRemoteRenderMode)(int uid, VideoRenderMode renderMode)|
|abstract int   	|   	[startPreview](#startPreview)()|
|abstract int   	|   	[stopPreview](#stopPreview)()|
|abstract int   	|   	[enableLocalVideo](#enableLocalVideo)(bool enabled)|
|abstract int   	|   	[muteLocalVideoStream](#muteLocalVideoStream)(bool muted)|
|abstract int   	|   	[muteRemoteVideoStream](#muteRemoteVideoStream)(int uid, bool muted)|
|abstract int   	|   	[muteAllRemoteVideoStreams](#muteAllRemoteVideoStreams)(bool muted)|
|abstract int   	|   	[setDefaultMuteAllRemoteVideoStreams](#setDefaultMuteAllRemoteVideoStreams)(bool muted)|
|abstract int   	|   	[setLocalVoiceChanger](#setLocalVoiceChanger)(VoiceChanger changer)|
|abstract int   	|   	[setLocalVoicePitch](#setLocalVoicePitch)(double pitch)|
|abstract int   	|   	[setLocalVoiceEqualizationOfBandFrequency](#setLocalVoiceEqualizationOfBandFrequency)(AgoraAudioEqualizationBandFrequency bandFrequency, int gain)|
|abstract int   	|   	[setLocalVoiceReverbOfType](#setLocalVoiceReverbOfType)( AgoraAudioReverbType reverbType, int value)|
|abstract int   	|   	[setLocalVoiceReverbPreset](#setLocalVoiceReverbPreset)(AgoraAudioReverbType reverbType)|
|abstract int   	|   	[enableSoundPositionIndication](#enableSoundPositionIndication)(bool enabled)|
|abstract int   	|   	[setRemoteVoicePosition](#setRemoteVoicePosition)(int uid, double pan, int gain)|
|abstract int   	|   	[setDefaultAudioRouteToSpeaker](#setDefaultAudioRouteToSpeaker)(bool defaultToSpeaker)|
|abstract int   	|   	[setEnableSpeakerphone](#setEnableSpeakerphone)(bool enabled)|
|abstract bool   	|   	[isSpeakerphoneEnabled](#isSpeakerphoneEnabled)()|
|abstract int   	|   	[setRemoteUserPriority](#setRemoteUserPriority)(int uid, UserPriority userPriority)|
|abstract int   	|   	[setLocalPublishFallbackOption](#setLocalPublishFallbackOption)(StreamFallbackOptions options)|
|abstract int   	|   	[setRemoteSubscribeFallbackOption](#setRemoteSubscribeFallbackOption)( StreamFallbackOptions options)|
|abstract int   	|   	[enableDualStreamMode](#enableDualStreamMode)(bool enabled)|
|abstract int   	|   	[setRemoteVideoStreamType](#setRemoteVideoStreamType)(int uid, int streamType)|
|abstract int   	|   	[setRemoteDefaultVideoStreamType](#setRemoteDefaultVideoStreamType)(int streamType)|
|abstract int   	|   	[setLiveTranscoding](#setLiveTranscoding)(AgoraLiveTranscoding config)|
|abstract int   	|   	[addPublishStreamUrl](#addPublishStreamUrl)(String url, bool enable)|
|abstract int   	|   	[removePublishStreamUrl](#removePublishStreamUrl)(String url)|
|abstract int   	|   	[addInjectStreamUrl](#addInjectStreamUrl)(String url, AgoraLiveInjectStreamConfig config)|
|abstract int   	|   	[removeInjectStreamUrl](#removeInjectStreamUrl)(String url)|
|abstract int   	|   	[setEncryptionSecret](#setEncryptionSecret)(String secret)|
|abstract int   	|   	[setEncryptionMode](#setEncryptionMode)(String encryptionMode)|
|abstract int   	|   	[startEchoTestWithInterval](#startEchoTestWithInterval)(int interval)|
|abstract int   	|   	[stopEchoTest](#stopEchoTest)()|
|abstract int   	|   	[enableLastmileTest](#enableLastmileTest)()|
|abstract int   	|   	[disableLastmileTest](#disableLastmileTest)()|
|abstract int   	|   	[startLastmileProbeTest](#startLastmileProbeTest)(AgoraLastmileProbeConfig config)|
|abstract int   	|   	[stopLastmileProbeTest](#stopLastmileProbeTest)()|
|abstract int   	|   	[addVideoWatermark](#addVideoWatermark)(String url, WatermarkOptions options)|
|abstract int   	|   	[clearVideoWatermarks](#clearVideoWatermarks)()|
|abstract int   	|   	[startAudioMixing](#startAudioMixing)(String filepath, bool loopback, bool replace, int cycle)|
|abstract int   	|   	[stopAudioMixing](#stopAudioMixing)()|
|abstract int   	|   	[pauseAudioMixing](#pauseAudioMixing)()|
|abstract int   	|   	[resumeAudioMixing](#resumeAudioMixing)|
|abstract int   	|   	[adjustAudioMixingVolume](#adjustAudioMixingVolume)(int volume)|
|abstract int   	|   	[adjustAudioMixingPlayoutVolume](#adjustAudioMixingPlayoutVolume)(int volume)|
|abstract int   	|   	[adjustAudioMixingPublishVolume](#adjustAudioMixingPublishVolume)(int volume)|
|abstract int   	|   	[getAudioMixingPlayoutVolume](#getAudioMixingPlayoutVolume)()|
|abstract int   	|   	[getAudioMixingPublishVolume](#getAudioMixingPublishVolume)()|
|abstract int   	|   	[getAudioMixingDuration](#getAudioMixingDuration)()|
|abstract int   	|   	[getAudioMixingCurrentPosition](#getAudioMixingCurrentPosition)()|
|abstract int   	|   	[setAudioMixingPosition](#setAudioMixingPosition)(int pos)|
|abstract int   	|   	[getEffectsVolume](#getEffectsVolume)()|
|abstract int   	| 	[setEffectsVolume](#setEffectsVolume)(double volume)|
|abstract int   	|   	[setVolumeOfEffect](#setVolumeOfEffect)()|
|abstract int   	|   	[playEffect](#playEffect)(int soundId, String filepath, int loopcount,double pitch, double pan, double gain, bool publish)|
|abstract int   	|   	[stopEffect](#stopEffect)(int soundId)|
|abstract int   		|   	[stopAllEffects](#stopAllEffects)()|
|abstract int  		|   	[preloadEffect](#preloadEffect)(int soundId, String filepath)|
|abstract int   	|   	[unloadEffect](#unloadEffect)(int soundId)|
|abstract int   	|   	[pauseEffect](#pauseEffect)(int soundId)|
|abstract int   	|   	[pauseAllEffects](#pauseAllEffects)()|
|abstract int   	|   	[resumeEffect](#resumeEffect)(int soundId)|
|abstract int   	|   	[resumeAllEffects](#resumeAllEffects)()|
|abstract int   	|   	[startChannelMediaRelay](#startChannelMediaRelay)(AgoraChannelMediaRelayConfiguration config)|
|abstract int   		|   	[removeChannelMediaRelay](#removeChannelMediaRelay)(AgoraChannelMediaRelayConfiguration config)|
|abstract int   	|   	[updateChannelMediaRelay](#updateChannelMediaRelay)(AgoraChannelMediaRelayConfiguration config)|
|abstract int   	|   	[stopChannelMediaRelay](stopChannelMediaRelay)()|
|abstract int   	|   	[enableInEarMonitoring](#enableInEarMonitoring)(bool enabled)|
|abstract int   		|   	[setInEarMonitoringVolume](#setInEarMonitoringVolume)(int volume)|
|abstract int   	|   	[switchCamera](#switchCamera)()|
|abstract int   	|   	[setLogFile](#setLogFile)(String filePath)|
|abstract int   		|   	[setLogFilter](#setLogFilter)(int filter)|
|abstract int   	|   	[setLogFileSize](#setLogFileSize)(int fileSizeInKBytes)|
|abstract int   	|   	[setParameters](#setParameters)(String params)|
|abstract String   	|   	[getParameters](#getParameters)(String params, String args)|


### Static Public Member Functions    
Static function calls

|	Return Type  	|Function	|
|---	|--		|	
|static synchronized [AgoraRtcEngine](#AgoraRtcEngine)|   	[create](#create)(String appid)|
|static synchronized void|   	[destroy](#destroy)|
|static String   	|   	[getSdkVersion](#getSdkVersion)()|


### Detailed Description

### AgoraRtcEngine
AgoraRtcEngine is the main interface class of the Agora SDK.

Call the methods of this class to use all functionalities of the SDK. We recommend calling the AgoraRtcEngine API methods in the same thread instead of in multiple threads.


#### setChannelProfile
```
setChannelProfile(ChannelProfile profile)
```
Sets the channel profile of the [AgoraRtcEngine](#AgoraRtcEngine).

The AgoraRtcEngine differentiates channel profiles and applies different optimization algorithms accordingly. For example, it prioritizes smoothness and low latency for a video call, and prioritizes video quality for a video broadcast.
Users in the same channel must use the same channel profile.

|Profile	|	The channel profile of AgoraRtcEngine|
|--:	|:--	|
|	0| `CHANNEL_PROFILE_COMMUNICATION`(0): (Default) The Communication profile. Use this profile in one-on-one calls or group calls, where all users can talk freely.
|1|`CHANNEL_PROFILE_LIVE_BROADCASTING`(1): The Live-Broadcast profile. Users in a live-broadcast channel have a role as either broadcaster or audience. A broadcaster can both send and receive streams; an audience can only receive streams.	|
| 2 | `CHANNEL_PROFILE_GAME`(2): The Gaming profile. This profile uses a codec with a lower bitrate and consumes less power. Applies to the gaming scenario, where all game players can talk freely.|

Returns

-   0: Success.
-   < 0: Failure.

> Note: Before calling this method to set a new channel profile, [destroy](#destroy) the current RtcEngine and [create](#create) a new RtcEngine first.
> Call this method before [joinChannel](#joinChannel), you cannot configure the channel profile when the channel is in use.


#### setClientRole()

```
setClientRole(ClientRole role)
```
Sets the role of a user (Live Broadcast only).

This method sets the role of a user, such as a host or an audience (default), before joining a channel.

This method can be used to switch the user role after a user joins a channel. In the Live Broadcast profile, when a user switches user roles after joining a channel, a successful setClientRole method call triggers the following callbacks:

-   The local client: [onClientRoleChanged](#onClientRoleChanged).
-   The remote client: onUserJoined or onUserOffline (USER_OFFLINE_BECOME_AUDIENCE).


|Role	|	Sets the role of user|
|--:	|:--	|
|	1|`CLIENT_ROLE_BROADCASTER`(1): Broadcaster. A broadcaster can both send and receive streams.|
|2|`CLIENT_ROLE_AUDIENCE`(2): Audience, the default role. An audience can only receive streams.|

Returns

-   0: Success.
-   < 0: Failure.


#### joinChannel()

```joinChannel(String token, String channelId, String info, int uid)```
Allows a user to join a channel.

Users in the same channel can talk to each other, and multiple users in the same channel can start a group chat. Users with different App IDs cannot call each other.

You must call the [leaveChannel](#leaveChannel) method to exit the current call before joining another channel.

A successful joinChannel method call triggers the following callbacks:

-   The local client: onJoinChannelSuccess.
-   The remote client: onUserJoined, if the user joining the channel is in the Communication profile, or is a BROADCASTER in the Live Broadcast profile.

When the connection between the client and Agora's server is interrupted due to poor network conditions, the SDK tries reconnecting to the server. When the local client successfully rejoins the channel, the SDK triggers the [onRejoinChannelSuccess]() callback on the local client.

Parameters

| token   |  |
|--|--|
|  |The token for authentication: |
|  |  In situations not requiring high security: You can use the temporary token generated at Console. For details, see [Get a temporary token](https://docs.agora.io/en/Agora%20Platform/token?platform=All%20Platforms#get-a-temporary-token).|
|	|	In situations requiring high security: Set it as the token generated at your server. For details, see [Generate a token](https://docs.agora.io/en/Interactive%20Broadcast/token_server_cpp?platform=CPP).|


|channelId|  |
|--|--|
|  | The unique channel name for the AgoraRTC session in the string format. The string length must be less than 64 bytes. Supported character scopes are: |
|	|	All lowercase English letters: a to z.|
|	|	All uppercase English letters: A to Z.|
|	|	All numeric characters: 0 to 9.|
|	|	The space character.|
|	|	Additional information about the channel. This parameter can be set as null or contain channel related information. Other users in the channel do not receive this message.|

|Info|  |
|--|--|
|  | (Optional) Additional information about the channel. This parameter can be set as null or contain channel related information. Other users in the channel do not receive this message. |

|uid|  |
|--|--|
|  | (Optional) User ID. A 32-bit unsigned integer with a value ranging from 1 to (2^32-1). `optionalUid` must be unique. If `optionalUid` is not assigned (or set to 0), the SDK assigns and returns `uid` in the [onJoinChannelSuccess]() callback. Your app must record and maintain the returned `uid` since the SDK does not do so. |


The `uid` is represented as a 32-bit unsigned integer in the SDK. Since unsigned integers are not supported by Java, the `uid` is handled as a 32-bit signed integer and larger numbers are interpreted as negative numbers in Java. If necessary, the `uid` can be converted to a 64-bit integer through “uid&0xffffffffL”.

> Note: A channel does not accept duplicate uids, such as two users with the same `uid`. If you set `uid` as 0, the system automatically assigns a `uid`.

> Warning: Ensure that the App ID used for creating the token is the same App ID used in the [create](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a35466f690d0a9332f24ea8280021d5ed) method for creating an AgoraRtcEngine object. Otherwise, CDN live streaming may fail.

Returns

-   0: Success.
-   < 0: Failure.
    -   [ERR_INVALID_ARGUMENT(-2)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a2421e6f4293acd6839bc8732ade46534)
    -   [ERR_NOT_READY(-3)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ace597d5ad96e5f2eb9545ae088abd022)
    -   [ERR_REFUSED(-5)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a41a37ce0744c931551d2fb677507b6f3)


#### switchChannel()
Switches to a different channel.

```switchChannel(String token, String channelId)```

This method allows the audience of a Live-broadcast channel to switch to a different channel.

After the user successfully switches to another channel, the [onLeaveChannel](#onLeaveChannel)() and [onJoinChannelSuccess](#onJoinChannelSuccess)() callbacks are triggered to indicate that the user has left the original channel and joined a new one.

> Note: This method applies to the audience role in a Live-broadcast channel only.

Parameters

| token |  |
|--|--|
|  |The token for authentication:|
||-   In situations not requiring high security: You can use the temporary token generated at Console. For details, see [Get a temporary token](https://docs.agora.io/en/Agora%20Platform/token?platform=All%20Platforms#get-a-temporary-token).|
||-   In situations requiring high security: Set it as the token generated at your server. For details, see [Generate a token](https://docs.agora.io/en/Interactive%20Broadcast/token_server_cpp?platform=CPP).|  

|channelId|  |
|--|--|
|  | The unique channel name for the AgoraRTC session in the string format. The string length must be less than 64 bytes. Supported character scopes are: |
|	|	All lowercase English letters: a to z.|
|	|	All uppercase English letters: A to Z.|
|	|	All numeric characters: 0 to 9.|
|	|	The space character.|
|	|	Additional information about the channel. This parameter can be set as null or contain channel related information. Other users in the channel do not receive this message.|

Returns

-   0: Success.
-   < 0: Failure.

#### leaveChannel()
```leaveChannel()```
Allows a user to leave a channel.

After joining a channel, the user must call the [leaveChannel](#) method to end the call before joining another channel. This method returns 0 if the user leaves the channel and releases all resources related to the call. This method call is asynchronous, and the user has not exited the channel when the method call returns. Once the user leaves the channel, the SDK triggers the [onLeaveChannel]() callback.

A successful leaveChannel method call triggers the following callbacks:

-   The local client: [onLeaveChannel]().
-   The remote client: [onUserOffline](), if the user leaving the channel is in the Communication channel, or is a BROADCASTER in the Live Broadcast profile.

>Note:
	>>If you call the [destroy](#) method immediately after calling the [leaveChannel](#) method, the leaveChannel process interrupts, and the SDK does not trigger the [onLeaveChannel](#) callback.
	>> If you call the [leaveChannel]() method during CDN live streaming, the SDK triggers the [removeInjectStreamUrl]() method. 

Returns

-   0: Success.
-   < 0: Failure.


#### renewToken()
```renewToken(String token)```
Renews the token when the current token expires.

The token expires after a period of time once the token schema is enabled when:

-   The SDK triggers the [onTokenPrivilegeWillExpire]() callback, or
-   The [onConnectionStateChanged]() callback reports the [CONNECTION_CHANGED_TOKEN_EXPIRED(9)]() error,

The app should retrieve a new token from the server and call this method to renew it. Failure to do so results in the SDK disconnecting from the server.

Parameters

|token|  |
|--|--|
|  | the new token |

Returns

-   0: Success.
-   < 0: Failure.

#### registerLocalUserAccount()
``` registerLocalUserAccount(String appID, String userAccount)```
Registers a user account.

Once registered, the user account can be used to identify the local user when the user joins the channel. After the user successfully registers a user account, the SDK triggers the [onLocalUserRegistered](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#aca1987909703d84c912e2f1e7f64fb0b) callback on the local client, reporting the user ID and user account of the local user.

To join a channel with a user account, you can choose either of the following:

-   Call the [registerLocalUserAccount]() method to create a user account, and then the [joinChannelWithUserAccount]() method to join the channel.
-   Call the [joinChannelWithUserAccount]() method to join the channel.

The difference between the two is that for the former, the time elapsed between calling the joinChannelWithUserAccount method and joining the channel is shorter than the latter.

>Note: 
	>> Ensure that you set the `userAccount` parameter. Otherwise, this method does not take effect.
	>> Ensure that the value of the `userAccount` parameter is unique in the channel.
	>> To ensure smooth communication, use the same parameter type to identify the user. For example, if a user joins the channel with a user ID, then ensure all the other users use the user ID too. The same applies to the user account. If a user joins the channel with the Agora Web SDK, ensure that the uid of the user is set to the same parameter type.


Parameters:

1. appID

|appID|  |
|--|--|
|  | The App ID of your project. |

2. userAccount

|userAccount|  |
|--|--|
|  | The user account. The maximum length of this parameter is 255 bytes. Ensure that you set this parameter and do not set it as null. Supported character scopes are: |
|	|	All lowercase English letters: a to z.|
|	|	All uppercase English letters: A to Z.|
|	|	All numeric characters: 0 to 9.|
|	|	The space character.|
|	|	Punctuation characters and other symbols, including: "!", "#", "$", "%", "&", "(", ")", "+", "-", ":", ";", "<", "=", ".", ">", "?", "@", "[", "]", "^", "_", " {", "}", "|", "~", ",".|

Returns

-   0: Success.
-   < 0: Failure.


#### joinChannelByUserAccount()
```joinChannelByUserAccount(String userAccount,String token, String channelId)```

Joins the channel with a user account.

After the user successfully joins the channel, the SDK triggers the following callbacks:

-   The local client: [onLocalUserRegistered]() and [onJoinChannelSuccess]().
-   The remote client: [onUserJoined]() and [onUserInfoUpdated](), if the user joining the channel is in the Communication profile, or is a BROADCASTER in the Live Broadcast profile.

> Note: To ensure smooth communication, use the same parameter type to identify the user. For example, if a user joins the channel with a user ID, then ensure all the other users use the user ID too. The same applies to the user account. If a user joins the channel with the Agora Web SDK, ensure that the uid of the user is set to the same parameter type.

Parameters:

 1. userAccount
	
|userAccount|  |
|--|--|
|  | The user account. The maximum length of this parameter is 255 bytes. Ensure that you set this parameter and do not set it as null. Supported character scopes are: |
|	|	All lowercase English letters: a to z.|
|	|	All uppercase English letters: A to Z.|
|	|	All numeric characters: 0 to 9.|
|	|	The space character.|
|	|	Punctuation characters and other symbols, including: "!", "#", "$", "%", "&", "(", ")", "+", "-", ":", ";", "<", "=", ".", ">", "?", "@", "[", "]", "^", "_", " {", "}", "|", "~", ",".|

 2. token

|token  |  |
|--|--|
|  | The token generated at your server: |
|	|	In situations not requiring high security: You can use the temporary token generated at Console. For details, see [Get a temporary token](https://docs.agora.io/en/Agora%20Platform/token?platform=All%20Platforms#get-a-temporary-token).|
|	|	In situations requiring high security: Set it as the token generated at your server. For details, see [Generate a token](https://docs.agora.io/en/Interactive%20Broadcast/token_server_cpp?platform=CPP).|

 3. channelId


|channelId|  |
|--|--|
|  | The unique channel name for the AgoraRTC session in the string format. The string length must be less than 64 bytes. Supported character scopes are: |
|	|	All lowercase English letters: a to z.|
|	|	All uppercase English letters: A to Z.|
|	|	All numeric characters: 0 to 9.|
|	|	The space character.|
|	|	Punctuation characters and other symbols, including: "!", "#", "$", "%", "&", "(", ")", "+", "-", ":", ";", "<", "=", ".", ">", "?", "@", "[", "]", "^", "_", " {", "}", "|", "~", ",".|

Returns

-   0: Success.
-   < 0: Failure.
    -   [ERR_INVALID_ARGUMENT(-2)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a2421e6f4293acd6839bc8732ade46534)
    -   [ERR_NOT_READY(-3)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ace597d5ad96e5f2eb9545ae088abd022)
    -   [ERR_REFUSED(-5)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a41a37ce0744c931551d2fb677507b6f3)


#### getUserInfoByUserAccount()
```getUserInfoByUserAccount(String userAccount)```
Gets the user information by passing in the user account.

After a remote user joins the channel, the SDK gets the user account of the remote user, caches them in a mapping table object ([UserInfo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1models_1_1_user_info.html)), and triggers the [onUpdatedUserInfo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#aa3e9ead25f7999272d5700c427b2cb3d) callback on the local client.

After receiving the `onUpdatedUserInfo` callback, you can call this method to get the user ID of the remote user from the userInfo object by passing in the user account.

Parameters

 1. userAccount

| userAccount |  |
|--|--|
|  |  The user account of the user. Ensure that you set this parameter.|  

2. userInfo

|userInfo|  |
|--|--|
|  |  [in/out] A userInfo object that identifies the user. For details, see [UserInfo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1models_1_1_user_info.html).|
|	|	Input: A UserInfo object.|
|	|	Output: A UserInfo object that contains the user account and user ID of the user.|

Returns

-   0: Success.
-   < 0: Failure.

#### getUserInfoByUid()

```getUserInfoByUid(int uid)```

Gets the user information by passing in the user ID.

After a remote user joins the channel, the SDK gets the user ID and user account of the remote user, caches them in a mapping table object ([UserInfo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1models_1_1_user_info.html)), and triggers the [onUpdatedUserInfo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#aa3e9ead25f7999272d5700c427b2cb3d) callback on the local client.

After receiving the `onUpdatedUserInfo` callback, you can call this method to get the user ID of the remote user from the userInfo object by passing in the user account.     

 1. uid

| uid |  |
|--|--|
|  |  The user ID of the user. Ensure that you set this parameter.|  

2. userInfo

|userInfo|  |
|--|--|
|  |  [in/out] A userInfo object that identifies the user. For details, see [UserInfo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1models_1_1_user_info.html).|
|	|	Input: A UserInfo object.|
|	|	Output: A UserInfo object that contains the user account and user ID of the user.|


#### enableWebSdkInteroperability()
```enableWebSdkInteroperability(bool enabled)```

Enables interoperability with the Agora Web SDK (Live Broadcast only).

If the channel has Web SDK users, ensure that you call this method, or the video of the Native user will be a black screen for the Web user.

Use this method when the channel profile is Live Broadcast. Interoperability with the Agora Web SDK is enabled by default when the channel profile is Communication.         

Parameters:

1. enabled

|  enabled|  |
|--|--|
|  | Sets whether to enable/disable interoperability with the Agora Web SDK: |
|  |true: Enable.  |
|  | false: (Default) Disable. |

Returns

-   0: Success.
-   < 0: Failure.


#### getConnectionState()
```getConnectionState()```

Gets the connection state of the SDK.

Returns

The connection state:

-   [CONNECTION_STATE_DISCONNECTED(1)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a834e800c4d376ac5b50a4f6ab9900386): The SDK is disconnected from Agora's edge server.
-   [CONNECTION_STATE_CONNECTING(2)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a50d2fadb8bd81756a5d5d3dc4f890f1a): The SDK is connecting to Agora's edge server.
-   [CONNECTION_STATE_CONNECTED(3)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#aca12bee1bc392321a7c35809c2fef68e): The SDK joined a channel and is connected to Agora's edge server. You can now publish or subscribe to a media stream in the channel.
-   [CONNECTION_STATE_RECONNECTING(4)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a153882e41a0a784324d601324949e90c): The SDK keeps rejoining the channel after being disconnected from a joined channel because of network issues.
-   [CONNECTION_STATE_FAILED(5)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a4a9127b509851c81b876b8d94145a284): The SDK fails to join the channel.

#### enableAudio()
```enableAudio()```

Enables the audio module.

The audio module is enabled by default.  

> Note: 
 >- This method affects the internal engine and can be called after calling the [leaveChannel](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a2929e4a46d5342b68d0deb552c29d597) method. You can call this method either before or after joining a channel.
 >- This method resets the internal engine and takes some time to take effect. We recommend using the following API methods to control the audio engine modules separately:
	 >>- [enableLocalAudio](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a06cf8c022aceb38f34596e9def2107ad): Whether to enable the microphone to create the local audio stream.
	 >>- [muteLocalAudioStream](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a838a04b744e6fb53bd1548d30bff1302): Whether to publish the local audio stream.
	 >>- [muteRemoteAudioStream](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a3e17b5d2b71d628206d740d895044c5d): Whether to subscribe to and play the remote audio stream.
	 >>- [muteAllRemoteAudioStreams](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a867911826213a3930fc9976d182ae190): Whether to subscribe to and play all remote audio streams.

Returns

-   0: Success.
-   < 0: Failure.


#### disableAudio()

```disableAudio()```

Disables the audio module.

> Note: 
 >- This method affects the internal engine and can be called after calling the [leaveChannel](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a2929e4a46d5342b68d0deb552c29d597) method. You can call this method either before or after joining a channel.
 >- This method resets the internal engine and takes some time to take effect. We recommend using the following API methods to control the audio engine modules separately:
	 >>- [enableLocalAudio](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a06cf8c022aceb38f34596e9def2107ad): Whether to enable the microphone to create the local audio stream.
	 >>- [muteLocalAudioStream](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a838a04b744e6fb53bd1548d30bff1302): Whether to publish the local audio stream.
	 >>- [muteRemoteAudioStream](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a3e17b5d2b71d628206d740d895044c5d): Whether to subscribe to and play the remote audio stream.
	 >>- [muteAllRemoteAudioStreams](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a867911826213a3930fc9976d182ae190): Whether to subscribe to and play all remote audio streams.

Returns

-   0: Success.
-   < 0: Failure.


#### setAudioProfile()
```setAudioProfile(int profile, int scenario)```

Sets the audio parameters and application scenarios.

Parameters:

 1. profile

|profile|  |
|--|--|
|  |  Sets the sample rate, bitrate, encoding mode, and the number of channels. See [Audio Profile](https://docs.agora.io/en/Video/API%20Reference/java/enumio_1_1agora_1_1rtc_1_1_constants_1_1_audio_profile.html).|

 2. scenario

|  scenario|  |
|--|--|
|  |  Sets the audio application scenarios. See [Audio Scenario](https://docs.agora.io/en/Video/API%20Reference/java/enumio_1_1agora_1_1rtc_1_1_constants_1_1_audio_scenario.html). Under different audio scenarios, the device uses different volume tracks, i.e. either the in-call volume or the media volume. For details, see [What is the difference between the in-call volume and the media volume?](https://docs.agora.io/en/faq/system_volume).|

>Note: 
	>- You must call this method before calling the [joinChannel]() method.
	>- In the Communication and Live Broadcast profiles, the bitrates may be different from your settings due to network self-adaptation.
	>- In scenarios requiring high-quality audio, we recommend setting `profile` as AUDIO_SCENARIO_SHOWROOM(4) and `scenario` as AUDIO_SCENARIO_GAME_STREAMING(3). For example, for music education scenarios.


#### adjustRecordingSignalVolume ()
```adjustRecordingSignalVolume (int volume)```

Adjusts the recording volume.

Parameters:

|volume|  |
|--|--|
|  |  Recording volume. The value ranges between 0 and 400:|
|	|0: Mute.	|
|	|100: Original volume.|
|	|400: (Maximum) Four times the original volume with signal-clipping protection.|

Returns

-   0: Success.
-   < 0: Failure.


#### adjustPlaybackSignalVolume()
```adjustPlaybackSignalVolume(int volume)```

Adjusts the playback volume.

>Note: 
>- This method adjusts the playback volume which is mixed volume of all remote users.
>- To mute the local audio playback, call both `adjustPlaybackSignalVolume` and [adjustAudioMixingVolume](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a13c5737248d5a5abf6e8eb3130aba65a), and set `volume` as 0.


Parameters:

|volume|  |
|--|--|
|  |  Recording volume. The value ranges between 0 and 400:|
|	|0: Mute.	|
|	|100: Original volume.|
|	|400: (Maximum) Four times the original volume with signal-clipping protection.|

Returns

-   0: Success.
-   < 0: Failure.


#### enableAudioVolumeIndication() 
```enableAudioVolumeIndication(int interval, int smooth, bool vad)```

Enables the onAudioVolumeIndication callback at a set time interval to report on which users are speaking and the speakers' volume.

Once this method is enabled, the SDK returns the volume indication in the onAudioVolumeIndication callback at the set time interval, regardless of whether any user is speaking in the channel.

Parameters:

 1. interval

|interval|  |
|--|--|
|  |  Sets the time interval between two consecutive volume indications:|
|	|	≤ 0: Disables the volume indication.|
|	|	> 0: Time interval (ms) between two consecutive volume indications. We recommend setting interval ≥ 200 ms.|

 2. smooth

|smooth|  |
|--|--|
|  |  The smoothing factor sets the sensitivity of the audio volume indicator. The value ranges between 0 and 10. The greater the value, the more sensitive the indicator. The recommended value is 3.|

 3. vad

|vad|  |
|--|--|
|  |true: Enable the voice activity detection of the local user. Once it is enabled, the `vad` parameter of the onAudioVolumeIndication callback reports the voice activity status of the local user.  |
|	|false: (Default) Disable the voice activity detection of the local user. Once it is enabled, the `vad` parameter of the onAudioVolumeIndication callback does not report the voice activity status of the local user, except for scenarios where the engine automatically detects the voice activity of the local user.	|


Returns

-   0: Success.
-   < 0: Failure.


#### enableLocalAudio()
```enableLocalAudio(bool enabled)```

Enables/Disables the local audio capture.

The audio function is enabled by default. This method disables/re-enables the local audio function, that is, to stop or restart local audio capture and processing.

This method does not affect receiving or playing the remote audio streams, and enableLocalAudio(false) is applicable to scenarios where the user wants to receive remote audio streams without sending any audio stream to other users in the channel.

The SDK triggers the onMicrophoneEnabled callback once the local audio function is disabled or re-enabled.

Parameters

|  enabled|  |
|--|--|
|  | Sets whether to enable/disable interoperability with the Agora Web SDK: |
|  |true: (Default) Re-enable the local audio function, that is, to start local audio capture and processing.  |
|  | false: Disable the local audio function, that is, to stop local audio capture and processing. |


>Note: 
>- This method is different from the muteLocalAudioStream method:
>>- enableLocalAudio: Disables/Re-enables the local audio capture and processing. If you disable or re-enable local audio recording using the `enableLocalAudio` method, the local user may hear a pause in the remote audio playback.
>>- muteLocalAudioStream: Stops/Continues sending the local audio streams.

Returns

-   0: Success.
-   < 0: Failure.

#### muteLocalAudioStream()
```muteLocalAudioStream(bool muted)```

Stops/Resumes sending the local audio stream.

A successful muteLocalAudioStream method call triggers the onUserMuteAudio on the remote client.

Parameters:

|muted|  |
|--|--|
|  |  Sets whether to send/stop sending the local audio stream:|
|	|	true: Stop sending the local audio stream.|
|	|	false: (Default) Send the local audio stream.|

>Note: 
>- When `muted` is set as `true`, this method does not disable the microphone and thus does not affect any ongoing recording.
>- If you call `setChannelProfile` after this method, the SDK resets whether or not to mute the local audio according to the channel profile and user role. Therefore, we recommend calling this method after the `setChannelProfile` method.

Returns

-   0: Success.
-   < 0: Failure.


#### muteRemoteAudioStream() 
```muteRemoteAudioStream(int uid, bool muted)```

Stops/Resumes receiving a specified audio stream.

Parameters

 1. uid

|uid|  |
|--|--|
|  |ID of the specified remote user.  |

 2. muted

|muted|  |
|--|--|
|  |  Sets whether to send/stop sending the local audio stream:|
|	|	true: Stop sending the local audio stream.|
|	|	false: (Default) Send the local audio stream.|

>Note: If you called the [muteAllRemoteAudioStreams](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a867911826213a3930fc9976d182ae190) method and set `muted` as `true` to stop receiving all remote video streams, ensure that the [muteAllRemoteAudioStreams](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a867911826213a3930fc9976d182ae190) method is called and set `muted` as `false` before calling this method. The [muteAllRemoteAudioStreams](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a867911826213a3930fc9976d182ae190) method sets all remote audio streams, while the [muteRemoteAudioStream](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a3e17b5d2b71d628206d740d895044c5d) method sets a specified remote user's audio stream.

Returns

-   0: Success.
-   < 0: Failure.


#### muteAllRemoteAudioStream()
```muteAllRemoteAudioStream(bool muted)```

Stops/Resumes receiving all remote audio streams.

Parameters:

|muted|  |
|--|--|
|  |  Sets whether to send/stop sending the local audio stream:|
|	|	true: Stop sending the local audio stream.|
|	|	false: (Default) Send the local audio stream.|

Returns

-   0: Success.
-   < 0: Failure.


#### setDefaultMuteAllRemoteAudioStreams()
```setDefaultMuteAllRemoteAudioStreams(bool muted)```

Sets whether to receive all remote audio streams by default.

You can call this method either before or after joining a channel. If you call `setDefaultMuteAllRemoteAudioStreams`(true) after joining a channel, you will not receive the audio streams of any subsequent user.

>Note: If you want to resume receiving audio streams, call `muteRemoteAudioStream`(false), and specify the ID of the remote user that you want to subscribe to. To resume audio streams of multiple users, call `muteRemoteAudioStream` as many times. Calling `setDefaultMuteAllRemoteAudioStreams`(false) resumes receiving audio streams of the subsequent users only.

Parameters:

|muted|  |
|--|--|
|  |  Sets whether to send/stop sending the local audio stream:|
|	|	true: Stop sending the local audio stream.|
|	|	false: (Default) Send the local audio stream.|

Returns

-   0: Success.
-   < 0: Failure.

#### enableVideo()
```enableVideo()```

Enables the video module.

You can call this method either before joining a channel or during a call. If you call this method before joining a channel, the service starts in the video mode. If you call this method during an audio call, the audio mode switches to the video mode.

A successful enableVideo method call triggers the onUserEnableVideo(true) callback on the remote client.

To disable the video, call the disableVideo method.

>Note: 
>- This method affects the internal engine and can be called after calling the leaveChannel method. You can call this method either before or after joining a channel.
>- This method resets the internal engine and takes some time to take effect. We recommend using the following API methods to control the video engine modules separately:
>>- [enableLocalVideo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#ad3f719c42e061019b4e1b9478971571a): Whether to enable the camera to create the local video stream.
>>- [muteLocalVideoStream](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a949cd7044eec55ffd0b63ad3004db756): Whether to publish the local video stream.
>>- [muteRemoteVideoStream](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a4bb8c03a82b8aff52e38552e197dc8b3): Whether to subscribe to and play the remote video stream.
>>- [muteAllRemoteVideoStreams](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a1364cc35798b66094ff3799225911fda): Whether to subscribe to and play all remote video streams.

abstract int io.agora.rtc.RtcEngine.enableVideo

(

)

abstract

Enables the video module.

You can call this method either before joining a channel or during a call. If you call this method before joining a channel, the service starts in the video mode. If you call this method during an audio call, the audio mode switches to the video mode.

A successful enableVideo method call triggers the [onUserEnableVideo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#af87247218ec1ef398a9478672ad4dd49)(true) callback on the remote client.

To disable the video, call the [disableVideo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a8d6fad1572e62c553a660a70663c682f) method.

>Note
>-   This method affects the internal engine and can be called after calling the [leaveChannel](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a2929e4a46d5342b68d0deb552c29d597) method. You can call this method either before or after joining a channel.
>-   This method resets the internal engine and takes some time to take effect. We recommend using the following API methods to control the video engine modules separately:
    >>-   [enableLocalVideo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#ad3f719c42e061019b4e1b9478971571a): Whether to enable the camera to create the local video stream.
    >>-   [muteLocalVideoStream](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a949cd7044eec55ffd0b63ad3004db756): Whether to publish the local video stream.
    >>-   [muteRemoteVideoStream](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a4bb8c03a82b8aff52e38552e197dc8b3): Whether to subscribe to and play the remote video stream.
    >>-   [muteAllRemoteVideoStreams](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a1364cc35798b66094ff3799225911fda): Whether to subscribe to and play all remote video streams.

Returns

-   0: Success.
-   < 0: Failure.


#### disableVideo()
```disableVideo()```

Disables the video module.

You can call this method before joining a channel or during a call. If you call this method before joining a channel, the service starts in audio mode. If you call this method during a video call, the video mode switches to the audio mode.

A successful disableVideo method call triggers the [onUserEnableVideo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#af87247218ec1ef398a9478672ad4dd49)(false) callback on the remote client.

To enable the video mode, call the [enableVideo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a99ae52334d3fa255dfcb384b78b91c52) method.

>Note
>-   This method affects the internal engine and can be called after calling the [leaveChannel](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a2929e4a46d5342b68d0deb552c29d597) method. You can call this method either before or after joining a channel.
>-   This method resets the internal engine and takes some time to take effect. We recommend using the following API methods to control the video engine modules separately:
    >>-   [enableLocalVideo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#ad3f719c42e061019b4e1b9478971571a): Whether to enable the camera to create the local video stream.
    >>-   [muteLocalVideoStream](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a949cd7044eec55ffd0b63ad3004db756): Whether to publish the local video stream.
    >>-   [muteRemoteVideoStream](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a4bb8c03a82b8aff52e38552e197dc8b3): Whether to subscribe to and play the remote video stream.
    >>-   [muteAllRemoteVideoStreams](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a1364cc35798b66094ff3799225911fda): Whether to subscribe to and play all remote video streams.

Returns

-   0: Success.
-   < 0: Failure.


#### setVideoEncoderConfiguration()
```setVideoEncoderConfiguration(VideoEncoderConfiguration config)```

Sets the video encoder configuration.

Each video encoder configuration corresponds to a set of video parameters, including the resolution, frame rate, bitrate, and video orientation. The parameters specified in this method are the maximum values under ideal network conditions. If the video engine cannot render the video using the specified parameters due to poor network conditions, the parameters further down the list are considered until a successful configuration is found.

If you do not set the video encoder configuration after joining the channel, you can call this method before calling the [enableVideo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a99ae52334d3fa255dfcb384b78b91c52) method to reduce the render time of the first video frame.

Parameters

|config|  |
|--|--|
|  |  The local video encoder configuration. See [VideoEncoderConfiguration](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1video_1_1_video_encoder_configuration.html).|


Returns

-   0: Success.
-   < 0: Failure.



#### createNativeView()
```createNativeView(Function(int viewId) created, {Key key})```

Creates the video renderer Widget.

The Widget is identified by viewId, the operation and layout of the Widget are managed by the app.

>Note: Ensure that you call this method in the UI thread.

Parameters

viewId

|viewId|  |
|--|--|
|  |View Id used to identify the widget.|


Returns
-UiKitView


#### removeNativeView()
```removeNativeView(int viewId)```

Remove the video renderer Widget.

Parameters

|viewId|  |
|--|--|
|  |The native viewId can be used to set up remote view  |


#### setupLocalVideo()
```setupLocalVideo(int viewId, VideoRenderMode renderMode)```

Initializes the local video view.

This method initializes the video view of the local stream on the local device. It affects only the video view that the local user sees, not the published local video stream.

Call this method to bind the local video stream to a video view and to set the rendering and mirror modes of the video view.

>Note:
>-   Call this method before joining a channel.
>-   To update the rendering or mirror mode of the local video view during a call, use [setLocalRenderMode](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a8978be2e06307e632abee88c4824b8f6).

Parameters:

 1. viewId

|viewId|  |
|--|--|
|  |viewId is used here to set up the local view  |

 2. renderMode

|renderMode|  |
|--|--|
|  | Sets the local video display mode: |
|	|	RENDER_MODE_HIDDEN(1): Uniformly scale the video until it fills the visible boundaries (cropped). One dimension of the video may have clipped contents.|
|	|	RENDER_MODE_FIT(2): Uniformly scale the video until one of its dimension fits the boundary (zoomed to fit). Areas that are not filled due to the disparity in the aspect ratio are filled with black.|
|	|	RENDER_MODE_ADAPTIVE(3): This mode is deprecated and Agora does not recommend using this mode.|

 3. uid

|uid|  |
|--|--|
|  |user ID of the local user.  |




#### setupRemoteVideo()
```setupRemoteVideo(int viewId, VideoRenderMode renderMode, int uid)```

Initializes the video view of a remote user.

This method initializes the video view of a remote stream on the local device. It affects only the video view that the local user sees.

Call this method to bind the remote video stream to a video view and to set the rendering and mirror modes of the video view.

Typically, the app specifies the `uid` of the remote user sending the video in the method call before the remote user joins a channel. If the `uid` of the remote user is unknown to the app, set the `uid` when the app receives the [onUserJoined](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#aa466d599b13768248ac5febd2978c2d3) callback.

If the Video Recording function is enabled, the Video Recording Service joins the channel as a dummy client, causing other clients to also receive the [onUserJoined](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#aa466d599b13768248ac5febd2978c2d3) callback. Do not bind the dummy client to the app view because the dummy client does not send any video streams. If your app does not recognize the dummy client, bind the remote user to the view when the SDK triggers the [onFirstRemoteVideoDecoded](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#ac7144e0124c3d8f75e0366b0246fbe3b) callback.

To unbind the remote user from the view, set `view` in [Video Canvas](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1video_1_1_video_canvas.html) as `null`. Once the remote user leaves the channel, the SDK unbinds the remote user.

>Note:
>-   Ensure that you call this method in the UI thread.
>-   To update the rendering or mirror mode of the remote video view during a call, use [setRemoteRenderMode](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#ad3e02c615451858e16f50c05b294307c).

Parameters:

 1. viewId

|viewId|  |
|--|--|
|  |viewId is used to set up remote view  |

 2. renderMode

|renderMode|  |
|--|--|
|  | Sets the local video display mode: |
|	|	RENDER_MODE_HIDDEN(1): Uniformly scale the video until it fills the visible boundaries (cropped). One dimension of the video may have clipped contents.|
|	|	RENDER_MODE_FIT(2): Uniformly scale the video until one of its dimension fits the boundary (zoomed to fit). Areas that are not filled due to the disparity in the aspect ratio are filled with black.|
|	|	RENDER_MODE_ADAPTIVE(3): This mode is deprecated and Agora does not recommend using this mode.|

 3. uid

|uid|  |
|--|--|
|  | User ID of the remote user |


#### setLocalRenderMode()
```setLocalRenderMode(int renderMode)```

Sets the local video display mode.

Parameters:

|renderMode|  |
|--|--|
|  | Sets the local video display mode: |
|	|	RENDER_MODE_HIDDEN(1): Uniformly scale the video until it fills the visible boundaries (cropped). One dimension of the video may have clipped contents.|
|	|	RENDER_MODE_FIT(2): Uniformly scale the video until one of its dimension fits the boundary (zoomed to fit). Areas that are not filled due to the disparity in the aspect ratio are filled with black.|
|	|	RENDER_MODE_ADAPTIVE(3): This mode is deprecated and Agora does not recommend using this mode.|

Returns

-   0: Success.
-   < 0: Failure.


#### setRemoteRenderMode()
```setRemoteRenderMode(int uid, int renderMode)```

Sets the remote video display mode.
This method can be invoked multiple times during a call to change the display mode.

Parameters

 1. uid

|uid|  |
|--|--|
|  | User ID of the remote user |

 2. renderMode


|renderMode|  |
|--|--|
|  | Sets the local video display mode: |
|	|	RENDER_MODE_HIDDEN(1): Uniformly scale the video until it fills the visible boundaries (cropped). One dimension of the video may have clipped contents.|
|	|	RENDER_MODE_FIT(2): Uniformly scale the video until one of its dimension fits the boundary (zoomed to fit). Areas that are not filled due to the disparity in the aspect ratio are filled with black.|
|	|	RENDER_MODE_ADAPTIVE(3): This mode is deprecated and Agora does not recommend using this mode.|

Returns

-   0: Success.
-   < 0: Failure.


#### startPreview()
```startPreview()```

Starts the local video preview before joining a channel.

Before calling this method, you must:

-   Call the [setupLocalVideo]() method to set the local preview window and configure the attributes.
-   Call the [enableVideo]() method to enable the video.

>Note: 
>-   By default, the local preview enables the mirror mode.
>-   Once you call this method to start the local video preview, if you leave the channel by calling the [leaveChannel]() method, the local video preview remains until you call the [stopPreview]() method to disable it.

Returns

-   0: Success.
-   < 0: Failure.


#### stopPreview()
```stopPreview()```

Stops the local video preview and the video.

Returns

-   0: Success.
-   < 0: Failure.


#### enableLocalVideo()
```enableLocalVideo(bool enabled)```

Disables/Re-enables the local video capture.

This method disables or re-enables the local video capturer, and does not affect receiving the remote video stream.

After you call the [enableVideo]() method, the local video capturer is enabled by default. You can call enableLocalVideo(false) to disable the local video capturer. If you want to re-enable it, call enableLocalVideo(true).

After the local video capturer is successfully disabled or re-enabled, the SDK triggers the [onUserEnableLocalVideo]() callback on the remote client.
 
 Parameters:

|enabled|  |
|--|--|
|  |  Sets whether to disable/re-enable the local video, including the capturer, renderer, and sender:|
|  |  true: (Default) Re-enable the local video.|
|  |  false: Disable the local video. Once the local video is disabled, the remote users can no longer receive the video stream of this user, while this user can still receive the video streams of other remote users. When you set `enabled` as `false`, this method does not require a local camera.|

>Note:  This method affects the internal engine and can be called after calling the [leaveChannel]() method.

Returns

-   0: Success.
-   < 0: Failure.


#### muteLocalVideoStream()
```muteLocalVideoStream(bool muted)```

Stops/Resumes sending the local video stream.

A successful muteLocalVideoStream method call triggers the [onUserMuteVideo]() callback on the remote client.

Parameters

|muted|  |
|--|--|
|  |Sets whether to send/stop sending the local video stream:|
|	|	true: Stop sending the local video stream.|
|	|	false: (Default) Send the local video stream.|

>Note
>-   When you set `muted` as `true`, this method does not disable the camera and thus does not affect the retrieval of the local video streams. This method responds faster than calling the [enableLocalVideo]() method and set `muted` as `false`, which controls sending the local video stream.
>-   If you call `setChannelProfile` after this method, the SDK resets whether or not to mute the local video according to the channel profile and user role. Therefore, we recommend calling this method after the `setChannelProfile` method.

Returns

-   0: Success.
-   < 0: Failure.


#### muteRemoteVideoStream()
```muteRemoteVideoStream(int uid, bool muted)```

Stops/Resumes receiving a specified remote user's video stream.

Parameters

 1. uid

|uid|  |
|--|--|
|  | User ID of the remote user |

 2. muted

|muted|  |
|--|--|
|  |Sets whether to send/stop sending the local video stream:|
|	|	true: Stop sending the local video stream.|
|	|	false: (Default) Send the local video stream.|

>Note: If you call the [muteAllRemoteVideoStreams]() method and set set `muted` as `true` to stop receiving all remote video streams, ensure that the [muteAllRemoteVideoStreams]() method is called and set `muted` as `false` before calling this method. The [muteAllRemoteVideoStreams]() method sets all remote streams, while this method sets a specified remote user's stream. 

Returns

-   0: Success.
-   < 0: Failure.


#### setDefaultMuteAllRemoteVideoStreams()
```setDefaultMuteAllRemoteVideoStreams(bool muted)```

Sets whether to receive all remote video streams by default.

You can call this method either before or after joining a channel. If you call `setDefaultMuteAllRemoteVideoStreams`(true) after joining a channel, you will not receive the video stream of any subsequent user.

>Note: If you want to resume receiving video streams, call `muteRemoteVideoStream`(false), and specify the ID of the remote user that you want to subscribe to. To resume receiving video streams of multiple users, call `muteRemoteVideoStream` as many times. Calling `setDefaultMuteAllRemoteVideoStreams`(false) resumes receiving video streams of the subsequent users only.

Parameters


|muted|  |
|--|--|
|  |Sets whether to send/stop sending the local video stream:|
|	|	true: Stop sending the local video stream.|
|	|	false: (Default) Send the local video stream.|

Returns

-   0: Success.
-   < 0: Failure.


#### setLocalVoiceChanger()
```setLocalVoiceChanger(int changer)```

Sets the local voice changer option.

Parameters

|changer|  |
|--|--|
|  |  The local voice changer option:|
|  |  [VOICE_CHANGER_OFF(0)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a20aea3d5833df74226566c35fae7395f): the original voice (no local voice change).|
|  | [VOICE_CHANGER_OLDMAN(1)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a7a385284480c8bdb59ea81cce1020cd5): an old man's voice. |
|  |  [VOICE_CHANGER_BABYBOY(2)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a3db58b2116bf18ebafe853f76c55366b): a little boy's voice.|
|  |  [VOICE_CHANGER_BABYGILR(3)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#abb2a0e6b97526f14402cbd73d5f6810c): a little girl's voice.|
|  |  [VOICE_CHANGER_ZHUBAJIE(4)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#af89d30c1b2dbf7cc42e14ccac47d55a6): Zhu Bajie's voice (Zhu Bajie is a character from Journey to the West who has a voice like a growling bear).|
|	|	[VOICE_CHANGER_ETHEREAL(5))](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a3e4beb6bc63986d54a2da775ae5920ae): ethereal vocal effects.|
|	|	-   [VOICE_CHANGER_HULK(6))](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ad8d15b2464ce1c773ee43b8e947d7462): Hulk's voice.|

Returns

-   0: Success.
-   -1: Failure.


#### setLocalVoicePitch()
```setLocalVoicePitch(double pitch)```

Changes the voice pitch of the local speaker.

Parameters

|pitch|  |
|--|--|
|  |  Sets the voice pitch. The value ranges between 0.5 and 2.0. The lower the value, the lower the voice pitch. The default value is 1.0 (no change to the local voice pitch).|


Returns

-   0: Success.
-   -1: Failure.

#### setLocalVoiceEqualizationOfBandFrequency()
```setLocalVoiceEqualizationOfBandFrequency(int bandFrequency, int gain)```

Sets the local voice equalization effect.

Parmeters

 1. bandFrequency

|bandFrequency|  |
|--|--|
|  |  Sets the band frequency. The value ranges between 0 and 9; representing the respective 10-band center frequencies of the voice effects, including 31, 62, 125, 500, 1k, 2k, 4k, 8k, and 16k Hz.|

 2. gain

|gain|  |
|--|--|
|  | Sets the gain of each band (dB). The value ranges between -15 and 15. The default value is 0. |

Returns

-   0: Success.
-   -1: Failure.


#### setLocalVoiceReverbOfType()
```setLocalVoiceReverbOfType(int reverbType, int value)```

Sets the local voice reverberation.

>Note: You can also use [setLocalVoiceReverbPreset]() method which is  more user-friendly for setting the local voice reverberation. You can use this method to set the local reverberation effect, such as Popular, R&B, Rock, Hip-hop, and more.

Parameters

 1. reverbType

|reverbType|  |
|--|--|
|  |  Sets the reverberation key. This method contains five reverberation keys. For details, see the description of each @ value.|

 2. value

|value|  |
|--|--|
|  | Sets the local voice reverberation value: |
|  | [AUDIO_REVERB_DRY_LEVEL(0)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a30b9099e5ea7ea0b58561471393eb0bb): Level of the dry signal (-20 to 10 dB). |
|  |[AUDIO_REVERB_WET_LEVEL(1)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a88a2dee6b6550cb5dac3c032fe6f6650): Level of the early reflection signal (wet signal) (-20 to 10 dB).  |
|  |[AUDIO_REVERB_ROOM_SIZE(2)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ad693c7787122420505aa05f9603cfa1a): Room size of the reflection (0 to 100 dB).  |
|  | [AUDIO_REVERB_WET_DELAY(3)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#abb072963012718498082bf464b1d70ec): Length of the initial delay of the wet signal (0 to 200 ms). |
|	|	[AUDIO_REVERB_STRENGTH(4)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ae31453b5d8bce0e119d6dd757829afd8): Strength of the late reverberation (0 to 100).`|

Returns

-   0: Success.
-   -1: Failure.


#### setLocalVoiceReverbPreset()
```setLocalVoiceReverbPreset(int reverbType)```

Sets the preset local voice reverberation effect.

>Note:
>- Do not use this method together with [setLocalVoiceReverbOfType]().
>- Do not use this method together with [setLocalVoiceChanger](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#ade6883c7878b7a596d5b2563462597dd), or the method called eariler does not take effect.

Parameter

|reverbType|  |
|--|--|
|  | The local voice reverberation preset: |
|  | [AUDIO_REVERB_OFF(0)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ab6fb039dc9f0544db24ae343d5949ece): the original voice (no local voice reverberation). |
|  |[AUDIO_REVERB_POPULAR(1)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a39950cf9979440882351a67bdd06a174): pop music.  |
|  |[AUDIO_REVERB_RNB(2)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#af4b85b43c6ff3d0c89f72f7b513fe0a2): R&B.  |
|  | [AUDIO_REVERB_ROCK(3)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a05a64cc39821c9572f8b1bf71236598c): rock music. |
|  |[AUDIO_REVERB_HIPHOP(4)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#adcaa211e3d0cb926f4dd159b705bce91): hip-hop.  |
|  |[AUDIO_REVERB_VOCAL_CONCERT(5)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a73674f8e5ae486f5185afa7cafe9e568): pop concert.  |
|  |  [AUDIO_REVERB_KTV(6)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#aafa5de3ebc1673930eb75f906e3a6c33): Karaoke.|
|  | [AUDIO_REVERB_STUDIO(7)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#afd7d7362c022f07188fe625b2053f55d): recording studio. |

Returns

-   0: Success.
-   -1: Failure.


#### enableSoundPositionIndication()
```enableSoundPositionIndication(bool enabled)```

Enables/Disables stereo panning for remote users.

>Note: Ensure that you call this method before [joinChannel]() to enable stereo panning for remote users so that the local user can track the position of a remote user by calling [setRemoteVoicePosition]().

Parameter

 
| enabled |  |
|--|--|
|  |  Sets whether or not to enable stereo panning for remote users:|
|  |true: enables stereo panning.  |
|  |false: disables stereo panning.  |

Returns

-   0: Success.
-   -1: Failure.


#### setRemoteVoicePosition()
```setRemoteVoicePosition(int uid, double pan, int gain)```

Sets the sound position of a remote user.

When the local user calls this method to set the sound position of a remote user, the sound difference between the left and right channels allows the local user to track the real-time position of the remote user, creating a real sense of space. This method applies to massively multiplayer online games, such as Battle Royale games.

>Note: 
>-   For this method to work, enable stereo panning for remote users by calling the [enableSoundPositionIndication]() method before joining a channel.
>- This method requires hardware support. For the best sound positioning, we recommend using a stereo headset.

Parameters

 1. uid

|uid|  |
|--|--|
|  |The ID of the remote user.  |

 2. pan

|pan|  |
|--|--|
|  |The sound position of the remote user. The value ranges from -1.0 to 1.0:  |
|	|0.0: the remote sound comes from the front.	|
|	|-1.0: the remote sound comes from the left.	|
|	|1.0: the remote sound comes from the right.	|

 3. gain

|gain|  |
|--|--|
|  | Gain of the remote user. The value ranges from 0.0 to 100.0. The default value is 100.0 (the original gain of the remote user). The smaller the value, the less the gain. |

Returns

-   0: Success.
-   -1: Failure.


#### setDefaultAudioRouteToSpeaker()
```setDefaultAudioRouteToSpeaker(bool defaultToSpeaker)```

Sets the default audio playback route.

This method sets whether the received audio is routed to the earpiece or speakerphone by default before joining a channel. If a user does not call this method, the audio is routed to the earpiece by default. If you need to change the default audio route after joining a channel, call the [setEnableSpeakerphone]() method.

The default audio route for each scenario:

-   In the Communication profile:
    -   For a voice call, the default audio route is the earpiece.
    -   For a video call, the default audio route is the speaker. If the user disables the video using `disableVideo`, or `muteLocalVideoStream`and `muteAllRemoteVideoStreams`, the default audio route automatically switches back to the earpiece.
-   In the Live Broadcast profile: The default audio route is the speaker.

>Note:
>-   This method applies to the Communication profile only.
>-   Call this method before the user joins a channel.

Parameter

|defaultToSpeaker|  |
|--|--|
|  |  Sets the default audio route:|
|	|	true: Route the audio to the speaker. If the playback device connects to the earpiece or Bluetooth, the audio cannot be routed to the earpiece.|
|	|	false: (Default) Route the audio to the earpiece. If a headset is plugged in, the audio is routed to the headset.|

Returns

-   0: Success.
-   < 0: Failure.


#### setEnableSpeakerphone()
```setEnableSpeakerphone(bool enabled)```

Enables/Disables the audio playback route to the speakerphone.

This method sets whether the audio is routed to the speakerphone or earpiece. After calling this method, the SDK returns the [onAudioRouteChanged]() callback to indicate the changes.

Parameter

|enabled|  |
|--|--|
|  |Sets whether to route the audio to the speakerphone or earpiece:  |
|  |true: Route the audio to the speakerphone.  |
|  |false: Route the audio to the earpiece. If the headset is plugged in, the audio is routed to the headset.  |

>Note:
>- Ensure that you have successfully called the [joinChannel]() method before calling this method.
>- This method is invalid for audience users in the Live Broadcast profile.

Returns

-   0: Success.
-   < 0: Failure.


#### isSpeakerphoneEnabled()
```isSpeakerphoneEnabled()```

Checks whether the speakerphone is enabled.

Returns

-   true: The speakerphone is enabled, and the audio plays from the speakerphone.
-   false: The speakerphone is not enabled, and the audio plays from devices other than the speakerphone. For example, the headset or earpiece.


#### setRemoteUserPriority()
```setRemoteUserPriority(int uid, int userPriority)```

Sets the priority of a remote user's media stream.

Use this method with the [setRemoteSubscribeFallbackOption]() method. If the fallback function is enabled for a subscribed stream, the SDK ensures the high-priority user gets the best possible stream quality.

>Note: The Agora SDK supports setting userPriority as high for one user only.

Parameters

 1. uid

|uid|  |
|--|--|
|  |The ID of the remote user.  |

 2. userPriority

| userPriority |  |
|--|--|
|  | The priority of the remote user: |
|  |[USER_PRIORITY_HIGH(50)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#af473faaaf21ebc7bc388dae8f5ab7316): the user's priority is high.  |
|  | [USER_PRIORITY_NORANL(100)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ae080e934bc940d38b8e20af95bf0feed): (default) the user's priority is normal. |

Returns

-   0: Success.
-   <0: Failure.


#### setLocalPublishFallbackOption()
```setLocalPublishFallbackOption(int options)```

Sets the fallback option for the locally published video stream based on the network conditions.

If `option` is set as [STREAM_FALLBACK_OPTION_AUDIO_ONLY(2)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ace1810225ee42e99eea4cc73dc0056c9), the SDK will:

-   Disable the upstream video but enable audio only when the network conditions deteriorate and cannot support both video and audio.
-   Re-enable the video when the network conditions improve.

When the locally published video stream falls back to audio only or when the audio-only stream switches back to the video, the SDK triggers the [onLocalPublishFallbackToAudioOnly](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a899d84de53c9e21de614a9611f6e062b).

Parameters

|option|  |
|--|--|
|  |Sets the fallback option for the locally published video stream:  |
|  |[STREAM_FALLBACK_OPTION_DISABLED(0)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a3e453c93766e783a7e5eca05b1776238): (Default) No fallback behavior for the locally published video stream when the uplink network condition is poor. The stream quality is not guaranteed. |
|  |[STREAM_FALLBACK_OPTION_AUDIO_ONLY(2)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ace1810225ee42e99eea4cc73dc0056c9): The locally published video stream falls back to audio only when the uplink network condition is poor.  |

>Note: Agora does not recommend using this method for CDN live streaming, because the remote CDN live user will have a noticeable lag when the locally published video stream falls back to audio only.

Returns

-   0: Success.
-   <0: Failure.


#### setRemoteSubscribeFallbackOption()
```setRemoteSubscribeFallbackOption(int options)```

Sets the fallback option for the remotely subscribed video stream based on the network conditions.

If `option` is set as [STREAM_FALLBACK_OPTION_AUDIO_ONLY(2)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ace1810225ee42e99eea4cc73dc0056c9), the SDK automatically switches the video from a high-stream to a low-stream, or disables the video when the downlink network condition cannot support both audio and video to guarantee the quality of the audio. The SDK monitors the network quality and restores the video stream when the network conditions improve. When the remotely subscribed video stream falls back to audio only, or the audio-only stream switches back to the video, the SDK triggers the [onRemoteSubscribeFallbackToAudioOnly](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#ad14676019bf51b9d9a9c5520e6e578dd) callback.

Parameters


|option|  |
|--|--|
|  |Sets the fallback option for the locally published video stream:  |
|  |[STREAM_FALLBACK_OPTION_DISABLED(0)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a3e453c93766e783a7e5eca05b1776238): (Default) No fallback behavior for the locally published video stream when the uplink network condition is poor. The stream quality is not guaranteed. |
|	|	[STREAM_FALLBACK_OPTION_VIDEO_STREAM_LOW(1)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#abdb0027249f14955ef2b7fda8808822a): (Default) The remotely subscribed video stream falls back to the low-stream video when the downlink network condition worsens. This option works only for this method and not for the [setLocalPublishFallbackOption](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#ac8c08e79844a4e62e0670553484cbe90) method.|
|  |[STREAM_FALLBACK_OPTION_AUDIO_ONLY(2)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ace1810225ee42e99eea4cc73dc0056c9): The locally published video stream falls back to audio only when the uplink network condition is poor.  |

Returns

-   0: Success.
-   < 0: Failure.


#### enableDualStreamMode()
```enableDualStreamMode(bool enabled)```

Enables/Disables the dual video stream mode.

If dual-stream mode is enabled, the receiver can choose to receive the high stream (high-resolution high-bitrate video stream) or low stream (low-resolution low-bitrate video stream) video.

Parameters

|enabled|  |
|--|--|
|  | Sets the stream mode: |
|  |true: Dual-stream mode.  |
|  | false: (Default) Single-stream mode.false: (Default) Single-stream mode. |

Returns

-   0: Success.
-   < 0: Failure.


#### setRemoteVideoStreamType()
```setRemoteVideoStreamType(int uid, int streamType)```

Sets the stream type of the remote video.

Under limited network conditions, if the publisher has not disabled the dual-stream mode using `enableDualStreamMode(false)`, the receiver can choose to receive either the high-video stream (the high resolution, and high bitrate video stream) or the low-video stream (the low resolution, and low bitrate video stream).

By default, users receive the high-video stream. Call this method if you want to switch to the low-video stream. This method allows the app to adjust the corresponding video stream type based on the size of the video window to reduce the bandwidth and resources.

The aspect ratio of the low-video stream is the same as the high-video stream. Once the resolution of the high-video stream is set, the system automatically sets the resolution, frame rate, and bitrate of the low-video stream.

The SDK reports the result of calling this method in the [onApiCallExecuted]() callback.

Parameters

 1. uid


|uid|  |
|--|--|
|  | User ID of the remote user |
 2. streamType

|streamType|  |
|--|--|
|  |Sets the video-stream type:  |
|  | High-resolution, high-bitrate video: [High-stream video(0)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a2bf96b985cd7586476ccee80ce6d5509) |
|  |Low-resolution, low-bitrate video: [Low-stream video(1)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#aad79cd1fa4a06c37df7673f299c85446)  |

Returns

-   0: Success.
-   < 0: Failure.


#### setRemoteDefaultVideoStreamType()
```setRemoteDefaultVideoStreamType(int streamType)```

Sets the default video-stream type of the remotely subscribed video stream when the remote user sends dual streams.

Parameter

|streamType|  |
|--|--|
|  |Sets the video-stream type:  |
|  | High-resolution, high-bitrate video: [High-stream video(0)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a2bf96b985cd7586476ccee80ce6d5509) |
|  |Low-resolution, low-bitrate video: [Low-stream video(1)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#aad79cd1fa4a06c37df7673f299c85446)  |

Returns

-   0: Success.
-   < 0: Failure.


#### setLiveTranscoding()
```setLiveTranscoding(AgoraLiveTranscoding config)```

Sets the video layout and audio settings for CDN live.

The SDK triggers the [onTranscodingUpdated]() callback when you call this method to update the `LiveTranscoding`class. If you call this method to set the `LiveTranscoding` class for the first time, the SDK does not trigger the `onTranscodingUpdated` callback.

>Note: Before calling the methods listed in this section:
>-   This method applies to Live Broadcast only.
>-   Ensure that you enable the RTMP Converter service before using this function. See [Prerequisites](https://docs.agora.io/en/Interactive%20Broadcast/cdn_streaming_android?platform=Android#prerequisites).
>-   Ensure that you call the [setClientRole](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#aa2affa28a23d44d18b6889fba03f47ec) method and set the user role as the host.
>-   Ensure that you call the [setLiveTranscoding](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a3cb9804ae71819038022d7575834b88c) method before calling the [addPublishStreamUrl](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a4445b4ca9509cc4e2966b6d308a8f08f) method.

Parameters

|config|  |
|--|--|
|  | Sets the CDN live audio/video transcoding settings |

Returns

-   0: Success.
-   < 0: Failure.


#### addPublishStreamUrl()
```addPublishStreamUrl(String url, bool enable)```

Publishes the local stream to the CDN.

The addPublishStreamUrl method call triggers the [onRtmpStreamingStateChanged](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a7b9f1a5d87480cfd6187c3da0ade3f94) callback on the local client to report the state of adding a local stream to the CDN.

Parameters

 1. url

|url|  |
|--|--|
|  |The CDN streaming URL in the RTMP format. The maximum length of this parameter is 1024 bytes. The URL address must not contain special characters, such as Chinese language characters.  |

 2. enable

|enable|  |
|--|--|
|  |  Sets whether transcoding is enabled/disabled. If you set this parameter as `true`, ensure that you call the [setLiveTranscoding](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a3cb9804ae71819038022d7575834b88c) method before this method.|
|	|	true: Enable transcoding. To [transcode](https://docs.agora.io/en/Agora%20Platform/terms?platform=All%20Platforms#transcoding) the audio or video streams when publishing them to CDN live, often used for combining the audio and video streams of multiple hosts in CDN live.|
|	|	Disable transcoding.|

>Note:
>-   Ensure that you enable the RTMP Converter service before using this function. See [Prerequisites](https://docs.agora.io/en/Interactive%20Broadcast/cdn_streaming_android?platform=Android#prerequisites).
>-   This method applies to Live Broadcast only.
>-   Ensure that the user joins a channel before calling this method.
>-   This method adds only one stream HTTP/HTTPS URL address each time it is called.

Returns

-   0: Success.
-   < 0: Failure.
-   [ERR_INVALID_ARGUMENT(2)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a2421e6f4293acd6839bc8732ade46534): Invalid parameter, usually because the URL address is null or the string length is 0.
-   [ERR_NOT_INITIALIZED(7)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a5a2e5578a199a66fc4a76ee52a0fdf70): You have not initialized [RtcEngine](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html) when publishing the stream.


#### removePublishStreamUrl()
```removePublishStreamUrl(String url)```

Removes an RTMP stream from the CDN.

This method removes the RTMP URL address (added by [addPublishStreamUrl](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a4445b4ca9509cc4e2966b6d308a8f08f)) from a CDN live stream. The SDK reports the result of this method call in the [onRtmpStreamingStateChanged](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a7b9f1a5d87480cfd6187c3da0ade3f94) callback.

Parameters

|url|  |
|--|--|
|  |The RTMP URL address to be removed. The maximum length of this parameter is 1024 bytes. The URL address must not contain special characters, such as Chinese language characters.  |

>Note:
>-   Ensure that you enable the RTMP Converter service before using this function. See [Prerequisites](https://docs.agora.io/en/Interactive%20Broadcast/cdn_streaming_android?platform=Android#prerequisites).
>-   Ensure that the user joins a channel before calling this method.
>-   This method applies to Live Broadcast only.
>-   This method removes only one stream RTMP URL address each time it is called.

Returns

-   0: Success.
-   < 0: Failure.


#### removeInjectStreamUrl()
```removeInjectStreamUrl(String url)```

Removes the injected online media stream from a live broadcast.

This method removes the URL address (added by [addInjectStreamUrl](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a67547508dd8b98318b55d764eb0da311)) from a live broadcast.

If this method call is successful, the SDK triggers the [onUserOffline](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a9fbb08177fbc8f74d64044a78aea0dda) callback and returns a stream uid of 666.

Parameters

|url|  |
|--|--|
|  |HTTP/HTTPS URL address of the added stream to be removed.  |

Returns

-   0: Success.
-   < 0: Failure.


#### setEncryptionSecret()
```setEncryptionSecret(String secret)```

Enables built-in encryption with an encryption password before joining a channel.

All users in a channel must set the same encryption password. The encryption password is automatically cleared once a user leaves the channel. If the encryption password is not specified or set to empty, the encryption functionality is disabled.

>Note: For optimal transmission, ensure that the encrypted data size does not exceed the original data size + 16 bytes. 16 bytes is the maximum padding size for AES encryption.

Parameters

|secret|  |
|--|--|
|  |  Encryption password.|

>Note: Do not use this method for CDN live streaming.

Returns

-   0: Success.
-   < 0: Failure.


#### setEncryptionMode()
```setEncryptionMode(String encryptionMode)```

Sets the built-in encryption mode.

The Agora SDK supports built-in encryption, which is set to `aes-128-xts` mode by default. Call this method to set the encryption mode to use other encryption modes. All users in the same channel must use the same encryption mode and password.

Refer to the information related to the AES encryption algorithm on the differences between the encryption modes.

Parameters

|encryptionMode|  |
|--|--|
|  |Sets the encryption mode:  |
|  |"aes-128-xts": 128-bit AES encryption, XTS mode.  |
|  | "aes-128-ecb": 128-bit AES encryption, ECB mode. |
|  |"aes-256-xts": 256-bit AES encryption, XTS mode.  |
|  |"": When encryptionMode is set as null, the encryption is in “aes-128-xts” by default.  |

>Note: Call the [setEncryptionSecret](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a3586017747a74d79ea6e7421af6b1a20) method before calling this method.

Returns

-   0: Success.
-   < 0: Failure.


#### startEchoTestWithInterval()
```startEchoTestWithInterval(int interval)```

Starts an audio call test.

In the audio call test, you record your voice. If the recording plays back within the set time interval, the audio devices and the network connection are working properly.

>Note:
>-   Call this method before joining a channel.
>-   After calling this method, call the [stopEchoTest](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a01b8067275003c011f6d81bb41ee0fe1) method to end the test. Otherwise, the app cannot run the next echo test, or call the [joinchannel](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a8b308c9102c08cb8dafb4672af1a3b4c) method.
>-   In the Live Broadcast profile, only a host can call this method.

Parameters

|interval|  |
|--|--|
|  |  The time interval (s) between when you speak and when the recording plays back.|

Returns

-   0: Success.
-   < 0: Failure.


#### stopEchoTest()
```stopEchoTest()``` 

Stops the audio call test.

Returns

-   0: Success.
-   < 0: Failure.
	-   [ERR_REFUSED(-5)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a41a37ce0744c931551d2fb677507b6f3). Failed to stop the echo test. The echo test may not be running.


#### enableLastmileTest()
```enableLastmileTest()```

Enables the network connection quality test.

This method tests the quality of the users' network connections and is disabled by default.

Before users join a channel or before an audience switches to a host, call this method to check the uplink network quality. This method consumes additional network traffic, which may affect the communication quality. Call the [disableLastmileTest](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a79dd996df69b1e7141ff036c469cc2dc) method to disable this test after receiving the [onLastmileQuality](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a2887941e3c105c21309bd2643372e7f5) callback, and before the user joins a channel or switches the user role.

>Note:
>-   Do not use this method with the [startLastmileProbeTest](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a81c6541685b1c4437d9779a095a0f871) method.
>-   Do not call any other methods before receiving the [onLastmileQuality](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a2887941e3c105c21309bd2643372e7f5) callback. Otherwise, the callback may be interrupted by other methods and may not execute.
>-   In the Live Broadcast profile, a host should not call this method after joining a channel.
>-   If you call this method to test the last-mile quality, the SDK consumes the bandwidth of a video stream, whose bitrate corresponds to the bitrate you set in the [setVideoEncoderConfiguration](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#af5f4de754e2c1f493096641c5c5c1d8f) method. After you join the channel, whether you have called the [disableLastmileTest](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a79dd996df69b1e7141ff036c469cc2dc) method or not, the SDK automatically stops consuming the bandwidth.

Returns

-   0: Success.
-   < 0: Failure.


#### disableLastmileTest()
```disableLastmileTest()```

Disables the network connection quality test.

Returns

-   0: Success.
-   < 0: Failure.


#### startLastmileProbeTest()
```startLastmileProbeTest(AgoraLastmileProbeConfig config)```

Starts the last-mile network probe test before joining a channel to get the uplink and downlink last-mile network statistics, including the bandwidth, packet loss, jitter, and round-trip time (RTT).

Once this method is enabled, the SDK returns the following callbacks:

-   [onLastmileQuality](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a2887941e3c105c21309bd2643372e7f5): the SDK triggers this callback within two seconds depending on the network conditions. This callback rates the network conditions with a score and is more closely linked to the user experience.
-   [onLastmileProbeResult](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#ad74a9120325bfeccdec4af4611110281): the SDK triggers this callback within 30 seconds depending on the network conditions. This callback returns the real-time statistics of the network conditions and is more objective.

Call this method to check the uplink network quality before users join a channel or before an audience switches to a host.

>Note:
>-   This method consumes extra network traffic and may affect communication quality. We do not recommend calling this method together with [enableLastmileTest](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a35d045b585649ca89377ed82e9cf0662).
>-   Do not call other methods before receiving the [onLastmileQuality](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a2887941e3c105c21309bd2643372e7f5) and [onLastmileProbeResult](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#ad74a9120325bfeccdec4af4611110281) callbacks. Otherwise, the callbacks may be interrupted by other methods.
>-   In the Live Broadcast profile, a host should not call this method after joining a channel.

Parameters

|config|  |
|--|--|
|  |  The configurations of the last-mile network probe test. For details, see [LastmileProbeConfig](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1internal_1_1_lastmile_probe_config.html).|

Returns

-   0: Success.
-   < 0: Failure.

#### stopLastmileProbeTest()
```stopLastmileProbeTest()```

Stops the last-mile network probe test.

Returns

-   0: Success.
-   < 0: Failure.


#### addVideoWatermark()
```addVideoWatermark(String url, WatermarkOptions options)```

Adds a watermark image to the local video.

This method adds a PNG watermark image to the local video stream in a live broadcast. Once the watermark image is added, all the audience in the channel (CDN audience included), and the recording device can see and capture it.

Agora supports adding only one watermark image onto the local video, and the newly watermark image replaces the previous one.

The watermark position depends on the settings in the [setVideoEncoderConfiguration](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#af5f4de754e2c1f493096641c5c5c1d8f) method:

-   If the orientation mode of the encoding video is ORIENTATION_MODE_FIXED_LANDSCAPE, or the landscape mode in ORIENTATION_MODE_ADAPTIVE, the watermark uses the landscape orientation.
-   If the orientation mode of the encoding video is ORIENTATION_MODE_FIXED_PORTRAIT, or the portrait mode in ORIENTATION_MODE_ADAPTIVE, the watermark uses the portrait orientation.
-   When setting the watermark position, the region must be less than the dimensions set in the setVideoEncoderConfiguration method. Otherwise, the watermark image will be cropped.

>Note:
>-   Ensure that you have called the [enableVideo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a99ae52334d3fa255dfcb384b78b91c52) method to enable the video module before calling this method.
>-   If you only want to add a watermark image to the local video for the audience in the CDN live broadcast channel to see and capture, you can call this method or the [setLiveTranscoding](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a3cb9804ae71819038022d7575834b88c) method.
>-   This method supports adding a watermark image in the PNG file format only. Supported pixel formats of the PNG image are RGBA, RGB, Palette, Gray, and Alpha_gray.
>-   If the dimensions the PNG image differ from your settings in this method, the image will be cropped or zoomed to conform to your settings.
>-   If you have enabled the local video preview by calling the [startPreview](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a9143c9bb03165fe8b07c0c1e5a455ffb) method, you can use the `visibleInPreview` member in the `WatermarkOptions` class to set whether or not the watermark is visible in preview.
>-   If you have enabled the mirror mode for the local video, the watermark on the local video is also mirrored. To avoid mirroring the watermark, Agora recommends that you do not use the mirror and watermark functions for the local video at the same time. You can implement the watermark function in your application layer.

Parameters

 1. URL

|URL|  |
|--|--|
|  |  The local file path of the watermark image to be added. This method supports adding a watermark image from either the local file path or the assets file path. If you use the assets file path, you need to start with `/assets/` when filling in this parameter.|

 2. options

|options|  |
|--|--|
|  |  The options of the watermark image to be added. See [Watermark Options](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1video_1_1_watermark_options.html).|

Returns

-   0: Success.
-   < 0: Failure.


#### clearVideoWatermarks()
```clearVideoWatermarks()```

Removes the watermark image from the video stream added by [addVideoWatermark]().

Returns

-   0: Success.
-   < 0: Failure.


#### startAudioMixing()
```startAudioMixing(String filepath, bool loopback, bool replace, int cycle)```

Starts playing and mixing the music file.

This method mixes the specified local or online audio file with the audio stream from the microphone, or replaces the microphone’s audio stream with the specified local or remote audio file. You can choose whether the other user can hear the local audio playback and specify the number of playback loops. When the audio mixing file playback finishes after calling this method, the SDK triggers the [onAudioMixingFinished](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a9352d5db6b206605b130bfd2f6739faf) callback.

A successful startAudioMixing method call triggers the [onAudioMixingStateChanged](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#aee0aa9286a39654312b162750713e986)(MEDIA_ENGINE_AUDIO_EVENT_MIXING_PLAY) callback on the local client.

When the audio mixing file playback finishes, the SDK triggers the [onAudioMixingStateChanged](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#aee0aa9286a39654312b162750713e986)(MEDIA_ENGINE_AUDIO_EVENT_MIXING_STOPPED) callback on the local client.

Parameters

 1. filepath

|filepath|  |
|--|--|
|  |Specifies the absolute path (including the suffixes of the filename) of the local or online audio file to be mixed. For example, `/sdcard/emulated/0/audio.mp4`. Supported audio formats: mp3, mp4, m4a, aac, 3gp, mkv, and wav.  |
|  |If the path begins with /assets/, the audio file is in the /assets/ directory.  |
|  |Otherwise, the audio file is in the absolute path.  |

 2. loopback

|loopback  |  |
|--|--|
|  | Sets which user can hear the audio mixing: |
|  | true: Only the local user can hear the audio mixing. |
|  |false: Both users can hear the audio mixing.  |

 3. replace

|replace|  |
|--|--|
|  |Sets the audio mixing content:  |
|  |true: Only publish the specified audio file; the audio stream from the microphone is not published.  |
|  |false: The local audio file is mixed with the audio stream from the microphone.  |

 4. cycle

|cycle|  |
|--|--|
|  |Sets the number of playback loops:  |
|	|	Positive integer: Number of playback loops|
|	|	-1: Infinite playback loops|

>Note: 
>-   To use this method, ensure that the Android device is v4.2 or later, and the API version is v16 or later.
>-   Call this method when you are in the channel, otherwise it may cause issues.
>-   If you want to play an online music file, ensure that the time interval between calling this method is more than 100 ms, or the AUDIO_FILE_OPEN_TOO_FREQUENT = 702 warning occurs.
>-   If you want to play an online music file, Agora does not recommend using the redirected URL address. Some Android devices may fail to open a redirected URL address.
>-   If the local audio mixing file does not exist, or if the SDK does not support the file format or cannot access the music file URL, the SDK returns [WARN_AUDIO_MIXING_OPEN_ERROR = 701](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a1052ee12a826906a57e135a2a0dc1327).
>-   If you call this method on an emulator, only the MP3 file format is supported.

Returns

-   0: Success.
-   < 0: Failure.
    -   [WARN_AUDIO_MIXING_OPEN_ERROR (701)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a1052ee12a826906a57e135a2a0dc1327): If the local audio file does not exist, or the online audio packet is not received within five seconds after it is opened, the SDK assumes that the media file cannot be used and returns this warning.


#### stopAudioMixing()
```stopAudioMixing()```

Stops playing or mixing the music file.

Call this method when you are in a channel.

Returns

-   0: Success.
-   < 0: Failure.


#### pauseAudioMixing()
```pauseAudioMixing()```

Pauses playing and mixing the music file.

Call this method when you are in a channel.

Returns

-   0: Success.
-   < 0: Failure.


#### resumeAudioMixing()
```resumeAudioMixing()```

Resumes playing and mixing the music file.

Call this method when you are in a channel.

Returns

-   0: Success.
-   < 0: Failure.


#### adjustAudioMixingVolume()
```adjustAudioMixingVolume(int volume)```

Adjusts the volume of audio mixing.

Call this method when you are in a channel.

>Note: Calling this method does not affect the volume of the audio effect file playback invoked by the [playEffect](https://docs.agora.io/en/Video/API%20Reference/java/interfaceio_1_1agora_1_1rtc_1_1_i_audio_effect_manager.html#a6fd330db3e3e5735f7f8d5c36bc3fea1) method.

Parameters

|volume|  |
|--|--|
|  |  Audio mixing volume. The value ranges between 0 and 100 (default).|

Returns

-   0: Success.
-   < 0: Failure.


#### adjustAudioMixingPlayoutVolume()
```adjustAudioMixingPlayoutVolume(int volume)```

Adjusts the volume of audio mixing for local playback.

ParametersAdjusts the volume of audio mixing for local playback.

Parameters

|volume|  |
|--|--|
|  |  Audio mixing volume for local playback. The value ranges between 0 and 100 (default).|

Returns

-   0: Success.
-   < 0: Failure.


#### adjustAudioMixingPublishVolume()
```adjustAudioMixingPublishVolume(int volume)```

Adjusts the volume of audio mixing for publishing (sending to other users).Adjusts the volume of audio mixing for publishing (sending to other users).


Parameters

|volume|  |
|--|--|
|  |  Audio mixing volume for publishing. The value ranges between 0 and 100 (default).|

Returns

-   0: Success.
-   < 0: Failure.


#### getAudioMixingPlayoutVolume()
```getAudioMixingPlayoutVolume()```

Gets the audio mixing volume for local playback.

This method helps troubleshoot audio volume related issues.

Returns

-   Returns the audio mixing volume for local playback, if the method call is successful. The value range is [0,100].
-   < 0: Failure.


#### getAudioMixingPublishVolume()
```getAudioMixingPublishVolume()```

Gets the audio mixing volume for publishing.

This method helps troubleshoot audio volume related issues.

Returns

-   Returns the audio mixing volume for publishing, if the method call is successful. The value range is [0,100].
-   < 0: Failure.


#### getAudioMixingDuration()
```getAudioMixingDuration()```

Gets the duration (ms) of the music file.

Call this method when you are in a channel.

Returns

-   Returns the audio mixing duration, if the method call is successful.
-   < 0: Failure.


#### getAudioMixingCurrentPosition()
```getAudioMixingCurrentPosition()```

Gets the playback position (ms) of the music file.

Call this method when you are in a channel.

Returns

-   Returns the current playback position of the audio mixing, if the method call is successful.
-   < 0: Failure.


#### setAudioMixingPosition()
```setAudioMixingPosition(int pos)```

Sets the playback position (ms) of the music file to a different starting position (the default plays from the beginning).

Parameters

|pos|  |
|--|--|
|  |The playback starting position (ms) of the audio mixing file.  |

Returns

-   0: Success.
-   < 0: Failure.


#### getEffectsVolume()
```getEffectsVolume()```

Gets the effects volume.

Returns

-   0: Success.
-   < 0: Failure.


#### setEffectsVolume()
```setEffectsVolume(double volume)```

Sets the volume for the effect.

|volume|  |
|--|--|
|  |  Effects volume. The value ranges between 0 and 100 (default).|

Returns

-   0: Success.
-   < 0: Failure.


#### playEffect()
```playEffect(int soundId, String filepath, int loopcount,double pitch, double pan, double gain, bool publish)```

Plays a specified local or online audio effect file.

With this method, you can set the loop count, pitch, pan, and gain of the audio effect file and whether the remote user can hear the audio effect.

To play multiple audio effect files simultaneously, call this method multiple times with different soundIds and filePaths. We recommend playing no more than three audio effect files at the same time.

When the audio effect file playback is finished, the SDK triggers the [onAudioEffectFinished](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#aa7a6c771353ad2097e05133622161090) callback.

Parameters

 1. soundId

|soundId|  |
|--|--|
|  |ID of the specified audio effect. Each audio effect has a unique ID. If you preloaded the audio effect into the memory through the [preloadEffect](https://docs.agora.io/en/Video/API%20Reference/java/interfaceio_1_1agora_1_1rtc_1_1_i_audio_effect_manager.html#a0815d837d9a01b5d3a916ab788845b33) method, ensure that the `soundID` value is set to the same value as in the [preloadEffect](https://docs.agora.io/en/Video/API%20Reference/java/interfaceio_1_1agora_1_1rtc_1_1_i_audio_effect_manager.html#a0815d837d9a01b5d3a916ab788845b33) method.  |

 2. filepath

|filepath  |  |
|--|--|
|  |The absolute file path (including the suffixes of the filename) of the audio effect file or the URL of the online audio effect file. For example, `/sdcard/emulated/0/audio.mp4`. Supported audio formats: mp3, mp4, m4a, aac. 3gp, mkv, and wav.  |

 3. loopcount

|loopcount|  |
|--|--|
|  |Sets the number of times the audio effect loops:  |
|  |0: Plays the audio effect once.  |
|  | 1: Plays the audio effect twice. |
|  |-1: Plays the audio effect in a loop indefinitely, until you call the [stopEffect](https://docs.agora.io/en/Video/API%20Reference/java/interfaceio_1_1agora_1_1rtc_1_1_i_audio_effect_manager.html#a37a08cbd9d0c9045349888a49dc2b217) or [stopAllEffects](https://docs.agora.io/en/Video/API%20Reference/java/interfaceio_1_1agora_1_1rtc_1_1_i_audio_effect_manager.html#a45afed476a26393eb4e63a68eebdf171) method.  |

 4. pitch

|pitch|  |
|--|--|
|  |Sets the pitch of the audio effect. The value ranges between 0.5 and 2. The default value is 1 (no change to the pitch). The lower the value, the lower the pitch.  |

 5. pan

|pan  |  |
|--|--|
|  | Sets the spatial position of the audio effect. The value ranges between -1.0 and 1.0. |
|  |0.0: The audio effect shows ahead.  |
|  | 1.0: The audio effect shows on the right. |
|  |-1.0: The audio effect shows on the left.  |

 6. gain

|gain|  |
|--|--|
|  | Sets the volume of the audio effect. The value ranges between 0.0 and 100,0. The default value is 100.0. The lower the value, the lower the volume of the audio effect. |

 7. publish

|publish|  |
|--|--|
|  |Set whether or not to publish the specified audio effect to the remote stream:  |
|  |true: The locally played audio effect is published to the Agora Cloud and the remote users can hear it.  |
|  |false: The locally played audio effect is not published to the Agora Cloud and the remote users cannot hear it.  |

Returns

-   0: Success.
-   < 0: Failure.


#### stopEffect()
```stopEffect(int soundId)```

Stops playing a specified audio effect.

Parameter

|soundId|  |
|--|--|
|  |ID of the specified audio effect. Each audio effect has a unique ID.  |

>Note: If you preloaded the audio effect into the memory through the [preloadEffect]() method, ensure that the `soundID` value is set to the same value as in the [preloadEffect]() method.

Returns

-   0: Success.
-   < 0: Failure.


#### stopAllEffects()
```stopAllEffects()```

Stops playing all audio effects.

Returns

-   0: Success.
-   < 0: Failure.


#### preloadEffect()
```preloadEffect(int soundId, String filepath)```

Preloads a specified audio effect file into the memory.

Supported audio formats: mp3, aac, m4a, 3gp, wav.

>Note: This method does not support online audio effect files.

Parameters

 1. soundId

|soundId|  |
|--|--|
|  |ID of the audio effect. Each audio effect has a unique ID.  |

2. filepath 

|filepath|  |
|--|--|
|  |Absolute path of the audio effect file.  |

>Note: To ensure smooth communication, limit the size of the audio effect file. We recommend using this method to preload the audio effect before calling the [joinChannel]() method.

Returns

-   0: Success.
-   < 0: Failure.


#### unloadEffect()
```unloadEffect(int soundId)```

Releases a specified preloaded audio effect from the memory.

Parameter

|soundId|  |
|--|--|
|  | ID of the audio effect. Each audio effect has a unique ID. |

Returns

-   0: Success.
-   < 0: Failure.


#### pauseEffect()
```pauseEffect(int soundId)```

Pauses a specified audio effect.

Parameters

|soundId|  |
|--|--|
|  | ID of the audio effect. Each audio effect has a unique ID. |

Returns

-   0: Success.
-   < 0: Failure.


#### pauseAllEffects()
```pauseAllEffects()```

Pauses all audio effects.

Returns

-   0: Success.
-   < 0: Failure.


#### resumeEffect()
```resumeEffect(int soundId)```

Resumes playing a specified audio effect.

Parameters

|soundId|  |
|--|--|
|  | ID of the audio effect. Each audio effect has a unique ID. |

Returns

-   0: Success.
-   < 0: Failure.


#### resumeAllEffects()
```resumeAllEffects()```

Resumes playing all audio effects.

Returns

-   0: Success.
-   < 0: Failure.




#### startChannelMediaRelay()
```startChannelMediaRelay(AgoraChannelMediaRelayConfiguration config)```

Starts to relay media streams across channels.

After a successful method call, the SDK triggers the [onChannelMediaRelayStateChanged](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a89fd95b3536e8e6afd5f001926162f66) and [onChannelMediaRelayEvent](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a6fe2367e9ea61e48a4cc3b373d198b54) callbacks, and these callbacks return the state and events of the media stream relay.

-   If the `onChannelMediaRelayStateChanged` callback returns RELAY_STATE_RUNNING(2) and RELAY_OK(0), and the `onChannelMediaRelayEvent` callback returns RELAY_EVENT_PACKET_SENT_TO_DEST_CHANNEL(4), the SDK starts relaying media streams between the original and the destination channel.
-   If the `onChannelMediaRelayStateChanged` callback returns RELAY_STATE_FAILURE(3), an exception occurs during the media stream relay.

>Note

>-   Contact [sales-us@agora.io](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#) before implementing this function.
>-   We do not support string user accounts in this API.
>-   Call this method after the [joinChannel](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a8b308c9102c08cb8dafb4672af1a3b4c) method.
>-   This method takes effect only when you are a broadcaster in a Live-broadcast channel.
>-   After a successful method call, if you want to call this method again, ensure that you call the [stopChannelMediaRelay](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a0f9f19e48c21190dd4e697dec632c328) method to quit the current relay.


Parameters

| config |  |
|--|--|
|  | The configuration of the media stream relay: [ChannelMediaRelayConfiguration](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1video_1_1_channel_media_relay_configuration.html). |

Returns

-   0: Success.
-   < 0: Failure.


#### removeChannelMediaRelay()
```removeChannelMediaRelay(AgoraChannelMediaRelayConfiguration config)```

Removes relay media streams across channels.

Parameters

|config  |  |
|--|--|
|  |The media stream relay configuration: [ChannelMediaRelayConfiguration](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1video_1_1_channel_media_relay_configuration.html).  |

Returns

-   0: Success.
-   < 0: Failure.


#### updateChannelMediaRelay()
```updateChannelMediaRelay(AgoraChannelMediaRelayConfiguration config)```

Updates the channels for media relay.

After the channel media relay starts, if you want to relay the media stream to more channels, or leave the current relay channel, you can call the `updateChannelMediaRelay` method.

After a successful method call, the SDK triggers the [onChannelMediaRelayEvent](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a6fe2367e9ea61e48a4cc3b373d198b54) callback with the RELAY_EVENT_PACKET_UPDATE_DEST_CHANNEL(7) state code.

>Note
>-   Call this method after the `startChannelMediaRelay` method to update the destination channel.
>-   This method supports adding at most four destination channels in the relay. If there are already four destination channels in the relay, remove the unnecessary ones with the [removeDestChannelInfo](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1video_1_1_channel_media_relay_configuration.html#a7b1ddbc12d5d84dc97d7154f2736a2b0) method in `ChannelMediaRelayConfiguration` before calling this method.

Parameters

|config  |  |
|--|--|
|  |The media stream relay configuration: [ChannelMediaRelayConfiguration](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1video_1_1_channel_media_relay_configuration.html).  |

Returns

-   0: Success.
-   < 0: Failure.


#### stopChannelMediaRelay()
```stopChannelMediaRelay()```

Stops the media stream relay.

Once the relay stops, the broadcaster quits all the destination channels. After a successful method call, the SDK triggers the [onChannelMediaRelayStateChanged](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_i_rtc_engine_event_handler.html#a89fd95b3536e8e6afd5f001926162f66) callback. If the callback returns RELAY_STATE_IDLE(0) and RELAY_OK(0), the broadcaster successfully stops the relay.

>Note: If the method call fails, the SDK triggers the `onChannelMediaRelayStateChanged` callback with the RELAY_ERROR_SERVER_NO_RESPONSE(2) or RELAY_ERROR_SERVER_CONNECTION_LOST(8) state code. You can leave the channel by calling the [leaveChannel](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a2929e4a46d5342b68d0deb552c29d597) method, and the media stream relay automatically stops.

Returns

-   0: Success.
-   < 0: Failure.


#### enableInEarMonitoring()
```enableInEarMonitoring(bool enabled)```

Enables in-ear monitoring.

Parameters

|enabled|  |
|--|--|
|  |Sets whether to enable/disable in-ear monitoring:  |
|  |true: Enable.  |
|  |false: (Default) Disable.  |

Returns

-   0: Success.
-   < 0: Failure.


#### setInEarMonitoringVolume()
```setInEarMonitoringVolume(int volume)```

Sets the volume of the in-ear monitor.

Parameters

|volume|  |
|--|--|
|  |Sets the volume of the in-ear monitor. The value ranges between 0 and 100 (default).  |

Returns

-   0: Success.
-   < 0: Failure.


#### switchCamera()
```switchCamera()```

Switches between front and rear cameras.

Returns

-   0: Success.
-   < 0: Failure.


#### setLogFile()
```setLogFile(String filePath)```

Specifies an SDK output log file.

The log file records all log data for the SDK’s operation. Ensure that the directory for the log file exists and is writable.

>Note: Ensure that you call this method immediately after calling the [create](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#a35466f690d0a9332f24ea8280021d5ed) method, otherwise the output log may not be complete.

Parameters

|filePath  |  |
|--|--|
|  |File path of the log file. The string of the log file is in UTF-8. The default file path is /storage/emulated/0/Android/data/<package name>="">/files/agorasdk.log.  |

Returns

-   0: Success.
-   < 0: Failure.


#### setLogFilter()
```setLogFilter(int filter)```

Sets the output log level of the SDK.

You can use one or a combination of the filters. The log level follows the sequence of OFF, CRITICAL, ERROR, WARNING, INFO, and DEBUG. Choose a level to see the logs preceding that level. For example, if you set the log level to WARNING, you see the logs within levels CRITICAL, ERROR, and WARNING.

Parameters

|filter|  |
|--|--|
|  |Sets the log filter level:  |
|  |[LOG_FILTER_DEBUG(0x80f)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ade86d3e07f6dea38fc200ee301b43888): Output all API logs. Set your log filter as DEBUG if you want to get the most complete log file.  |
|  |-   [LOG_FILTER_INFO(0x0f)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#ae87810752556891f81d0099f9a002c03): Output logs of the CRITICAL, ERROR, WARNING, and INFO level. We recommend setting your log filter as this level.  |
|  |[LOG_FILTER_WARNING(0x0e)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a9383a123b1c5d49fd0b7717468e367b2): Output logs of the CRITICAL, ERROR, and WARNING level.  |
|  |[LOG_FILTER_ERROR(0x0c)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a98cfa35bbf56f69f25328bc422bebca9): Output logs of the CRITICAL and ERROR level.  |
|  |[LOG_FILTER_CRITICAL(0x08)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#a06affcaeffa3f3a94c05bc9ff3bec76f): Output logs of the CRITICAL level.  |
|  |[LOG_FILTER_OFF(0)](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_constants.html#aede0f95348f3450f0f2bd76e70eaddda): Do not output any log.  |

Returns

-   0: Success.
-   < 0: Failure.


#### setLogFileSize()
```setLogFileSize(int fileSizeInKBytes)```

Sets the log file size (KB).

The Agora SDK has two log files, each with a default size of 512 KB. If you set `fileSizeInKBytes` as 1024 KB, the SDK outputs log files with a total maximum size of 2 MB. If the total size of the log files exceed the set value, the new output log files overwrite the old output log files.

Parameters

|fileSizeInKBytes|  |
|--|--|
|  |The SDK log file size (KB).  |

Returns

-   0: Success.
-   < 0: Failure.


#### setParameters()
```setParameters(String params)```

Provides technical preview functionalities or special customizations by configuring the SDK with JSON options.

The JSON options are not public by default. Agora is working on making commonly used JSON options public in a standard way.

Parameters

|params  |  |
|--|--|
|  | Sets the parameter as a JSON string in the specified format. |

Returns

-   0: Success.
-   < 0: Failure.


#### setParameters()
```setParameters(String params)```

Provides technical preview functionalities or special customizations by configuring the SDK with JSON options.

The JSON options are not public by default. Agora is working on making commonly used JSON options public in a standard way.

Parameters

|params  |  |
|--|--|
|  | Sets the parameter as a JSON string in the specified format. |

Returns

-   0: Success.
-   < 0: Failure.


#### getParameters()
```getParameters(String params, String args)```

Gets the Agora SDK’s parameters for customization purposes. This method is not disclosed yet. Contact [support@agora.io](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#) for more information.


#### create()
```create(String appid)```

Creates an [AgoraRtcEngine](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html) instance.

The Agora SDK only supports one [AgoraRtcEngine](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html) instance at a time, therefore the app should create one [AgoraRtcEngine](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html) object only. Unless otherwise specified:

-   All called methods provided by the [AgoraRtcEngine](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html) class are executed asynchronously. We recommend calling the interface methods in the same thread.
-   The following rule applies to all API methods whose return values are integer types:
    -   0: The method call succeeds.
    -   < 0: The method call fails.

Parameters

|appid  |  |
|--|--|
|  |The App ID issued to you by Agora. Apply for a new App ID from Agora if it is missing from your kit.  |

Returns

-   The [AgoraRtcEngine](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html) instance, if the method call succeeds.
-   < 0, if the method call fails.
    -   ERR_INVALID_APP_ID(101): The app ID is invalid. Check if it is in the correct format.

>Exceptions: Fails to create an [AgoraRtcEngine](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html) instance.

>Note
>-   Ensure that you call this method before calling any other API.
>-   Only users with the same App ID can join the same channel and call each other.
>-   An App ID can create only one [RtcEngine](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html) object. For multiple App IDs in an app, you need to create multiple [RtcEngine](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html) objects. Call [destroy](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#afb808cdc9025a77af7dd2bce98311bfe) first to destroy the current [RtcEngine](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html) instance before calling this method.


#### destroy()
```destroy()```

Destroys the [AgoraRtcEngine](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html) instance and releases all resources used by the Agora SDK.

This method is useful for apps that occasionally make voice or video calls, to free up resources for other operations when not making calls.

>Note
>-   Call this method in the subthread.
>-   Once the app calls [destroy](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html#afb808cdc9025a77af7dd2bce98311bfe) to destroy the created [AgoraRtcEngine](https://docs.agora.io/en/Video/API%20Reference/java/classio_1_1agora_1_1rtc_1_1_rtc_engine.html) instance, you cannot use any method or callback in the SDK.


#### getSdkVersion()
```getSdkVersion()```

Gets the SDK version.

Returns

The version of the current SDK in the string format. For example, 1.0.8


## Agora Superstar
This documentation is written and maintained by [Meherdeep Thakur](https://github.com/Meherdeep/) an Agora superstar. Meherdeep has a strong knowledge of ML/AI and Flutter app development. The Agora Superstar program empowers developers around the world to share their passion and technical expertise, and create innovative real-time communications apps and projects using Agora’s customizable SDKs. Think you’ve got what it takes to be an Agora Superstar? Apply [here]( https://www.agora.io/en/superstars-program/)
