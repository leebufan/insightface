# Using Midjourney and InsightFaceSwap Bot to create a personalized portrait

## Updates

**`2023-04-18`**: Now we support Discord application commands(AKA. slash commands), please remember joining our [Discord group](https://discord.gg/65Ma47ymPc) to get notification.

## Introduction

For over 99% of people, using Midjourney to create your own portraits is not feasible unless you're a famous celebrity with thousands or millions of photos online. But now, with the InsightFaceSwap Discord bot, you can accomplish this task easily with just a few steps.

<div align="left">
<img src="https://raw.githubusercontent.com/nttstar/insightface-resources/master/images/swapd0.jpg" width="800"/>
</div>

## Discord Slash Commands

InsightFaceSwap bot can help you with the following commands:

### /saveid ``name`` ``upload-image``

Used to upload and register your own photos or ID features for subsequent facial replacement and editing. You can upload up to 10 instances permanently and use them without having to upload them repeatedly.

### /setid ``name(s)``

Set current/default identity name(s), for image generation using context menu. If you need to set multiple ID names, please use commas to separate them.

### /listid

List all registered identity names.

### /delid ``name``

Delete specific identity name.

### /delall 

Delete all registered names.

### /swapid ``name(s)`` ``upload-image``

Replace the face with the registered identity name(s) on target image.

## Discord Context Menu

### Apps/INSwapper

Replace the face with the current/default identity name(s) on target image.


   

## Step-by-step guide:

1. Refer to [this link](https://docs.midjourney.com/docs/invite-the-bot) to register Discord app, create a new chat room, and invite the Midjourney bot to the chat room.
2. Invite the InsightFaceSwap bot to the chat room by this link: <https://discord.com/api/oauth2/authorize?client_id=1090660574196674713&permissions=274877945856&scope=bot>.
<div align="left">
<img src="https://raw.githubusercontent.com/nttstar/insightface-resources/master/images/swapd1.jpg" width="480"/>
</div>
3. Use ``/saveid`` command to register your identity name and feature. Here 'mnls' is the registered name, which can be any alphabets or numbers up to 8 characters long. If everything goes well, the bot will tell you that the save was successful. Note that the newly created identity will be automatically set as the default identity.
<div align="left">
<img src="https://raw.githubusercontent.com/nttstar/insightface-resources/master/images/swapd2.jpg" width="640"/>
</div>
4. Next, we can experiment with creating the portrait. Let's start chanting the Midjourney prompt and enlarge one of the outputs.
<div align="left">
<img src="https://raw.githubusercontent.com/nttstar/insightface-resources/master/images/swapd3.jpg" width="640"/>
</div>
5. After the enlargement is complete, we can simply use the ``INSwapper`` context menu to generate our portrait. Right click on the target image and then select ``Apps-INSwapper`` menu. Note that we can also use ``/setid`` command to change the default identity name.
<div align="left">
<img src="https://raw.githubusercontent.com/nttstar/insightface-resources/master/images/swapd4.jpg" width="640"/>
</div>
6. Generally, the task is completed in less than a second and we can see the result.
<div align="left">
<img src="https://raw.githubusercontent.com/nttstar/insightface-resources/master/images/swapd5.jpg" width="640"/>
</div>
7. In addition to processing photos generated by Midjourney, we can also process locally uploaded photos by using ``/swapid`` command explicitly.
<div align="left">
<img src="https://raw.githubusercontent.com/nttstar/insightface-resources/master/images/swapd6.jpg" width="640"/>
</div>
8. Hit to complete!
<div align="left">
<img src="https://raw.githubusercontent.com/nttstar/insightface-resources/master/images/swapd7.jpg" width="640"/>
</div>
9. Note that the ``INSwapper`` context menu can also work on user uploaded images in your Discord channel.



## Other notes:

1. You can use ``/listid`` command to list all the registered IDs. The total number of registered IDs cannot exceed 10. And also you can use ``/delid`` and ``/delall`` commands to delete registered IDs.
2. The registered ID name can only be alphabets and numbers, and cannot exceed 8 characters.
3. For multi-facial replacement, you can input a comma splitted idname list, such as ``/setid me,you,him,her``
4. You can overwrite old ID features by re-uploading with the same ID name.
5. If you don't want to upload your own photo, you can use the insightface python package to generate your own facial features and save them as a .npy file, where shape=(512,), for uploading.
6. Each Discord account can execute 50 commands per day to avoid automated scripts.
7. This is in early development stage, so we cannot guarantee that the result will be great in every cases.
8. Please use it for personal entertainment purposes only.
9. If there's any problem, please join our Discord group: [link](https://discord.gg/65Ma47ymPc)