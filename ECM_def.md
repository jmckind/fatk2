# ECM Format Definition
```
[brent's_relocatable_format]
    byte 9                      ; Probably denotes an ECM device
	ptr si_names                ; Points to the name structure at the bottom.
    word 1                      ; Jammer Weight
    byte $0                     ; Is this a spacer?
    word $0                     ; 16 - Jammer Installed
                                ; 256 - IR Jammer
                                ; 32 - CW Jamming
                                ; 64 - Pulse Jamming
                                ; 128 - Frequency Hop Jamming
    byte 0                      ; Chaff Count
    byte 0                      ; Chaff Spoof Chance
    byte 0                      ; Chaff Launch Angle (hex) 90 = 99?
    byte 0                      ; Chaff Launch Pitch (hex) 45 = 49?
    byte 0                      ; Flare Count
    byte 0                      ; Flare Spoof Chance
    byte 0                      ; Flare Launch Angle (hex) 100 = 71?
    byte 0                      ; Flare Launch Pitch (hex) 45 = 31?
    byte 30                     ; Radar Jammer Missile Miss Percent
    word 100                    ; Radar Jammer Increase to RCS
    byte 0                      ; Radar Jammer Max Detect Cone
    byte 0                      ; Radar Jammer Min Detect Cone
    byte 40                     ; IR Jammer Missile Miss Percent
    word 100                    ; IR Jammer Increase to ICS
    byte 0                      ; Lock Loss Time
:si_names
	string "INTERNAL_NAME"      ; Object's Internal Name
	string "DESCRIPTION"        ; Description of the Jammer
	string "OBJECT.ECM"         ; Object Name
	end
```
