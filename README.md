# RPi-Pico-Baremetal

Do you pine for the nice days of 8-bit microcontrollers, when men were men and wrote their own device drivers?


Tips:
- Use a Raspberry Pi with Raspbian as your development machine. Most official guides are tested on Raspbian, so you may not find any issues on your Linux environment. 
    -  By using Microsoft Visual Studio Code with the Remote SSH extension on your Destop PC, you can work remotely on the source code and flash the Pico on the Raspberry Pi (via SSH).
- The UF2 converter provided in the pico-sdk follows a strict memory map. As I'm not usiong the linkler script used on the SDK, sometimes my elf file did not fulfill the converter restrictions. For that reason I searched for another open source UF2 converter and found the one from Microsoft.
- Serial port:
    - When working with serial port with RPI4, use "sudo raspi-conmfig" -> 3 Interfaces Options -> I6 Serial port to disable shell messages on the serial port and to enable it.
    - if still there is unwanted data on the RPI4 serial port, then disable the following services: "sudo systemctl disable serial-getty@serial0.service"

References:
- Raspberry Pi
    - Github
        - https://github.com/raspberrypi/pico-sdk
        - https://github.com/raspberrypi/pico-examples
        - https://github.com/microsoft/uf2
    - Documentation
        - https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf
        - https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf
- ARM
    - Documentation
        - https://developer.arm.com/documentation/ddi0484/latest
        - https://developer.arm.com/documentation/dui0662/b/The-Cortex-M0--Processor
- UF2
    - Covenrter
        - https://github.com/microsoft/uf2
- ASCII art: https://manytools.org/hacker-tools/ascii-banner/
