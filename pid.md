First up, let's calibrate PID. Yes, I know, you did that as part of the Setup Guide. But did you heat soak first? Yes? Good lad, move on. 

No you didn't? Keep reading.

Heat soaking is a really important process for enclosed printers, that matters even more the larger the printer is. You can find various guidance and advice on the Discord about soak times, but as an example I tend to soak my V0 for 30 minutes, and I soak my V2 300 for 90 minutes. This means setting target temperatures to where you want your bed and hotend to be, and leaving it sat there to heat up<sup>1</sup>.

Depending on your ambient temperature in the room, what temperatures you're heating to etc, you're likely to end up with a chamber temperature in the region of 40C - 50C. If you added a thermistor during your build to tell you this then you already know - if not then consider it, it's really useful information.

So now that you've heat soaked the printer, THEN run the PID calibration on your hotend and bed. I think there is marginal if any benefit in running it on the hotend, however it can absolutely affect your beds temperature accuracy.

Example: PID_CALIBRATE HEATER=extruder TARGET=250

Don't forget to save_config afterwards. It's annoying when you forget.




1. If you find that after a period of time your heaters set themselves to zero, you're probably reaching idle timeout in klipper. You can change this in printer.cfg (it's in seconds).
   [idle_timeout]
   # Timeout in seconds (Seconds to minutes example: 1200=20min / 3600=60min etc.)
   timeout: 2400
   
[Back](README.md)

Further reading: 
https://github.com/KevinOConnor/klipper/blob/master/docs/Config_checks.md
https://en.wikipedia.org/wiki/PID_controller
