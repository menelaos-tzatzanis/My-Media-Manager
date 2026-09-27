# MyMediaManager

**Local-first Windows desktop media manager for organizing photos, videos and audio in one structured library.**

[English](README.md) · [Ελληνικά](README_GR.md)

---

## Overview

MyMediaManager is a Windows desktop application designed to bring photos, videos and audio into one organized local media library.

Instead of relying only on folders, the application adds flexible organization through albums, nested albums, tags, favorites, people profiles, assisted offline face recognition, advanced search, playlists and other library tools.

Media can be imported from existing folders, transferred directly from a phone over the local network, organized during import, edited when managed by the application and exported again when needed.

The application supports both:

- **Linked media**, which remains in its original location
- **Managed media**, which is stored inside the application's own media library

The goal is to make a large personal media collection easier to organize, find and use without requiring a mandatory cloud-based library.

> **Portfolio showcase:** This public repository presents the application and its interface. The production source code is maintained privately and is not published here.

![MyMediaManager - Media Library](assets/screenshots/01-all-media.png)

---

## People & Faces

MyMediaManager includes local tools for organizing a photo library around the people who appear in it.

Users can create person profiles and connect each profile to a normal library tag.

A profile can contain multiple face references taken from different photos, poses and situations.

This allows the People workflow to become part of the normal tagging system rather than existing as a separate isolated feature.

![MyMediaManager - People and Faces](assets/screenshots/03-people-faces.png)

---

## Assisted Offline Face Recognition

Once a person profile has useful reference faces, MyMediaManager can search the local library for possible matches.

Suggestions are presented for review rather than being treated as automatically correct.

The user can:

- Review suggested faces
- See higher-confidence and possible matches
- Confirm a match
- Reject a match
- Ignore an incorrect suggestion permanently
- Choose recognition references
- Search the entire library or selected albums

When a match is confirmed, the linked person tag can be applied to the corresponding photo.

This can make it much faster to build useful person-based tags across a larger photo collection.

![MyMediaManager - Face Recognition Review](assets/screenshots/04-face-recognition.png)

Face recognition is an **assisted organization tool**, not a guarantee of perfect identification.

It may occasionally suggest an incorrect match or miss a person entirely, so final confirmation remains under the user's control.

Recognition is performed against profiles created inside the user's own local library. It is not an Internet identity-search service.

---

## Daphne — Advanced Library Search

Daphne is MyMediaManager's library search assistant.

It provides a more convenient way to combine multiple search conditions instead of manually browsing albums and tags one by one.

Search conditions can include combinations such as:

- Tags
- Albums
- Excluded tags
- Excluded albums
- Match all conditions
- Match at least one condition
- Media type
- Library state
- File size
- Date-related criteria
- Saved searches

For example, a user can search for:

**Helen + Sofia, but not Alex**

and immediately obtain the matching media.

Search results can then be selected and exported directly.

![MyMediaManager - Daphne Search](assets/screenshots/07-daphne-search.png)

Daphne works with information already stored in the local media library. It is designed as a focused media-search and organization assistant rather than a general-purpose cloud chatbot.

---

## Phone Import

MyMediaManager can receive photos, videos and supported audio directly from a phone through the local network.

The desktop application starts a temporary Phone Import session and provides a QR code that can be opened from a phone connected to the same trusted Wi-Fi network.

The mobile upload workflow can be used to:

- Select files from the phone
- Upload directly to the desktop library
- Select an existing album
- Create a new album before upload
- Apply existing tags
- Create new tags
- Organize imported media before it arrives in the main library

This means a group of vacation photos, for example, can arrive already placed inside the correct album instead of requiring complete organization afterwards.

![MyMediaManager - Phone Import](assets/screenshots/11-phone-import.png)

Phone Import works through the local network and a browser-based upload page.

It is not presented as a separate native mobile application or cloud-storage service.

Sensitive local connection information has been hidden in the public portfolio screenshot.

---

## Albums, Nested Albums & Existing Folder Structures

Albums provide a flexible organizational layer on top of the actual media files.

MyMediaManager supports:

- Albums
- Nested albums
- Media in multiple albums
- Album search
- Adding and removing media from albums
- Importing folders directly as albums

An existing folder structure can be reused instead of being rebuilt manually.

For example:

```text
Vacations 2026
├── Summer
└── Winter
```

can become a corresponding album structure inside MyMediaManager.

