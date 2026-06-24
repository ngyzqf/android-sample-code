style test
===================
style test sample code. 

```java {.line-numbers}
aidl_interface {
    name: "com.ftd.gyn",
    vendor_available: true,
    srcs: [":gyn_aidl"],
    stability: "vintf",
    backend: {
        java: {
            platform_apis: true,
        },
        cpp: {
            enabled: false,
        },
    },
    versions: ["1"],
}

