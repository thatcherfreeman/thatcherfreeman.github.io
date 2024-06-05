---
title: Camera Profiling
subtitle: Color Space Transform DCTLs
description: We profiled many cameras and built transforms to integrate them into color management.
featured_image: /images/projects/idts/idts0000.jpg
tags: color management idts odts dwg aces log curves gamuts primaries chart regression input output device transforms linear conversion
---

## Camera Profiling DCTLs

Many camera manufacturers don't release the specifications of their camera color spaces, so we have been profiling many of these cameras and using a regression system to fit their log curves and primaries.

<a href="https://github.com/thatcherfreeman/dwg-transforms" class="button button--large">DWG/DI Transforms</a> <a href="https://github.com/thatcherfreeman/aces-transforms" class="button button--large">ACES Transforms</a>

In order to profile these cameras, it generally consists of two steps. The first is fitting the log encoding, which is done from an exposure bracket using the below tool:

<a href="https://github.com/thatcherfreeman/log2lin-finder" class="button button--large">Log 2 Lin Finder</a>

Once the image is linearized, we then use images of a color chart under known lighting to estimate a best-fit 3x3 matrix transform to the desired color primaries.

<a href="https://github.com/thatcherfreeman/rgb-matrix-finder" class="button button--large">RGB Matrix Finder</a>
