# AgentPivot website

Marketing site for AgentPivot, which finds Japanese cars worth importing to Australia. It translates auction sheets, works out the landed and Victorian driveaway cost, and checks Australian resale prices.

It is a single static page (`index.html`) with its images and videos in `media/`, hosted with GitHub Pages from the `main` branch.

## Editing

Edit `index.html` and push to `main`. GitHub Pages republishes the site within a minute or two.

The early-access form is not connected to anything yet. To collect sign-ups, point it at a form service or your own backend.

## Custom domain

To serve the site from your own domain (for example `theagentpivot.com`):

1. Add a `CNAME` file to this repo containing the domain name.
2. At your DNS provider, point the apex domain's A records at GitHub Pages (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153) and add a `www` CNAME record pointing to `agent47-2026.github.io`.
3. In **Settings → Pages**, enter the domain and turn on **Enforce HTTPS** once the certificate is issued.

## Photo and video credits

All photos and the video come from Wikimedia Commons:

- Toyota Alphard GF (black) by Tokumeigakarinoaoshima, [CC0](https://commons.wikimedia.org/wiki/File:Toyota_ALPHARD_GF_(H30W)_front.jpg). Plate replaced.
- Toyota Alphard X (silver) by TTTNIS, [CC0](https://commons.wikimedia.org/wiki/File:2018-2023_Toyota_Alphard_X.jpg).
- Toyota Supra SZ (A80) by Tokumeigakarinoaoshima, [CC0](https://commons.wikimedia.org/wiki/File:Toyota_Supra_SZ_(A80)_front.jpg).
- 1999 Nissan Skyline GT-R by Calreyn88, [CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:1999_Nissan_Skyline_GT-R.jpg). Background and plate replaced (`media/r34-studio.jpg`); the edited image is shared under CC BY-SA 4.0.
- Nissan Skyline GT-R V-spec, Brussels, by Matti Blume, [CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:Nissan_Skyline_GT-R_V-spec,_BAS_24,_Brussels_(P1170369-RR).jpg). Plate replaced; the edited image is shared under CC BY-SA 4.0.
- Adria Ace, Port of Melbourne, by Bernard Spragg, [CC0](https://commons.wikimedia.org/wiki/File:Adria_Ace._Car_carrier_Port_of_Melbourne._(21860228040).jpg).
- "Car carrier 01" video by Koffermejia, [CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:Car_carrier_01.webm). Trimmed and re-encoded (`media/carrier.mp4`); shared under CC BY-SA 4.0.

The studio images and `media/studio-reveal.mp4` were made from these photos with [BiRefNet](https://huggingface.co/ZhengPeng7/BiRefNet) (MIT) for background removal and a [YOLOS licence-plate detector](https://huggingface.co/nickmuchi/yolos-small-finetuned-license-plate-detection), then assembled with FFmpeg.
