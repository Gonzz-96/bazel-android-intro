load("@build_bazel_rules_android//android:rules.bzl", "android_library", "android_binary")

# To import a .aar file, this rule must be included:
# aar_import

# aar_import(
#     name = "some-sdk",
#     aar = "path/to/sdk-1.0.aar",
# )

android_library(
    name = "main",
    srcs = ["MainActivity.java"],
    manifest = "AndroidManifest.xml",
    resource_files = glob(["res/**"]),
    deps = [
        "//mediarecorder/java/com/example/android/common/media:media",
    ]
)

android_binary(
    name = "mediarecorder",
    manifest = "AndroidManifest.xml",
    deps = [":main"],
)
