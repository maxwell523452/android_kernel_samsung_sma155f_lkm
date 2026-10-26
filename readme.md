# android_kernel_samsung_sma155f_lkm

automated KernelSU-Next LKM boot image patching for the samsung galaxy a15 4g (SM-A155F).

## features

- automatically checks for new upstream stock optimized releases
- downloads the upstream kernel archive and extracts `boot.img`
- patches the boot image using KernelSU-Next LKM
- validates the generated image and publishes it as a github release
- includes sha256 checksums for verification
- skips upstream builds that have already been published
- runs automatically every six hours

## device information

| property | value |
| --- | --- |
| device | samsung galaxy a15 4g |
| model | SM-A155F |
| kernel series | 5.10 |
| root method | KernelSU-Next LKM |

## upstream

the original stock optimized kernel and release assets are provided by poqdavid:

- source repository: https://github.com/poqdavid/android_kernel_samsung_sma155f
- upstream releases: https://github.com/poqdavid/android_kernel_samsung_sma155f/releases

## how it works

1. github actions checks upstream releases.
2. the latest matching stock optimized archive is downloaded.
3. the workflow extracts the original `boot.img`.
4. KernelSU-Next's LKM patching tool patches the image.
5. the workflow validates the output and calculates sha256 checksums.
6. the patched image is packaged and published as a github release.

if any required step fails, the workflow stops without publishing a release.

## usage

1. open the [releases](https://github.com/Maxwell523452/android_kernel_samsung_sma155f_lkm/releases) page.
2. download `android_kernel_samsung_sma155f_lkm.tar`.
3. verify that the build matches your exact firmware version.
4. keep your original boot image available before flashing.

flashing an incompatible boot image can prevent the device from booting. use the image at your own risk.

## credits

- **poqdavid** — original stock optimized kernel and release assets: https://github.com/poqdavid/android_kernel_samsung_sma155f
- **KernelSU-Next** — LKM implementation and patching tools: https://github.com/KernelSU-Next/KernelSU-Next

this is an unofficial community project and is not affiliated with or endorsed by the upstream developers.

## license

the upstream kernel and KernelSU-Next components are subject to their respective licenses. consult the original repositories for license terms and corresponding source code.
