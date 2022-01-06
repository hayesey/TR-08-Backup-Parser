# Roland TR-08 Pattern Backup File Parser

## Files:

* tr-08_backup_parser.py - Python script
* example_input.prm - example of a backup pattern file from my TR-08. They are just text files.
* example_output.txt - example of the depiction of the drum pattern using the example input file.

## How To Use:

`python3 tr-08_backup_parser.py example_input.prm`

## Example Output:

(this is also in the txt file)

```
Scale = 1
Part = 1
Length = 32
Part = 2
Length = 32

** Variation A **
** 1st Part **
INST |1 2 3 4|5 6 7 8|9 1 1 1|1 1 1 1
     |       |       |  0 1 2|3 4 5 6
-----|-------|-------|-------|-------
 AC  |- - - -|x - - -|- - - -|x - - -
 BD  |x - - -|x - - -|x - - -|x - - -
 SD  |- - - -|x - - -|- - - -|x - - -
 LT  |- - - -|- - - -|- - - -|- - - -
 MT  |- - - -|- - - -|- - - -|- - - -
 HT  |- - - -|- - - -|- - - -|- - - -
 RS  |- - - -|- - - -|- - - -|- - - -
 CP  |- - - -|- - - -|- - - -|- - - -
 CB  |- - - -|- - - -|- - - -|- - - -
 CY  |- - x -|- - x -|- - x -|- - x -
 OH  |- - x -|- - x -|- - x -|- - x -
 CH  |x - - -|x - - -|x - - -|x - - -

** 2nd Part **
INST |1 2 3 4|5 6 7 8|9 1 1 1|1 1 1 1
     |       |       |  0 1 2|3 4 5 6
-----|-------|-------|-------|-------
 AC  |- - - x|- - - -|- - - -|x - - -
 BD  |x - - -|x - - -|x - - -|x - - -
 SD  |- - - -|x - - -|- - - -|x - - -
 LT  |- - - -|- - - -|- - - -|- - - -
 MT  |- - - -|- - - -|- - - -|- - - -
 HT  |- - - -|- - - -|- - - -|- - - -
 RS  |- - - -|- - - -|- - - -|- - - -
 CP  |- - - -|x x - x|- x x -|- - - -
 CB  |- - - -|- - - -|- - - -|- - - -
 CY  |- - x -|- - x -|- - x -|- - x -
 OH  |- - x -|- - x -|- - x -|- - x -
 CH  |x - - -|x - - -|x - - -|x - - -


** Variation B **
** 1st Part **
INST |1 2 3 4|5 6 7 8|9 1 1 1|1 1 1 1
     |       |       |  0 1 2|3 4 5 6
-----|-------|-------|-------|-------
 AC  |- - - -|- - - -|- - - -|- - - -
 BD  |x - - -|- - - -|x - - -|- - x -
 SD  |- - - -|- - - -|- - - -|- - - -
 LT  |- - - -|- - - -|- - - -|- - x -
 MT  |- - - -|- - - -|- - x -|- - - -
 HT  |- - - -|- - x -|- - - -|- - - -
 RS  |- - - x|- - - -|- - - -|x - - -
 CP  |- - - -|- - - -|- - - -|- - - -
 CB  |- - - -|- - - -|- - - -|- - - -
 CY  |- - - -|- - - -|- - - -|- - - -
 OH  |- - - -|- - - -|- - - -|- - - -
 CH  |x - x x|x - x -|x - x -|x - x -

** 2nd Part **
INST |1 2 3 4|5 6 7 8|9 1 1 1|1 1 1 1
     |       |       |  0 1 2|3 4 5 6
-----|-------|-------|-------|-------
 AC  |- - - -|- - - -|- - - -|- - - -
 BD  |- - - -|- - - -|- - - -|- - - -
 SD  |- - - -|- - - -|- - - -|- - - -
 LT  |- - - -|- - - -|- - - -|- - - -
 MT  |- - - -|- - - -|- - - -|- - - -
 HT  |- - - -|- - - -|- - - -|- - - -
 RS  |- - - -|- - - -|- - - -|- - - -
 CP  |- - - -|- - - -|- - - -|- - - -
 CB  |- - - -|- - - -|- - - -|- - - -
 CY  |- - - -|- - - -|- - - -|- - - -
 OH  |- - - -|- - - -|- - - -|- - - -
 CH  |- - - -|- - - -|- - - -|- - - -
```

## Caveats/limitations:

* currently only works with 16 step parts even though it's possible to have up to 32 steps, length always seems to be 32 or 0 though
* outputs both parts and both variations even if there is nothing in some of them
* I've only done a very small amount of testing but the results do match the patterns in my TR-08. 

Paul Hayes - paul@polog40.co.uk