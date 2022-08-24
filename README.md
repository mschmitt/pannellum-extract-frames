# pannellum-extract-frames

## Name

**pannellum-extract-frames** - Extract frames from a pannellum panorama

## Synopsis

pannellum-extract-frames [-h] --url URL [--width WIDTH] [--height HEIGHT] [--pitch PITCH] [--yaw YAW] [--browser BROWSER] [--format {jpg,png}] [--debug]

## Description

Extract frames from a *pannellum* panorama (running *pannellum*'s *standalone.js*), as if in a circular motion, by remote controlling and screenshotting a *Chrome/Chromium* browser, for conversion into a video or animation.

## Dependencies

- **numpy** for calculating the yaw angle increments
- **pyppeteer** for remote controlling *Chrome/Chromium*
  - Note: Using the embedded _Chrome_ from the *pyppeteer* distribution is **not implemented (at all)** because of instability/unusability issues.

## Limitations

Dependent on _standalone.js_ from the _pannellum_ distribution.

Detection of when the panorama is done rendering (_waitForSelector()_, _waitForFunction()_) is based on own guesswork.

FIXME: Uses a single _Chrome/Chromium_ instance with multiple page loads, but no attempts are made to self-repair if the browser process dies. (Which has never happened during testing.)

## See also

- Pannelum - https://pannellum.org/
- Pyppeteer - https://github.com/pyppeteer/pyppeteer
- Puppeteer - https://pptr.dev/

# Copyright and License

[![License: Unlicense](https://img.shields.io/badge/license-Unlicense-blue.svg)](http://unlicense.org/)

```
This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org/>
```
