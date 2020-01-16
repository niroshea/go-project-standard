# `/internal`

Private application and library code. This is the code you don't want others importing in their applications or libraries. Note that this layout pattern is enforced by the Go compiler itself. See the Go 1.4 [`release notes`](https://golang.org/doc/go1.4#internalpackages) for more details. Note that you are not limited to the top level `internal` directory. You can have more than one `internal` directory at any level of your project tree.

You can optionally add a bit of extra structure to your internal packages to separate your shared and non-shared internal code. It's not required (especially for smaller projects), but it's nice to have visual clues showing the intended package use. Your actual application code can go in the `/internal/app` directory (e.g., `/internal/app/myapp`) and the code shared by those apps in the `/internal/pkg` directory (e.g., `/internal/pkg/myprivlib`).

Examples:

* https://github.com/hashicorp/terraform/tree/master/internal
* https://github.com/influxdata/influxdb/tree/master/internal
* https://github.com/perkeep/perkeep/tree/master/internal
* https://github.com/jaegertracing/jaeger/tree/master/internal
* https://github.com/moby/moby/tree/master/internal
* https://github.com/satellity/satellity/tree/master/internal

私有应用程序和库代码。 这是您不希望其他人在其应用程序或库中导入的代码。 请注意，此布局模式由Go编译器本身强制执行。 有关更多详细信息，请参见Go 1.4发行说明。 请注意，您不限于顶层内部目录。 在项目树的任何级别上，您都可以具有多个内部目录。

您可以选择向内部软件包中添加一些额外的结构，以分隔共享和非共享内部代码。 它不是必需的（尤其是对于较小的项目），但是最好有视觉提示来显示包装的预期用途。 您的实际应用程序代码可以放在/ internal / app目录（例如/ internal / app / myapp）中，而这些应用程序共享的代码可以在/ internal / pkg目录中（例如/ internal / pkg / myprivlib）。