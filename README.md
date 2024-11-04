## prerequisite

Please turn off your internet connection. So you can notice the difference easily between terminal and file.

## with deno

### in terminal

Run below command:
```sh
deno install --log-level debug npm:zustand
```
Notice the last line, ansi color displayed.

### in file

Run below command:
```sh
deno install --log-level debug npm:zustand &> deno.malformed.log
```
Please notice the last line in deno.malformed.log, ansi color is malformed. But it should be striped.

If you run below command:
```sh
NO_COLOR=1 deno install --log-level debug npm:zustand &> deno.log
```
Notice the last line in deno.log, ansi color is striped.

## with npm

Installing zustand with npm took 8 minutes or so. So be patient.

### in terminal

Run below command:
```sh
npm install --loglevel verbose zustand
```
Ansi color displayed correctly.

### in file

Run below command:
```sh
npm install --loglevel verbose zustand &> npm.log
```
In npm.log, you will find that ansi color was striped.