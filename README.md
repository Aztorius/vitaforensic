# Vita Forensic

## Step 0 : remove passcode

If there is an unknown passcode at startup, then you will need to remove it.
To do so, you will need to check if the PS Vita is a 1st gen (PCH-100X) or 2nd gen (PCH-200X).

IN ANY CASE : MAKE A FORENSIC COPY OF THE MEMORY CARD

### Remove passcode on 1st gen PS Vita (NOT TESTED, playstation credentials REQUIRED)

- Turn off the PS Vita
- Remove all storage cards from the console
- Hold power button for 30 seconds
- On the recovery menu reset the system
- Once the initialisation is done you need to log in with the user credentials of the same playstation account that was on the console
- Then turn off the console and put back the memory card
- Now your PS Vita should be able to see all content inside the memory card and you have removed the passcode !

### Remove passcode on 2nd gen PS Vita (NOT TESTED, playstation credentials REQUIRED)

- Be sure there is a storage card inserted in the console
- If there is no card, it may be possible all data are inside the internal storage and YOU SHOULD NOT GO ANY FURTHER

- Hold power button for 30 seconds
- On the recovery menu reset the system
- Once the initialisation is done you need to log in with the user credentials of the same playstation account that was on the console
- Then turn off the console and put back the memory card
- Now your PS Vita should be able to see all content inside the memory card and you have removed the passcode !

## Step 1 : create a backup with QCMA

https://github.com/codestation/qcma

## Step 2 : get the decryption key from cma.henkaku.xyz

The AID used on the PSVita is a 16 caracters string that is shown inside the backup folder.

## Step 3 : decrypt the backup with psvimgtools

https://github.com/yifanlu/psvimgtools

```
psvimg-extract -K [the encryption key] [your backup].psvimg [destination folder]
```

## Step 4 : launch vitaforensic analysis

### Important files

- Contacts : ur0_contacts/database/addressbook.db
- List of apps on the live area : ur0_shell/db/app.db
- Each user have one folder in ur0_user/ like 00/, 01/, ...
- Near app database : ur0_user/XX/near/data_sys/db/near.db
- Internet browser save files : ur0_user/XX/savedata/NPXS10003/
- Internet browser bookmarks : ur0_user/XX/savedata/NPXS10003/webbrowser_bookmark.db
- Internet browser history : ur0_user/XX/savedata/NPXS10003/webbrowser_history.db
- User and contacts events : ur0_user/XX/shell/db/act.db
- Calendar : ux0_calendar/calendar.db
- Emails : ux0_email/message/mail.db
- Playlists : ux0_mms/music/AVContent.db ux0_mms/photo/AVContent.db ux0_mms/video/AVContent.db
- Pictures : ux0_picture/CAMERA/
- Screenshots : ux0_picture/SCREENSHOT/
- All images : ux0_picture/ALL/
