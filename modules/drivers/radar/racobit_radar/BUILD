load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "racobit_radar_message_manager",
    srcs = [
        "racobit_radar_message_manager.cc",
    ],
    hdrs = [
        "racobit_radar_message_manager.h",
    ],
    deps = [
        "//modules/drivers/canbus:sensor_gflags",
        "//modules/drivers/canbus/can_client:can_client_factory",
        "//modules/drivers/canbus/can_comm:can_sender",
        "//modules/drivers/canbus/can_comm:message_manager_base",
        "//modules/drivers/radar/racobit_radar/protocol:drivers_racobit_radar_protocol",
    ],
)

# cc_test(
#     name = "racobit_radar_message_manager_test",
#     size = "small",
#     srcs = [
#         "racobit_radar_message_manager_test.cc",
#     ],
#     deps = [
#         "racobit_radar_message_manager",
#         "@gtest//:main",
#     ],
# )

cc_library(
    name = "racobit_radar_canbus_lib",
    srcs = [
        "racobit_radar_canbus_component.cc",
    ],
    hdrs = [
        "racobit_radar_canbus_component.h",
    ],
    deps = [
        ":racobit_radar_message_manager",
        "//cyber",
        "//modules/common",
        "//modules/common/adapters:adapter_gflags",
        "//modules/common/monitor_log",
        "//modules/drivers/canbus:sensor_gflags",
        "//modules/drivers/canbus/can_client:can_client_factory",
        "//modules/drivers/canbus/can_comm:can_receiver",
        "//modules/drivers/canbus/can_comm:message_manager_base",
        "//modules/drivers/proto:sensor_proto",
        "//modules/drivers/radar/racobit_radar/protocol:drivers_racobit_radar_protocol",
    ],
    copts = ['-DMODULE_NAME=\\"racobit_radar_canbus\\"'],
)

cc_binary(
    name = "libracobit_radar_canbus_component.so",
    deps = [":racobit_radar_canbus_lib"],
    linkshared = True,
    linkstatic = False,
)

cpplint()
