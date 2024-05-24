## Features

Very basic (but thorough) syntax highlighting for various IKEMEN GO code files, for Visual Studio Code.

## Installation
[Install vsce by following these instructions,](https://code.visualstudio.com/api/working-with-extensions/publishing-extension#vsce) then, run `vsce package` in the root of the extension's folder.

To install the resulting .vsix file, either run `code --install-extension ikemen-highlighting-0.5.0.vsix`, or open up VS Code, go to the Extensions view, click **Views and More Actions...**, and select **Install from VSIX...**.

## Known Issues
- This has not yet undergone rigorous testing, so there might be some things mishighlighted, or things that should be highlighted that aren't.
- There are a number of teneous leaps in logic to try and apply standard programming archetypes to MUGEN/IKEMEN stuff. For example: triggers are highlighted as functions, whereas state controllers are highlighted as classes. Trigger redirects are, for some reason, highlighted as regex (IKEMEN doesn't use regex so this should be fine, probably). The goal of all this is to try and ensure there is a lot of separatation and distinction made between each different type, even if the IKEMEN concepts are only roughly analogous to their respective highlighting rule.
- Because several triggers and state controllers have identical names (and because of certain inherent limitations in the TextMate language grammar system that defines the highlighting rules), picking what category to highlight them as presents a challenge. In general, the only major problem happens with `SprPriority`, which will be only highlighted as a state controller if there is a `{` immediately following it on the same line (in all other cases, it will be highlighted as a trigger).
- As a constantly updating engine, new triggers, state controllers, and others are constantly being added to IKEMEN's lexicon, so this is probably already out of date at time of release.

## Release Notes

### 0.5.0

Alpha release, .zss file compatability only.