# Embedding videos in Help Center

Chatwoot's Help Center supports automatic embedding of videos from multiple platforms. When you paste supported video URLs on their own lines (surrounded by empty lines), they will be automatically converted to embedded video players.

## Supported Video Platforms

| Platform | URL Format | How to Get the URL |  
|----------|------------|---------------------|  
| YouTube | `https://www.youtube.com/watch?v=VIDEO_ID` or `https://youtu.be/VIDEO_ID` | Copy URL from browser address bar or use "Share" button |  
| Vimeo | `https://vimeo.com/VIDEO_ID` | Copy URL from browser address bar or use "Share" button |  
| Loom | `https://loom.com/share/VIDEO_ID` | Use "Share" button after recording or from video library |  
| Wistia | `https://SUBDOMAIN.wistia.com/medias/VIDEO_ID` | Copy URL from browser or use "Share & Embed" option |  
| Arcade | `https://app.arcade.software/share/VIDEO_ID` | Use "Share" button from your demo library |  
| Bunny CDN | `https://iframe.mediadelivery.net/play/LIBRARY_ID/VIDEO_ID` | Get iframe URL from Bunny CDN dashboard |  
| Direct MP4 | Any URL ending in `.mp4` | Use direct link to MP4 file from any hosting service |

## Important Requirements

1. **Empty Lines**: Video URLs must be surrounded by empty lines (blank lines above and below)

2. **Standalone Links**: The URL must be on its own line, not embedded in other text

3. **Must be a Link:** The URL must be formatted as a clickable link in markdown (not plain text)                                        

4. **Exact Format**: URLs must match the exact patterns shown above

The video embedding system automatically detects these patterns and replaces the URLs with responsive video players that work across all devices.
