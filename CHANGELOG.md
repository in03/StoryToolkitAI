# Changelog

All notable changes to this project will be documented in this file, starting with version 0.17.7.

## [0.18.3] - 2023-05-02

### Info

Early update available for Patreon Frequent Users and Producers only - more info on [patreon.com/StoryToolkitAI](https://www.patreon.com/StoryToolkitAI)

### Added
- Group Questions - use AI to automatically detect and group questions from transcripts
- Ability to export transcript to Blackmagic Fusion Text+ via menu button
- Time Intervals in the Transcription Settings Window can now be set using timecodes too
- Show transcription in File Explorer menu button

### Fixes
- Fixed a bug that was preventing CUDA machines from using the CPU for transcriptions

## [0.18.2] - 2023-04-28

### Info

Early update available for Patreon Frequent Users and Producers only - more info on [patreon.com/StoryToolkitAI](https://www.patreon.com/StoryToolkitAI)
Please back up your StoryToolkitAI configuration folder before updating to this version if updating from 0.17

### Added
- Ability to use timecodes for copying transcript segments even without Resolve API connection
- Export to Avid DS format via menu button
- Transcriptions of audio rendered from Resolve are now auto-linked to their respective timelines

### Fixes
- The Find menu button now works correctly for all windows
- Disable Resolve API menu button now disables all Resolve-related menu buttons
- API Token is now validated correctly


## [0.18.1] - 2023-04-19

### Info
This update improves the usability of the Transcription Window and adds more menu buttons for easier access to features.

Early update available for Patreon Frequent Users and Producers only - more info on [patreon.com/StoryToolkitAI](https://www.patreon.com/StoryToolkitAI)
Please back up your StoryToolkitAI configuration folder before updating to this version if updating from 0.17

### Added
- Ability to export transcripts as SRT and Text files via menu buttons
- Most transcription related features are now available via menu buttons
- Connect and Disable Resolve API menu buttons
- Open Last Used Folder button in File menu 
- Custom Punctuation Marks via Preferences Window to be used for splitting segments on punctuation
- Warning when trying to add markers to non-linked timeline in Resolve

### Changed
- Resolve API connection is disabled by default on new tool installations - see [Connecting to the Resolve API](https://github.com/octimot/StoryToolkitAI/blob/main/FEATURES.md#connecting-to-the-resolve-api)
- Additional buttons on the Transcription Window for easier access to features

### Bugfixes
- Fixed a bug that prevented the tool from using some Resolve API features introduced in version 0.18.0
- Fixed a bug that didn't allow aligning and splitting segments according to Resolve playhead position

## [0.18.0] - 2023-04-11

### Info
Early update available for Patreon Frequent Users and Producers only - more info on [patreon.com/StoryToolkitAI](https://www.patreon.com/StoryToolkitAI)
Please back up your StoryToolkitAI configuration folder before updating to this version.

### Added
- Ability to cancel transcriptions from the queue
- Auto Add button in Transcription Groups allows adding of segments to group when they're selected 
- Select All button to Find feature in Transcription Window allows selecting all segments that match the search results
- Ability to Open Transcriptions and Transcribe via menu click
- Added Search and Assistant menus

### Changed
- Major restructuring of code and files, please backup StoryToolkit configuration folder before updating!
- New start command - see [here](https://github.com/octimot/StoryToolkitAI/blob/main/INSTALLATION.md#running-the-non-standalone-tool) 
- CMD/CTRL+A now also deselects segments in Transcription Window

### Bugfixes
- Resolve-related buttons now refresh correctly in the Transcription window on resolve connection status change
- Re-transcribing a re-transcribed transcription in the same session now works correctly
- Closing of transcription windows is now handled correctly
- Fixed a bug that prevented adding selected segments to groups with non-lowercase names 

## [0.17.19] - 2023-04-07

### Info
Early update available for Patreon Frequent Users and Producers only - more info on [patreon.com/StoryToolkitAI](https://www.patreon.com/StoryToolkitAI)

### Added
- Split On Punctuation setting in the Transcription Settings window - more info in  [Transcription Settings](https://github.com/octimot/StoryToolkitAI/blob/main/FEATURES.md#transcription-settings)
- Prevent Gaps Shorter Than setting in the Transcription Settings window - more info in [Transcription Settings](https://github.com/octimot/StoryToolkitAI/blob/main/FEATURES.md#transcription-settings)
- CMD+SHIFT+G in transcription window adds the selected segments to the currently selected group without clearing the group 
- Assistant [calc] function to get the minimum number of tokens you're sending with each message to OpenAI

### Bugfixes
- Fixed API token check default value
- Fixed project settings file check
- Fixed m shortcut bug in transcription window

## [0.17.18] - 2023-03-30

### Info

This update allows you to use ChatGPT for whatever section of your transcripts you want and leverage state-of-the-art AI in your process.
More ChatGPT-related optimizations will be added in the future!
Early update available for Patreon Frequent Users and Producers only - more info on [patreon.com/StoryToolkitAI](https://www.patreon.com/StoryToolkitAI)

### Added

- Direct interface to ChatGPT via Assistant window
- Key O sends selected transcript segments to Assistant window as context for conversation
- SHIFT+O includes times when sending transcript segments to Assistant window
- OpenAI Key entry in the Preferences window - needed to use ChatGPT

### Bugfixes

- Fixed a bug that prevented the tool from starting on Windows machines
- Fixed a formatting bug for text windows

## [0.17.17] - 2023-03-28

### Added

- Max. Words Per Line setting in the Transcription Settings window - more info in [Transcription Settings](https://github.com/octimot/StoryToolkitAI/blob/main/FEATURES.md#transcription-settings)
- Max. Characters Per Line setting in the Transcription Settings window - more info in [Transcription Settings](https://github.com/octimot/StoryToolkitAI/blob/main/FEATURES.md#transcription-settings)

### Bugfixes

- Fixed python_check and project path checks

## [0.17.16] - 2023-03-25

### Added

- Automatically disable Resolve API connection if running on a Windows machine and multiple Python versions are installed
- Tool accepts --skip-python-check argument to skip the above Python version check
- App Icons for Windows and MacOS

### Changed

- Improved the way the tool checks for updates internally

### Bugfixes

- Small interface improvements
- Advanced Search search_corpus_min_length can now be set via config.json to prevent the tool from not searching single-character languages properly.

## [0.17.15] - 2023-03-20

### Added

- "Increased Time Precision" gives better transcription timestamps due to the new openai-whisper module
- Tool now warns user on exit if there still are transcriptions in progress
- User can choose to not be notified about the current update
- User Token check - see [StoryToolkit on Patreon](https://www.patreon.com/StoryToolkitAI) for more info

### Bugfixes

- Fixed a bug that caused the transcription process to fail for files with an associated render.json file

## [0.17.14] - 2023-03-04

### Added

- Transcription progress now shown in the Transcription Log window
- Status change when tool is pre-detecting speech in the Transcription Log window
- mots_whisper.py (experimental - more info below)
- Auto-install of required packages if requirements are not met

### Changed

- Update notifications based on the user's machine and architecture for the standalone version

### Bugfixes

- Fixed a bug that caused the tool to ignore pre_detect_speech when reloading transcription queues at startup
- Fixed a bug that ignored transcribing audio without pre_detect_speech enabled

### Additional Info

- Starting with this update we're using a custom version of the openai-whisper module which will allow us more precise transcriptions and process visibility. 
- Word-level timings and other transcription-related updates coming soon!

## [0.17.13] - 2023-02-22

### Added

- Option to Pre-Detect Speech in the Transcription Settings window aiming to reduce the transcription time and AI hallucinations

### Additional Info

- Please use `pip install -r requirements.txt` to add the new required packages

## [0.17.12] - 2023-02-21

### Added

- The Advanced Search now supports changing the model using the command [model:<model_name>] (prompt [help] in Advanced Search for more details)
- The Advanced Search window now has a prompt history that can be navigated using the up and down arrow keys (only available for the current session)
- Preferences -> Skip Transcription Settings allows the user to make the Tool skip the Transcription Settings window on new transcriptions, by using the saved Transcription settings
- Tool Update notifications now include the CHANGE LOG for the new updates

### Fixed

- Transcription Log Window lets the user know when the log is empty instead of rendering and empty window
- Updated requirements.txt to use future==0.18.3 due to a security vulnerability in the previous future version

### Bugfixes

- Fixed crashes due to wrong encoding when reading certain files for Advanced Search
- Fixed re-opening of Preferences window causing a crash

### Additional Info

- Please use `pip install -r requirements.txt` to add the new required packages

## [0.17.11] - 2023-02-20

### Added

- CMD/CTRL+M in the Transcription Window now select all segments under markers filtered by color or name from the current Resolve timeline
- "Starts With" can be used to filter the markers to be rendered when using the "Render Markers to Stills" or "Render Markers to Clips" buttons
- When adding timeline markers from Transcription Window both the marker name and the color can be entered
- ESC key now closes the Transcription Settings window
- SHIFT+A if text is selected in the Transcription Window will now select all segments under that text

### Fixed

- Tool knows which window is currently focused - to be used for future features

## [0.17.10] - 2023-02-19

### Added

- Ability to semantically search markers from project.json files using the "Advanced Search" button in the main window 

### Changed

- Advanced Search is now performed in a console-like window to improve functionality and to preserve search history
- Advanced Search window now has a Find function (Ctrl/CMD+F) to search for text in the window

## [0.17.9] - 2023-02-18

### Added

- Advanced search results of text files are now opened and highlighted in a new window
- Resolve timeline markers are now saved in the project.json file to allow future project-wide marker searches
- Groups button in transcription window opens up the groups window for that transcription (same as SHIFT+G)

### Changed

- Find function in transcripts is now moved to its own window (use Ctrl/CMD+F to open it)

## [0.17.8] - 2023-02-17

### Added

- Ability to search semantically in any .txt file on your machine using the "Advanced Search" button in the main window
- Advanced search caching for significantly faster searches
- Using --noresolve argument on main script disables Resolve API polling for that run

## [0.17.7] - 2023-02-08

### Changed

- Switched to new openai-whisper module which supports the large-v2 model

### Bugfixes

- Fixed a few Resolve API communication issues on timeline and project change
