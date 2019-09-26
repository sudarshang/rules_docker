load("@io_bazel_rules_docker//java:image.bzl", "java_image")

java_binary(
    name = "ProjectRunner",
    srcs = glob(["src/main/java/com/example/ProjectRunner.java"]),
    deps = [":greeter"],
)

java_library(
    name = "greeter",
    srcs = ["src/main/java/com/example/Greeting.java"],
    visibility = ["//src/main/java/com/example/cmdline:__pkg__"],
)

java_image(
    name = "RunnerDocker",
    main_class = "com.example.ProjectRunner",
    srcs = glob(["src/main/java/com/example/ProjectRunner.java"]),
    deps = [":greeter"],
)