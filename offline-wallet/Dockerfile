FROM python:3   

# uncomment following line in case you need to download tgz file
# RUN wget https://wallet.trezor.io/data/mytrezor-archive.tgz

# uncomment following line in case you arealdy downloaded tgz file
    ADD mytrezor-archive.tgz .

    RUN tar zxvfp mytrezor-archive.tgz .

    ENTRYPOINT [ "python3 -m http.server 8000" ] 