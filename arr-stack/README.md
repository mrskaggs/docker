# Media Automation Docker Compose

This project sets up a media automation system using Docker Compose. The following services are included: Jackett, Radarr, qBittorrent, SABnzbd, Sonarr, and Overseerr.

## Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Services

### Jackett

Jackett works as a proxy server and translates queries from Sonarr and Radarr to search various torrent sites.

### Radarr

Radarr is a movie collection manager for Usenet and BitTorrent users.

### qBittorrent

qBittorrent is an open-source BitTorrent client.

### SABnzbd

SABnzbd is an open-source binary newsreader written in Python.

### Sonarr

Sonarr is a PVR for Usenet and BitTorrent users to download TV shows.

### Overseerr

Overseerr is a request management and media discovery tool for the Plex ecosystem.

## Setup Instructions

1. **Install Docker and Docker Compose:**  
   Follow the official instructions for [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/install/).

2. **Create Directory Structure:**  
   Create the necessary directories for configurations and media files:
   ```sh
   mkdir -p /srv/docker/jackett/config
   mkdir -p /srv/docker/radarr/config
   mkdir -p /srv/docker/qbittorrent/config
   mkdir -p /srv/docker/sabnzbd/config
   mkdir -p /srv/docker/sonarr/config
   mkdir -p /srv/docker/overseerr/config
   mkdir -p /mnt/media/Movies
   mkdir -p /mnt/media/Shows
   mkdir -p /mnt/media/downloads

3. **Adjust User and Group IDs:**  
   Ensure the PUID and PGID values match your system's user and group IDs. You can find these by running:
   ```sh
   id $(whoami)

4. **Adjust Timezones:**  
   Update the TZ environment variable to match your local timezone.

5. **Start the Services:**  
   Run Docker Compose to start all services:
   ```sh
   docker-compose up -d

6. **Access the Services:**  
   - Jackett: http://<your-docker-host>:9117
   - Radarr: http://<your-docker-host>:7878
   - qBittorrent: http://<your-docker-host>:8080
   - SABnzbd: http://<your-docker-host>:8081
   - Sonarr: http://<your-docker-host>:8989
   - Overseerr: http://<your-docker-host>:5055

## Setup Instructions

- **Adjust User and Group IDs:** 
