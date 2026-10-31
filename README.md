# AutoPivot website

Website for AutoPivot at https://theautopivot.com. AutoPivot helps Australian car dealers find Japanese cars worth importing, cost them to the road and price the resale, then turn photos taken on a phone into studio listing photos.

It is a single static page (`index.html`) with its images and videos in `media/`, hosted with GitHub Pages from the `main` branch.

## Editing

Edit `index.html` and push to `main`. GitHub Pages republishes the site within a minute or two.

The sign-up form sends its details through [Web3Forms](https://web3forms.com) with the access key in `index.html` (`WEB3FORMS_ACCESS_KEY`). Messages arrive at the inbox that key was created for; the address itself is not on the site. To send to a different inbox, create a new key at web3forms.com and replace it.

## Custom domain

The site is served at https://theautopivot.com (domain registered with Squarespace). The `CNAME` file in this repo sets the domain for GitHub Pages.

DNS records at Squarespace:

- `A` records for `@`: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
- `CNAME` record for `www`: `agent47-2026.github.io`

## Photo and video credits

The RAV4 demo photos, the capture outline and the studio backdrop come from the AutoPivot app (autopivot-expo). The other photos and the car-carrier video come from Wikimedia Commons:

- Toyota Alphard GF (black) by Tokumeigakarinoaoshima, [CC0](https://commons.wikimedia.org/wiki/File:Toyota_ALPHARD_GF_(H30W)_front.jpg). Plate replaced.
- Toyota Alphard X (silver) by TTTNIS, [CC0](https://commons.wikimedia.org/wiki/File:2018-2023_Toyota_Alphard_X.jpg).
- Toyota Supra SZ (A80) by Tokumeigakarinoaoshima, [CC0](https://commons.wikimedia.org/wiki/File:Toyota_Supra_SZ_(A80)_front.jpg).
- 1999 Nissan Skyline GT-R by Calreyn88, [CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:1999_Nissan_Skyline_GT-R.jpg). Background and plate replaced in `media/studio-reveal.mp4`; the edited version is shared under CC BY-SA 4.0.
- Nissan Skyline GT-R V-spec, Brussels, by Matti Blume, [CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:Nissan_Skyline_GT-R_V-spec,_BAS_24,_Brussels_(P1170369-RR).jpg). Plate replaced; the edited image is shared under CC BY-SA 4.0.
- Adria Ace, Port of Melbourne, by Bernard Spragg, [CC0](https://commons.wikimedia.org/wiki/File:Adria_Ace._Car_carrier_Port_of_Melbourne._(21860228040).jpg).
- "Car carrier 01" video by Koffermejia, [CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:Car_carrier_01.webm). Trimmed and re-encoded (`media/carrier.mp4`); shared under CC BY-SA 4.0.

`media/rav4-studio.jpg`, `media/studio-reveal.mp4` and the replaced plates were made from these photos with [BiRefNet](https://huggingface.co/ZhengPeng7/BiRefNet) (MIT) for background removal and a [YOLOS licence-plate detector](https://huggingface.co/nickmuchi/yolos-small-finetuned-license-plate-detection), then assembled with FFmpeg.
