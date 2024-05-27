# Telescope Setup & Calibration

1. **Initialize camera** - on Sleipnir the Slow, open Evora (`http://localhost/` on Sleip, or `http://72.233.250.83/` elsewhere on the network). 
	1. [ ] Initialize and set temperature to **-82° C**. 
	2. [ ] Press 'Home' on the filter wheel. 
2. **Initialize telescope** - open Bifrost on Heimdall. 
	1. [ ] 'Initialize telescope systems'
	2. [ ] Make sure control paddle is set to `set` not `slew`
	3. [ ] Turn telescope on with key on RA skirt in dome
		1. [ ] Confirm 4 green lights in / around mount
3. [ ] **Slew to zenith** - use bubble level and hand paddle to bring scope to zenith.
	1. [ ] 'Load Zenith Coordinates' on Bifrost once this is done, then 'Update Telescope Coordinates'

Wait till sunset now. 
1. [ ] **Open dome**
	1. Unclip dome power cables
	2. Plug in 3-prong lower shutter door motor, and round upper-shutter motor cable (note the upper-shutter cable has a specific orientation to follow). 
	3. Raise upper shutter until the lower shutter motor turns on. Continue raising upper shutter, but you can now open the lower shutter. 
	4. Once both are fully open, re-clip power cables where they were. 
2. [ ] **Remove telescope covers**
	1. Make sure telescope is at zenith with correct RA/DEC in Bifrost
	2. 'Slew to Cover Position' in Bifrost - *watch telescope cables*. Emergency stop if it looks like anything's going to get caught. 
	3. Use the ladder to remove the main telescope cover & the 6" finder cover. Store both on south table. 
3. [ ] **Take bias exposure** 
	1. It should look [similar to this example bias](images/bias_example.png).
4. [ ] **Take twilight flats**
	1. Move the telescope ~20 degrees east of zenith (west for morning flats)
5. [ ] **Calibrate pointing**
	1. Load `pointing_stars.txt` in Bifrost and select a bright start with a low airmass. 
	2. Turn on tracking, slew to the star and then try to center the star in the finderscope manually with the Xbox remote. Click 'Update Pointing to Target' once it's lined up.
	3. Check another bright star nearby to be sure. Fine-tune to get to center-ish of FoV. 
6. [ ] **Calibrate focus** - use a dimmer star for this one
	1. Goal is to *minimize* star PSF. Use focus helper in Evora for this - large leaps in focus increments on Bifrost are okay.
	2. *Remember*: **focus is a relative measurement** on the telescope, not absolute - "zero" focus is physically wherever the focus was when Bifrost booted up.

## End-of-night
**If dome flats needed**: close dome, turn on dome flat light and point telescope at a relatively matte / flat area. Take flats as needed, then follow procedure below. 

1. [ ] Shutdown Evora.
2. [ ] **Attach covers**
	1. 'Slew to Cover Position' in Bifrost, then replace covers. **Pay attention to cables**.
	2. 'Park Telescope' to slew back to zenith
3. [ ] Turn off the telescope with the key, then close Bifrost.
4. [ ] **Close dome**
	1. Rotate dome so cables are near ports
	2. Plug cables in - close smaller shutter (3-prong plug) first, followed by upper shutter
	3. After dome is closed, unplug and reclip cables. 

## Calibration Frames

| **Frame type** | **Details**                                                                                            | **Exptime** | **Num**             | **Periodicity** |
| -------------- | ------------------------------------------------------------------------------------------------------ | ----------- | ------------------- | --------------- |
| **Bias**       | Readout noise on CCD - 'static' you see on low exposure times.                                         | 0           | 50-100              | Few weeks       |
| **Flat**       | Help mitigate effect of dust and lens vingetting on lights - also acts as per-pixel correction factor. | 1-50        | ~50                 | Every run       |
| **Dark**       | Try to capture noise from temp and ISO over length of exposure time.                                   | LIGHTs      | At least 5, ~20/exp | Every new exp   |

**Notes**:
- Bias frames are filter-irrelevant
- Flat frames are filter-specific - 1 every 5 exptime steps should work
- Rerun darks every once in a while  - build a library with ISO, temp and exptime