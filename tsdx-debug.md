# Debug wit tsdx in visual studio code:

Just create a launch.json in visualStudio with:

```json
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Node.js: Debug TSDX Jest Tests",
            "type": "node",
            "request": "launch",                        
            "runtimeArgs": [
                "--inspect-brk",
                "${workspaceRoot}/node_modules/tsdx/dist/index.js",
                "test",
                "--runInBand"
            ],
            "console": "integratedTerminal",
            "internalConsoleOptions": "neverOpen",
            "port": 9229
            

        }
    ]
}
```

ref: https://github.com/formium/tsdx/issues/577