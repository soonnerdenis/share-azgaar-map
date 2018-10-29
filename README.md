# 🗺️ share-azgaar-map

Small app to generate links to maps generated by azgaar/fantasy-map-generator.

![](https://user-images.githubusercontent.com/15332326/47097431-afd4f600-d231-11e8-99ef-a92c0705cef3.gif)

## Links

* frontend -- https://map-share.now.sh/
* service -- https://map-share-service.now.sh/

## 🔌 Development

### `yarn updateSubmodules`

Pulls map generator.

### `yarn dev`

Serves map generator and launches service and frontend dev servers.

#### process.env.IP

Test on local network.

```
  yarn cross-env IP="192.168.137.1" yarn dev c f s
```

## Deployment

### Add secrets to now

```
now secrets add DROPBOX_ACCESS_TOKEN "access-token"
```

## 🔍 About and todo lists

- `/azgaars-map-generator` **[submodule]** <- my fork of azgaar's map generator
  - Added map upload from link in query -- `?maplink=<link-to-map>`
- `/map-share-service` <- uploads maps and generates access links \
   _Needs `DROPBOX_ACCESS_TOKEN` in `process.env`._
  - permalinks for maps on dropbox -- `<url>/<map-name>.map`
- `/map-share-frontend` <- catalog of maps uploaded with the app
