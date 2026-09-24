# PSMD (Peak width of Skeletonized Mean Diffusivity)

> [!IMPORTANT]
> **PSMD has a successor: [DELTA-SVD](https://delta-svd.com).** DELTA-SVD is optimised for longitudinal processing and reports PSMD alongside MSMD and the free-water metric MSFW. This repository is archived and no longer maintained. The PSMD tool, its releases and its container images remain available for ongoing studies and for reproducing published results.
>
> PSMD values from DELTA-SVD are **not comparable** with values from this tool. Do not mix both pipelines in one analysis. See [PSMD is now DELTA-SVD](https://delta-svd.com/psmd/).

PSMD is a robust, fully-automated and easy-to-implement marker for cerebral small vessel disease based on diffusion tensor imaging, white matter tract skeletonization (as implemented in FSL-TBSS) and histogram analysis.

> [!CAUTION]
> PSMD is NOT a medical device and **for academic research use only**. Do not use PSMD for diagnosis, prognosis, monitoring or any other clinical routine use. Any application in clinical routine is forbidden by law, e.g. by Medical Device Regulation article 5 in the EU.

## Usage

As of version 1.9.0, the preferred way of using PSMD is a [pre-built container image](https://github.com/miac-research/psmd/pkgs/container/psmd), which can be used with Docker, Apptainer, and compatible container platforms.

The usage is simple. For more detailed information on usage, including FAQ, please visit [the PSMD Wiki](https://github.com/miac-research/psmd/wiki/).

**Using Apptainer:**

```shell
# 1. Pull the container image and save as .sif file 
apptainer build psmd.sif docker://ghcr.io/miac-research/psmd:latest

# See available command line options:
apptainer run psmd.sif -h
```

**Using Docker**: 

```shell
# 1. Pull the container image into your local registry
docker pull ghcr.io/miac-research/psmd:latest
docker tag ghcr.io/miac-research/psmd:latest psmd:latest

# For advanced usage, see available command line options:
docker run --rm psmd:latest -h
```

**Local installation (not recommended)**: Alternatively, you can download the PSMD script from the [releases page](https://github.com/miac-research/psmd/releases) and run it in your local environment with all requried dependencies installed.

## Version history

Starting with version 1.6, all development is done in this GitHub repository. 
See the [releases page](https://github.com/miac-research/psmd/releases) for the version history and the [packages page](https://github.com/miac-research/psmd/pkgs/container/psmd) for available pre-built container images.

> [!NOTE]  
> For a new project, take the latest release. It is best practice to **stick with one release version or – even better – the same container image** throughout a project.

## License

The PSMD script itself is published under the BSD 3-clause license. Please see the `LICENSE` file provided in this repository.

> [!IMPORTANT]  
> Please note that an [FSL license](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/Licence) is required to run PSMD, regardless of whether you are using the container or a local installation.

Please consult the [documentation](https://github.com/isdneuroimaging/psmd/wiki#license--referencing) regarding publications to cite when using PSMD. 

## Support

The PSMD project was initiated at the Institue for Stroke and Dementia Research (ISD), Munich, Germany, with funding support by the LMU FöFoLe program (grant 808), the Else Kröner-Fresenius-Stiftung (EKFS, grant 2014_A200), and the Vascular Dementia Research Foundation.
