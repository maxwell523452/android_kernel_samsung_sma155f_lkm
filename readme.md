# __THIS PROJECT HAS BEEN INTEGRATED TO THE ORIGINAL REPOSITORY__
# __https://github.com/poqdavid/android_kernel_samsung_sma155f__

# android_kernel_samsung_sma155f_lkm

automated KernelSU-Next LKM boot image patching for the samsung galaxy a15 4g (SM-A155F).

## features

- checks for new upstream stock optimized releases
- downloads the upstream archive and extracts both `boot.img` and `android_kernel_samsung_sma155f_lkm.tar`
- patches the image using KernelSU-Next LKM
- validates the output and publishes a github release
- provides sha256 checksums
- skips builds that have already been published
- checks for updates every day

## upstream

- source: https://github.com/poqdavid/android_kernel_samsung_sma155f
- releases: https://github.com/poqdavid/android_kernel_samsung_sma155f/releases

## how it works

1. checks upstream releases.
2. downloads the stock optimized archive.
3. extracts the original `boot.img`.
4. patches the image using KernelSU-Next.
5. validates the output and calculates checksums.
6. packages the patched image and publishes a release.

if a required step fails, the workflow must stop without publishing a release.

## usage

1. open the [releases page](https://github.com/Maxwell523452/android_kernel_samsung_sma155f_lkm/releases).
2. download `android_kernel_samsung_sma155f_lkm.tar` or `boot.img` .
3. verify that the image matches your exact firmware.
4. keep the original boot image for recovery.

flashing an incompatible image can prevent the device from booting. use at your own risk.

## credits

- **poqdavid** — original stock optimized kernel and release assets: https://github.com/poqdavid/android_kernel_samsung_sma155f
- **KernelSU-Next** — LKM implementation and patching tools: https://github.com/KernelSU-Next/KernelSU-Next

this is an unofficial community project and is not affiliated with the upstream developers.

## license

the upstream kernel and KernelSU-Next components are subject to their respective licenses. consult the original repositories for license terms and source code.
