# skate.community

This is the supplemental web service used by Skate3. It is used for Skate Parks/Replays/Feed/Teams.

## WCF Pages

These are services that allow for both SOAP HTTP and WCF HTTP requests, but Skate3 does not make use of the SOAP part.

* SkateDLC.asmx
* SkateFeed.asmx
* SkateProfile.asmx
* SkateReel.asmx
* SkateStats.asmx
* SkateTeam.asmx

Endpoints:

* http://downloads.skate.online.ea.com/skate3/webkit/PS3/English/i/Sessions/LogOn
* http://downloads.skate.online.ea.com/skate3/webkit/XBL2/English/i/Sessions/LogOn
* http://downloads.skate.online.ea.com/skate3/ws/SkateProfile.asmx
* http://downloads.skate.online.ea.com/skate3/ws/SkateReel.asmx
* http://downloads.skate.online.ea.com/skate3/ws/SkateDLC.asmx
* http://downloads.skate.online.ea.com/skate3/ws/SkateFeed.asmx

Config Endpoints:

* http://downloads.skate.online.ea.com/skate3/config/PS3.xml
* http://downloads.skate.online.ea.com/skate3/config/XBL2.xml

Url format:
`${BASE_URL}/skate3/${USER}/${PLATFORM}/${LANGUAGE}/${UNITS}/Sessions/GameLogin/${SESSION}/leaderboards`

CAS stands for "Create a Spot"

Platform URL may be `PS3F` instead of `PS3` for flipped layout buttons? (same for xbox `XBL2F` and `XBL2`)

Upload TypeId:

* 1 video
* 2 photo
* 13 skate park

Input button names:

* dpad_up_button
* dpad_down_button
* dpad_left_button
* dpad_right_button
* start_button
* select_button
* fake_cross_button
* cross_button
* triangle_button
* square_button
* fake_circle_button
* circle_button
* l1_button
* r1_button
* r2_button
* l2_button

Custom javascript functions:

* EA.ResetCursor - same as update nav?
* EA.MessageBox - opens a native message box
* EA.TagInputs - tells browser to re look at inputs?
* EA.UpdateNav - resets navigation (paginate)
* EA.PlayAudio - plays a sound
