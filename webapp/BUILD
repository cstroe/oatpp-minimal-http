cc_library(
    name = "static_controller",
    hdrs = ["StaticController.hpp"],
    deps = ["@oatpp//:main"],
)

cc_library(
    name = "status_dto",
    hdrs = ["StatusDto.hpp"],
    copts = ["-Iexternal/oatpp"],
    deps = ["@oatpp//:main"],
)

cc_library(
    name = "app_component",
    hdrs = ["AppComponent.hpp"],
    deps = ["@oatpp//:main"],
)

cc_library(
    name = "error_handler",
    srcs = ["ErrorHandler.cpp"],
    hdrs = ["ErrorHandler.hpp"],
    copts = ["-Iexternal/oatpp"],
    deps = [
        ":status_dto",
        "@oatpp//:main",
    ],
)

cc_binary(
    name = "webapp",
    srcs = ["App.cpp"],
    copts = ["-Iexternal/oatpp"],
    deps = [
        ":app_component",
        ":error_handler",
        ":static_controller",
        "@oatpp//:main",
    ],
)

