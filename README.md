[![MELPA](https://melpa.org/packages/org-emms-badge.svg)](https://melpa.org/#/org-emms)

# org-emms

This package provides a new org link type for playing back multimedia files from org-mode using EMMS, The Emacs Multimedia System. If the link contains a track position, playback will start at the specified position. For example:

```
[[emms:/path/to/audio.mp3::2:43]]     Starts playback at 2 min 43 sec.
[[emms:/path/to/audio.mp3::1:10:45]]  Starts playback at 1 hr 10 min 45 sec.
[[emms:/path/to/audio.mp3::49]]       Starts playback at 0 min 49 sec.
```

The two main commands are `org-emms-insert-track` and `org-emms-insert-track-position`. The latter is especially useful for aligning text with audio when transcribing spoken language.

It is also possible to make a usual org link (with `org-store-link` command) from EMMS playlist and browser buffers, and then insert it into an org-mode buffer (with `org-insert-link` command).

## Open issue from Jelle Licht

### Support urls via emms-play-url

Does it make sense to have org-emms support urls as well? I currently hacked around things to support youtube videos in emms using MPV. If you think this is out of scope for org-emms, never mind.

If you do think it makes sense, I could try to clean up my hacks using e.g. `cl-defgeneric`.
