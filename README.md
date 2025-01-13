# File and Folder Structure for jellyfin server & *arr Stack (radarr, sonarr, etc)

This mini quickstart guide offers useful links and explanations for setting up the file and folder structure for the Jellyfin server and *arr stack. 
The provided docker-compose file can be used to quickly set up a Jellyfin server and *arr stack environment.

⚠️ Important: Before running the docker-compose file, ensure that you create the necessary file structure as described in the links and using the Linux terminal commands provided below.

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
⚠️ Make sure that your user has the required permissions for the created file structure. If not, you may encounter permission issues when running jellyfin or *arr apps.

## Change ownership to your current user 
 ```sh
sudo chown -R your_users_name_here:your_users_name_here /mnt/data 
# Set the correct permissions 
sudo chmod -R 755 /mnt/data
```

## To Verify and Display File Structure
 ```sh
sudo apt install tree
tree /mnt/data
```
