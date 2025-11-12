# Datasets

We provide the datasets in a Deltille format. The [Deltille detector](https://github.com/facebookarchive/deltille) is a robust deltille and checkerboard detector. It comes with detector library, example detector code, and MATLAB bindings. [BabelCalib](https://ylochman.github.io/babelcalib) provides functions for calibration and evaluation using the Deltille software's outputs. Calibration from Deltille detections requires format conversion which is peformed by [`import_ODT`](https://github.com/ylochman/babelcalib/blob/main/core/feature/import_ODT.m). Please see a complete [calibration example](https://github.com/ylochman/babelcalib/blob/main/calib_run_opt2.m) from Deltille data.


### Kalibr dataset
* 6 lenses ranging from 126° to 195° FOV
    * BF2M2020S23
    * BF5M13720
    * BM2820
    * BM4018S118
    * EUROC
    * GOPRO
* 1 ENTANIYA-M12 lens with 250° FOV
* 1 camera from TUM-VI with 195° FOV

**Calibration target:** Aprilgrid (see details [here](https://github.com/ethz-asl/kalibr/wiki/Calibration-targets)) with the following configurations:
    - tagCols: 6
    - tagRows: 6
    - tagSize: 88 mm
    - tagSpacing: 0.3  # -> space: 0.3 * 88 mm = 26.4 mm


### OCamCalib dataset
* 5 fisheye cameras
  * Fisheye1
  * Fisheye2
  * Fisheye190deg
  * GOPR
  * Ladybug
* 4 catadioptric systems
  * KaidanOmni
  * MiniOmni
  * Omni
  * VMRImage

**Calibration target:** The checkerboards of differenet (unknown) sizes.

### UZH dataset
* 4 fisheye cameras "DAVIS"
    * indoor_45
    * indoor_forward
    * outdoor_45
    * outdoor_forward
* 4 fisheye cameras "Snapdragon"
    * indoor_45
    * indoor_forward
    * outdoor_45
    * outdoor_forward

**Calibration target:** Aprilgrid (see details [here](https://github.com/ethz-asl/kalibr/wiki/Calibration-targets)) with the following configurations:
    - tagCols: 5
    - tagRows: 4
    - tagSize: 75 mm
    - tagSpacing: 0.2 # -> space: 0.2 * 75 mm = 15 mm


### OV dataset 
* 16 lenses ranging from 90° to 180° FOV
    * 2012-A0 (single-plane target)
    * 3136-H0 (single-plane target)
    * 5501-C4 (single-plane target)
    * 130108MP (single-plane target)
    * ov00—ov07 (corner target)
    * ov00—ov03 (cube target)

**Calibration target:** The three types of checkerboards containing AprilTags (see details [here](https://github.com/facebookarchive/deltille)):
* **single-plane target** — one planar board that has the following configurations:
    - cols: 22
    - rows: 22
    - squareSize: 40 mm

* **corner target** — three planar boards, each board has the following configurations:
    - cols: 18
    - rows: 18
    - squareSize: 60 mm

* **cube target** — four planar boards, each board has the following configurations:
    - cols: 14
    - rows: 14
    - squareSize: 7.5 mm


## Citation

If you find the `OV` dataset useful in your research, please consider citing:

```bibtex
@InProceedings{Lochman-ICCV21,
    title     = {BabelCalib: A Universal Approach to Calibrating Central Cameras},
    author    = {Lochman, Yaroslava and Liepieshov, Kostiantyn and Chen, Jianhui and Perdoch, Michal and Zach, Christopher and Pritts, James},
    booktitle = {Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)},
    year      = {2021},
}
```
