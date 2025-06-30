# Facebook Auto Friend Request Bot

## 📋 Project Overview

This is a Python-based automation script that uses Selenium WebDriver to automatically send friend requests on Facebook. The script navigates to Facebook's friend suggestions page and automatically sends friend requests to suggested users.

## ⚠️ **IMPORTANT WARNINGS**

### Terms of Service Violations
- **This script may violate Facebook's Terms of Service**
- Automated friend requests can lead to account restrictions or permanent bans
- Facebook actively detects and prevents automated behavior

### Privacy and Ethical Concerns
- Sending automated friend requests to strangers may be considered inappropriate
- Consider the privacy and comfort of others before using this tool
- Respect Facebook's community standards

### Account Security Risks
- Your Facebook account may be flagged or suspended
- Use at your own risk and discretion
- Consider using a test account if available

## 🚀 Features

- **Automated Login**: Automatic Facebook login using provided credentials
- **Friend Suggestions Navigation**: Automatically navigates to Facebook's friend suggestions page
- **Smart Button Detection**: Finds and clicks "Add Friend" buttons using XPath selectors
- **Auto Scrolling**: Automatically scrolls down to load more suggestions
- **Error Handling**: Includes basic error handling for failed clicks
- **Progress Tracking**: Shows progress with emoji indicators

## 📦 Requirements

### Python Dependencies
```bash
pip install selenium
```

### System Requirements
- Python 3.6 or higher
- Google Chrome browser
- Chrome WebDriver (automatically managed by Selenium)

## 🛠️ Installation & Setup

1. **Clone or download the project**
   ```bash
   git clone <repository-url>
   cd "Facebook Auto Frnd"
   ```

2. **Install dependencies**
   ```bash
   pip install selenium
   ```

3. **Configure credentials**
   - Open `facebook.py`
   - Replace the placeholder credentials:
     ```python
     EMAIL = "your_facebook_email_or_phone"
     PASSWORD = "your_facebook_password"
     ```

4. **Run the script**
   ```bash
   python facebook.py
   ```

## 📝 Code Structure

### Main Components

```python
# Configuration
EMAIL = "your_facebook_email_or_phone"
PASSWORD = "your_facebook_password"

# WebDriver Setup
driver = webdriver.Chrome()
driver.get("https://www.facebook.com/")

# Login Process
email_input = driver.find_element(By.ID, "email")
password_input = driver.find_element(By.ID, "pass")
# ... login logic

# Friend Request Automation
driver.get("https://www.facebook.com/friends/suggestions")
# ... automation loop
```

### Key Functions

1. **Login Automation**: Handles Facebook login process
2. **Navigation**: Moves to friend suggestions page
3. **Button Detection**: Finds "Add Friend" buttons using XPath
4. **Auto Scrolling**: Scrolls to load more suggestions
5. **Error Handling**: Manages click failures gracefully

## ⚙️ Configuration Options

### Adjustable Parameters

```python
# Number of scroll iterations (default: 30)
for i in range(30):

# Delay between friend requests (default: 1.5 seconds)
time.sleep(1.5)

# Delay after scrolling (default: 4 seconds)
time.sleep(4)

# Login wait time (default: 10 seconds)
time.sleep(10)
```

### Recommended Safe Settings

For safer operation, consider these modifications:

```python
# Reduce number of requests
for i in range(10):  # Instead of 30

# Increase delays
time.sleep(3)  # Between requests
time.sleep(8)  # After scrolling
```

## 🚨 Safety Recommendations

### Before Running
1. **Review Facebook's Terms of Service**
2. **Consider using a test account**
3. **Start with small numbers of requests**
4. **Monitor your account for warnings**

### During Operation
1. **Don't run multiple instances simultaneously**
2. **Monitor the browser for any security prompts**
3. **Be prepared to stop if you receive warnings**

### After Running
1. **Check your Facebook account status**
2. **Review any friend request responses**
3. **Monitor for account restrictions**

## 🔧 Troubleshooting

### Common Issues

1. **"element click intercepted"**
   - Facebook's interface changes frequently
   - Try increasing delays between actions
   - The script includes error handling for this

2. **Login failures**
   - Check your credentials
   - Ensure 2FA is disabled or handled
   - Try manual login first

3. **Chrome WebDriver issues**
   - Ensure Chrome is up to date
   - Selenium should auto-manage WebDriver

### Error Messages

- `🟢 Found X Add Friend buttons`: Successfully found buttons
- `✅ Friend request sent`: Successfully sent request
- `⚠️ Could not click button`: Click failed (handled gracefully)
- `❌ Error in scroll loop`: General error in main loop

## 📊 Usage Statistics

The script is designed to:
- Send up to 30 friend requests per session
- Handle multiple suggestions per scroll
- Continue despite individual failures
- Provide real-time progress feedback

## 🤝 Contributing

If you want to improve this project:

1. **Focus on safety improvements**
2. **Add better error handling**
3. **Implement rate limiting**
4. **Add configuration options**

## 📄 License

This project is for educational purposes only. Use responsibly and at your own risk.

## ⚖️ Disclaimer

- This tool is provided "as is" without warranties
- Users are responsible for compliance with Facebook's Terms of Service
- The authors are not responsible for any account restrictions or bans
- Use at your own risk and discretion

## 🔗 Related Resources

- [Facebook Terms of Service](https://www.facebook.com/terms)
- [Selenium Documentation](https://selenium-python.readthedocs.io/)
- [Facebook Community Standards](https://www.facebook.com/communitystandards/)

---

**Remember**: Respect others' privacy and Facebook's community standards. Use automation tools responsibly and ethically.

## 👨‍💻 Developer Promotion

Developed by: **❤️ MD SAHADAT HOSSAIN ❤️**
- 🚀 For custom automation solutions, freelance projects, or collaboration, contact me at: fiverprince34@gmail.com
- 🌐 Portfolio: [developersahadat.vercel.app](https://developersahadat.vercel.app)
- 💬 Connect on LinkedIn: [your-linkedin-profile](https://linkedin.com/in/your-linkedin-profile)

---

# 🚧 Coming Soon Project

Stay tuned for upcoming features and improvements:
- ✅ Gender and location-based friend request filtering (with privacy and ethical considerations)
- ✅ Enhanced error handling and reporting
- ✅ Configurable friend request limits and delays
- ✅ Support for other social platforms
- ✅ User-friendly GUI for easier operation

Have suggestions? Open an issue or contact the developer! 
