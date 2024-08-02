package(default_visibility = ["//visibility:public"])

load("@rules_kotlin//kotlin:android.bzl", "kt_android_library")

kt_android_library(
    name = "main-activity",
    srcs = glob(["**/MainActivity.kt"]),
    custom_package = "com.example.kotlinactivityapp",
    manifest = "main/java/com/example/kotlinactivityapp/LibraryManifest.xml",
    resource_files = glob(["main/res/**/*"]),
    deps = [
        "@maven//:androidx_appcompat_appcompat",
        "@maven//:androidx_games_games_activity",
    ],
)

android_binary(
    name = "hello-android-kotlin",
    custom_package = "com.example.kotlinactivityapp",
    manifest = "main/AndroidManifest.xml",
    deps = [
        ":main-activity",
    ],
)
