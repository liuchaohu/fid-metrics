# Notion
> https://github.com/npurson/fid-metrics

This code repository is a correction to the problems in calculating FVD in the above projects.

- `fid_metrics/dataset.py` Line 97 `glob.glob(video_path + '/*')`
- `fid_metrics/dataset.py` Line 147 `return os.listdir(path)[0].endswith(f'.{ext}')`

# How to Use

1. Download model `i3d_pretrained_400.pt`
2. add two paths (dir not file) in `configs/config.yaml`


# FID/FVD Metrics

This repository provides a toolkit for computing Fréchet Inception Distance (FID) and Fréchet Video Distance (FVD) metrics, widely utilized for assessing the quality of generative models in the fields of image and video generation.

## Installation

    ```bash
    pip install -r requirements.txt
    ```

## Usage

In the absence of setting up the package, users can currently utilize it by the following as a temporal fix.

0. **Setup**

    ```shell
    export PYTHONPATH=`pwd`:$PYTHONPATH
    ```

1. **Calculating FID/FVD**

    ```shell
    python fid_metrics/main.py paths=[path1,path2]
    ```

## Acknowledgements

The code in this repository is based on [pytorch-fid](https://github.com/mseitzer/pytorch-fid) and [fvd-comparison](https://github.com/universome/fvd-comparison).

## License

Released under the [MIT](LICENSE) License.
