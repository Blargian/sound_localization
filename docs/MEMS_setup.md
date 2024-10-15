# MEMS setup

The STM32F746G-DISCO board has two [IMP34DT05TR](https://www.st.com/resource/en/datasheet/imp34dt05.pdf) MEMS microphones:

From sheet 6 of the [hardware schematic](https://www.st.com/content/ccc/resource/technical/layouts_and_diagrams/schematic_pack/group1/ff/cd/ce/2d/f8/fb/40/69/mb1191-F746NGH6-C01_schematic/files/mb1191-F746NGH6-C01_schematic.pdf/jcr:content/translations/en.mb1191-F746NGH6-C01_schematic.pdf):

<img width="620" alt="image" src="https://github.com/user-attachments/assets/b40e5645-7741-44d5-9dea-a0eb6ce6c2a5">

- U20 has the L/R pin connected to VDD via a 10K resistor.
- U21 has the L/R pin pulled low.

  The L/R pin is used to choose on what edge of the clock the microphone will provide data (see [page 12 of imp34dt05 datasheet](https://www.st.com/resource/en/datasheet/imp34dt05.pdf)).
  > L/R pulled high = right configuration = data is provided on the falling edge of the clock.
  > L/R pulled low = left configuration = data is provided on the rising edge of the clock.

  <img width="568" alt="image" src="https://github.com/user-attachments/assets/974019d6-0d27-4ca0-9b22-17215e96d4ac">
