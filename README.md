# microfreak-patches

![](https://medias.arturia.net/cdn-cgi/image/quality=80/images/products/microfreak/de-content-7.png)

This repository contains 2 python scripts:
- `src/0_preprocess.ipynb` to parse `.mfprojz` preset banks into `csv` format
- `src/1_process.ipynb` to categorize presets by instrument type and generate preset banks

Some learnings from the experiment:
- `.mfprojz` files are just `.zip` files in disguise, you can just rename them, unzip them and look into them
- preset banks are made of `.mbp` files
- to create a custom preset bank, let's call it `Freaky sounds`, you need to:
    - have a folder named `Freaky sounds`
    - have a subfolder, under `Freaky sounds`, named `01-Freaky sounds-A`
    - have all your `.mbp` presets inside the `01-Freaky sounds-A` folder, making sure to name each one incrementally like this:
        - `01-Freaky sounds-A1.mbp`
        - `01-Freaky sounds-A2.mbp`
        - ...
- the Arturia MIDI Control Center usually freaks (xD) out if you try to import those banks while the Microfreak is plugged in, so make sure to do those imports with the Microfreak turned off

## TLDR

The presets, grouped by instrument type, can be found [here](https://github.com/Zatfer17/microfreak-patches/tree/main/patches/generated) and they comprehend:
- _Factory 3.0_
- _New Presets 4.0_
- _New Presets 5.0_
- _Factory 6.0_

and all the [official free sound banks from Arturia](https://www.arturia.com/store/presets-sound-banks?filters=%257B%2522compatible_hosts_and_instruments%2522%253A%255B%252201dp22zyr0vsg29a5hkn2m271r%2522%255D%252C%2522is_free%2522%253A%2522true%2522%257D&p=1)

## Usage

If you want to run the scripts yourself you need to:
- clone the repo
- have Python installed
- create a venv with:
`python -m venv .venv`
- activate the venv with:
`source .venv/bin/activate`
- install the requirements with:
`pip install -r requirements.txt`
- run the notebooks using the venv as kernel