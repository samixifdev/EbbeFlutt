name: ebbe-flutt # you probably want to 'snapcraft register <name>'
base: core22 # the base snap is the execution environment for this snap
version: '1.0.0' # just for humans, typically '1.2+git' or '1.3.2'
title: EbbeFlut
summary: Embark on an enchanting adventure in Ebbeflut! # 79 char long summary
description: |
  As a skilled navigator, you'll steer your vessel through treacherous currents, solve perplexing puzzles, and uncover the secrets hidden within the river's depths.

grade: stable # must be 'stable' to release into candidate/stable channels
confinement: strict # use 'strict' once you have the right plugs and slots

apps:
  ebbe-flutt:
    command: bin/ebbe-flutt-bin
    extensions: [gnome]
    plugs:
      - network
      - unity7
      - network-status

layout:
  /usr/lib/${SNAPCRAFT_ARCH_TRIPLET}/webkit2gtk-4.1:
    bind: $SNAP/gnome-platform/usr/lib/$SNAPCRAFT_ARCH_TRIPLET/webkit2gtk-4.0

parts:
  ebbe-flutt:
    plugin: dump
    source: .
    organize:
      ebbe-flutt-bin: bin/
