---
Title: "Daydream Ottawa's organizer pcb"
Author: "Sophia"
Description: "Basically a sprig but with the bare rp2040 and ressembling a gameboy"
Created On: "21/8/2025"
---

# August 22nd: Basic plan

**Time: 1h**

(I'm journalling this retrospectively) I originally intended for this to be a rp2040 devboard, hence I started with that an began looking through some resources 
(mainly the rp2040 [datasheet](https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf) and [design](https://datasheets.raspberrypi.com/rp2040/hardware-design-with-rp2040.pdf) documents. This was researching session.

# August 31st: Back to work

**Time: 1.5h**

Had some personal stuff but now we're back and better than ever. I finalized my idea to basically be a version of the sprig, as there are already firmare and hundreds of pre-coded games!
The schematic is still quite lacking and there are a lot more specificities I need to figure out so that the sprig games will run on this. Some differences is I will be using 4.5 via 3 x AAA batteries and potentially have a larger display (not sure about this one).

My hierachial pages are still empty and the I haven't quite figured out how I want to flash this.
<img width="900" alt="image" src="https://github.com/user-attachments/assets/a691713b-f501-4e17-84c7-302e0b4d450f" />

# September 5th:
**Time: 0.5h**

I ended up switching to using a RT615BGQW (the pi pico uses the 3.3v version) and it'll provide 800mA which should be enough. 

# Sept 6-15th:
#### During the chunk from sept 6-15th I was working whenever I had some spare time and didn't even up documenting it (sorry reviewer!).

(M time was tracked in hackatime **~14h**, not including the many hours looking at datasheets and forgetting to run kicad-wakatime)

#### So here's a summary of all the things I did:
- Realized incorporating audio is too expensive
- After multiple iterations I settled on having 2xaaa batteries (3.0V) as the power source then having it converted to 3.3V via the TPS61230DRCR:

<img width="1001" height="280" alt="image" src="https://github.com/user-attachments/assets/f18d0c80-87b7-490b-9c62-c6f2ad01d8a2" />
^^ its really messy and will be cleaned up in the future

- Switched from the TK to W25Q16JVUXIQ as I realized I didn't need much storage (I copied this part from the pi pico): 
<img width="416" height="201" alt="image" src="https://github.com/user-attachments/assets/65495235-709f-481a-af56-32bbd7db9937" />

- Added all my peripherals:
<img width="780" height="418" alt="image" src="https://github.com/user-attachments/assets/0206caf1-104b-47e5-99c2-e4e89e5bd253" />

- Created a basic layout, very rough but it existed 

# September 16th:

**Time: 5.5h**

Lots of progress made:
- aligned buttons
- finalized the edge cut
- added silkscreen art/text
- followed the rp2040 hardware design guide for the pours under the mcu
- added additional gpio pin headers

<img width="800px" src="https://hc-cdn.hel1.your-objectstorage.com/s/v3/3da0cb02b2cf8298a052557a562a2c04a3dd823a_1.png">
(i realize the angle is weird)

# September 17th:

**Time: 3h**

- made a footprint for the inductor
- made footprint for the ST7735 (with help from the sprig) and realized my schematic was completely wrong (it was for the microsd card version of this display)
- finalized the placements
- temporarily removed the test points
- added silk screen art
- realized I don't need mounting holes (I may go back on this)
- found footprints for all the remaining power section components and routed all of those
- found all lcsc parts

I finally finished this. Well mostly. 

Before I finalize this i'll change the font, finalize the silkscreen art, clean up the schematic, make silkscreen text consistent and clear, check all my datasheets, add in test points, verify all my lcsc parts and hope.

<img height="700" alt="image" src="https://github.com/user-attachments/assets/3a69bec0-ecc8-496c-a16f-7b6918fea5ac" />
<img height="700" alt="image" src="https://github.com/user-attachments/assets/4aee7987-b861-4f27-8509-1c2532564ead" />

