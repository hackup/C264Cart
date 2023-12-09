# C264Cart

The C264Cart ist a modernized ROM cartrdige for the Commodore 264 familiy of 8-bit computers, the Commodore C16, C116, and Plus/4.

![C264Cart Rev.1](media/c264cart_rev1.jpg)

I started out by first reverse engineering and replicating the layout of an original ROM cartridge. Then I adapted it to better suit EPROMS and EEPROMS still easily available today like the W27C512 and W27C020. While the layout was also reduced in size in order to save shipping costs, it still fits the original cartidge shells.

See my [blog post](https://www.hackup.net/2023/12/making-cartridges-for-the-commodore-c16-c116-and-plus-4/) for more details.

I also created a simplified version of the original cartridge shells for 3D printing that goes well with the C264Cart. It is currently available for personal use on [Thingiverse](https://www.thingiverse.com/thing:6309306) and [Printables](https://www.printables.com/model/644139-commodore-264-cartridge-case-redux-for-c16-and-plu).


## Configuration Options

There are two things that need to be configured, the type of EPROM to be used and the size of the targeted ROM images. 

The C264Cart can be configured to support either 16k ROM images or 32k ROM images by setting JP6 and JP7 accordingly. 32k ROM images for the 264 computers usually consist of two 16k parts that were originally stored in two seperate ROMs. On the C264Cart in 32k mode, both parts go into the same EPROM with the upper part directly following the lower one. As a consequence, A14 cannot **not** be used for external bank switching in 32k mode. It is selected automatically by the cartridge.

If the C264Cart is configured for 16k mode R1, D1, and D2 don't need to be populated. These components are used in 32k mode, only.

The C264Cart supports 27C512, 27C020, and 27C040 (E)EPROMs. Make sure to always align those ICs to the top of the cartridge as indicated on the silkscreen and to properly configure jumpers JP4 and JP5!








## License

 **USE AT YOUR OWN RISK!**.

[![Creative Commons License](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)
](http://creativecommons.org/licenses/by-nc-sa/4.0/)

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/).
