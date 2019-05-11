FROM python:3   
LABEL maintainer="M Matos me@mmatos.com"

    EXPOSE 8000

# uncomment following line in case you need to download tgz file
# RUN wget https://wallet.trezor.io/data/mytrezor-archive.tgz

# uncomment following line in case you arealdy downloaded tgz file
    ADD mytrezor-archive.tgz .
    WORKDIR /mytrezor
    # ENTRYPOINT [ "/usr/local/bin/python3" ]
    CMD ["python", "-m", "http.server", "8000"]
