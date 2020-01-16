# `/cmd`

Main applications for this project.

The directory name for each application should match the name of the executable you want to have (e.g., `/cmd/myapp`).

Don't put a lot of code in the application directory. If you think the code can be imported and used in other projects, then it should live in the `/pkg` directory. If the code is not reusable or if you don't want others to reuse it, put that code in the `/internal` directory. You'll be surprised what others will do, so be explicit about your intentions!

It's common to have a small `main` function that imports and invokes the code from the `/internal` and `/pkg` directories and nothing else.

Examples:

* https://github.com/heptio/ark/tree/master/cmd (just a really small `main` function with everything else in packages)
* https://github.com/moby/moby/tree/master/cmd
* https://github.com/prometheus/prometheus/tree/master/cmd
* https://github.com/influxdata/influxdb/tree/master/cmd
* https://github.com/kubernetes/kubernetes/tree/master/cmd
* https://github.com/satellity/satellity/tree/master/cmd/satellity
* https://github.com/dapr/dapr/tree/master/cmd

该项目的主要应用。

每个应用程序的目录名称应与您想要的可执行文件的名称匹配（例如，/ cmd / myapp）。

不要在应用程序目录中放置很多代码。 如果您认为该代码可以导入并在其他项目中使用，则应将其放在/ pkg目录中。 如果该代码不可重用，或者您不希望其他人重用它，则将该代码放在/ internal目录中。 您会惊讶于其他人会做什么，因此要明确您的意图！

通常有一个小的main函数可以导入和调用/ internal和/ pkg目录中的代码，而没有别的什么。