# Toaplan v2 / Raizing MiSTer Cores

This project contains the MiSTer core for Raizing boards operating on the Toaplan v2 board platform.


## Supported Games

| Title                                                                                                                 | Status        | Additional Information   |
|-----------------------------------------------------------------------------------------------------------------------|---------------|--------------------------|
| [**Armed Police Batrider**](https://en.wikipedia.org/wiki/Armed_Police_Batrider)                                      | Public        |                          |
| [**Battle Bakraid**](https://en.wikipedia.org/wiki/Battle_Bakraid)                                                    | Public        |                          |
| [**Battle Garegga**](https://en.wikipedia.org/wiki/Battle_Garegga)                                                    | Public        |                          | 
| [**Kingdom Grandprix / Shippu Mahou Daisakusen**](https://en.wikipedia.org/wiki/Kingdom_Grand_Prix)                   | Public        |                          | 
| [**Sorcer Striker**](https://en.wikipedia.org/wiki/Sorcer_Striker)                                                    | Public        |                          |
| [**Batsugun**](https://en.wikipedia.org/wiki/Batsugun)                                                                | N/A           | MCU: NEC V25             |
| [**Dogyuun**](https://en.wikipedia.org/wiki/Dogyuun)                                                                  | N/A           | MCU: NEC V25             |
| [**FixEight**](https://en.wikipedia.org/wiki/FixEight)                                                                | N/A           | MCU: NEC V25             |
| [**Ghox**](https://en.wikipedia.org/wiki/Ghox)                                                                        | N/A           | MCU: Hitachi HD647180    |
| [**Grind Stormer / V-Five**](https://en.wikipedia.org/wiki/Grind_Stormer)                                             | N/A           | MCU: NEC V25             |
| [**Knuckle Bash**](https://en.wikipedia.org/wiki/Knuckle_Bash)                                                        | N/A           | MCU: NEC V25             |
| [**Pipi & Bibis / Whoopee!!**](https://en.wikipedia.org/wiki/Pipi_%26_Bibi%27s)                                       | N/A           |                          |
| [**Snow Bros. 2 / Otenki Paradise**](https://en.wikipedia.org/wiki/Snow_Bros._2:_With_New_Elves)                      | N/A           |                          |
| [**Teki Paki**](https://en.wikipedia.org/wiki/Teki_Paki)                                                              | N/A           | MCU: Hitachi HD647180    |
| [**Truxton II / Tatsujin Oh**](https://en.wikipedia.org/wiki/Truxton_II)                                              | N/A           |                          |


## Development

This core uses JTFrame, however, I have only utilized the template of JTFrame as I do not use linux. I added some stuff to it, but fairly minimal.
Upgrading for the most part is a matter of dropping in the latest release in modules.

To compile the cores, I have included separate qsf files for each core. There are a total of 3 cores entitled bakraid, batrider and garegga.

The garegga core will play Sorcer Striker & Kingdom Grandprix as well.

It is a matter of loading up the project in quartus, and synthesizing/ building to get the rbf which you can put on your sd card for MiSTer.

Note:
- the JT9346 I have in Bakraid is not compatible with 93C66 chips, I made some changes to make it compatible.
- the YMZ280b module comes from Nullobject, I have isolated and generated the module as standalone in scala, which emits verilog. No changes.
## License

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.
