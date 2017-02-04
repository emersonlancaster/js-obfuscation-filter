# js-obfuscation-filter

This project is an experiment aiming to reproduce (and possibly improve) the use of Naive Bayesian filters to detect obfuscated JavaScript.

The current goal is a proof-of-concept with a minimal amount of moving parts.


## Requirements

bsfilter
uglifyjs


## Running

To get up and running:
- Copy one set of non-obfuscated JavaScript files into `./training/goodjs/`.
- Copy another set of non-obfuscated JavaScript files into `./testing/goodjs/`.
- Run `./setup.js_files` to generate obfuscated JavaScript files in `./training/badjs`.
- Run `./setup.bsfilter` to train bsfilter with `./training/goodjs/` and `./training/badjs` (this will use the local directory `./bsfilter.home/` to store bsfilter's files).
- Run `./test.bsfilter` to run bsfilter on `./testing/goodjs/` and `./testing/badjs`.
