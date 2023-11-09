#imports go at the top
from microbit import *
from ssd1306 import clear_oled
from ssd1306n import initialize
from ssd 1306_text import add_text

def read_temperature():
    temperatire1 = temperature()
    if temperature > 25:
       pin8.write_digital(1)
    else:
        pin8.write_digital(0)

def read_light():
    light1 = pin0.read_analog()
    pin1.write_analog(1023 - light1)
def write_temp_light():
    temperature1 = temperature()
    light1 = pin0.read.analog()
    add_text(2,1,str(light1))
    add_text(2,2,str(temperature1))
    sleep (500)

while true:
    initialize()
    clear_oled
    motion = pin2.read.digital()
    if motion == 1
     read_temperature()
     read_light(
   write_temp_light
     )
