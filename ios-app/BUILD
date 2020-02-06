load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

swift_library(
    name = "UrlGetClasses",
    srcs = glob([
         "UrlGet/*.swift"
    ]),
)

ios_application(
    name = "ios-app",
    bundle_id = "Google.UrlGet",
    families = [
        "iphone",
        "ipad",
    ],
    minimum_os_version = "9.0",
    infoplists = [":UrlGet/Info.plist"],
    visibility = ["//visibility:public"],
    deps = [":UrlGetClasses"],
)
