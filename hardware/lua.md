# LUA on rusEFI Proteus

### As of 2021 a popular open source Lua scripting engine.
### Some ECUs (EGS, ABS/ASC) in my BMW 8-series need a PWM (100Hz) modulated throttle signal to work error free. LUA gives us the possibility to realize it.

How is LUA configured now? Here are the necessary steps:
- assign output
- set PWM frequency and initial duty cycle
- update duty cycle in event

```Lua
startPwm(0, 100, 0) -- starts PWM on output #0 (check TunerStudio) with 100Hz and initial duty cycle o 0%
```

```Lua
function onTick()
    pedalPosition = getSensor("Tps1") -- get actual value of Tps1
    print('pedal position: ' ..pedalPosition) -- do some output
    setPwmDuty(0, pedalPosition) -- set duty cycle. the correct value is between 0 (= 0%) and 1 (100%)
end
```