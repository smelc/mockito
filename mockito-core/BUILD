java_library(
    name = "mockito-core",
    srcs = glob(["src/main/java/**/*.java"]),
    visibility = ["//visibility:public"],
    deps = [
        "@maven//:net_bytebuddy_byte_buddy",
        "@maven//:net_bytebuddy_byte_buddy_agent",
        "@maven//:org_objenesis_objenesis",
        "@maven//:junit_junit",
        "@maven//:org_opentest4j_opentest4j",
        "@maven//:org_hamcrest_hamcrest",
    ],
)

java_test(
    name = "tests",
    srcs = glob(["src/test/java/**/*.java"]),
    use_testrunner = False,
    main_class = "org.junit.platform.console.ConsoleLauncher",
    args = [
        "--scan-classpath",
    ],
    deps = [
        ":mockito-core",
        "@maven//:org_assertj_assertj_core",
        "@maven//:org_junit_jupiter_junit_jupiter_api",
        "@maven//:org_junit_jupiter_junit_jupiter_params",
        "@maven//:org_junit_jupiter_junit_jupiter_engine",
        "@maven//:org_junit_platform_junit_platform_launcher",
        "@maven//:junit_junit",
        "@maven//:org_hamcrest_hamcrest",
    ],
)
