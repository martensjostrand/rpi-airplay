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
Run: `$ ansible-playbook -i hosts.yml main.yml`

Use:
---
Connect your AirPlay client to "Vardagsrummet" and enjoy!
