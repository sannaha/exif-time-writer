# exif-time-writer

In order to ensure that the pictures and videos are displayed in an orderly manner on the timeline.

Get date info from parent directory name, write time information to exif of JPG/JPEG files, or change the creation time, modify time and access time of non-JPG files.

为了保证图片和视频在导入图库后在时间轴上有序展示。从父目录的文件夹名称中获取日期信息，写入到 JPG/JPEG 文件的 exif 中，对于 PNG/MP4 等不含 exif 的文件，则修改文件的创建时间、修改时间和访问时间。

# How to use

1. Install requirements with `pip install -r requirements.txt`
2. Run `python exif-time-writer.py --path 'D:\photo_path' --date-format 'YYYY-MM-DD'`

# Options

- `--path PATH`：Input path, required.
- `--date-format`: Date format of directory name, support `YYYYMMDD`, `YYYY-MM-DD`, `YYYYMM` and `YYYY-MM`, `YYYYMMDD` is the default. (Directory name example: `20221130 香山秋色`, `2022-11-30 香山秋色`, `202211 香山秋色`, `2022-11 香山秋色` )
- `--force`: TODO. Update the exif of all JPG files with the time of the parent directory, even if the exif already exists.