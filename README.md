# Clock Divider (type 2)

```
      ----  ----  ----  ----  ----  ----  ----  ----  ----
IN    |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
    ---  ----  ----  ----  ----  ----  ----  ----  ----  ---
      ----              ----              ----
OUT   |  |              |  |              |  |
n=3 ---  ----------------  ----------------  ---------------
```

This clock divider takes a regular clock signal and generates one pulse every `n` input steps. A knob allows you choose `n` between 1 and 10. Combine this with the [binary clock divider](https://www.github.com/thismatters/EurorackClockDiv/) in my series to generate many permutations on a clock signal.

The circuit here is based on the [Yusynth Clock Divider](https://yusynth.net/Modular/EN/DIVIDER/index.html) with minor tweaks to make it more Eurorack friendly. The changes I've made are thus:
* Selected resistors appropriate for +/-12V rails,
* Added polarity protection so that a backward power header doesn't fry anything (twin series schotty diodes: BAT54SL),
* Full surface mount design,
* More step options!

The Yusynth page is a treasure trove of information about this circuit that I am too amateur to claim as my own; please read that outstanding page before using this circuit. The page provides many details and other implementations of this circuit that you may find suitable.

The KiCAD project here uses the library/footprints [found in my companion repo](https://github.com/thismatters/EurorackKiCAD).


## Width

10hp on a 1u rack (Intellijel).

## Inputs

Jacks:
- Clock input
- Reset gate

Knobs:
- 10 position switch for choosing the frequency of gate outputs

## Outputs

Gate output. LED indicator.

## Vendors

There are part numbers in the [BOM](clkdiv2.csv) for many of the parts (not for basic passives though) at the following vendors:

* [Mouser](https://www.mouser.com): Needs no introduction. Get your ICs from here (or [digikey](https://www.digikey.com)).
* [Tayda Electronics](https://www.taydaelectronics.com/): Good supplier for passive components; audio jacks, and potentiometers. Their audio jacks are slightly smaller than the thonkiconn from thonk.
* [Love My Switches](https://lovemyswitches.com/): Has [really good knobs](https://lovemyswitches.com/anodized-aluminum-knob-the-lo-fi-1-4-smooth-shaft-12-5mm-od/) to go on those potentiometers!
* [OSHPark](https://oshpark.com/): Fast and (relatively) cheap PCB manufacturer. Prototype run pending.


## Changelog
