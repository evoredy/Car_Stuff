# Welcome to Evoredy's Tuned 2.3 2G Eclipse ROM Suite v0.0.2a

The Mitsubishi Lancer Evolution 7/8/9/10 ECUs are very robust. They have been "cracked" and defined with significant open source resources to reflash them as well as conduct logging for scientific reproduction. I have learned that if a modification system is followed, variances in ROMs are very little as most of the required parameters (like for injectors) have been defined by the community. The community has also added new code subroutines/functions/etc. for new features like "speed density (AFM delete)," "no lift to shift / flat shift," and monitoring of other sensors using available or hijacked ADCs. The Mitsubishi software and hardware engineers worked very hard on the parts of the ECU software that allow very good daily drivability and startup which is seldom if ever replicated with an aftermarket ECU. This leads to very comfortable and drivable 400-800HP cars with significant reliability and alternative fuel support.     

These files will get you started and running with your 95-99 Eclipe Turbo if you copy all of my modifications and apply the necessary ECU patches (included). The timing, fuel, and VE tables are set up for a 2.3 liter 4G63 stroker, but everything else to get a car started is there.

This is to faclitate getting the car started, idleing, and also getting the proper injector latencies for the prescribed injectors. Included are also definitions that are helpful for futher tweaking compiled from the EvolutionM/ECUFlash forums. They are absolutely required if modifications deviate from the control list provided here. 

__This is for expiremental use. Please use with caution and understand hardware and software limitations as well as vulnerabilities. Drive safely and respect others.__

To run and/or compile, you will need
    * [ECUFlash >= v1.42]
    * [Tactrix Openport Cable or equivalent]
    * [An EVO 8 2003-2005 ECU wired in correctly and some form of 4G63 engine]

This will run turn-key if you have:
    * [4G63 2.3 @ ~ 8.5:1]
    * [OEM MLS gasket w/ ARP L19 or equivalent head studs]
    * [OEM 2G intake manifold]
    * [OEM 1Gb throttle body w/ sensors]
    * [OEM 2G head]
    * [GSC S2 cams or equivalent]
    * [Garrett GT35R w/ hot parts and .68 AR (test car has an FP35 and FP race manifold)]
    * [3 inch TBE w/ wideband for monitoring]
    * [Dual Walbro GSS342 fuel pumps (both running) with AFPR at 40PSI idle]
    * [FIC 2150cc injectors w/ resistor pack delete]
    * [At least 2400# clutch and kevlar disc for 93 or twin-disc for E85 (comp twin-disc used)]
    * [Built transmission needed for E85 / OEM gear ratios for 2-5 OK]
    * [EVO 8 ECU]
    * [Motorola 4 bar MAP sensor (OEM location)]
    * [GM IAT sensor (wired to OEM IAT wires from AFM plug)]
    * [Hallman MBC @ 25 PSI for 93 or 30 PSI for E85]
    * [NGK BPR8ES or BR8ES @ 0.022 gap]


## Getting started

To run and/or compile
```

```

To run
```

```

Notes and Errata:

```

```


## Changelog v0.0.1a
```
  - initial commit
```

## Changelog v0.0.2a
```
  - "Decel Fuel Cut Resume" address changed to 0x35f4 for TephraMOD-96530706-v7 definition as it was erronous
  - added various files and definitions
```

## Known Issues
```
  - need to add "howto" info under "Getting started" 
  - need to add E85 logs
  - possibly add evoscan definition files (unsure)
  - more refinement in lists of objects provided 
```