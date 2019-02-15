package(
    default_visibility = ["//visibility:public"],
)

cc_binary(
    name = "sat_example",
    srcs = ["sat_example.cc"],
    deps = [
        "@com_github_google_ortools//ortools/sat:cp_model",
        "@com_github_google_ortools//ortools/sat:model",
        "@com_github_google_ortools//ortools/sat:sat_parameters_cc_proto",
    ],
)
