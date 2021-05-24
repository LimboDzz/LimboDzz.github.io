---
title: "What to do with err code: ERR_INVALID_ARG_TYPE after nrm installation"
date: 2021-05-24 16:16:34
tags:
  - P&S
  - npm
---

## Problem

命令`npm install nrm -g`安装成功后，運行 nrm 報錯

```sh
[TypeError [ERR_INVALID_ARG_TYPE]: The "path" argument must be of type string. Received undefined
at validateString (internal/validators.js:122:11)
at Object.join (path.js:375:7)
at Object.<anonymous> (C:\Users\DZZ\AppData\Roaming\npm\node_modules\nrm\cli.js:17:20)
at Module._compile (internal/modules/cjs/loader.js:1076:30)
at Object.Module._extensions..js (internal/modules/cjs/loader.js:1097:10)
at Module.load (internal/modules/cjs/loader.js:941:32)
at Function.Module._load (internal/modules/cjs/loader.js:782:14)
at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:72:12)
at internal/main/run_main_module.js:17:47
] {
code: 'ERR_INVALID_ARG_TYPE'
}
```

## Solution

vscode 打開報錯文件

> code C:\Users\DZZ\AppData\Roaming\npm\node_modules\nrm\cli.js

17 行

`const NRMRC = path.join(process.env.HOME, '.nrmrc');`

改成

`const NRMRC = path.join(process.env.USERPROFILE, '.nrmrc');`

## References

1. <https://blog.csdn.net/a806488840/article/details/113869522>
2. <https://blog.csdn.net/qq_42046421/article/details/113851930>
