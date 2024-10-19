# Lua on rusEFI Proteus

## As of 2021 rusEFI uses a popular open source Lua scripting engine, see [rusEFI documentation](https://github.com/rusefi/rusefi/wiki/Lua-Scripting)

## Some ECUs (EGS, ABS/ASC/MSR) in my BMW 8-series need a PWM (100Hz) modulated throttle position signal to work error free. Lua gives us the possibility to realize it

How is Lua configured now? Here are the necessary steps

- assign output
- set PWM frequency and initial duty cycle
- update duty cycle in event

### Assign Lua output, go for "Advanced" -> "Lua Script PWM Outputs"

![alt text][lua_outputs]

### set PWM frequency and initial duty cycle

```Lua
startPwm(0, 100, 0) -- starts PWM on output #0 (check TunerStudio) with 100Hz and initial duty cycle of 0%
```

### update duty cycle in event

```Lua
function onTick()
    local pedalPosition = getSensor("AcceleratorPedal") -- get actual value of AcceleratorPedal, should by between 0 and 100
    pedalPosition = (pedalPosition == nil and 'invalid pedalPosition' or pedalPosition)
    local pwmValue = pedalPosition / 100
    setPwmDuty(0, pwmValue) -- set duty cycle. the correct value is between 0 (= 0%) and 1 (100%)
    print('pedal position: ' .. pedalPosition .. ' duty cycle ' .. pwmValue) -- do some output
    print('')
end
```

### Whole code  

```Lua
startPwm(0, 100, 0) -- starts PWM on output #0 (check TunerStudio) with 100Hz and initial duty cycle o 0%

function onTick()
    local pedalPosition = getSensor("AcceleratorPedal") -- get actual value of AcceleratorPedal, should by between 0 and 100
    pedalPosition = (pedalPosition == nil and 'invalid pedalPosition' or pedalPosition)
    local pwmValue = pedalPosition / 100
    setPwmDuty(0, pwmValue) -- set duty cycle. the correct value is between 0 (= 0%) and 1 (100%)
    print('pedal position: ' .. pedalPosition .. ' duty cycle ' .. pwmValue) -- do some output
    print('')
end
```

[lua_outputs]: ./pictures/lua_outputs.jpg "lua outputs"
