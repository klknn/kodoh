load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Bazel Skylib required by absl.
http_archive(
    name = "bazel_skylib",  # 2023-05-31T19:24:07Z
    sha256 = "08c0386f45821ce246bbbf77503c973246ed6ee5c3463e41efc197fa9bc3a7f4",
    strip_prefix = "bazel-skylib-288731ef9f7f688932bd50e704a91a45ec185f9b",
    urls = ["https://github.com/bazelbuild/bazel-skylib/archive/288731ef9f7f688932bd50e704a91a45ec185f9b.zip"],
)

http_archive(
    name = "absl",
    urls = ["https://github.com/abseil/abseil-cpp/archive/refs/tags/20230802.0.zip"],
    strip_prefix = "abseil-cpp-20230802.0",
    sha256 = "2942db09db29359e0c1982986167167d226e23caac50eea1f07b2eb2181169cf",
)

http_archive(
    name = "imgui",
    url = "https://github.com/ocornut/imgui/archive/refs/tags/v1.89.8.zip",
    strip_prefix = "imgui-1.89.8",
    build_file = "@//third_party:BUILD.imgui",
    sha256 = "16b9d46385fb38340691c4dce7cf4547b161866f9c85fa588293df27e1667bfd",
)

http_archive(
    name = "glfw",
    url = "https://github.com/glfw/glfw/releases/download/3.3.8/glfw-3.3.8.zip",
    strip_prefix = "glfw-3.3.8",
    build_file = "//third_party:BUILD.glfw",
    sha256 = "4d025083cc4a3dd1f91ab9b9ba4f5807193823e565a5bcf4be202669d9911ea6",
)

# Hedron's Compile Commands Extractor for Bazel
# https://github.com/hedronvision/bazel-compile-commands-extractor
# Usage: $ bazel run @hedron_compile_commands//:refresh_all
COMPILE_COMMANDS_COMMIT = "e16062717d9b098c3c2ac95717d2b3e661c50608"
http_archive(
    name = "hedron_compile_commands",
    url = "https://github.com/hedronvision/bazel-compile-commands-extractor/archive/" + COMPILE_COMMANDS_COMMIT + ".tar.gz",
    strip_prefix = "bazel-compile-commands-extractor-" + COMPILE_COMMANDS_COMMIT,
)
load("@hedron_compile_commands//:workspace_setup.bzl", "hedron_compile_commands_setup")
hedron_compile_commands_setup()
