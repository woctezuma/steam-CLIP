# Steam CLIP: match Steam Banners with OpenAI's CLIP

[![Build status with Github Action][build-image-action]][build-action]
[![Code coverage][codecov-image]][codecov]
[![Code Quality][codacy-image]][codacy]

This repository contains Python code to retrieve Steam games with similar store banners, using [OpenAI's CLIP][openai-clip] (Contrastive Language-Image Pre-Training).

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

The most recent data snapshot was downloaded in August 2020 with [this Colab notebook][download_steam_banners].
[![Open In Colab][colab-badge]][download_steam_banners]
It consists of 19,049 **vertical** Steam banners resized from 300x450 to 256x256 resolution.

## Usage

TODO

## Results

TODO

## References

-   CLIP:
    - [OpenAI's CLIP][openai-clip]
    - [`steam-CLIP`][banner-repository-CLIP]: retrieve games with similar store banners, using OpenAI's CLIP (resolution 224),
-   MobileNet v3:
    - [`match-steam-banners`][banner-repository-mobilenet-v3]: retrieve Steam games with similar store banners, using MobileNet v3 (resolution 256),
-   MobileNet v1:
    - [`download-steam-banners`][banner-repository-mobilenet-v1]: retrieve Steam games with similar store banners, using MobileNet v1 (resolution 128),
    - [`download-steam-screenshots`][screenshot-repository-mobilenet-v1]: retrieve Steam games with similar store screenshots, using MobileNet v1 (resolution 128).

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

[openai-clip]: <https://github.com/openai/CLIP>
[banner-repository-CLIP]: <https://github.com/woctezuma/steam-CLIP>
[banner-repository-mobilenet-v3]: <https://github.com/woctezuma/match-steam-banners>
[banner-repository-mobilenet-v1]: <https://github.com/woctezuma/download-steam-banners>
[screenshot-repository-mobilenet-v1]: <https://github.com/woctezuma/download-steam-screenshots>

[colab-badge]: <https://colab.research.google.com/assets/colab-badge.svg>