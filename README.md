## Lazarus3DS
A set of GodMode9 scripts to restore bricked 3DS consoles. Named after the [Lazarus Pit](http://dc.wikia.com/wiki/Lazarus_Pit) in DC Comics.

### Requirements
1. A method to boot GodMode9.firm, be that NTRBootHax, hard mod, or pre-installed hack.

2. The following files:
    1. Prepared donor `ctrnand.bin`, `nand_hdr.bin`, `twln.bin`, `twlp.bin` files & SHAs for your console (o3DS / n3DS + USA / EUR / JPN / CHN / TWN / KOR + retail / dev).
	   KOR, CHN, and TWN need different twln.bin files, as they require a different TWLFontTable, and in the case of CHN and KOR, a different DS Download Play client.

    2. A clean `sector0x96.bin`, `boot9strap.bin`, `sighax_hdr.bin` & SHA for your type of console (retail / dev).

    3. A copy of `twlmbr.bin` & SHA.
3. A copy of Luma3DS named as `luma.firm` & GodMode9 v1.4+ named as `boot.firm`.

### Setup
1. Copy the the files listed in Requirements (section 2) for your console type and region plus their SHA files to a folder on the root of your SD card called `pit`.

2. Copy `Lazarus3DS.gm9` to your `SD:/gm9/scripts/` folder.

4. Copy Luma3DS as `luma.firm` to the root of your SD card.

5. Copy GodMode9 as `boot.firm` to the root of your SD card.

### Instructions
1. Boot GodMode9 any method you can.

2. Press HOME, go to `Scripts` and run `Lazarus3DS`.

3. Provide input to unlock sysNAND writing and wait while the files are verified against their SHAs.

4. Once `Lazarus3DS` finishes the script will make Luma3DS the new boot.firm, copy Luma3DS to NAND, install boot9strap, remove all Lazarus3DS support files and restart the 3DS.

##### Notes
Consoles revived in this fashion will not be able to uninstall CFW without specially prepared CTRNAND images. Uninstalling CFW will render the console unable to boot once more.

To prepare a CTRNAND image to allow CFW uninstallation, properly signed files are needed for movable.sed, SecureInfo_A, and LocalFriendCodeSeed_B.

If you would like to create donor files for use with this script, please contact fox8091 on the [Nintendo Homebrew Discord](https://discord.gg/C29hYvh) for instructions.

##### Credits
Special thanks go to [d0k3](https://gbatemp.net/members/d0k3.29073/) for the splendid tool GodMode9 and intimate knowledge of the NAND layout and signature verifications, without which this wouldn't be possible.

Also thanks to [mvmiranda](https://gbatemp.net/members/mvmiranda.338095/) of GBATemp forums for being my first guinea pig and first successful resurrection by this script and [xeonhawk](https://gbatemp.net/members/xeonhawk.356731/) for n3DS and 3D testing on an emergency revived console.
