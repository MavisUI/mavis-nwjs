# mavis-nwjs

## Was erreicht werden muss...

Die Software mit der Rheinknie-Brücke läuft nach yarn build und yarn dev so wie sie im Repo ist. Die Rheinknie-Brücke muss raus und die Oberkasseler rein, ohne Prüfergebnisse, die muss mein Dad dann anlegen.

## Stand

-   Habe unter app/data einen neuen Order "oberkassel" angelegt und da die Daten reinkopiert (struktur identisch zu den Daten in /rheinknie nur andere Inhalte).
-   Dann in app/data/appstate.de die Einträge von rheinknie auf oberkassel geändert
-   Und in app/react/Store.js auch von rheinknie auf oberkassel gedreht
-   gebaut und yarn dev gestartet... applikation startet und hängt...

## Debugging

Hab' ich nicht... Mein verdacht ist, dass nwjs im nwFlavor=sdk laufen muss und nicht tut, meine Versuche das zu ändern sind aber gescheitert... Mehr dazu unter https://docs.nwjs.io/en/latest/For%20Users/Debugging%20with%20DevTools/#open-developer-tools

## Anmerkungen

-   Ein Unterschied ist, dass es nur 4 Kameras gibt und nicht 6 wie bei der Rheinknie...

## Basic Setup

Orignially taken from this boilerplate: https://github.com/jarden-liu/node-webkit-webpack-starter (make sure to install the nwjs SDK). All other stuff included can be found in package.json.

## App Structure

```javascript
package.json
README.md
/app
  index.html
  index.js
  nwjs.json
  styles.less
  /assets
    /fonts
    /js
  /components
    /..
  /data
    appstate.db
    /[bridgename]
      classes.db
      construction.db
      metrics.db
      modules.db
      results.db
      /0
      /1
      /...
/build
  build.js
  config.js
  hotReload.js
  server.js
  utils.js
  webpack.config.js
  webpack.dev.config.js
  webpack.prod.config.js
/dist
/node_modules
```

## Structure

### Global

-   /app/components/Data
-   /app/components/Filter
-   /app/components/Global
-   /app/components/Header
-   /app/components/LoadingScreen
-   /app/components/MainMenu
-   /app/components/Notifications
-   /app/components/Pages

### Report

-   /app/components/Report

### 3D Model

-   /app/components/Model

### Visual Inspection

-   /app/components/Inspection

### Settings

-   /app/components/Settings