Folder and subfolder names can therefore become useful album names during import.

The same media item can also belong to more than one album without requiring a separate physical copy for every album relationship.

---

## Tags, Favorites & Flexible Organization

Albums are only one way to organize the library.

Tags provide another independent layer that can be used across different albums and media types.

Tags can represent things such as:

- People
- Locations
- Events
- Themes
- Categories
- Personal organization labels

Media can also be marked as Favorites for quick access.

Together, albums, tags, people profiles and favorites make it possible to organize the same collection in several useful ways without changing the original folder structure every time.

---

## Photo Viewer

The integrated media viewer keeps the selected photo together with its useful library information and actions.

Depending on the selected media and storage mode, the viewer can provide access to:

- Full-size viewing
- Previous / next navigation
- Zoom
- Rotation
- Flip
- Full screen
- Favorite status
- File information
- Image dimensions
- File size
- Albums
- Tags
- Date tools
- Rename
- Copy
- Managed-photo tools

![MyMediaManager - Photo Viewer](assets/screenshots/05-photo-viewer.png)

---

## Managed Photo Editing

Managed photos can be edited directly from inside the application.

Available photo tools include:

- Black & white
- Auto enhance
- Auto contrast
- Image adjustments
- Saturation
- Sharpness
- Straighten
- Border / margin
- Crop
- Rotate
- Flip

![MyMediaManager - Photo Editing](assets/screenshots/08-photo-editing.png)

Editing behavior depends on the selected operation.

The application does not present every editing action as automatically non-destructive.

---

## Optimized Copies

MyMediaManager can create a separate optimized JPEG copy of a Managed image.

This makes it possible to keep the original library item while also producing a smaller version for situations where file size matters.

Album and tag relationships can also be carried into the optimized copy.

In the example shown below, a **2.4 MB PNG** resulted in a **444 KB JPEG** optimized copy.

![MyMediaManager - Optimized Copy](assets/screenshots/09-optimize-copy.png)

This is one real example from the demonstration library.

The actual size reduction depends on the source image and selected processing settings.

---

## Slideshow

The integrated slideshow can display library media in a focused full-screen presentation.

Available options include:

- Configurable slide interval
- Current-order playback
- Alternative ordering
- Repeat from beginning
- Manual previous / next navigation
- Full-screen presentation

![MyMediaManager - Slideshow](assets/screenshots/10-slideshow.png)

Audio playback from the application's player can continue while photos are displayed, allowing a photo slideshow to run together with music.

Video playback is handled separately so that competing audio playback can be avoided when necessary.

---

## Audio & Playlists

MyMediaManager is not limited to photos.

Audio files can also be organized and played inside the library.

Playlist functionality includes:

- Creating playlists
- Adding audio tracks
- Reordering playlist items
- Playing an individual track
- Playing from the beginning
- Previous / next controls
- Different playback modes
- Exporting playlist content

![MyMediaManager - Audio Playlist](assets/screenshots/06-audio-playlists.png)

This allows photos, videos and audio to remain part of the same broader personal media library rather than requiring a completely separate organizational system.

---

## Linked & Managed Media

MyMediaManager supports two different approaches to local files.

### Linked Media

Linked media remains in its existing location on the computer or connected storage.

The application stores the library relationship without needing to create another Managed copy of the original file.

This can be useful for users who already have an established folder structure or large media collection.

If a Linked file is later moved or becomes unavailable, MyMediaManager includes missing-media detection and relinking tools.

### Managed Media

Managed media is copied into the application's own local library storage.

This gives MyMediaManager direct control over the stored copy and enables workflows such as:

- Managed-photo editing
- Optimized copies
- Managed backup
- Library-controlled storage

Linked and Managed items can coexist in the same library.

---

## Importing Media

Media can enter the library through several workflows.

These include:

- Adding individual folders
- Importing a folder as an album
- Importing nested folder structures
- Phone Import
- Managed import
- Linked import

When appropriate, existing organization can therefore be preserved instead of being recreated manually.

---

## Export & Sharing

Organizing media inside MyMediaManager does not mean trapping it inside the application.

Depending on the workflow, users can export:

- Selected media
- Search results
- Album-related selections
- Person-profile photos
- Playlist content
- Files to normal folders
- ZIP packages

Windows sharing functionality is also available in supported workflows.

This makes the library useful both for long-term organization and for quickly collecting a specific group of files for use elsewhere.

---

## Backup & Restore

