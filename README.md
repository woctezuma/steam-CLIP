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

It consists of **vertical** Steam banners (300x450 resolution, available for 29982 out of 48792 games, i.e. 61.4% of games).

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

[openai-clip]: <https://github.com/openai/CLIP>
[banner-repository-CLIP]: <https://github.com/woctezuma/steam-CLIP>
[banner-repository-mobilenet-v3]: <https://github.com/woctezuma/match-steam-banners>
[banner-repository-mobilenet-v1]: <https://github.com/woctezuma/download-steam-banners>
[screenshot-repository-mobilenet-v1]: <https://github.com/woctezuma/download-steam-screenshots>

[colab-badge]: <https://colab.research.google.com/assets/colab-badge.svg>
