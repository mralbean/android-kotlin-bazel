workspace(name = "android-kotlin-test")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

## Rules for compling Kotlin code.
http_archive(
    name = "rules_kotlin",
    sha256 = "3b772976fec7bdcda1d84b9d39b176589424c047eb2175bed09aac630e50af43",
    url = "https://github.com/bazelbuild/rules_kotlin/releases/download/v1.9.6/rules_kotlin-v1.9.6.tar.gz",
)

load("@rules_kotlin//kotlin:repositories.bzl", "kotlin_repositories", "kotlinc_version")

kotlin_repositories(
    compiler_release = kotlinc_version(
        release = "1.9.25",
        sha256 = "6ab72d6144e71cbbc380b770c2ad380972548c63ab6ed4c79f11c88f2967332e",
    ),
)

load("@rules_kotlin//kotlin:core.bzl", "kt_register_toolchains")

kt_register_toolchains()

android_sdk_repository(
    name = "androidsdk",
    api_level = 34,
    build_tools_version = "34.0.0",
    path = "/Users/alvinportillo/Library/Android/sdk",
)
