FROM ubuntu:latest

WORKDIR /home

RUN mkdir /home/user

WORKDIR /home/user

RUN apt update && apt upgrade -y

RUN apt install -y software-properties-common \
    curl \
    libpulse0 \
    pulseaudio-utils \
    alsa-utils \
    wget \
    dotnet-runtime-8.0 \
    git \
    fonts-dejavu \
    sed \
    mpv \
    grep \
    ffmpeg \
    fzf \
    aria2 \
    yt-dlp \
    && rm -rf /var/lib/apt/lists/*

RUN git clone "https://github.com/pystardust/ani-cli.git"
WORKDIR /home/user/ani-cli
RUN cp ani-cli /usr/bin

WORKDIR /home/user


CMD ["/usr/bin/ani-cli"]
