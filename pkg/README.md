# `/pkg`

Library code that's ok to use by external applications (e.g., `/pkg/mypubliclib`). Other projects will import these libraries expecting them to work, so think twice before you put something here :-) Note that the `internal` directory is a better way to ensure your private packages are not importable because it's enforced by Go. The `/pkg` directory is still a good way to explicitly communicate that the code in that directory is safe for use by others. The [`I'll take pkg over internal`](https://travisjeffery.com/b/2019/11/i-ll-take-pkg-over-internal/) blog post by Travis Jeffery provides a good overview of the `pkg` and `internal` directories and when it might make sense to use them.

It's also a way to group Go code in one place when your root directory contains lots of non-Go components and directories making it easier to run various Go tools (as mentioned in these talks: [`Best Practices for Industrial Programming`](https://www.youtube.com/watch?v=PTE4VJIdHPg) from GopherCon EU 2018, [GopherCon 2018: Kat Zien - How Do You Structure Your Go Apps](https://www.youtube.com/watch?v=oL6JBUk6tj0) and [GoLab 2018 - Massimiliano Pippi - Project layout patterns in Go](https://www.youtube.com/watch?v=3gQa1LWwuzk)).

Note that this is not a universally accepted pattern and for every popular repo that uses it you can find 10 that don't. It's up to you to decide if you want to use this pattern or not. Regardless of whether or not it's a good pattern more people will know what you mean than not. It is a bit confusing for new Go devs, but it's a pretty simple confusion to resolve and that's one of the goals for this project layout repo.

Ok not to use it if your app project is really small and where an extra level of nesting doesn't add much value (unless you really want to). Think about it when it's getting big enough and your root directory gets pretty busy (especially if you have a lot of non-Go app components).

Examples:

* https://github.com/prometheus/prometheus/tree/master/pkg
* https://github.com/jaegertracing/jaeger/tree/master/pkg
* https://github.com/istio/istio/tree/master/pkg
* https://github.com/google/gvisor/tree/master/pkg
* https://github.com/google/syzkaller/tree/master/pkg
* https://github.com/perkeep/perkeep/tree/master/pkg
* https://github.com/minio/minio/tree/master/pkg
* https://github.com/heptio/ark/tree/master/pkg
* https://github.com/argoproj/argo/tree/master/pkg
* https://github.com/heptio/sonobuoy/tree/master/pkg
* https://github.com/helm/helm/tree/master/pkg
* https://github.com/kubernetes/kubernetes/tree/master/pkg
* https://github.com/kubernetes/kops/tree/master/pkg
* https://github.com/moby/moby/tree/master/pkg
* https://github.com/grafana/grafana/tree/master/pkg
* https://github.com/influxdata/influxdb/tree/master/pkg
* https://github.com/cockroachdb/cockroach/tree/master/pkg
* https://github.com/derekparker/delve/tree/master/pkg
* https://github.com/etcd-io/etcd/tree/master/pkg
* https://github.com/oklog/oklog/tree/master/pkg
* https://github.com/flynn/flynn/tree/master/pkg
* https://github.com/jesseduffield/lazygit/tree/master/pkg
* https://github.com/gopasspw/gopass/tree/master/pkg
* https://github.com/sosedoff/pgweb/tree/master/pkg
* https://github.com/GoogleContainerTools/skaffold/tree/master/pkg
* https://github.com/knative/serving/tree/master/pkg
* https://github.com/grafana/loki/tree/master/pkg
* https://github.com/bloomberg/goldpinger/tree/master/pkg
* https://github.com/crossplaneio/crossplane/tree/master/pkg
* https://github.com/Ne0nd0g/merlin/tree/master/pkg
* https://github.com/jenkins-x/jx/tree/master/pkg
* https://github.com/DataDog/datadog-agent/tree/master/pkg
* https://github.com/dapr/dapr/tree/master/pkg
* https://github.com/cortexproject/cortex/tree/master/pkg
* https://github.com/dexidp/dex/tree/master/pkg
* https://github.com/pusher/oauth2_proxy/tree/master/pkg
* https://github.com/pdfcpu/pdfcpu/tree/master/pkg
* https://github.com/weaveworks/kured/pkg
* https://github.com/weaveworks/footloose/pkg
* https://github.com/weaveworks/ignite/pkg
* https://github.com/tmrts/boilr/tree/master/pkg

外部应用程序可以使用的库代码（例如/ pkg / mypubliclib）。其他项目将导入这些库，希望它们能正常工作，因此在将某些内容放到这里之前，请三思：-)注意，内部目录是确保您的私有软件包不可导入的更好方法，因为它由Go强制执行。 / pkg目录仍然是明确传达该目录中的代码可被他人安全使用的好方法。 Travis Jeffery撰写的关于内部博客的pkg文章将很好地概述了pkg和内部目录以及何时使用它们。

当您的根目录包含大量非Go组件和目录时，这也是一种将Go代码分组到一个位置的方法，这使得运行各种Go工具变得更加容易（如在这些演讲中提到的那样：GopherCon EU 2018工业编程最佳实践，GopherCon 2018：Kat Zien-您如何构建Go应用程序和GoLab 2018-Massimiliano Pippi-Go中的项目布局模式）。

请注意，这不是普遍接受的模式，对于使用该模式的每个常见回购，您都可以找到10个不使用的模式。由您决定是否要使用此模式。不管这是否是一个好模式，更多的人都会了解您的意思。对于新的Go开发人员来说，这有点令人困惑，但这是一个非常简单的解决困惑，这是此项目布局回购的目标之一。

如果您的应用程序项目很小，并且嵌套的额外层次不会增加太多价值（除非您确实想要这样做），请不要使用它。当它变得足够大并且您的根目录变得非常繁忙时（特别是如果您有很多非Go应用程序组件），请考虑一下。