<p align="center">
  <img height="200px" class="comment" src="images/nfc.svg" alt="nfc"/>
</p>

[![Donate to this project using PayPal](https://shields.io/badge/Paypal-Donate-blue?logo=paypal&style=flat)](https://www.paypal.com/donate/?business=2667RS4MQ9M5Y&no_recurring=1&item_name=Please+support+me+if+you+like+my+work.+Thank+you%21&currency_code=EUR)
[![Donate to this project using Buy Me A Coffee](https://shields.io/badge/Buy%20me%20a%20coffee-Donate-yellow?logo=buymeacoffee&style=flat)](https://buymeacoff.ee/mcpat)
[![LICENSE](https://shields.io/badge/license-GPL-lightgrey)](https://raw.githubusercontent.com/mcpat-it/TagReader/main/LICENSE)
[![Platform](https://shields.io/badge/platform-esp32--s3%20(waveshare)-lightgrey)](https://github.com/mcpat-it/TagReader)
[![GitHub issues open](https://img.shields.io/github/issues/mcpat-it/TagReader.svg)](https://github.com/mcpat-it/TagReader/issues)
[![Downloads total](https://img.shields.io/github/downloads/mcpat-it/TagReader/total)](https://github.com/mcpat-it/TagReader/releases)
[![Latest release](https://img.shields.io/github/v/release/mcpat-it/TagReader)](https://github.com/mcpat-it/TagReader/releases)

[![forks](https://img.shields.io:/github/forks/mcpat-it/TagReader?style=social)](https://github.com/mcpat-it/TagReader)
[![stars](https://img.shields.io:/github/stars/mcpat-it/TagReader?style=social)](https://github.com/mcpat-it/TagReader)
[![watchers](https://img.shields.io:/github/watchers/mcpat-it/TagReader?style=social)](https://github.com/mcpat-it/TagReader)
[![followers](https://img.shields.io:/github/followers/mcpat-it?style=social)](https://github.com/mcpat-it)

# Install TagReader

<!--[Visit installer website](https://tagreader.mcpat.com/)-->
<!--<div class="meta_for_parser" style="visibility:hidden">-->
  <!--<button onclick="getElementById('flashcontent').innerHTML=Date()">Flash ESP <a class="comment" href="https://tagreader.mcpat.com/">here</a></button>-->
  <a class="comment" href="https://tagreader.mcpat.com/">Flash ESP via web installer here</a>
  <p id="flashcontent"></p>
  <!--<p id="demo2">YOUR CONTENT HERE</p>-->
<!--</div>-->
<!--<p align="center">
  <a class="comment" href="https://tagreader.mcpat.com/">Visit installer website</a>
</p>-->

# Tag Reader for Home Assistant

The tag reader is a simple to build/use NFC tag reader, specially created for [Home Assistant](https://www.home-assistant.io). It is using a Waveshare ESP32-S3 and the PN532 NFC module. The firmware is built using [ESPhome](https://www.esphome.io) or can directly flashed via web installer.

> I will create a 3D model for printing later.

![Photos of the final product](xxx)

## Building the tag reader

To build your own tag reader, you need the following components:

 - [ESP32-S3](https://amzn.to/3Z6NLpT)
 - [PN532 NFC Reader](https://amzn.to/4kCX8Wq)
 - [Buzzer](https://amzn.to/3Z0kNYM)

The 3D models for the case are [here](xxx).

### Connecting the components

![Photo of schematics](xxx)

There are not too many components to connect, but it does require soldering. You will need the following:

- [Solder](xxx)
- [Soldering iron with a fairly thin tip](xxx)
- [About 40cm of thin wire (at least 5 different colors)](xxx)


Also, make sure that you have set the switches on the PN532 to the following:
- Switch 1: On (up)
- Switch 2: Off (down)

This enables the PN532 module to communicate with the D1 over I2C, and is required for the modules to work together!

To flash the reader firmware to your ESP32-S3 you point ESPHome at [tagreader.yaml](/src/tagreader.yaml).  
> :warning: The tag reader requires ESPHome at least `2025.0.x`.

If you're new to ESPHome, we recommend that you use the [ESPHome Home Assistant add-on](https://esphome.io/guides/getting_started_hassio.html).

![Open Case](xxx)

## Configuring for use with Home Assistant

The tag reader requires [Home Assistant](https://www.home-assistant.io) 0.115 or later.

If the tag reader is unable to connect to a wifi network, it will start a WiFi access point with a captive portal to allow you to enter your WiFi credentials.

The tag reader will be automatically discovered by Home Assistant once the tag reader is connected to the same network. You can follow the instructions in the UI to set it up.

## Usage

Scanned tags can be managed from the tags interface in Home Assistant. You can find it under config -> tags.

![Screenshot of the Home Assistant tag UI](xx)

## Disclamer

We use Amazon affiliate links for the components and the tools. Some Ad-blockers might block these links and thus they seem to appear broken. You will have to temporarily disable the ad-blocker to open these links. 
