# Shower Duration Watch

The automations for this functionality make use of the following helpers:

- **input_datetime.shower_start** (to capture the timestamp indicating the beginning of the shower)
- **input_datetime.shower_end**   (to capture the timestamp indicating the end of the shower)
- **timer.shower_duration_1**     (time after which the light in the bathroom will change from green to orange)
- **timer.shower_duration_2**     (time after which the light in the bathroom will change from orange to red)
- **timer.shower_duration_3**     (time after which the light in the bathroom will change from red to flashing red)

These helpers are all created via Configuration > Helpers

Furthermore, the following items are required:

 - A flood sensor attachted to the shower head (see attached pictures) that will indicate when the shower is on or off.
   In my case, I am using a Fibaro Flood Sensor for this.
   
   Name entity_id used in my automations: **binary_sensor.bathroom_flood_sensor**
 
 - A media player to broadcast the duration of the shower

   Name entity_id used in my automations: **media_player.sonos_bathroom**
   
 - A light to signal the duration of the shower

   Name entity_id used in my automations: **light.bathroom**
 
 - A TTS platform the broadcast the duration of the shower.

   I am using the TTS platform integrated in Home Assistant (Configuration > Home Assistant Cloud > Text to Speech) 
 
 _In case you are using other entity_ids for the abovementioned items, simply find & replace them in my automations.
 In case another TTS service is used, change the name of the service used in my automations **(tts.cloud_say)** to the service your TTS platform is using._
