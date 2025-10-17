# MediaTek BPF Kernel Patcher(GUI Version)
![License](https://img.shields.io/github/license/R0rt1z2/mtk-bpf-patcher)
![GitHub Issues](https://img.shields.io/github/issues-raw/Hy1Fly/mtk-bpf-patcher-GUI?color=red)

### What is this?
This is a simple Python script that applies a binary patch to the given kernel image. Its purpose is to revert the BPF commit introduced by MTK, which indirectly broke arraymap while attempting to fix ubsan errors. The [specified commit](https://gist.github.com/R0rt1z2/8af7735c6c3802148fa4da61b3cba506), caused connectivity issues on Android 12 based ROMs.

### How does it work?
The patch applied by this script is quite simple. It just NOPs the offending code, in order to allow the `memcpy()` call to be executed.

### Supported kernel(s)
* This tool has only been tested with `4.14.X` and `4.19.X` based kernel(s).
* If your kernel isn't listed, feel free to try the script and report back the results.
* It's possible that each version uses different set of instructions, so beware of that.