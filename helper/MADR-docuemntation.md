# Visual Studio ADR Manager

## Install Extension in Visual Studo Code
- Install the extension `ADR Manger`

## Install adr-log
```shell
npm install -g adr-log
```

## Open ADR Manager
- Click `Command + Shift + P`

## Changed ADR Directory
- Type the `ADR Manager: ADR Change Directory` enter `architecture-desision-record`

## Initial ADR Directory
- Type the `ADR Manager: Initialize ADR Directory`

## Create ADR 
- Open ADR Manager

## Generate adr-log
```shell
# Printing the adr log to stdout
adr-log -d .

# Generating an index.md file containing the adr log
adr-log -i "README.md"
```

## References
* https://github.com/adr/vscode-adr-manager-introduction
* https://github.com/adr/adr-log