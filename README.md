# Scripts

This is a collection of useful bash scripts.

## Requirements

You'll need an environment that can run bash scripts. In addition, you'll need a few packages:

- **imagemagick** for image transformation.

  `brew install imagemagick`

- **jpegoptim** for optimizing jpgs.

  `brew install jpegoptim`

## Installation

Clone this repository on your machine:

```bash
git clone git@github.com:braican/scripts.git
```

To enable the scripts to work from anywhere on your machine, you can include the path to this scripts directory to your environment's `$PATH` variable. Generally, this is done by opening your configuration file (`.bashrc`, .zshrc`, etc.) and adding the following line:

```bash
export PATH=$PATH:/path/to/scripts
```

## The scripts

### `jpg-optimizer`

Allows you to resize and change quality of a directory of jpgs.

**Usage:**

```bash
jpg-optimizer <source_directory> [-w|--max-width <max_width>] [-h|--max-height <max_height>] [-q|--jpg-quality <jpg_quality>] [-r|--resize-dir <resize_dir>]
```

**Options:**

```bash
-w, --max-width    <max_width>    Specify the maximum width for resizing (default: 800)
-h, --max-height   <max_height>   Specify the maximum height for resizing (default: 600)
-q, --jpg-quality  <jpg_quality>  Specify the JPEG quality (default: 50)
-r, --resize-dir   <resize_dir>   Specify the name of the resize directory (default: resized)
```

### `convert-heic-to-jpg`

Converts a directory of heic files into jpgs.

**Usage:**

```bash
convert-heic-to-jpg <source_directory>
```