# ECE 250 Test Cases
This repo is intened to host test cases for students to run against their ECE 250 projects. This does not garentee that by passing
all cases that it will pass the automarker

# Running Test Cases on Windows 10 (PowerShell)
Place the following in a .ps1 file
```
$testin=$args[0]
$testout=$args[1]
$testdriver=$args[2]
diff (cat $testin | %testdriver) (cat $testout)
```
Example running a test: 
.\runTest.ps1 test1.in test1.out .\testDriver.exe

# Running Test Cases using `test_runner.py`

Note that this tool only works in linux/unix environments. It will run on WSL in windows.

Usage: `python3 test_runner.py <exacutable location> <tests folder>`

Example for project 0:

```
# cd into ECE250-testCases
python3 test_runner.py ../playlistdriver p0
```


### Owner
Quinn Hodges
