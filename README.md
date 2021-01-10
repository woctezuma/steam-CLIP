# Steam CLIP: match Steam Banners with OpenAI's CLIP

[![Build status with Github Action][build-image-action]][build-action]
[![Code coverage][codecov-image]][codecov]
[![Code Quality][codacy-image]][codacy]

This repository contains Python code to retrieve Steam games with similar store banners, using [OpenAI's CLIP][openai-clip].

Image similarity is assessed by the cosine similarity between image features encoded by CLIP.

![Similar vertical banners][wiki-cover]

## Requirements

-   Install the latest version of [Python 3.X][download-python].
-   Install the required packages:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## Data

Data is available in [`download-steam-banners-data/`][banner-data-repository].

The most recent data snapshot was downloaded with [this Colab notebook][download_steam_banners] on January 9, 2021.
[![Open In Colab][colab-badge]][download_steam_banners]

This snapshot is shared as an archive (`original_vertical_steam_banners.tar`, 1.5 GB) [on Google Drive][gdrive-banner-data].

It consists of **vertical** Steam banners (300x450 resolution), available for 29982 out of 48792 games, i.e. 61.4% of games.

Resized images are provided in the same repository for resolutions 256, 224, 128, 64, etc.

The list of appIDs (before any potential filtering) is from [`steam-store-snapshots`][steam-store-snapshots].

### Filtering out

Information is also provided in `.txt` logs about a possible filtering out of images based on:
-   blank images: there are 2 images either totally black or totally white,
-   image size (before resizing images): there is 1 image with resolution 600x900,
-   image channels (before and after resizing images): most images are RGB, but a few are L or CMYK.

It is up to the reader to filter out the dataset based on these logs.
Logs can be reproduced with [this Colab notebook][filter_out_steam_banners].
[![Open In Colab][colab-badge]][filter_out_steam_banners]

## Usage

TODO

## Results

TODO

## References

-   CLIP (Contrastive Language-Image Pre-Training):
    - [OpenAI's CLIP][openai-clip]
    - [`steam-CLIP`][banner-repository-CLIP]: retrieve games with similar banners, using OpenAI's CLIP (resolution 224),
-   MobileNet v3:
    - [`match-steam-banners`][banner-repository-mobilenet-v3]: retrieve games with similar banners, using MobileNet v3 (resolution 256),
-   MobileNet v1:
    - [`download-steam-banners`][banner-repository-mobilenet-v1]: retrieve games with similar banners, using MobileNet v1 (resolution 128),
    - [`download-steam-screenshots`][screenshot-repository-mobilenet-v1]: retrieve games with similar screenshots, using MobileNet v1 (resolution 128).

<!-- Definitions -->

[build-action]: <https://github.com/woctezuma/steam-CLIP/actions>
[build-image-action]: <https://github.com/woctezuma/steam-CLIP/workflows/Python application/badge.svg?branch=main>

[codecov]: <https://codecov.io/gh/woctezuma/steam-CLIP>
[codecov-image]: <https://codecov.io/gh/woctezuma/steam-CLIP/branch/master/graph/badge.svg>

[codacy]: <https://www.codacy.com/app/woctezuma/steam-CLIP>
[codacy-image]: <https://api.codacy.com/project/badge/Grade/72fecbb5ff4e40a894849f26c00a5cdf>

[wiki-cover]: <https://github.com/woctezuma/steam-CLIP/wiki/img/illustration.jpg>
[download-python]: <https://www.python.org/downloads/>
[banner-data-repository]: <https://github.com/woctezuma/download-steam-banners-data>
[download_steam_banners]: <https://colab.research.google.com/github/woctezuma/google-colab/blob/master/download_steam_banners.ipynb>

[gdrive-banner-data]: <https://drive.google.com/drive/folders/1BU8R1JMdzOqc4pzEkpQY6w6FuaretxUH>
[steam-store-snapshots]: <https://github.com/woctezuma/steam-store-snapshots>

[openai-clip]: <https://github.com/openai/CLIP>
[banner-repository-CLIP]: <https://github.com/woctezuma/steam-CLIP>
[banner-repository-mobilenet-v3]: <https://github.com/woctezuma/match-steam-banners>
[banner-repository-mobilenet-v1]: <https://github.com/woctezuma/download-steam-banners>
[screenshot-repository-mobilenet-v1]: <https://github.com/woctezuma/download-steam-screenshots>

[filter_out_steam_banners]: <https://colab.research.google.com/github/woctezuma/steam-CLIP/blob/main/filter_out_steam_banners.ipynb>
[colab-badge]: <https://colab.research.google.com/assets/colab-badge.svg>
