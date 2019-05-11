FROM python:3   

# uncomment following line in case you need to download tgz file
# RUN wget https://wallet.trezor.io/data/mytrezor-archive.tgz

# uncomment following line in case you arealdy downloaded tgz file
    ADD mytrezor-archive.tgz .
#    WORKDIR /mytrezor
    CMD [ "/usr/local/bin/python3", "-m", "http.server 8000" ]
    EXPOSE 8000
