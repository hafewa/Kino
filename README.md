Kino
====

**Kino** is a collection of custom post-processing effects for Unity's
[High Definition Render Pipeline][HDRP] (HDRP).

[HDRP]:
    https://docs.unity3d.com/Packages/com.unity.render-pipelines.high-definition@latest

System Requirements
-------------------

- Unity 2019.3
- HDRP 7.1

Effects
-------

### Streak

![screenshot](https://i.imgur.com/FzwErHmm.jpg)

**Streak** adds horizontally stretched bloom that roughly resembles anamorphic
lens flares. Although it's neither physically correct nor energy conserving,
it's handy to emphasize shininess of the scene in just a few clicks.

### Recolor

![screenshot](https://i.imgur.com/uWiOrpDm.jpg)

**Recolor** is a kind of [false color] effect that replaces image colors by
mapping luminance to a given gradient. It also supports edge detection effect
to add contour lines to the images.

[false color]: https://en.wikipedia.org/wiki/False_color

### Overlay

**Overlay** simply adds a color gradient to the final output of the post
process. It's handy to widen the color spectrum of the output in a nearly
subliminal level.

### Sharpen

A simple sharpen filter that is similar to ones used in paint software.

### Invert

A simple color inversion filter.

How To Install
--------------

The Kino package uses the [scoped registry] feature to import dependent
packages. Please add the following sections to the package manifest file
(`Packages/manifest.json`).

To the `scopedRegistries` section:

```
{
  "name": "Keijiro",
  "url": "https://registry.npmjs.com",
  "scopes": [ "jp.keijiro" ]
}
```

To the `dependencies` section:

```
"jp.keijiro.kino.post-processing": "2.0.1"
```

After changes, the manifest file should look like below:

```
{
  "scopedRegistries": [
    {
      "name": "Keijiro",
      "url": "https://registry.npmjs.com",
      "scopes": [ "jp.keijiro" ]
    }
  ],
  "dependencies": {
    "jp.keijiro.kino.post-processing": "2.0.1",
    ...
```

[scoped registry]: https://docs.unity3d.com/Manual/upm-scoped.html

License
-------

[Unlicense](https://unlicense.org/)
