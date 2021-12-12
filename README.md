# Vita Forensic

## Step 1 : create a backup with QCMA

https://github.com/codestation/qcma

## Step 2 : get the decryption key from cma.henkaku.xyz

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
- Screenshorts : ux0_picture/SCREENSHOT/
- All images : ux0_picture/ALL/

