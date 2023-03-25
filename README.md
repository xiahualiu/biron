# biron

Biron is an open source soldering iron hardware based on Baxandall Oscillator. This is a homebrew project that I am doing during the free time at home.

## Software Requirements

* KiCAD v7.0.0 or above to view the schematic and PCB files.
* LTSpice 17.1.6.0 or above to view the SPICE simulation.

## Disclaimer

This is an open source project that involves high voltage and hot surfaces. You must have enough experience to build it in real life and wear PPE, I don't want people get hurt.

![result](https://user-images.githubusercontent.com/49677912/217614569-726dd97b-1ab7-452a-995a-8929e3cdaac0.png)

![image](https://user-images.githubusercontent.com/49677912/227742764-72126fb5-3cbf-455f-9290-d98be726c441.png)

![image](https://user-images.githubusercontent.com/49677912/227742811-0678681f-8cdf-427c-a5b6-fb92b0f3e117.png)

This project follows the Ti's [DAQ system requirements](https://www.ti.com/solution/data-acquisition-daq), the control system is fully galvanized isolated from the physical and power signals.

![image](https://user-images.githubusercontent.com/49677912/227743218-670e518b-6d94-4211-ab95-7ef33206d251.png)

### Power isolation

I used a minimal push-pull converter for the DC/DC part:

![image](https://user-images.githubusercontent.com/49677912/227743017-2968dbc7-d50a-410b-9b91-1439948330e1.png)

### Sensor signal isolation

Sensor signals are amplifier through a TL082H (not practical in the real world because of the high Vos, you want Vos<100uV if possible). The signal is read by a RV1S9353A from Renasas.

![image](https://user-images.githubusercontent.com/49677912/227743113-4e1a8014-fca3-4c39-b6d4-6a0e95e7fdf3.png)
