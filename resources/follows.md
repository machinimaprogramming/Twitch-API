# Follows (Unstable)

**Warning:** This API method is currently experimental and the format may change without warning.

### Get a list of followed channels

`GET /users/:login/follows/channels`

#### Response

```json
{
  "_links": {
    "self": "https://api.twitch.tv/kraken/users/hebo/follows/channels/funami"
  },
  "channel": {
    "name": "funami",
    "game": null,
    "created_at": "2011-05-01T14:50:12Z",
    "teams": [],
    "background": null,
    "updated_at": "2012-10-13T18:18:43Z",
    "banner": null,
    "logo": "http://static-cdn.jtvnw.net/jtv_user_pictures/funami-profile_image-9bd02ad8f4f5bc97-300x300.jpeg",
    "url": "http://www.twitch.tv/funami",
    "_links": {
      "stream_key": "https://api.twitch.tv/kraken/channels/funami/stream_key",
      "self": "https://api.twitch.tv/kraken/channels/funami",
      "chat": "https://api.twitch.tv/kraken/chat/funami",
      "commercial": "https://api.twitch.tv/kraken/channels/funami/commercial",
      "videos": "https://api.twitch.tv/kraken/channels/funami/videos",
      "features": "https://api.twitch.tv/kraken/channels/funami/features"
    },
    "_id": 22125774,
    "mature": true,
    "video_banner": null,
    "display_name": "Funami",
    "status": "Not Live"
  }
}
```

### Follow a user

`PUT /users/:user/follows/channels/:target`

**[Authenticated]**  Scope: `user_follows_edit`

In the above path, `:user` is the authenticated user's name and `:target` is the name of the user to be followed.

#### Response

```json
{
  "_links": {
    "self": "https://api.twitch.tv/kraken/users/hebo/follows/channels/funami"
  },
  "channel": {
    "name": "funami",
    "game": null,
    "created_at": "2011-05-01T14:50:12Z",
    "teams": [],
    "background": null,
    "updated_at": "2012-10-13T18:18:43Z",
    "banner": null,
    "logo": "http://static-cdn.jtvnw.net/jtv_user_pictures/funami-profile_image-9bd02ad8f4f5bc97-300x300.jpeg",
    "_links": {
      "stream_key": "https://api.twitch.tv/kraken/channels/funami/stream_key",
      "self": "https://api.twitch.tv/kraken/channels/funami",
      "chat": "https://api.twitch.tv/kraken/chat/funami",
      "commercial": "https://api.twitch.tv/kraken/channels/funami/commercial",
      "videos": "https://api.twitch.tv/kraken/channels/funami/videos",
      "features": "https://api.twitch.tv/kraken/channels/funami/features"
    },
    "url": "http://www.twitch.tv/funami",
    "_id": 22125774,
    "mature": true,
    "video_banner": null,
    "display_name": "Funami",
    "status": "Not Live"
  }
}
```

### Unfollow a user

`DELETE /users/:user/follows/channels/:target`

**[Authenticated]**  Scope: `user_follows_edit`

In the above path, `:user` is the authenticated user's name and `:target` is the name of the user to be followed.

#### Response

`204 No Content` if successful.