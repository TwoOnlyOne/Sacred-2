
====================================================================================================================================

sound options
-------------

*** THE FOLLOWING SOUND OPTIONS ARE USED FOR ALL QUALITY MODES ***

plugin: current possible sound plugins are "MILES" and "OPENAL"
	"MILES":	supports software modes with up to 8.1 speakers
	"OPENAL"	this works with highend soundcards w/ OpenAL 1.1 Native Device support (Creative Audigy2/4, X-Fi)
		it supports EAX5.0 hardware mode (also with Windows Vista)
provider(depends on plugin):
	MILES:	does not need a provider
	OPENAL:	leave empty for auto-detection or insert name of the device to use. this will override any auto-detection.

quality:
	1 = high sound quality (default)
	2 = low sound quality (use internal profile)

speakers: (all modes with 4 speakers and more will use the dynamic fight music system)
		0 = default: auto-detection w/ windows settings (5.1 music soundtrack if at least 4 speakers available)
		1 = stereo + stereo music soundtrack
		2 = 4 speakers (4.0) + 4.0 music soundtrack
		3 = 6 speakers (5.1) + 5.1 music soundtrack
		4 = 7 speakers (6.1) + 5.1 music soundtrack
		5 = 8 speakers (7.1) + 5.1 music soundtrack
		6 = 9 speakers (8.1) + 5.1 music soundtrack

volume_master: master volume (0..100; 0 means OFF, >0 means ON; default = 100)
volume_master_music: master volume for all music groups (0..100; 0 means OFF, >0 means ON; default = 100)
volume_master_sfx: master volume for all sfx groups (0..100; 0 means OFF, >0 means ON; default = 80)
volume_master_speech: master volume for all speech groups (0..100; 0 means OFF, >0 means ON; default = 100)
volume_group01..volume_group31:	volume for all sounds in group 1..30 (0..100; 0 means OFF, >0 means ON; default = 80)
			        	default groups:	region music=1, fight music=2, fx=3, atmo=4, atmo sfx=5, atmo sfx2=6, footsteps=7,
			                        		sfx generic=8, forest cluster=9, lava cluster=10, water cluster=11, t-energy cluster=12,
			                        		weather=13, speech=14, items=15, weapon attack=16, weapon defense=17, soundclouds=18,
			                        		pre-hits=19, gui=20
mastergroup_group01..mastergroup_group30: defines to which mastergroup a group belongs (1=master_music, 2=master_sfx, 3=master_speech; default=2)

listener_mode:	0 = mixed  (orientation taken from camera, position taken from player; default)
		1 = camera (orientation and position taken from camera)
		2 = player (orientation and position taken from player)

volume_2d:	some soundcards play 2D sounds with an other volume then 3D sounds. you can match different 2D/3D volumes with this
		2D volume factor (in percent from 1..200; default = 100)
			1..99     = plays 2D sounds lower then 3D sounds (1..99 % of 3D volume)
			100       = plays 2D sounds with same volume as 3D sounds (100% of 3D volume)
			101..200  = plays 2D sounds with higher volume 3D sounds (101..200% of 3D volume)

zoom_falloff: volume changes while zooming in/out; only when listener is not set to camera)
		0 = off, 1 = on (default = 0)				

falloffpower: 3D falloff power - a higher value gives the sound more "3D feeling" (works w/ MILES only!)
		1..10 (default = 5)

hero_on_center:	all hero sound effects (footsteps, weapon/armor etc.) will be played on the center speaker
		instead of front left/front right (5.1 speakers or higher only; default = 0)

speech_commentary: how often are commentaries of player and NPCs played
	  0 = never
		1 = sometimes (default)
		2 = more often
		3 = very often

chat_notify: play a sound when a new chat message arrives
		0 = off, 1 = on (default = 1)

                     
*** THE FOLLOWING SOUNDOPTIONS ARE FOR HIGH QUALITY ONLY AND WILL BE IGNORED IN LOW QUALITY MODE ***

voices_3d:	max. num of 3D sound voices (default = 50)

system_sleep_ms:  update time for the soundengine in ms (default = 10)
plugin_update_ms: update time for the sound plugins in ms (default = 50)

obstruction_detection: detect sound obstructions (walls, crates, windows, doors) for more realistic soundscape
		0 = off, 1 = on (default = 1)

samplerate: mixer samplerate (11025, 22050, 32000, 44100 or 48000; default = 48000)

memorybudget: memory used used to cache sounddata in megabytes (1-255; default = 48)

====================================================================================================================================

