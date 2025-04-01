FROM --platform=$TARGETOS/$TARGETARCH node:21-bullseye-slim

RUN apt update \
    && apt -y install ffmpeg iproute2 git sqlite3 libsqlite3-dev python3 python3-dev ca-certificates dnsutils tzdata zip tar curl build-essential libtool   

RUN npm install npm@latest -g

WORKDIR /app/data
COPY        ./../entrypoint.sh /entrypoint.sh
RUN         chmod +x /entrypoint.sh
# Corrected CMD section
CMD ["sh", "/entrypoint.sh"]
