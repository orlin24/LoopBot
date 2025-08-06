# LoopBot - YouTube Live Stream Automation Tool

## 🚀 Features

- **Automated YouTube Live Streaming** - Create and manage multiple live streams
- **License System** - Secure licensing with offline mode support
- **Content Management** - Auto-rotate titles, randomize content, avoid duplicates
- **Advanced Settings** - Duration control, delay management, concurrent streams
- **Comprehensive Setup Guide** - Step-by-step instructions for beginners
- **Interactive Tooltips** - Hover help for all settings
- **Clean Logging** - Timestamp-based activity logs in Indonesian

## 📋 Setup Requirements

1. **YouTube API Credentials**
   - Google Cloud Console project
   - YouTube Data API v3 enabled
   - OAuth 2.0 credentials

2. **License** 
   - Valid license from http://loopbotiq.com
   - Required for full functionality

3. **Content Files**
   - `titles.txt` - Stream titles (one per line)
   - `descriptions.txt` - Stream descriptions (supports spintax)
   - `keystream.txt` - YouTube stream keys (one per line)
   - `thumbnails/` folder - Thumbnail images (1280x720 recommended)

## 🛠️ Installation

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install customtkinter google-auth google-auth-oauthlib google-auth-httplib2 google-api-python-client pillow requests cryptography
   ```
3. Copy `client_secrets_example.json` to `client_secrets.json`
4. Add your Google OAuth credentials to `client_secrets.json`
5. Run the application:
   ```bash
   python run.py
   ```

## ⚙️ Settings Explained

### Duration
- **Format**: Hours:Minutes:Seconds (HH:MM:SS)
- **Example**: `00:10:00` = 10 minutes
- **Recommendation**: Start with 10-15 minutes for testing

### Delay
- **Purpose**: Time between creating new streams
- **Unit**: Minutes
- **Recommendation**: 3-5 minutes for safety
- **Why**: Prevents YouTube rate limiting

### Max Duplicates
- **Purpose**: How many times one stream key can be used simultaneously
- **Beginner**: Use 1 (one key = one stream)
- **Advanced**: 2-3 maximum
- **Warning**: Higher values may cause conflicts

### Checkboxes

- **Filter Low Viewers**: Avoid time slots with few viewers (recommended: OFF for beginners)
- **Auto-Rotate Titles**: Change title for each new stream (recommended: ON)
- **Randomize Content**: Select content randomly vs sequentially (recommended: ON)
- **Avoid Duplicates**: Prevent same content from repeating (recommended: ON)

## 📱 License Verification

The application shows different license states:

- **✅ Active License**: Full access with expiry date
- **❌ Not Activated**: License key required
- **❌ Expired**: License renewal needed
- **❌ Invalid**: License not recognized or blocked

## 🆘 Support

- **Setup Guide**: Click "Setup Guide" button in the application
- **Documentation**: Comprehensive tooltips on hover
- **License**: Contact http://loopbotiq.com

## 🔐 Security

- Credentials are stored securely
- License verification with device binding
- No sensitive data in repository
- Local encryption for cached data

## 📄 License

This is a proprietary application requiring a valid license for operation.