# 🎵 Nostr Playlists

> Discover and download decentralized music playlists from the Nostr network

[![Live Demo](https://img.shields.io/badge/🌐-Live%20Demo-blue)](https://nostrapps.github.io/playlists/)
[![MIT License](https://img.shields.io/badge/📄-MIT%20License-green)](LICENSE)
[![Nostr](https://img.shields.io/badge/⚡-Nostr%20Protocol-purple)](https://nostr.com/)

## 🌟 Features

- **🔍 Discover Playlists**: Browse music playlists shared on the Nostr decentralized network
- **📥 Download M3U Files**: Save playlists as standard .m3u files for use with any media player
- **🎨 Beautiful UI**: Modern, responsive interface with smooth animations
- **⚡ Real-time Updates**: Live connection to multiple Nostr relays for the latest content
- **🎯 No Server Required**: Fully client-side application - no backend needed
- **📱 Mobile Friendly**: Works seamlessly on desktop and mobile devices

## 🚀 Quick Start

### Online Usage

Simply visit **[nostrapps.github.io/playlists](https://nostrapps.github.io/playlists/)** to start discovering playlists immediately!

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/nostrapps/playlists.git
   cd playlists
   ```

2. **Serve the files locally**
   ```bash
   # Using Python
   python3 -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Using PHP
   php -S localhost:8000
   ```

3. **Open in browser**
   Navigate to `http://localhost:8000`

## 📖 Usage Guide

### Discovering Playlists

1. **Connect to Nostr**: Click "🔄 Fetch Latest Playlists" to connect to Nostr relays
2. **Browse Results**: Playlists will appear as cards showing:
   - Playlist name and metadata
   - Number of tracks and creation date
   - Author information with link to their Nostr profile
   - Complete track listings with thumbnails

### Downloading Playlists

1. **Find a Playlist**: Browse the discovered playlists
2. **Download**: Click the "📥 Download .m3u" button on any playlist card
3. **Use Anywhere**: Open the downloaded .m3u file in:
   - VLC Media Player
   - iTunes/Apple Music
   - Windows Media Player
   - Any M3U-compatible application

### Creating Playlists

- Click "➕ Create Playlist" to visit [mp3url.org](https://mp3url.org/create.html)
- Create your playlist and publish it to Nostr
- It will appear in the discovery feed for others to find

## 🏗️ Technical Architecture

### Core Technologies

- **Frontend**: Vanilla JavaScript, HTML5, CSS3
- **Protocol**: Nostr (Notes and Other Stuff Transmitted by Relays)
- **Format**: M3U/M3U8 playlist standard
- **Deployment**: GitHub Pages (static hosting)

### Nostr Integration

- **Event Type**: Kind 32100 (Playlist events)
- **Relays**: Connects to multiple public Nostr relays:
  - `wss://relay.damus.io`
  - `wss://nos.lol`
  - `wss://relay.nostr.band`
  - `wss://nostr-pub.wellorder.net`

### M3U Generation

The application generates standard M3U files with:
- `#EXTM3U` header
- Playlist metadata as comments
- `#EXTINF` entries with duration, logo, and group information
- Direct media URLs for playback

### Client-Side Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Web Browser   │────│  Nostr Relays   │────│  M3U Download   │
│                 │    │                 │    │                 │
│ • UI/UX         │    │ • WebSocket     │    │ • Blob API      │
│ • WebSocket     │    │ • JSON Events   │    │ • File Download │
│ • Event Parsing │    │ • Real-time     │    │ • Format Gen    │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 🛠️ Development

### Project Structure

```
playlists/
├── index.html          # Main application file
├── README.md          # This file
├── LICENSE            # MIT license
└── .gitignore         # Git ignore rules
```

### Key Components

- **NostrPlaylistApp**: Main application class
- **Relay Management**: WebSocket connections to Nostr relays
- **Event Processing**: Parsing of Nostr playlist events
- **M3U Generation**: Converting playlists to standard format
- **UI Rendering**: Dynamic playlist card creation

### Browser Compatibility

- ✅ Chrome/Chromium 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+
- ⚠️ Internet Explorer: Not supported (requires WebSocket and modern JavaScript)

## 🤝 Contributing

We welcome contributions! Here's how to get started:

### Development Setup

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes
4. Test thoroughly in multiple browsers
5. Commit with clear messages
6. Push and create a pull request

### Code Style

- Use modern JavaScript (ES6+)
- Follow existing indentation (2 spaces)
- Add comments for complex logic
- Ensure mobile responsiveness
- Test WebSocket connections

### Reporting Issues

Please use the [GitHub Issues](https://github.com/nostrapps/playlists/issues) page to:
- Report bugs
- Request features
- Ask questions
- Discuss improvements

## 📚 Related Projects

- **[Nostr Protocol](https://nostr.com/)**: The decentralized protocol powering this app
- **[MP3URL.org](https://mp3url.org/)**: Create and publish playlists to Nostr
- **[Nostr.rocks](https://nostr.rocks/)**: Explore Nostr users and content

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- The Nostr community for building an amazing decentralized protocol
- All relay operators maintaining the Nostr network
- Contributors and users of this application

---

**Built with ❤️ for the decentralized web**

*Discover music without borders, download without limits*