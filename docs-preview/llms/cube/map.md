# Map

Cube component `Map` from `@bosagent/cube-ui/map`.

- 分层：Cube
- 包：`@bosagent/cube-ui/map`
- 状态：建设中

## Import

```tsx
import { Map } from "@bosagent/cube-ui/map";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 否 | `—` | — |
| `isLoading` | `boolean` | 否 | `—` | Controlled loading veil shown over the map. |
| `mapStyle` | `MapStyleOption` | 否 | `—` | Single MapLibre-compatible style URL/object. Overrides `styles` when provided. |
| `projection` | `MapLibreGL.ProjectionSpecification` | 否 | `—` | Map projection. Use `{type: "globe"}` for globe maps. |
| `styles` | `{ dark?: MapStyleOption; light?: MapStyleOption; }` | 否 | `—` | Theme-aware MapLibre-compatible styles. Provide these from your app or map provider. |
| `theme` | `MapTheme` | 否 | `—` | Force a map theme. If omitted, the document class/system preference is used. |
| `viewport` | `Partial<MapViewport>` | 否 | `—` | Controlled viewport. Pair with `onViewportChange` to drive the map from React state. |
| `workerUrl` | `string` | 否 | `—` | Custom MapLibre worker URL. Applied via `maplibre.setWorkerUrl` before creating the map. |
| `anisotropicFilterPitch` | `number` | 否 | `—` | The pitch above which to apply anisotropic filtering to the map's raster layers (0-180). |
| `aroundCenter` | `boolean` | 否 | `—` | Determines the rotation interaction model: - When true: Uses "Orbital" logic where rotation is relative to the pivot center. Dragging right at the top rotates clockwise, while dragging right at the bottom rotates counter-clockwise (like spinning a physical globe). - When false: Uses "Linear" logic where horizontal mouse movement translates directly to bearing change regardless of cursor position. |
| `attributionControl` | `false \| AttributionControlOptions` | 否 | `—` | If set, an \{@link AttributionControl\} will be added to the map with the provided options. To disable the attribution control, pass `false`. !!! note Showing the logo of MapLibre is not required for using MapLibre. |
| `bearing` | `number` | 否 | `—` | The initial bearing (rotation) of the map, measured in degrees counter-clockwise from north. If `bearing` is not specified in the constructor options, MapLibre GL JS will look for it in the map's style object. If it is not specified in the style, either, it will default to `0`. |
| `bearingSnap` | `number` | 否 | `—` | The threshold, measured in degrees, that determines when the map's bearing will snap to north. For example, with a `bearingSnap` of 7, if the user rotates the map within 7 degrees of north, the map will automatically snap to exact north. |
| `bounds` | `LngLatBoundsLike` | 否 | `—` | The initial bounds of the map. If `bounds` is specified, it overrides `center` and `zoom` constructor options. |
| `boxZoom` | `boolean \| BoxZoomHandlerOptions` | 否 | `—` | If `true`, the "box zoom" interaction is enabled (see \{@link BoxZoomHandler\}). An `Object` value configures \{@link BoxZoomHandler\} options. If `boxZoomEnd` is provided, the callback runs instead of the default fit-to-box zoom. |
| `cancelPendingTileRequestsWhileZooming` | `boolean` | 否 | `—` | Determines whether to cancel, or retain, tiles from the current viewport which are still loading but which belong to a farther (smaller) zoom level than the current one. * If `true`, when zooming in, tiles which didn't manage to load for previous zoom levels will become canceled. This might save some computing resources for slower devices, but the map details might appear more abruptly at the end of the zoom. * If `false`, when zooming in, the previous zoom level(s) tiles will progressively appear, giving a smoother map details experience. However, more tiles will be rendered in a short period of time. |
| `canvasContextAttributes` | `WebGLContextAttributesWithType` | 否 | `—` | Set of WebGLContextAttributes that are applied to the WebGL context of the map. See https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement/getContext for more details. `contextType` is restricted to `'webgl2'`. This option is kept as a forward-looking API for future WebGPU support. |
| `center` | `LngLatLike` | 否 | `—` | The initial geographical centerpoint of the map. If `center` is not specified in the constructor options, MapLibre GL JS will look for it in the map's style object. If it is not specified in the style, either, it will default to `[0, 0]` !!! note MapLibre GL JS uses longitude, latitude coordinate order (as opposed to latitude, longitude) to match GeoJSON. |
| `centerClampedToGround` | `boolean` | 否 | `—` | If true, the elevation of the center point will automatically be set to the terrain elevation (or zero if terrain is not enabled). If false, the elevation of the center point will default to sea level and will not automatically update. Defaults to true. Needs to be set to false to keep the camera above ground when pitch \> 90 degrees. |
| `className` | `string` | 否 | `—` | — |
| `clickTolerance` | `number` | 否 | `—` | The max number of pixels a user can shift the mouse pointer during a click for it to be considered a valid click (as opposed to a mouse drag). |
| `collectResourceTiming` | `boolean` | 否 | `—` | If `true`, Resource Timing API information will be collected for requests made by GeoJSON and Vector Tile web workers (this information is normally inaccessible from the main Javascript thread). Information will be returned in a `resourceTiming` property of relevant `data` events. |
| `cooperativeGestures` | `boolean` | 否 | `—` | If `true` or set to an options object, the map is only accessible on desktop while holding Command/Ctrl and only accessible on mobile with two fingers. Interacting with the map using normal gestures will trigger an informational screen. With this option enabled, "drag to pitch" requires a three-finger gesture. Cooperative gestures are disabled when a map enters fullscreen using \{@link FullscreenControl\}. |
| `crossSourceCollisions` | `boolean` | 否 | `—` | If `true`, symbols from multiple sources can collide with each other during collision detection. If `false`, collision detection is run separately for the symbols in each source. |
| `doubleClickZoom` | `boolean` | 否 | `—` | If `true`, the "double click to zoom" interaction is enabled (see \{@link DoubleClickZoomHandler\}). |
| `dragPan` | `boolean \| DragPanOptions` | 否 | `—` | If `true`, the "drag to pan" interaction is enabled. An `Object` value is passed as options to \{@link DragPanHandler.enable\}. |
| `dragRotate` | `boolean` | 否 | `—` | If `true`, the "drag to rotate" interaction is enabled (see \{@link DragRotateHandler\}). |
| `elevation` | `number` | 否 | `—` | The elevation of the initial geographical centerpoint of the map, in meters above sea level. If `elevation` is not specified in the constructor options, it will default to `0`. |
| `fadeDuration` | `number` | 否 | `—` | Controls the duration of the fade-in/fade-out animation for label collisions after initial map load, in milliseconds. This setting affects all symbol layers. This setting does not affect the duration of runtime styling transitions or raster tile cross-fading. |
| `fitBoundsOptions` | `FitBoundsOptions` | 否 | `—` | A \{@link FitBoundsOptions\} options object to use _only_ when fitting the initial `bounds` provided above. |
| `hash` | `string \| boolean` | 否 | `—` | If `true`, the map's position (zoom, center latitude, center longitude, bearing, and pitch) will be synced with the hash fragment of the page's URL. For example, `https://example.com#2.59/39.26/53.07/-24.1/60`. An additional string may optionally be provided as an alternative to indicate a parameter-styled hash. For example, passing `hash: "foo"` will produce a hash like `https://example.com#foo=2.59/39.26/53.07/-24.1/60`. This is usefull for allowing multiple maps or other state. |
| `interactive` | `boolean` | 否 | `—` | If `false`, no mouse, touch, or keyboard listeners will be attached to the map, so it will not respond to interaction. |
| `keyboard` | `boolean` | 否 | `—` | If `true`, keyboard shortcuts are enabled (see \{@link KeyboardHandler\}). |
| `locale` | `Record<string, string>` | 否 | `—` | A patch to apply to the default localization table for UI strings, e.g. control tooltips. The `locale` object maps namespaced UI string IDs to translated strings in the target language; see `src/ui/default_locale.js` for an example with all supported string IDs. The object may specify all UI strings (thereby adding support for a new translation) or only a subset of strings (thereby patching the default translation table). For an example, see https://maplibre.org/maplibre-gl-js/docs/examples/locale-switching/ Alternatively, search the official plugins page for plugins related to localization. |
| `localIdeographFontFamily` | `string \| false` | 否 | `—` | Defines a CSS font-family for locally overriding generation of Chinese, Japanese, and Korean characters. For these characters, font settings from the map's style will be ignored, except for font-weight keywords (light/regular/medium/bold). Set to `false`, to enable font settings from the map's style for these glyph ranges. The purpose of this option is to avoid bandwidth-intensive glyph server requests. |
| `logoPosition` | `ControlPosition` | 否 | `—` | A string representing the position of the MapLibre wordmark on the map. Valid options are `top-left`,`top-right`, `bottom-left`, or `bottom-right`. |
| `maplibreLogo` | `boolean` | 否 | `—` | If `true`, the MapLibre logo will be shown. |
| `maxBounds` | `LngLatBoundsLike` | 否 | `—` | If set, the map will be constrained to the given bounds. |
| `maxCanvasSize` | `[number, number]` | 否 | `—` | The canvas' `width` and `height` max size. The values are passed as an array where the first element is max width and the second element is max height. You shouldn't set this above WebGl `MAX_TEXTURE_SIZE`. A larger canvas is not refused: the pixel ratio is lowered to fit and a warning is logged once. |
| `maxPitch` | `number` | 否 | `—` | The maximum pitch of the map (0-180). |
| `maxTileCacheSize` | `number` | 否 | `—` | The maximum number of tiles stored in the tile cache for a given source. If omitted, the cache will be dynamically sized based on the current viewport which can be set using `maxTileCacheZoomLevels` constructor options. |
| `maxTileCacheZoomLevels` | `number` | 否 | `—` | The maximum number of zoom levels for which to store tiles for a given source. Tile cache dynamic size is calculated by multiplying `maxTileCacheZoomLevels` with the approximate number of tiles in the viewport for a given source. |
| `maxZoom` | `number` | 否 | `—` | The maximum zoom level of the map. Users cannot zoom in beyond this level. (0–24) |
| `minPitch` | `number` | 否 | `—` | The minimum pitch of the map (0-180). |
| `minZoom` | `number` | 否 | `—` | The minimum zoom level of the map. Users cannot zoom out beyond this level. (0–24) |
| `pitch` | `number` | 否 | `—` | The initial pitch (tilt) of the map, measured in degrees away from the plane of the screen (0-85). If `pitch` is not specified in the constructor options, MapLibre GL JS will look for it in the map's style object. If it is not specified in the style, either, it will default to `0`. Values greater than 60 degrees are experimental and may result in rendering issues. If you encounter any, please raise an issue with details in the MapLibre project. |
| `pitchSpeed` | `number` | 否 | `—` | Degrees the map's pitch changes per pixel of vertical drag. Negative, so that dragging up pitches the map toward the horizon. |
| `pitchWithRotate` | `boolean` | 否 | `—` | If `false`, the map's pitch (tilt) control with "drag to rotate" interaction will be disabled. |
| `pixelRatio` | `number` | 否 | `—` | The pixel ratio. The canvas' `width` attribute will be `container.clientWidth * pixelRatio` and its `height` attribute will be `container.clientHeight * pixelRatio`. Defaults to `devicePixelRatio` if not specified. |
| `reduceMotion` | `boolean` | 否 | `—` | If `true`, gesture inertia (such as panning) is disabled. If not provided, gesture inertia defaults to the user's device settings. |
| `refreshExpiredTiles` | `boolean` | 否 | `—` | If `false`, the map won't attempt to re-request tiles once they expire per their HTTP `cacheControl`/`expires` headers. |
| `renderWorldCopies` | `boolean` | 否 | `—` | If `true`, multiple copies of the world will be rendered side by side beyond -180 and 180 degrees longitude. If set to `false`: - When the map is zoomed out far enough that a single representation of the world does not fill the map's entire container, there will be blank space beyond 180 and -180 degrees longitude. - Features that cross 180 and -180 degrees longitude will be cut in two (with one portion on the right edge of the map and the other on the left edge of the map) at every zoom level. |
| `roll` | `number` | 否 | `—` | The initial roll angle of the map, measured in degrees counter-clockwise about the camera boresight. If `roll` is not specified in the constructor options, MapLibre GL JS will look for it in the map's style object. If it is not specified in the style, either, it will default to `0`. |
| `rollEnabled` | `boolean` | 否 | `—` | If `false`, the map's roll control with "drag to rotate" interaction will be disabled. |
| `rotateSpeed` | `number` | 否 | `—` | Degrees the map's bearing changes per pixel of horizontal drag when rotating. |
| `scrollZoom` | `boolean \| AroundCenterOptions` | 否 | `—` | If `true`, the "scroll to zoom" interaction is enabled. \{@link AroundCenterOptions\} are passed as options to \{@link ScrollZoomHandler.enable\}. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `aria-describedby` | `string` | 否 | `—` | — |
| `aria-label` | `string` | 否 | `—` | — |
| `aria-labelledby` | `string` | 否 | `—` | — |
| `onViewportChange` | `(viewport: MapViewport) => void` | 否 | `—` | Fired as the map moves. Used standalone or with `viewport` for controlled mode. |

</details>

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

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Map
