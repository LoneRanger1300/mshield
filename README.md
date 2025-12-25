
# Siyeenove mShield extension

![](/image.jpg/)

> Open this page at [https://siyeenove.github.io/pxt_mshield/](https://siyeenove.github.io/pxt_mshield/)

This library is designed to drive mShield, You can get mShield here:   

[Buy](https://www.amazon.com/dp/B0FQ5ZP1GW)    
[SIYEENOVE](https://siyeenove.com/buy/)   

Product Tutorial: 

[SIYEENOVE](https://siyeenove.com/tutorial/)    
[Github PDF](https://siyeenove.github.io/M1E0002/mShield%20Tutorial%20-%20English%202025-10-14.pdf)   

## Code Example

```JavaScript
// Motor1 runs clockwise at full speed.   
mShield.setMotorsDirectionSpeed(mShield.Motors.Motor1, mShield.MotorsDirection.CC, 100)   
```

```JavaScript
//Set the speed and direction of motor1 and motor2 of mShield.   
mShield.setMotorsSpeed(-100, 100)   
```

```JavaScript
//Set mShield motor1 and motor2 to stop.    
mShield.wheelStop(mShield.Motors.AllMotors)    
```

```JavaScript
//When the speed of the motors of the mShield board is inconsistent due to hardware reasons, 
//this function adjusts the speed of the motors and is permanently stored inside the mShield.    
mShield.motorsAdjustment(0, 0)    
```

```JavaScript
//Light all the leds of the mShield board.     
mShield.setLed(mShield.Leds.AllLED, true)    
```

```JavaScript
//Read and display the value of the "OK" key of the infrared remote control.     
mShield.irCallBack(function () {
    if (mShield.irButton(mShield.MshieldIrButtons.OK)) {
        basic.showNumber(mShield.irValue())
    }
})    
```

```JavaScript
//Set S1 to S4 pin to PWM mode.    
mShield.setS1ToS4Type(mShield.S1ToS4Type.PWM)

basic.forever(function () {
    //The pulse width of pins S1 to S4 is set to 200.
    mShield.extendPwmControl(mShield.PwmAndServoIndex.All, 200)
})    
```

```JavaScript
//Set S1 to S4 pin to servo mode.    
mShield.setS1ToS4Type(mShield.S1ToS4Type.Servo)

basic.forever(function () {
    //Set the 180° servo Angle from S1 to S4 pins to 0.
    mShield.extendServoControl(mShield.PwmAndServoIndex.S1, mShield.ServoType.Servo180, 0)
    basic.pause(1000)

    //Set the 180° servo Angle from S1 to S4 pins to 180.
    mShield.extendServoControl(mShield.PwmAndServoIndex.S1, mShield.ServoType.Servo180, 180)
    basic.pause(1000)
})   
```

```JavaScript
//Set S1 to S4 pin to servo mode.    
mShield.setS1ToS4Type(mShield.S1ToS4Type.Servo)

basic.forever(function () {
    //Set the 360° servo of pins S1 to S4 to run forward at full speed.
    mShield.continuousServoControl(mShield.PwmAndServoIndex.All, 100)
    basic.pause(1000)

    //Set the 360° servo of pins S1 to S4 to run backward at full speed.
    mShield.continuousServoControl(mShield.PwmAndServoIndex.All, -100)
    basic.pause(1000)
})   
```

```JavaScript
//Set mCar external 3 AA batteries, and infinite loop display power level.
basic.forever(function () {
    basic.showNumber(mShield.batteryLevel(mShield.BatteryType.AA3))
    basic.pause(1000)
})
```

```JavaScript
//Read the firmware version of the chip on the mShield.
basic.forever(function () {
    basic.showString(mShield.readVersions())
    basic.pause(1000)
}) 
```

## Supported targets

* for PXT/microbit

## License

* MIT



> Open this page at [https://loneranger1300.github.io/mshield/](https://loneranger1300.github.io/mshield/)

## Use as Extension

This repository can be added as an **extension** in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **New Project**
* click on **Extensions** under the gearwheel menu
* search for **https://github.com/loneranger1300/mshield** and import

## Edit this project

To edit this repository in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **Import** then click on **Import URL**
* paste **https://github.com/loneranger1300/mshield** and click import

#### Metadata (used for search, rendering)

* for PXT/microbit
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
