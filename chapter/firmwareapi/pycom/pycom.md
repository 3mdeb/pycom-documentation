# class pycom – Pycom Device Features
The pycom module contains functions to control specific features of the pycom devices, such as the heartbeat RGB LED.

### Quick Usage Example

```python
import pycom

pycom.heartbeat(False)  # disable the heartbeat LED
pycom.heartbeat(True)   # enable the heartbeat LED
pycom.heartbeat()       # get the heartbeat state
pycom.rgbled(0xff00)    # make the LED light up in green color
```

### Functions

<function>pycom.heartbeat([enable])</function>

Get or set the state (enabled or disabled) of the heartbeat LED. Accepts and returns boolean values (True or False).

<function>pycom.rgbled(color)</function>

Set the colour of the RGB LED. The color is specified as 24 bit value representing red, green and blue, where the red colour is represented by the 8 most significant bits. For instance, passing the value ``0x00FF00`` will light up the LED in a very bright green.

<function>pycom.nvs_set(key, value)</function>

Set the value of the specified key in the NVRAM memory area of the external flash. Data sored here is preserved across resets and power cycles. Value can only take 32-bit integers at the moment. Example:

```python
import pycom

pycom.nvs_set('temp', 25)
pycom.nvs_set('pulses', 10)
```

<function>pycom.nvs_get(key)</function>

Get the value the specified key from the NVRAM memory area of the external flash. Example:

```python
import pycom

pulses = pycom.nvs_get('pulses')
```
