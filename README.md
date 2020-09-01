## Spotify - Like prediction and song's recommendation


### Dataset: song playlists fetched using Spotify API
 - Spotify for developers: https://developer.spotify.com/


### Build docker image to run the notebook

```
docker build -t spotify_img .
```

### Run notebook server in docker

```bash
docker run -it --rm \
    -p 8888:8888 \
    -v $(pwd)/notebooks:/home/jovyan/notebooks \
    -v $(pwd)/data:/data/ \
    -v $(pwd)/images:/images/ \
    spotify_img \
    jupyter notebook --notebook-dir /home/jovyan/notebooks
```
