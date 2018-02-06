## Migrating to OpenEphys++

## Citations
- [ ] You need to cite
- [ ] How to cite

## What is it
- [ ] Old way of doing things
    - Lots of analog domain
    - A/D conversion using specialized PCB-level systems
    - Computational power spread over many PCs
    - Distributed Clocking etc
- [ ] Intan chips
    - Use integrated A/D conversion
    - Data serialization (time domain multiplexing) to reduce channel count
- [ ] Original Open Ephys 
    - Three major components
        1. Intan chip (headstage)
        2. USB to Intan bridge (Opal Kelly board)
        3. Host computer (Acqusition drivers and software)
    - Improvements over old system
        1. Much smaller analog domain
        2. Higher resolution A/D conversion in 0.01 - 10 kHz domain
        3. Simplified connectorization to acqusition PC
        4. Software ease of use and exapandability
        5. Tiny cost (2000 USD or so)
    - Regressions compared to old system
        1. Single Non selectable analog reference
            - Digital reference selection increases noise
        2. Intan amplifiers are pretty nonlinear for high amplitude signals and
           introduce considerable phase and amplitude distortion at the low end
           (< 2 Hz)
- [ ] Limitations of Open Ephys
    - All logic is still localized at host computer
        - Headstage is "dumb"
    - Connectorization is reduced, but still  scales linearly with the number
      of devices on headstage
        - i.e. hardware is not scalable, modular, or easily standardized
        - Commutation still relies on specilized devices
    - Although advertised for its closed-loop capabilites, the hardware has
      remarkable _bad_ closed loop performance (vs. MEABench)

- [ ] Goals of OpenEphys++
    1.  Scalable and modular design that allows increases in channel count and
        addition of future sensors with no increase in connectorization
    1.  Reduce and stabilize closed-loop latency
    1.  Use commodity hardware and standard interfaces wherever possible
    1.  Create modular firmware that can be extended to support future sensors
    1.  Create an API that is agnostic to language, OS, etc and can be easily
      integrated into _existing_ acquisition software

## OpenEphys++
- [ ] Overview

- [ ] Drive arrays
    - Designs
    - Where to buy
    - What to cite

- [ ] Electronic Hardware Components
    - headstage-64 and EIB-64
    - headstage-128-256, EIB-128, and EIB-256 [WIP]
    - PC interface boards
- [ ] Firmware

- [ ] Drivers, APIs, and Software

- [ ] Auxiliary Hardware Components
    - headstage test boards
    - programmer
    - nano-z adapter boards
- [ ] Closed loop performance