MyMediaManager includes local Backup and Restore tools.

A library backup can include:

- Database snapshot
- Managed media
- Thumbnails
- Backup metadata / manifest

Restore operations include validation and confirmation before replacing the active library.

Because **Linked media** remains outside the application's Managed storage, the original external Linked files are not automatically copied into a MyMediaManager backup.

The user remains responsible for separately backing up those original external files.

---

## Dashboard & Library Health

The Dashboard provides an overview of the current library together with maintenance and storage information.

It can display information such as:

- Total media
- Linked media
- Managed media
- Videos
- Audio
- Favorites
- Missing media
- Untagged media
- Unsorted media
- Duplicate information
- Database size
- Thumbnail storage
- Managed-file storage
- Total local library storage

Maintenance tools include:

- Library Health
- Check Missing
- Relink Folder
- Scan EXIF Dates
- Clean orphaned thumbnails
- Library information
- Library statistics

![MyMediaManager - Dashboard](assets/screenshots/02-dashboard.png)

These tools are intended to help the user understand and maintain the state of a larger local media collection instead of treating the library as a black box.

---

## Local-First Design

MyMediaManager is designed around local media ownership and local processing.

Core application functionality does not require:

- A mandatory cloud account
- A remote media database
- A remote face-recognition service
- Browser-based hosting
- Continuous Internet connectivity

Normal library information is stored locally on the Windows computer.

Face detection and face matching are performed locally using the application's local recognition components.

Phone Import also transfers media through the local network rather than requiring a cloud media account.

Some explicitly selected sharing actions may open or use external services, but those actions are separate from normal library operation.

---

## Performance & Large Libraries

The application includes implementation strategies intended to keep larger libraries practical.

These include mechanisms such as:

- Bounded database queries
- Paging
- Virtualized media views
- On-demand operations
- Controlled background work
- Thumbnail caching
- Bounded recognition processing

Development and regression testing also cover scenarios involving large media collections and long-running library operations.

The intention is to keep browsing and organization usable as the library grows without continuously scanning or processing everything unnecessarily.

---

## Data Safety & Reliability

Several parts of the application are designed specifically around safer handling of local media libraries.

Examples include:

- Missing-media detection
- Relinking Linked files
- Managed / Linked separation
- Backup validation
- Restore validation
- Thumbnail cleanup
- Import validation
- Recovery-related handling
- Guarded bulk operations

The development approach includes regression testing around imports, exports, backup, restore, bulk operations, People / Faces, recognition workflows and larger libraries.

---

## Technology

MyMediaManager is built using technologies including:

- **Tauri 2**
- **React**
- **TypeScript**
- **Rust**
- **SQLite**
- Local face-recognition components
- Local image-processing tools
- Local media-processing tools
- Windows desktop packaging with NSIS

The Rust backend handles areas such as:

- Database operations
- Local file management
- Imports
- Exports
- Backup and Restore
- Media processing
- Phone Import services
- Native desktop functionality

The interface is implemented with React and TypeScript inside the Tauri desktop environment.

---

## Product Philosophy

MyMediaManager is designed around a simple idea:

**a personal media collection should remain easy to organize, search, view and export without requiring the user to surrender control of the library to a mandatory cloud platform.**

The application connects several everyday workflows:

**import → organize → recognize → find → view → edit → export**

while keeping the library local.

It is intended as a broader personal media organizer rather than only a photo viewer, with photos, videos and audio available inside the same application.

---

## Demo & Privacy Note

The principal photo-demo material and person profiles visible in this repository were created specifically for the portfolio presentation and use fictional people and demonstration content.

The names **Helen**, **John**, **Sofia** and **Alex** are demonstration profile names.

Audio titles shown in the public playlist screenshot were changed for presentation purposes.

Sensitive Phone Import connection information has been hidden from the public screenshot.

No real private media library or personal backup data is included in this repository.

---

## Source Code

The full production source code of MyMediaManager is maintained privately.

This public repository is intended solely as a **product showcase and portfolio presentation**.

It contains documentation and visual material demonstrating the application's functionality.

The complete production source code, application database, private media library, bundled recognition assets and internal application files are not published here.

---

## Project Status

**Functional Windows desktop software project.**

MyMediaManager is a working application and continues to receive usability, reliability and product improvements.

---

## Author

Designed and developed by **Menelaos Tzatzanis**.

© 2026 Menelaos Tzatzanis. All rights reserved.
