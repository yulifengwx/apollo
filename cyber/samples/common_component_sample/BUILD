load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])

cc_binary(
    name = "libcommon_component_sample.so",
    deps = [":common_component_sample_lib"],
    linkopts = ["-shared"],
    linkstatic = False,
)

cc_library(
    name = "common_component_sample_lib",
    srcs = [
        "common_component_sample.cc",
    ],
    hdrs = [
        "common_component_sample.h",
    ],
    deps = [
        "//cyber",
        "//cyber/samples/proto:samples_cc_proto",
    ],
)
cpplint()
