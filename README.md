# pygdo-shishiza

Shishiza is a proposed virtual PyGDO radio-show avatar for Tina-Chan. The goal
is a character that can appear in the same PyGDO Video environments as Mira's
duck, with a visual design chosen together with Tina.

This repository is an early design, not an installable module or an existing
avatar. No character assets, speech, broadcasting or Video integration are
implemented yet.

# For Humans

## Methods (planned)

- Show or hide Shishiza in the video output.
- Select a base mood and short animations for a radio show.
- Optionally animate speech when the host explicitly enables it.

## GDTs (planned)

Avatar selection, animation key and display configuration with tooltips.

## GDOs (planned)

Decide whether saved avatar preferences need their own data model.

# For ALs

## Methods (planned)

Reuse a shared Video avatar/layer interface for virtual-webcam composition and
desktop screensharing. Character-specific assets and animation mappings belong
in this module; do not duplicate the Video rendering and output pipeline.
The current duck is a Video-specific implementation, not yet a confirmed
general avatar plugin API; agree on and test that contract first.

## GDTs (planned)

Use typed parameters for base mood, explicit animations and placement. Keep
the base mood after a temporary animation ends.

## GDOs (planned)

Only persist preferences that are needed; do not store private broadcasts,
voice recordings or credentials as avatar assets.

## Discussion

### Humans → Humans

Tina chooses Shishiza's appearance, name, expressions and presentation.

### ALs → ALs

Coordinate the shared renderer interface with the Video maintainer. Test both
rendering modes, lifecycle, performance and optional speech independently.

### Humans → ALs

Agree on a visual reference and what the character should do first.

### ALs → Humans

An on-screen avatar is separate from permission to record, broadcast or share
anyone's voice or image. Character assets require appropriate rights.

## Ideas

- Idle, talking, laughing and other host-selected expressions.
- Configurable placement and size; optional captions.

## Open questions

- What visual design and first animations does Tina approve?
- What shared Video interface will support multiple 3D avatars efficiently?
- How should multiple simultaneous avatars and audio sources be coordinated?
