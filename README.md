# aerout clip :D

a clipper for mac. hit one key n it saves the last bit of ur gameplay, like shadowplay or medal but built for macos.

made by aero

---

## what it does

it records ur screen quietly in the background. when somethin good happens u hit ur keybind n it saves the last 30 seconds (or whatever u set). u dont have to remember to start recordin first.

when ur done u hit stop n it saves the whole session too, so nothin gets lost.

---

## whats different about it

**it doesnt need a account or a login.** no sign up, no watermark, no upload limit. everythin stays on ur mac unless u choose to share it.

**it can record one app on its own.** pick roblox n thats the only thing in the clip. u can have discord n safari open on top the whole time n none of it shows up.

**it splits ur audio into separate tracks.** ur mic, ur game, n ur discord call each get their own track. later u can mute the music n keep the voices, or kill ur own mic if u said somethin dumb.

**it has its own audio driver.** macos normally doesnt let apps hear ur game sound at all. we wrote a driver so it can. no blackhole, no soundflower, no terminal.

**it has a built in editor.** trim it, crop it, mute a track, pull just the audio out. no exportin to another app.

**it turns clips into links.** one click n u get a link u can paste in discord. it plays right there in the chat.

---

## what mac do u need

| ur mac | what u get |
|---|---|
| macos 12.3 to 12.7 | everythin works, u install the little audio driver once |
| macos 13 n up | everythin works, **no driver at all**, sound just gets recorded |
| intel macs | works |
| apple silicon (m1, m2, m3, m4) | works |
| macos 12.2 or older | sorry, wont run |

**on macos 13 n newer** apple added a proper way for apps to hear system sound, so the app uses that instead. nothin to install, no password, no extra speakers in ur sound menu. the only thing u lose is the separate discord track.

**on macos 12** u hit one button in the audio tab n it installs the driver. it asks for ur password once n thats it, u never touch terminal.

---

## gettin started

1. download the dmg from [releases](https://github.com/wrealaero/aerout-clipper/releases) n drag it to applications
2. open it. macos will ask for **screen recording**. say yes, then **quit the app fully n open it again** (this part matters, it wont work til u do)
3. go to the **audio** tab n set up sound if u want it
4. go to **main**, set ur keybind n how long u want ur clips
5. hit **record** n go play

---

## the tabs

### main
ur keybind, how long a clip is, n the big record button. the numbers at the bottom show how long uve been recordin n how many clips uve saved.

**clip length** is how far back ur key reaches. 30 seconds catches most stuff. longer means more of ur disk gets used while it runs.

### capture
**record one app only** is the good one. flick it on, pick ur game, n thats the only thing that ends up in the clip. u can alt tab to discord n it still records ur game.

**quality** n **fps** are the two that decide if ur game lags. fps hurts way more than quality so if things feel choppy drop fps to 30 first.

**bitrate** is just how big the file is. it costs u nothin in fps. 8 is fine for discord, 20 or more if ur puttin it on youtube.

### clips
everythin uve saved. u can star ur favourites, make folders n drag clips into em, rename stuff, n sort it however u want. the folders are real folders so they show up in finder too.

the play button opens the editor.

### audio
where u turn sound on. pick which of the three u want in ur clips: **ur mic**, **game n everythin else**, n **voices** (ur discord call, macos 12 only).

theres also **mic boost** if ppl say ur too quiet. push the **mac input level** slider up first, then use boost on top.

### settings
colours, where clips get saved, what sound plays when somethin saves, n the update checker.

---

## the editor

hit the pencil on any clip.

- **drag the two blue grips** on the timeline to pick ur start n end
- **crop** lets u cut the edges off, with 16:9, 1:1 n 9:16 presets
- the **audio row** under the video lets u mute any track. double click one to solo it
- **save the cut** spits out a new file, ur original stays untouched
- **audio only** pulls just the sound out as a m4a

**shortcuts:** space plays, arrows step one frame, shift+arrows jump 5 seconds, `i` n `o` set ur start n end, `c` is crop, `+` n `-` zoom the timeline, `0` fits it all.

---

## sharing clips

in the clips tab hit **turn links on**. wait a few seconds, then every clip gets a link button. one click copies a link u can paste anywhere.

**u need cloudflared for this.** open terminal n run:

```
brew install cloudflared
```

**how it looks in discord** is a setting. **clean** gives u just the video playin with no box around it, which looks best. **card** n **big picture** add a title n a thumbnail.

heads up: the link only works while the app is open, n anyone with the link can watch it. hit **take all down** when ur done.

---

## splittin ur discord call onto its own track

**macos 12 only.** this is optional, skip it if u dont care.

1. open the discord app, settings, voice n video
2. set **output device** to **Aerout Chat Mix**
3. done

now ur call is on its own track in every clip. u wont hear any difference while ur playin.

this only works for apps that let u pick their own output, like discord, spotify n vlc. safari n roblox dont have that setting, so discord in a browser tab cant be split from youtube. use the discord app for that.

---

## if somethin goes wrong

**it says it cant see my screen**
go to system settings, privacy, screen recording, make sure aerout clip is ticked. then **quit the app completely n reopen it**. macos only applies it on a fresh launch.

**my clips have no sound**
audio tab, check both dots are lit up. on macos 12 u need the driver installed n recording turned on.

**my volume keys dont work**
on macos 12 with sound recordin on, macos blocks the normal volume slider. the app can take over ur volume keys instead, it just needs accessibility permission. theres a button in the audio tab that takes u there.

**my mic is too quiet**
audio tab. push **mac input level** to 90 then use **mic boost**. watch the bar while u talk, back off if it turns red.

**my game is laggin**
capture tab. drop fps to 30 first, then quality to 720p. if ur on an older mac use 720p at 30 n leave it there.

**my mic picks up my speakers**
use headphones. theres no software fix for a mic hearin ur own speakers.

---

## does it steal my stuff

no. clips stay in `~/Movies/AeroutClipper` on ur mac. nothin gets uploaded anywhere. theres no account, no tracking, no telemetry.

the only time anythin leaves ur mac is if **u** hit the share button, n those links die when u close the app.

---

## updates

the app checks github every few hours n shows a bar at the top when theres a new version. it **never** installs anythin by itself, u click the button.

u can also check manually in settings.

---

## thanks

to everyone who tested this n told me what was broken. especially desire n nick for findin half the bugs.
