FROM ubuntu:latest

WORKDIR /home

RUN mkdir /home/user

WORKDIR /home/user

RUN apt-get update && apt-get install -y \
    software-properties-common \
    findutils \
    coreutils \
    bash \
    fish \
    gawk \
    apt-transport-https \
    ca-certificates \
    gnupg \
    curl \
    wget \
    dotnet-runtime-8.0 \
    libgtk-4-1 \
    libadwaita-1-0 \
    libwebkit2gtk-4.1-0 \
    libgl1 \
    libgl1-mesa-dri \
    at-spi2-core \
    dbus-x11 \
    adwaita-icon-theme \
    fonts-dejavu \
    libwebkitgtk-6.0-4 \
    libnotify4 \
    libnss3 \
    libxss1 \
    xdg-utils \
    git \
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


CMD ["/usr/bin/ani-cli"]
