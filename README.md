# OpenVario Protocol

This document describes the OpenVario serial port protocol.

**Version: 1.0-dev**

## Specification

The OpenVario serial port protocol is built around the `$POV` NMEA sentence:

    $POV,<type>,<value>,<type>,<value>,...*<checksum>
    
A `$POV` sentence can contain multiple datapoints that are defined by `type` and `value`. The `type` part is a letter or number describing the type of the following value according to the following overview of supported types. The `value` part is a floating point number for all currently supported types of datapoints. Future versions of the protocol may support other value types too though.

The list of datapoints should be terminated with the usual asterisk and two character checksum.

## Supported Datapoints

The following section describes all datapoints supported by the current version of the OpenVario protocol.

### Pressure

* `P`: static pressure in `hPa`
* `Q`: dynamic pressure in `Pa`
* `R`: total pressure in `hPa`

### Airspeed

* `S`: true airspeed in `km/h`

### Temperature

* `T`: temperature in °C
