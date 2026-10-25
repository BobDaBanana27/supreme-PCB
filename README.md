# supreme-PCB
For Hack Club Half-Life
# PCBs – devlog

| Week | Tier | Hours logged | Entries |
| --- | --- | --- | --- |
| Week 1 | Tier 1 | 7h | 1 |

## Contents

The first hour consisted of nothing much but research into parts and fitting within the budget. I ended up settling on these parts, as seen in the image below. Hours 2-5 all consisted of working inside KiCad to build and test the PCB. For the PCB layout file, I built out a standard 1.6 mm thick board on an A4 sheet using KiCad. On the board, I used a USB-C connector for power and data, the RP2040-Zero as the computer, a couple of rotary encoders for dial controls, six tactile switches for the macro buttons, and an OLED display for visuals. To wrap up the power side, I added a 3.3V regulator along with its supporting components.

![image](https://halflife.hackclub-assets.com/hackclub-half-life/sessions/fpT4vKaaCxCaCu9yi3OynxGXkAPlXNzI/6f6c4dfe9877947a67334e78a8016a9e2e59694b699146eea5d5d6ef5e32cd97.png)

![image](https://halflife.hackclub-assets.com/hackclub-half-life/sessions/fpT4vKaaCxCaCu9yi3OynxGXkAPlXNzI/93a04b6a166d99aa3f422c3f152267bc2e179c4ca4b10abdc4310f4e8baa8d09.png)

 I set standard DRC rules in the project config file. Tracking a minimum of 0.2 mm, zero clearance, and 0.5 mm spacing from the board edge, while the default net class runs 0.2 mm tracks, 0.2 mm clearance, and uses 0.3 mm drill / 0.6 mm outer diameter vias to tie everything smoothly over to the main schematic file.

![Screenshot 2026-10-11 160624](https://halflife.hackclub-assets.com/hackclub-half-life/sessions/fpT4vKaaCxCaCu9yi3OynxGXkAPlXNzI/4c7cdf34164fe4e972d7a2daa708bbf860bafa7a202dcf0d747f8744ce3f6a61.png)

![Screenshot 2026-10-11 160720](https://halflife.hackclub-assets.com/hackclub-half-life/sessions/fpT4vKaaCxCaCu9yi3OynxGXkAPlXNzI/2cc6d7211c2b3fea3882ae8ba731cb5db89edd55aa4cb6c8a5f48306939f7ee6.png)

![Screenshot 2026-10-11 160901](https://halflife.hackclub-assets.com/hackclub-half-life/sessions/fpT4vKaaCxCaCu9yi3OynxGXkAPlXNzI/1dfe3e6964fd4cb2ba128cb11ae9a6c754b691c5bd50ee433e9e26a79b25ed38.png)

For the schematic, I split the layout into neat, manageable blocks covering USB power and regulation, the RP2040 controller, custom buttons, rotary dials, and a status display. Finally, I wired up all the key nets, including VBUS, +3V3, GND, the button lines, the encoder pins, ENC1_PUSH, and the I2C bus lines.

![image](https://halflife.hackclub-assets.com/hackclub-half-life/sessions/fpT4vKaaCxCaCu9yi3OynxGXkAPlXNzI/ae1d1c89df665b954f870a3923c5b0633365344cbadc82800cf47d374276b1a0.png)


EDIT: The image at the top **is** the final PCB.
