# Map

Cube component `Map` from `@bosagent/cube-ui/map`.

Cube component. Source: `packages/cube-ui/src/components/map`.

## Import

```tsx
import { Map } from "@bosagent/cube-ui/map";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `aria-describedby` | `string` | No | `—` | — |
| `aria-label` | `string` | No | `—` | — |
| `aria-labelledby` | `string` | No | `—` | — |
| `children` | `ReactNode` | No | `—` | — |
| `isLoading` | `boolean` | No | `—` | Controlled loading veil shown over the map. |
| `mapStyle` | `MapStyleOption` | No | `—` | Single MapLibre-compatible style URL/object. Overrides `styles` when provided. |
| `onViewportChange` | `(viewport: MapViewport) => void` | No | `—` | Fired as the map moves. Used standalone or with `viewport` for controlled mode. |
| `projection` | `MapLibreGL.ProjectionSpecification` | No | `—` | Map projection. Use `{type: "globe"}` for globe maps. |
| `styles` | `{ dark?: MapStyleOption; light?: MapStyleOption; }` | No | `—` | Theme-aware MapLibre-compatible styles. Provide these from your app or map provider. |
| `theme` | `MapTheme` | No | `—` | Force a map theme. If omitted, the document class/system preference is used. |
| `viewport` | `Partial<MapViewport>` | No | `—` | Controlled viewport. Pair with `onViewportChange` to drive the map from React state. |
| `workerUrl` | `string` | No | `—` | Custom MapLibre worker URL. Applied via `maplibre.setWorkerUrl` before creating the map. |
| `anisotropicFilterPitch` | `number` | No | `—` | The pitch above which to apply anisotropic filtering to the map's raster layers (0-180). |
| `aroundCenter` | `boolean` | No | `—` | Determines the rotation interaction model: - When true: Uses "Orbital" logic where rotation is relative to the pivot center. Dragging right at the top rotates clockwise, while dragging right at the bottom rotates counter-clockwise (like spinning a physical globe). - When false: Uses "Linear" logic where horizontal mouse movement translates directly to bearing change regardless of cursor position. |
| `attributionControl` | `false \| AttributionControlOptions` | No | `—` | If set, an \{@link AttributionControl\} will be added to the map with the provided options. To disable the attribution control, pass `false`. !!! note Showing the logo of MapLibre is not required for using MapLibre. |
| `bearing` | `number` | No | `—` | The initial bearing (rotation) of the map, measured in degrees counter-clockwise from north. If `bearing` is not specified in the constructor options, MapLibre GL JS will look for it in the map's style object. If it is not specified in the style, either, it will default to `0`. |
| `bearingSnap` | `number` | No | `—` | The threshold, measured in degrees, that determines when the map's bearing will snap to north. For example, with a `bearingSnap` of 7, if the user rotates the map within 7 degrees of north, the map will automatically snap to exact north. |
| `bounds` | `LngLatBoundsLike` | No | `—` | The initial bounds of the map. If `bounds` is specified, it overrides `center` and `zoom` constructor options. |
| `boxZoom` | `boolean \| BoxZoomHandlerOptions` | No | `—` | If `true`, the "box zoom" interaction is enabled (see \{@link BoxZoomHandler\}). An `Object` value configures \{@link BoxZoomHandler\} options. If `boxZoomEnd` is provided, the callback runs instead of the default fit-to-box zoom. |
| `cancelPendingTileRequestsWhileZooming` | `boolean` | No | `—` | Determines whether to cancel, or retain, tiles from the current viewport which are still loading but which belong to a farther (smaller) zoom level than the current one. * If `true`, when zooming in, tiles which didn't manage to load for previous zoom levels will become canceled. This might save some computing resources for slower devices, but the map details might appear more abruptly at the end of the zoom. * If `false`, when zooming in, the previous zoom level(s) tiles will progressively appear, giving a smoother map details experience. However, more tiles will be rendered in a short period of time. |
| `canvasContextAttributes` | `WebGLContextAttributesWithType` | No | `—` | Set of WebGLContextAttributes that are applied to the WebGL context of the map. See https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement/getContext for more details. `contextType` is restricted to `'webgl2'`. This option is kept as a forward-looking API for future WebGPU support. |
| `center` | `LngLatLike` | No | `—` | The initial geographical centerpoint of the map. If `center` is not specified in the constructor options, MapLibre GL JS will look for it in the map's style object. If it is not specified in the style, either, it will default to `[0, 0]` !!! note MapLibre GL JS uses longitude, latitude coordinate order (as opposed to latitude, longitude) to match GeoJSON. |
| `centerClampedToGround` | `boolean` | No | `—` | If true, the elevation of the center point will automatically be set to the terrain elevation (or zero if terrain is not enabled). If false, the elevation of the center point will default to sea level and will not automatically update. Defaults to true. Needs to be set to false to keep the camera above ground when pitch \> 90 degrees. |
| `className` | `string` | No | `—` | — |
| `clickTolerance` | `number` | No | `—` | The max number of pixels a user can shift the mouse pointer during a click for it to be considered a valid click (as opposed to a mouse drag). |
| `collectResourceTiming` | `boolean` | No | `—` | If `true`, Resource Timing API information will be collected for requests made by GeoJSON and Vector Tile web workers (this information is normally inaccessible from the main Javascript thread). Information will be returned in a `resourceTiming` property of relevant `data` events. |
| `cooperativeGestures` | `boolean` | No | `—` | If `true` or set to an options object, the map is only accessible on desktop while holding Command/Ctrl and only accessible on mobile with two fingers. Interacting with the map using normal gestures will trigger an informational screen. With this option enabled, "drag to pitch" requires a three-finger gesture. Cooperative gestures are disabled when a map enters fullscreen using \{@link FullscreenControl\}. |
| `crossSourceCollisions` | `boolean` | No | `—` | If `true`, symbols from multiple sources can collide with each other during collision detection. If `false`, collision detection is run separately for the symbols in each source. |
| `doubleClickZoom` | `boolean` | No | `—` | If `true`, the "double click to zoom" interaction is enabled (see \{@link DoubleClickZoomHandler\}). |
| `dragPan` | `boolean \| DragPanOptions` | No | `—` | If `true`, the "drag to pan" interaction is enabled. An `Object` value is passed as options to \{@link DragPanHandler.enable\}. |
| `dragRotate` | `boolean` | No | `—` | If `true`, the "drag to rotate" interaction is enabled (see \{@link DragRotateHandler\}). |
| `elevation` | `number` | No | `—` | The elevation of the initial geographical centerpoint of the map, in meters above sea level. If `elevation` is not specified in the constructor options, it will default to `0`. |
| `fadeDuration` | `number` | No | `—` | Controls the duration of the fade-in/fade-out animation for label collisions after initial map load, in milliseconds. This setting affects all symbol layers. This setting does not affect the duration of runtime styling transitions or raster tile cross-fading. |
| `fitBoundsOptions` | `FitBoundsOptions` | No | `—` | A \{@link FitBoundsOptions\} options object to use _only_ when fitting the initial `bounds` provided above. |
| `hash` | `string \| boolean` | No | `—` | If `true`, the map's position (zoom, center latitude, center longitude, bearing, and pitch) will be synced with the hash fragment of the page's URL. For example, `https://example.com#2.59/39.26/53.07/-24.1/60`. An additional string may optionally be provided as an alternative to indicate a parameter-styled hash. For example, passing `hash: "foo"` will produce a hash like `https://example.com#foo=2.59/39.26/53.07/-24.1/60`. This is usefull for allowing multiple maps or other state. |
| `interactive` | `boolean` | No | `—` | If `false`, no mouse, touch, or keyboard listeners will be attached to the map, so it will not respond to interaction. |
| `keyboard` | `boolean` | No | `—` | If `true`, keyboard shortcuts are enabled (see \{@link KeyboardHandler\}). |
| `locale` | `Record<string, string>` | No | `—` | A patch to apply to the default localization table for UI strings, e.g. control tooltips. The `locale` object maps namespaced UI string IDs to translated strings in the target language; see `src/ui/default_locale.js` for an example with all supported string IDs. The object may specify all UI strings (thereby adding support for a new translation) or only a subset of strings (thereby patching the default translation table). For an example, see https://maplibre.org/maplibre-gl-js/docs/examples/locale-switching/ Alternatively, search the official plugins page for plugins related to localization. |
| `localIdeographFontFamily` | `string \| false` | No | `—` | Defines a CSS font-family for locally overriding generation of Chinese, Japanese, and Korean characters. For these characters, font settings from the map's style will be ignored, except for font-weight keywords (light/regular/medium/bold). Set to `false`, to enable font settings from the map's style for these glyph ranges. The purpose of this option is to avoid bandwidth-intensive glyph server requests. |
| `logoPosition` | `ControlPosition` | No | `—` | A string representing the position of the MapLibre wordmark on the map. Valid options are `top-left`,`top-right`, `bottom-left`, or `bottom-right`. |
| `maplibreLogo` | `boolean` | No | `—` | If `true`, the MapLibre logo will be shown. |
| `maxBounds` | `LngLatBoundsLike` | No | `—` | If set, the map will be constrained to the given bounds. |
| `maxCanvasSize` | `[number, number]` | No | `—` | The canvas' `width` and `height` max size. The values are passed as an array where the first element is max width and the second element is max height. You shouldn't set this above WebGl `MAX_TEXTURE_SIZE`. A larger canvas is not refused: the pixel ratio is lowered to fit and a warning is logged once. |
| `maxPitch` | `number` | No | `—` | The maximum pitch of the map (0-180). |
| `maxTileCacheSize` | `number` | No | `—` | The maximum number of tiles stored in the tile cache for a given source. If omitted, the cache will be dynamically sized based on the current viewport which can be set using `maxTileCacheZoomLevels` constructor options. |
| `maxTileCacheZoomLevels` | `number` | No | `—` | The maximum number of zoom levels for which to store tiles for a given source. Tile cache dynamic size is calculated by multiplying `maxTileCacheZoomLevels` with the approximate number of tiles in the viewport for a given source. |
| `maxZoom` | `number` | No | `—` | The maximum zoom level of the map. Users cannot zoom in beyond this level. (0–24) |
| `minPitch` | `number` | No | `—` | The minimum pitch of the map (0-180). |
| `minZoom` | `number` | No | `—` | The minimum zoom level of the map. Users cannot zoom out beyond this level. (0–24) |
| `pitch` | `number` | No | `—` | The initial pitch (tilt) of the map, measured in degrees away from the plane of the screen (0-85). If `pitch` is not specified in the constructor options, MapLibre GL JS will look for it in the map's style object. If it is not specified in the style, either, it will default to `0`. Values greater than 60 degrees are experimental and may result in rendering issues. If you encounter any, please raise an issue with details in the MapLibre project. |
| `pitchSpeed` | `number` | No | `—` | Degrees the map's pitch changes per pixel of vertical drag. Negative, so that dragging up pitches the map toward the horizon. |
| `pitchWithRotate` | `boolean` | No | `—` | If `false`, the map's pitch (tilt) control with "drag to rotate" interaction will be disabled. |
| `pixelRatio` | `number` | No | `—` | The pixel ratio. The canvas' `width` attribute will be `container.clientWidth * pixelRatio` and its `height` attribute will be `container.clientHeight * pixelRatio`. Defaults to `devicePixelRatio` if not specified. |
| `reduceMotion` | `boolean` | No | `—` | If `true`, gesture inertia (such as panning) is disabled. If not provided, gesture inertia defaults to the user's device settings. |
| `refreshExpiredTiles` | `boolean` | No | `—` | If `false`, the map won't attempt to re-request tiles once they expire per their HTTP `cacheControl`/`expires` headers. |
| `renderWorldCopies` | `boolean` | No | `—` | If `true`, multiple copies of the world will be rendered side by side beyond -180 and 180 degrees longitude. If set to `false`: - When the map is zoomed out far enough that a single representation of the world does not fill the map's entire container, there will be blank space beyond 180 and -180 degrees longitude. - Features that cross 180 and -180 degrees longitude will be cut in two (with one portion on the right edge of the map and the other on the left edge of the map) at every zoom level. |
| `roll` | `number` | No | `—` | The initial roll angle of the map, measured in degrees counter-clockwise about the camera boresight. If `roll` is not specified in the constructor options, MapLibre GL JS will look for it in the map's style object. If it is not specified in the style, either, it will default to `0`. |
| `rollEnabled` | `boolean` | No | `—` | If `false`, the map's roll control with "drag to rotate" interaction will be disabled. |
| `rotateSpeed` | `number` | No | `—` | Degrees the map's bearing changes per pixel of horizontal drag when rotating. |
| `scrollZoom` | `boolean \| AroundCenterOptions` | No | `—` | If `true`, the "scroll to zoom" interaction is enabled. \{@link AroundCenterOptions\} are passed as options to \{@link ScrollZoomHandler.enable\}. |

