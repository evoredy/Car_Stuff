# Welcome to Evoredy's Tuned 2.3 2G Eclipse ROM Suite v0.0.2a

The Mitsubishi Lancer Evolution 7/8/9/10 ECUs are very robust. They have been "cracked" and defined with significant open source resources to reflash them as well as conduct logging for scientific reproduction. I have learned that if a modification system is followed, variances in ROMs are very little as most of the required parameters (like injectors scaling) have been defined by the community. The community has also added new code subroutines/functions/etc. for new features like "speed density (AFM delete)," "no lift to shift / flat shift," and monitoring of other sensors using available or hijacked ADCs (tephra and mrfred). The Mitsubishi software and hardware engineers worked very hard on the parts of the ECU software that allow very good daily drivability and startup which is seldom if ever replicated with an aftermarket ECU. This leads to very comfortable and drivable 400-800HP cars with significant reliability, economy, and alternative fuel support.     

These files will get you started and running with your 95-99 Eclipe Turbo (or 4G63 powerplant) if you replicate the modifications below and apply the necessary ECU patches (included). The timing, fuel, and VE tables are set up for a 2.3 liter 4G63 stroker, but everything else to get a car started is there. Even with a 2.0 liter OEM setup (given the proper required sensors), the car will start right up and idle close to stoich.

This is to faclitate getting the car started, idleing, and also getting the proper injector latencies for the prescribed injectors. Included are also definitions that are helpful for futher tweaking compiled from the EvolutionM/ECUFlash forums (modifications and corrections from tephra, mrfred, and evoredy are included). They are absolutely required if modifications deviate from the control list provided here. 

__This is for expiremental use. Please use with caution and understand hardware and software limitations as well as vulnerabilities. Drive safely and respect others.__

To run and/or compile, you will need
  * [ECUFlash >= v1.42]
  * [Tactrix Openport Cable or equivalent]
  * [An EVO 8 2003-2005 ECU wired in correctly and some form of 4G63 engine]

This will run turn-key if you have
  * [4G63 2.3 @ ~ 8.5:1]
  * [OEM MLS gasket w/ ARP L19 or equivalent head studs (required for E85)]
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
  * [Wideband O2 sensor 0-5V output wired into secondary O2 sensor input (for logging)]
  * [OEM primary O2 narrowband in OEM location and using OEM plug]
  * [Hallman MBC @ 25 PSI for 93 or 30 PSI for E85]
  * [NGK BPR8ES or BR8ES @ 0.022 gap]


## Getting started

To run and/or compile
```
- ensure ECU is installed and wired properly. there are modifications needed is retrofitting a 2003-2005 EVO 8 ECU into an 89-99 mitsubishi eclipse harness. 2003-2004 ECUs will plug right requiring some pin re-arragements while a 2005 ECU has a completely different harness/connector setup and will require considerable modification on the harness side.

- ensure ECUFlash is installed and drivers for your Tactrix cable are installed (included with ECUFlash).

- place the *.xml files (/definitions) into the "C:\Program Files (x86)\OpenECU\EcuFlash\rommetadata\mitsubishi\evo" directory and overwrite any files. make backups if you wish.

- open ECUFlash and conduct a flash backup of your current rom and save it. if this completes successfully, you are ready to flash.

- open the rom for the fuel you are using (93 octane or E85 ethanol) and flash it. close the program.
```

To run
```
- highly recommended: have a logger that can monitor 1-byte load, RPM, fuel and timing table, MAP, IAT, and O2 sensors (both of them). you will have to scale the voltage output of the secondary O2 sensor and MAP sensor to the brand of gauge/sensor setup you have

helpful scalings:
4 BAR MAP: 0.2369*x-14.2
WBO2: (0.9*x+125.1)/18
1-byte Load: 1.8x
IAT: x*1.8+32

- verify boost is under control via your method and monitor A/F ratios as well as timing for your boost levels at various loads. make adjustments as needed to the main timing and fuel maps as well as VE for global changes 
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
  - added to README
```

## Known Issues
```
  - need to add "howto" info under "Getting started" 
  - need to add E85 logs
  - possibly add evoscan definition files (unsure)
  - more refinement in lists of objects provided 
```
