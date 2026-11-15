# YouTube Downloader

This repository downloads YouTube videos with GitHub Actions and publishes them in a ZIP file attached to a GitHub Release.

## Run a download

1. Open **Actions** and select **Download YouTube Videos**.
2. Select **Run workflow**.
3. Enter one or more YouTube URLs, separated by spaces or new lines. URLs can be for individual videos, playlists, or channels (for example, a channel's `/videos` page).
4. Run the workflow. When it finishes, open the Release created by that run and download `youtube-downloads.zip`.

The ZIP contains MP4 videos named after their YouTube titles, with the video ID included to avoid filename collisions. Playlist and channel URLs download their available videos.

For videos that require your account, add a repository Actions secret named `YOUTUBE_COOKIES` containing cookies in Netscape format. Do not commit cookies to the repository.

Downloads are subject to YouTube availability and GitHub Actions/Release size and runtime limits. A large channel may exceed the six-hour workflow timeout or the 2 GB per-file GitHub Release limit.
