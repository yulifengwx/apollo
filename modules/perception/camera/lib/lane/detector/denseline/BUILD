load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])



cc_library(
    name = "denseline_lane_detector",
    srcs = [
        "denseline_lane_detector.cc",
    ],
    hdrs = [ 
        "denseline_lane_detector.h",
    ],
    deps = [
        "//modules/common/util:file_util",
        "//modules/perception/base:base",
        "//modules/perception/camera/common:common",
        "//modules/perception/camera/lib/interface:interface",
        "//modules/perception/camera/lib/lane/common:denseline_proto",
        "//modules/perception/inference:inference_factory_lib",
        "//modules/perception/inference/tensorrt:rt_net",
        "//modules/perception/inference/utils:inference_resize_lib",
        "//modules/perception/inference/utils:inference_util_lib",
        "//modules/perception/lib/registerer:registerer",
    ],
)

cpplint()
