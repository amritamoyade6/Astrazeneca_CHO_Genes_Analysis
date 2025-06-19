# Installation Instructions

## 1. Python dependencies

Install all Python packages with:

    ```bash
    pip install -r requirements.txt
    ```

## 2. MEME Suite isn’t distributed via PyPI. To install from source:

    1.	Download the latest release

        wget https://meme-suite.org/meme-software/5.5.0/meme-5.5.0.tar.gz

    2.	Extract

        tar -zxvf meme-5.5.0.tar.gz
        cd meme-5.5.0

    3.	Configure (you can specify an install prefix)

        ./configure --prefix=/usr/local/meme

    4.	Build & install

        make
        sudo make install

    5.	Add to your PATH (e.g. in ~/.bashrc or ~/.zshrc)

        export PATH="/usr/local/meme/bin:$PATH"

    6.	Verify

        meme --version
        fimo --version

Once done, you’ll have the meme and fimo commands available for your motif analyses.