Visual Object Dataset converter

Converts between object dataset formats.

Example: convert from data in KITTI format to Pascal VOC format:

$ python vod_converter/main.py --from kitti --from-path datasets/mydata-kitti --to voc --to-path datasets/mydata-voc

Usage

Flags:

    --from-path: Source dataset
    --from: Type of source dataset. This flag only accepts 4 values:
        kitti: KITTI.
        kitti-tracking: KITTI tracking.
        voc: Pascal VOC
        udacity-crowdai: Udacity CrowdAI.
        udacity-autti: Udacity AUTTI
    --to-path: Destination path
    --to: Type of destination dataset. This flag only accepts 2 values:
        kitti: KITTI.
        voc: Pascal VOC

See main.py for documentation on how to easily plug in additional data formats; you can define a function that can read in your data into a common format, and it will be then ready to convert to any supported format.

Similarly, you can implement a single function that takes the common format and outputs to the filesystem in your format and you will be ready to convert from e.g VOC to yours.
