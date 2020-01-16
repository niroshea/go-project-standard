# `/build`

Packaging and Continuous Integration.

Put your cloud (AMI), container (Docker), OS (deb, rpm, pkg) package configurations and scripts in the `/build/package` directory.

Put your CI (travis, circle, drone) configurations and scripts in the `/build/ci` directory. Note that some of the CI tools (e.g., Travis CI) are very picky about the location of their config files. Try putting the config files in the `/build/ci` directory linking them to the location where the CI tools expect them when possible (don't worry if it's not and if keeping those files in the root directory makes your life easier :-)).

Examples:

* https://github.com/cockroachdb/cockroach/tree/master/build

包装和持续集成。

将您的云（AMI），容器（Docker），操作系统（deb，rpm，pkg）软件包配置和脚本放在/ build / package目录中。

将您的CI（travis，circle，drone）配置和脚本放在/ build / ci目录中。 请注意，某些配置项工具（例如Travis CI）对于其配置文件的位置非常挑剔。 尝试将配置文件放在/ build / ci目录中，并在可能的情况下将它们链接到CI工具期望它们的位置（不要担心，如果不是，并且将这些文件保存在根目录中，将使您的生活更轻松:-)） 。