# IRTransceiver

A [Pmod](https://reference.digilentinc.com/reference/pmod/start) for emitting and receiving baseband IR signals.
It can be used to decode and emulate IR remote controls, IR communication or other IR-based sensors.

![IR Transceiver Pmod Image](docs/module.jpg)

This module contains simple analog signal conditioning circuitry to connect a LED and a photodiode to FPGAs or microcontrollers.
The digital interface consists of just two wires, an input and an output.
If the input is high, the IR LED is on.
If the photodiode receives a stronger-than-average IR light, the output is pulled high.
The nominal supply voltage is 3.3V.

The IR LED is driven by a simple MOSFET.

The receiver contains a transimpedance amplifier, a high-pass filter and comparator to produce a clean digital signal.
The high-pass rejects ambient light along with signals slower than about 10 kHz, the usable bandwidth is about 100 kHz.
The receiver circuit was inspired by [IRis](https://github.com/devttys0/IRis).


