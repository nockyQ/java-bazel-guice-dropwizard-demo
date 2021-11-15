load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

RULES_JVM_EXTERNAL_TAG = "4.1"
RULES_JVM_EXTERNAL_SHA = "f36441aa876c4f6427bfb2d1f2d723b48e9d930b62662bf723ddfb8fc80f0140"

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    sha256 = RULES_JVM_EXTERNAL_SHA,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [
        "com.google.inject:guice:5.0.1",
        "javax.inject:javax.inject:1",
        "io.dropwizard:dropwizard-core:2.0.25",
        "io.dropwizard:dropwizard-jersey:2.0.25",
        "io.dropwizard:dropwizard-metrics-graphite:2.0.25",

        "com.codahale.metrics:metrics-annotation:3.0.2",
        "com.codahale.metrics:metrics-healthchecks:3.0.2",

        "javax.ws.rs:javax.ws.rs-api:2.1.1"
    ],
    fetch_sources = True,
    repositories = [
        # Private repositories are supported through HTTP Basic auth
        # "http://username:password@localhost:8081/artifactory/my-repository",
        # "https://maven.google.com",
        "http://uk.maven.org/maven2",
        "https://jcenter.bintray.com/",
    ],
)