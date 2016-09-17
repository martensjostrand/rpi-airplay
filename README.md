Provision my Raspberry PI music machine.
===

Prerequisites:
---
Things that couldn't be automated:
- Flash SD card, I used `2016-05-27-raspbian-jessie-lite.img`
- Resize partition
- Find IP of your pi, ask google
- Add jukebox user
- Enable ssh without password, see `copy-ssh-id`

Installing:
---
Run:
```
$ ansible-playbook -i hosts.yml main.yml
```

### Override Variables

Variables can be overridden by passing --extra-vars "name1=value1 name2=value2"

You might want to override the following in order to match your system:
```
service_name: RPI Jukebox
audio_output_device: 'hw:1'

hard_drive:
  mount_point: /media/usbdrive
  mount_src: UUID=3db34317-0803-33c1-bc6e-95a49b7f56fd
  music_path: /media/music
  video_path: /media/video
```

Run:
```
$ ansible-playbook -i hosts.yml main.yml --extra-vars "audio_output_device='hw:0'"
```

To use build in sound card. (It sounds horrible...)

Use:
---
Connect your AirPlay client to "RPI Jukebox" or connect your UPnP client to RPI Jukebox and enjoy!