## Parts

- `Map.Arc`
- `Map.ClusterLayer`
- `Map.CompassControl`
- `Map.ControlButton`
- `Map.ControlGroup`
- `Map.ControlSeparator`
- `Map.Controls`
- `Map.FullscreenControl`
- `Map.LocateControl`
- `Map.Marker`
- `Map.MarkerContent`
- `Map.MarkerDot`
- `Map.MarkerLabel`
- `Map.MarkerPopup`
- `Map.MarkerTooltip`
- `Map.Popup`
- `Map.Route`
- `Map.ZoomControl`

## Example source

```tsx
'use client';

import { useState } from 'react';
import { Map } from '@components/map';
import { Card } from '@heroui/react';

const styles = {
  dark: 'https://basemaps.cartocdn.com/gl/dark-matter-gl-style/style.json',
  light: 'https://basemaps.cartocdn.com/gl/voyager-gl-style/style.json',
};

const dispatchRoute: [number, number][] = [
  [-122.39385, 37.79519],
  [-122.39412, 37.79548],
  [-122.39462, 37.79601],
  [-122.39475, 37.79603],
  [-122.39482, 37.79601],
  [-122.39483, 37.79588],
  [-122.39458, 37.79532],
  [-122.39435, 37.79502],
  [-122.39416, 37.79484],
  [-122.39367, 37.7945],
  [-122.3933, 37.79428],
  [-122.39325, 37.79425],
  [-122.39314, 37.79417],
  [-122.39271, 37.79382],
  [-122.39259, 37.7937],
  [-122.39225, 37.79339],
  [-122.39163, 37.79287],
  [-122.39134, 37.79255],
  [-122.39127, 37.79243],
  [-122.3911, 37.79204],
  [-122.39078, 37.79137],
  [-122.39051, 37.79105],
  [-122.39025, 37.79083],
  [-122.3899, 37.79056],
  [-122.38873, 37.78962],
  [-122.38853, 37.78939],
  [-122.38826, 37.78894],
  [-122.38803, 37.78805],
  [-122.38799, 37.78762],
  [-122.388, 37.78723],
  [-122.38802, 37.78699],
  [-122.38816, 37.78519],
  [-122.38819, 37.78489],
  [-122.38821, 37.78463],
  [-122.3884, 37.78232],
  [-122.38843, 37.78188],
  [-122.38846, 37.78135],
  [-122.38857, 37.78097],
  [-122.38886, 37.78059],
  [-122.38954, 37.78003],
  [-122.38978, 37.77985],
  [-122.39064, 37.77919],
  [-122.3908, 37.77907],
  [-122.39137, 37.77863],
  [-122.39186, 37.77823],
  [-122.39181, 37.77807],
  [-122.39161, 37.77791],
  [-122.39122, 37.7776],
  [-122.39107, 37.77749],
  [-122.39084, 37.77727],
  [-122.3907, 37.77716],
  [-122.39049, 37.77702],
  [-122.3901, 37.77652],
  [-122.39006, 37.77638],
  [-122.39003, 37.77614],
  [-122.38995, 37.77537],
  [-122.38995, 37.77468],
  [-122.38995, 37.77451],
  [-122.38995, 37.77443],
  [-122.38981, 37.77302],
  [-122.3898, 37.77286],
  [-122.38972, 37.77207],
  [-122.3897, 37.77181],
  [-122.38963, 37.77116],
  [-122.3896, 37.77076],
  [-122.38958, 37.77063],
  [-122.38945, 37.76919],
  [-122.38941, 37.76882],
  [-122.38919, 37.76884],
  [-122.38873, 37.76886],
  [-122.38779, 37.76892],
];

const stops = [
  {
    kind: 'start',
    label: 'Ferry Building',
    latitude: 37.79519,
    longitude: -122.39385,
    status: 'Pickup ready',
    time: '9:12 AM',
  },
  {
    kind: 'stop',
    label: 'Market Street',
    latitude: 37.7896,
    longitude: -122.3887,
    status: 'Next stop',
    time: '9:19 AM',
  },
  {
    kind: 'finish',
    label: 'Chase Center',
    latitude: 37.76892,
    longitude: -122.38779,
    status: 'Dropoff',
    time: '9:27 AM',
  },
];

const initialStop = stops[1]!;

export function Default() {
  const [selectedStop, setSelectedStop] = useState<
    (typeof stops)[number] | null
  >(initialStop);

  return (
    <div className="relative h-[70dvh] w-full overflow-hidden rounded-lg border">
      <Map
        center={[-122.3927, 37.7816]}
        className="absolute inset-0 size-full"
        pitch={26}
        styles={styles}
        zoom={13.25}
      >
        <Map.Route coordinates={dispatchRoute} />

        {stops.map((stop) => (
          <Map.Marker
            key={stop.label}
            latitude={stop.latitude}
            longitude={stop.longitude}
            onClick={() => setSelectedStop(stop)}
          >
            <Map.MarkerContent>
              <Map.MarkerDot
                color={stop.kind === 'start' ? '#22c55e' : undefined}
                ringColor={stop.kind === 'start' ? '#bbf7d0' : undefined}
              />
              <Map.MarkerLabel>
                {stop.kind === 'start' ? 'Start' : stop.label}
              </Map.MarkerLabel>
            </Map.MarkerContent>
            <Map.MarkerTooltip>
              <span className="font-medium">{stop.label}</span>
              <span className="ml-1 text-background/70">{stop.time}</span>
            </Map.MarkerTooltip>
          </Map.Marker>
        ))}

        {selectedStop ? (
          <Map.Popup
            closeButton
            closeOnClick={false}
            focusAfterOpen={false}
            latitude={selectedStop.latitude}
            longitude={selectedStop.longitude}
            offset={18}
            onClose={() => setSelectedStop(null)}
          >
            <div className="space-y-1 pr-4 text-xs">
              <p className="font-medium">{selectedStop.label}</p>
              <p className="text-muted">{selectedStop.status}</p>
              <p className="text-muted">Arrival {selectedStop.time}</p>
            </div>
          </Map.Popup>
        ) : null}

        <Map.Controls>
          <Map.ZoomControl />
          <Map.CompassControl />
          <Map.FullscreenControl />
        </Map.Controls>
      </Map>

      <Card className="absolute top-3 left-3 z-10 w-[230px] gap-3 bg-overlay p-4 shadow-overlay">
        <Card.Header>
          <Card.Title className="text-sm">Route planner</Card.Title>
          <Card.Description>Mission Bay dispatch</Card.Description>
        </Card.Header>
        <Card.Content className="grid grid-cols-3 gap-3 text-xs">
          <span>
            <strong className="block text-base text-foreground">7m</strong>
            ETA
          </span>
          <span>
            <strong className="block text-base text-foreground">3</strong>
            Stops
          </span>
          <span>
            <strong className="block text-base text-foreground">3.7</strong>
            Km
          </span>
        </Card.Content>
      </Card>
    </div>
  );
}
```
