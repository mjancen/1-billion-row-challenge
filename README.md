# 1-billion-row-challenge
A collection of solutions for the [1 billion row challenge](https://github.com/gunnarmorling/1brc) grouped by programming language.

The rules and limits of the challenge are:

- No external library dependencies may be used
- Implementations must be provided as a single source file
- The computation must happen at application runtime, i.e. you cannot process the measurements file at build time (for instance, when using GraalVM) and just bake the result into the binary
- Input value ranges are as follows:
    - Station name: non null UTF-8 string of min length 1 character and max length 100 bytes, containing neither ; nor \n characters. (i.e. this could be 100 one-byte characters, or 50 two-byte characters, etc.)
    - Temperature value: non null double between -99.9 (inclusive) and 99.9 (inclusive), always with one fractional digit
- There is a maximum of 10,000 unique station names
- Line endings in the file are \n characters on all platforms
- Implementations must not rely on specifics of a given data set, e.g. any valid station name as per the constraints above and any data distribution (number of measurements per station) must be supported
- The rounding of output values must be done using the semantics of IEEE 754 rounding-direction "roundTowardPositive"
