# File and Folder Structure for jellyfin server & *arr Stack

This guide provides useful links and explanations for setting up the file and folder structure for the jellyfin server & *arr stack.
The docker-compose file can be used to immediatly setup a jellyfin and *arr stack env.

## Useful Links and Explanations

- [Trash Guides](https://trash-guides.info/)
- [File and Folder Structure](https://trash-guides.info/File-and-Folder-Structure/)
- [How to Set Up File and Folder Structure](https://trash-guides.info/File-and-Folder-Structure/How-to-set-up/)

## File Structure

```plaintext
mnt
└── data
    ├── torrents
    │   ├── books
    │   ├── movies
    │   ├── music
    │   └── tv
    ├── usenet
    │   ├── incomplete
    │   └── complete
    │       ├── books
    │       ├── movies
    │       ├── music
    │       └── tv
    └── media
        ├── books
        ├── movies
        ├── music
        └── tv
```

## Creating the File Structure in Linux Using Terminal
 ```sh
sudo mkdir -p /mnt/data
cd /mnt/data
sudo mkdir -p torrents/books torrents/movies torrents/music torrents/tv
sudo mkdir -p usenet/incomplete usenet/complete
sudo mkdir -p usenet/complete/books usenet/complete/movies usenet/complete/music usenet/complete/tv
sudo mkdir -p media/books media/movies media/music media/tv
```

## To Verify and Display File Structure
 ```sh
sudo apt install tree
tree /mnt/data
```
