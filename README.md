# Telegram File Stream Frontend

A static HTML frontend for streaming and downloading Telegram files. Perfect for deployment on Vercel's free plan.

## 🚀 Live Demo

Deploy this repository to Vercel and access files like:
```
https://your-app.vercel.app/?file_url=https://api.telegram.org/file/bot123456/path/video.mp4
```

## ✨ Features

- **Universal Media Support**: Videos, audio, images, documents
- **Built-in Players**: HTML5 video/audio players with controls
- **Download Functionality**: Direct download from Telegram CDN
- **Mobile Responsive**: Works perfectly on all devices
- **Error Handling**: Graceful fallbacks for invalid links
- **Share Feature**: Copy link to clipboard or native sharing
- **Zero Backend**: Pure HTML, CSS, and JavaScript

## 🛠️ How It Works

1. **Query Parameter**: Reads `file_url` from URL parameters
2. **File Detection**: Automatically detects file type from extension
3. **Media Rendering**: Shows appropriate player (video/audio/image)
4. **Download Ready**: Provides instant download button

## 📱 Supported File Types

### Video Formats
- MP4, AVI, MOV, WMV, FLV, WebM, MKV, 3GP

### Audio Formats  
- MP3, WAV, OGG, AAC, FLAC, M4A

### Image Formats
- JPG, JPEG, PNG, GIF, WebP, BMP, SVG

### Document Formats
- PDF, DOC, DOCX, TXT, RTF, ZIP, RAR

## 🚀 Deployment on Vercel

### Quick Deploy

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/safielbit/telegram-file-stream)

### Manual Deployment

1. Fork or clone this repository
2. Go to [Vercel Dashboard](https://vercel.com/dashboard)
3. Click "New Project"
4. Import your GitHub repository
5. Deploy (no configuration needed!)

### Custom Domain (Optional)

After deployment, you can add a custom domain in Vercel settings.

## 🔗 URL Structure

Your deployed app will handle URLs like:

```
https://your-domain.vercel.app/?file_url=TELEGRAM_FILE_URL
```

**Example:**
```
https://my-stream.vercel.app/?file_url=https://api.telegram.org/file/bot123456:ABC/documents/file_1.pdf
```

## 🤖 Telegram Bot Integration

This frontend is designed to work with Telegram bots that generate file links. Your bot should:

1. Receive file uploads from users
2. Get file path from Telegram API
3. Generate streaming URL pointing to your Vercel deployment
4. Send the URL back to users

**Example bot response:**
```
🎥 Your video is ready!
Stream: https://your-app.vercel.app/?file_url=https://api.telegram.org/file/bot.../video.mp4
```

## 🎨 Customization

The frontend uses Bootstrap 5 and Feather Icons via CDN. You can customize:

- **Colors**: Modify the CSS gradient and color scheme
- **Layout**: Adjust Bootstrap classes and custom CSS
- **Features**: Add/remove functionality in the JavaScript

## 🔒 Security Notes

- Files are streamed directly from Telegram's CDN
- No files are stored on your Vercel deployment
- URLs are validated before loading
- CORS is handled automatically by browsers

## 📄 License

MIT License - feel free to use for personal or commercial projects.

## 🔧 Technical Details

- **Framework**: Pure HTML, CSS, JavaScript
- **Styling**: Bootstrap 5.1.3 (CDN)
- **Icons**: Feather Icons 4.29.0 (CDN)
- **Hosting**: Optimized for Vercel static hosting
- **Size**: Under 10KB total (excluding CDN resources)

Perfect for creating a professional file streaming service with zero server costs!