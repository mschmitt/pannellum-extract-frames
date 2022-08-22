# pannellum-extract-frames

## Name

**pannellum-extract-frames** - Extract frames from a pannellum panorama

## Synopsis

pannellum-extract-frames [-h] --url URL [--width WIDTH] [--height HEIGHT] [--pitch PITCH] [--yaw YAW] [--browser BROWSER]

## Description

Extract frames from a *pannellum* panorama (running *pannellum*'s *standalone.js*), as if in a circular motion, by remote controlling and screenshotting a *Chrome/Chromium* browser, for conversion into a video or animation.

## Dependencies

- **numpy** for calculating the yaw angle increments
- **pyppeteer** for remote controlling *Chrome/Chromium*
  - Note: Using the embedded Chrome from the *pyppeteer* distribution is **not implemented (at all)** because of instability/unusability issues.

## Limitations

Reliance on the browser's *networkidle0* event adds latency to every page load. Should rather detect completion of the panorama render operation based on something in the DOM or *pannellum*'s Javascript.

Operation on *Linux* is not overly unreasonably slow, but *Microsoft Windows* looks like it might benefit from using a single browser instance instead of starting a new browser for each frame.

## See also

- Pannelum - https://pannellum.org/
- Pyppeteer - https://github.com/pyppeteer/pyppeteer
- Puppeteer - https://pptr.dev/

# Copyright and License

[![License: Unlicense](https://img.shields.io/badge/license-Unlicense-blue.svg)](http://unlicense.org/)
