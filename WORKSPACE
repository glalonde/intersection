load("//tools:github.bzl", "github_archive")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

#Import the gflags files.
github_archive(
    name   = "com_github_google_ortools",
    repository = "google/or-tools",
    commit = "80426425408ddf9b9cc852bf7b9231658b9726a0",
    sha256 = "5f5bb8513bf1461e29743459a9c9b9800a7ad01089469a40e9ff90b8b8373ea4",
)

#Import the gflags files.
github_archive(
    name   = "com_github_gflags_gflags",
    commit = "28f50e0fed19872e0fd50dd23ce2ee8cd759338e",
    repository = "gflags/gflags",
    sha256 = "63ae70ea3e05780f7547d03503a53de3a7d2d83ad1caaa443a31cb20aea28654",
)

# Bazel toolchains
http_archive(
    name = "com_grail_bazel_toolchain",
    strip_prefix = "bazel-toolchain-master",
    urls = ["https://github.com/grailbio/bazel-toolchain/archive/master.tar.gz"],
)

load("@com_grail_bazel_toolchain//toolchain:configure.bzl", "llvm_toolchain")

llvm_toolchain(
    name = "llvm_toolchain",
    llvm_version = "7.0.0",
)

#Import the glog files.
github_archive(
    name   = "com_github_glog_glog",
    repository = "google/glog",
    commit = "41f4bf9cbc3e8995d628b459f6a239df43c2b84a",
    sha256 = "835888ec47ee8065b3098f3ec4373717d641954970f009833ed6d466c397409a"
)

# This com_google_protobuf repository is required for proto_library rule.
# It provides the protocol compiler binary (i.e., protoc).
http_archive(
    name = "com_google_protobuf",
    strip_prefix = "protobuf-master",
    urls = ["https://github.com/protocolbuffers/protobuf/archive/master.zip"],
)

github_archive(
    name = "com_google_absl",
    repository = "abseil/abseil-cpp",
    commit = "426eaa4aa44e4580418bee46c1bd13911151bfb1",
    sha256 = "8fb934c36fc5bc59f12e02084a3b0eba19e78dc23acbc69549ad3548b57c100f",
)

# This com_google_protobuf_cc repository is required for cc_proto_library
# rule. It provides protobuf C++ runtime. Note that it actually is the same
# repo as com_google_protobuf but has to be given a different name as
# required by bazel.
http_archive(
    name = "com_google_protobuf_cc",
    strip_prefix = "protobuf-master",
    urls = ["https://github.com/protocolbuffers/protobuf/archive/master.zip"],
)

http_archive(
    name = "bazel_skylib",
    sha256 = "bbccf674aa441c266df9894182d80de104cabd19be98be002f6d478aaa31574d",
    strip_prefix = "bazel-skylib-2169ae1c374aab4a09aa90e65efe1a3aad4e279b",
    urls = ["https://github.com/bazelbuild/bazel-skylib/archive/2169ae1c374aab4a09aa90e65efe1a3aad4e279b.tar.gz"],
)

http_archive(
    name = "net_zlib",
    build_file = "//third_party:zlib.BUILD",
    sha256 = "c3e5e9fdd5004dcb542feda5ee4f0ff0744628baf8ed2dd5d66f8ca1197cb1a1",
    strip_prefix = "zlib-1.2.11",
    urls = ["https://zlib.net/zlib-1.2.11.tar.gz"],
)

bind(
    name = "zlib",
    actual = "@net_zlib//:zlib",
)

load("@bazel_skylib//lib:versions.bzl", "versions")

new_http_archive(
    name = "gtest",
    url = "https://github.com/google/googletest/archive/release-1.8.0.zip",
    build_file = "@com_github_google_ortools//bazel:gtest.BUILD",
    strip_prefix = "googletest-release-1.8.0/googletest",
)

new_http_archive(
    name = "glpk",
    url = "http://ftp.gnu.org/gnu/glpk/glpk-4.52.tar.gz",
    sha256 = "9a5dab356268b4f177c33e00ddf8164496dc2434e83bd1114147024df983a3bb",
    build_file = "@com_github_google_ortools//bazel:glpk.BUILD",
)
