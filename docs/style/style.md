style test
===================
style test sample code. 

1.
<div class="highlight-sh notranslate"><table class="highlighttable"><tr><td class="linenos"><div class="linenodiv"><pre>1
2
3</pre></div></td><td class="code"><div class="highlight"><pre><span></span><span class="c1">#这里以rk356x系列4.19.232内核配置文件为例</span>
make <span class="nv">ARCH</span><span class="o">=</span>arm64 <span class="nv">CROSS_COMPILE</span><span class="o">=</span>aarch64-linux-gnu- lubancat2_defconfig
make <span class="nv">ARCH</span><span class="o">=</span>arm64 -j4 <span class="nv">CROSS_COMPILE</span><span class="o">=</span>aarch64-linux-gnu- dtbs
</pre></div>
</td></tr></table></div>

2.
```java
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
