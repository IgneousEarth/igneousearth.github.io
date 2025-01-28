> In a nutshell, the LVM is a spectroscopic survey of the Milky Way, Magellanic Clouds and local volume galaxies connecting pc-scale individual sources (stars and galaxies) to kpc-scale ISM properties - i.e. interstellar gas to sources.
> 
> "The 4-year survey covers the southern Milky Way disk at spatial resolutions of 0.05 to 1 pc, the Magellanic Clouds at 10 pc resolution, and nearby large galaxies at larger scales"

## Telescope Hardware

- Covered by a giant removable roof
- Four telescopes "sideroscopes" (SkyW, Sci, Spec, SkyE) connected to 4 spectrographs through a "sorting hat".
	- Set of optical fibers connected to an optical table which is assembled into a unified image via the IFU and AG, then sent via 

## The Job

Monitor telescope hardware and make sure it looks okay - make sure dome closes okay. 

- Overwatcher uses GORT to manage telescope (i.e. check weather, go to next tile, etc. a early-phase robot to replace humans)
- lvm-web displays info from Overwatcher and its subsystems, night logs, GORT logs etc

## Each night

1. Calibrate with twilight flats -> 30 mins after sunset -> quick cals using interior lamps w/ particular elements -> biases (electronic noise)
2. Open dome maybe 5 mins before twilight ends
3. **Start sequence**
	1. Get next tile from scheduler
	2. Focus telescopes (each hour to compensate for temp)
	3. Slew telescopes (2x guide cams to make sure looks ok)
	4. Acquire fields
	5. Expose (15 mins)
	6. Repeat (during readout)
4. Close dome at end of night
5. Send night log