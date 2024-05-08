## Adafruit S-35710 Low-Power Wake Up Timer Breakout - STEMMA QT / Qwiic PCB

<a href="http://www.adafruit.com/products/5959"><img src="assets/5959.jpg?raw=true" width="500px"><br/>
Click here to purchase one from the Adafruit shop</a>

PCB files for the Adafruit S-35710 Low-Power Wake Up Timer Breakout - STEMMA QT / Qwiic. 

Format is EagleCAD schematic and board layout
* https://www.adafruit.com/product/5959

### Description

The Adafruit S-35710 Wake Up Timer is a low power 'watchdog timer' chip that can be programmed to alert with a digitally-configurable alarm from 1 second up to 194 days, thanks to a 24-bit second counter. It's an interesting alternative to a real time clock or internal sleep timer and might be useful for some ultra-low-power projects that want to have a separate (and possibly separately-powered) chip to handle time-keeping and alarms. We covered this component on EYE ON NPI and thought it would make for a nice breakout in the shop.

Usage is pretty simple: on I2C write of the timer register, the chip starts counting from 0 seconds up and the OUT pin goes high. When the count matches the timer register, the OUT pin goes low. Simple, and like we mentioned, it's very low power, drawing only 0.2uA. The output is open-drain, and if you want to have it be inverted, there's a switch that will put the signal through an N-channel FET so the polarity goes the other way.

One thing to note, is that on power-up the OUT line is default low, which means its not good for a low-power sleep manager, only for watch-dog-like timings. That is to say, you cannot connect this to your microcontroller's reset or enable line to self-depower because it will be disabled/reset when powered up. Still, maybe a useful chip for some folks who want to signal after a long delay or have a more complex power management scheme.

To get you going fast, we spun up a custom-made PCB in the STEMMA QT form factor, making it easy to interface with. The STEMMA QT connectors on either side are compatible with the SparkFun Qwiic I2C connectors. This allows you to make solderless connections between your development board and the S-35710 or to chain it with a wide range of other sensors and accessories using a compatible cable.

### License

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from [Adafruit](https://www.adafruit.com)!

Designed by Limor Fried/Ladyada for Adafruit Industries.

Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution. 
See license.txt for additional details.
