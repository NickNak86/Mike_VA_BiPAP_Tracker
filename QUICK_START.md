# Quick Start Guide - Mike's BiPAP Tracker for Android Studio

Welcome! This guide will help you get Mike's BiPAP Tracker app running in Android Studio, even if you're new to Android development.

## 🚀 Opening the Project

### Step 1: Launch Android Studio
1. Open Android Studio
2. If you see the Welcome screen:
   - Click **"Open"**
   - Navigate to this folder: `/home/user/Mike_BiPAP_Tracker`
   - Click **"OK"**

3. If Android Studio is already open:
   - **File → Open**
   - Navigate to `/home/user/Mike_BiPAP_Tracker`
   - Click **"OK"**

### Step 2: Wait for Gradle Sync
- Android Studio will automatically detect the project
- You'll see "Syncing..." or "Building..." at the bottom
- **First time takes 2-5 minutes** - this is normal!
- Wait until you see "Gradle sync completed" or "Build successful"

### Step 3: Verify Project Structure
In the left panel (Project view), you should see:
```
Mike_BiPAP_Tracker
├── app
│   ├── src
│   │   └── main
│   │       ├── java/com/cpaptracker/
│   │       ├── res/
│   │       └── AndroidManifest.xml
│   └── build.gradle.kts
├── gradle/
└── build.gradle.kts
```

---

## 🔧 First-Time Setup

### Check Required Components

1. **Open SDK Manager:**
   - **Tools → SDK Manager** (or click the SDK Manager icon in toolbar)

2. **Verify these are installed:**
   - ✅ Android SDK Platform 34 (Android 14)
   - ✅ Android SDK Build-Tools 34.0.0
   - ✅ Android Emulator (if you don't have a physical device)

3. Click **"Apply"** if anything needs to be installed

### Set Up a Device

**Option A: Use Your Samsung Phone**
1. On your phone: **Settings → About Phone**
2. Tap **"Build Number"** 7 times (enables Developer Mode)
3. Go back to **Settings → Developer Options**
4. Enable **"USB Debugging"**
5. Connect phone to computer via USB
6. Accept the debugging prompt on your phone

**Option B: Create a Virtual Device (Emulator)**
1. **Tools → Device Manager**
2. Click **"Create Device"**
3. Select **"Phone" → "Pixel 6"** (or similar)
4. Select **API Level 34** system image
5. Click **"Finish"**

---

## ▶️ Running the App

### First Run

1. **Select Device:**
   - Look at the top toolbar
   - Click the device dropdown (next to the Run button ▶️)
   - Select your connected phone or emulator

2. **Click the Run Button:**
   - Green ▶️ button in top toolbar (or press **Shift+F10**)
   - If using emulator, it will start automatically (takes 1-2 minutes first time)

3. **Watch the Build:**
   - Bottom panel shows build progress
   - First build takes 2-5 minutes
   - You'll see "BUILD SUCCESSFUL" when ready

4. **App Launches:**
   - App automatically installs and opens on device
   - You'll see the BiPAP Tracker dashboard!

### What You'll See on First Launch

1. **Permission Request:**
   - The app will ask for notification permissions
   - Tap **"Allow"** to enable replacement reminders

2. **Dashboard Screen:**
   - Pre-loaded with your ResMed AirCurve 10 VAuto
   - Shows 7 replacement parts
   - All parts show "Not Tracked" initially

3. **Getting Started:**
   - Tap **"Replaced"** on each part when you first install them
   - This starts tracking from today
   - The app will calculate future replacement dates

---

## 📱 Using the App

### Initialize Your Parts

When you first install the app, tap **"Replaced"** for each part on the day you installed it:

1. **Go to "All Parts" tab** (bottom navigation)
2. For each part, tap the **"Replaced"** button:
   - Mask Cushion
   - Mask Frame
   - Headgear
   - Air Filter
   - Water Chamber
   - Tubing
   - Elbow Connector

3. The app will automatically calculate when each part needs replacement based on manufacturer schedules

### Understanding Status Colors

- 🟢 **Green (OK)** - Part is good, replacement not due yet
- 🟠 **Orange (Due Soon)** - Replace within 7 days
- 🔴 **Red (Overdue)** - Past replacement date
- 🔵 **Blue (Ordered)** - You've ordered a replacement
- ⚪ **Gray (Not Tracked)** - Part hasn't been initialized yet

### Daily Usage

1. **Check Dashboard** - See upcoming replacements at a glance
2. **Get Notifications** - App reminds you 7 days before parts are due
3. **Mark as Replaced** - When you replace a part, tap "Replaced"
4. **Track Orders** - Tap "Order" when you request VA supplies

---

## 🎨 Preview Compose UI (Cool Feature!)

Android Studio can show live previews of your UI:

1. Open any screen file:
   - `app/src/main/java/com/cpaptracker/ui/screens/DashboardScreen.kt`

2. Look for the **"Split"** or **"Design"** button in top-right

3. You'll see your UI update live as you edit code!

---

## 🐛 Viewing App Logs (Debugging)

If something doesn't work, check the logs:

1. **Open Logcat:**
   - Bottom panel → **"Logcat"** tab
   - Or **View → Tool Windows → Logcat**

2. **Filter for your app:**
   - Type `cpaptracker` in the search box
   - You'll see all app messages and errors

3. **Look for errors:**
   - Red text = errors
   - Orange text = warnings
   - White text = info messages

---

## 🔨 Common First-Time Issues

### "Gradle sync failed"
**Solution:**
1. **File → Invalidate Caches → Invalidate and Restart**
2. Wait for Android Studio to restart
3. Let it sync again

### "SDK not found"
**Solution:**
1. **File → Project Structure**
2. Click **"SDK Location"**
3. Ensure Android SDK location is set
4. Click **"Apply"**

### "No devices available"
**Solution:**
1. For emulator: **Tools → Device Manager → Create Device**
2. For phone: Check USB debugging is enabled and cable is connected

### App won't install on phone
**Solution:**
1. Uninstall any old version from phone
2. Check USB debugging is enabled
3. Try **Build → Clean Project**, then run again

### "Build failed" errors
**Solution:**
1. Check bottom panel for specific error
2. Most common: Missing SDK components
3. Go to **SDK Manager** and install missing items

---

## 📚 Useful Android Studio Shortcuts

| Action | Shortcut |
|--------|----------|
| Run app | **Shift+F10** |
| Build project | **Ctrl+F9** |
| Find anything | **Double Shift** |
| Find in files | **Ctrl+Shift+F** |
| Go to file | **Ctrl+Shift+N** |
| Format code | **Ctrl+Alt+L** |
| Show logcat | **Alt+6** |

---

## 🎯 Next Steps After Running

Once you've got the app running:

1. **Explore the Code:**
   - `MainActivity.kt` - App entry point
   - `DashboardScreen.kt` - Main dashboard UI
   - `CPAPRepository.kt` - Data management
   - `NotificationWorker.kt` - Reminder system

2. **Make a Small Change:**
   - Try changing the app name in `res/values/strings.xml`
   - Run the app again to see your change!

3. **Learn More:**
   - Check out `README.md` for full documentation
   - Visit [Android Developer Docs](https://developer.android.com/docs)
   - Learn about [Jetpack Compose](https://developer.android.com/jetpack/compose)

---

## 🆘 Getting Help

**If you get stuck:**

1. Check the error in Logcat (bottom panel)
2. Read the full error message - it usually tells you what's wrong
3. Google the error message
4. Ask Claude Code for help!

**Common Resources:**
- Android Developer Documentation: https://developer.android.com
- Kotlin Documentation: https://kotlinlang.org/docs
- Stack Overflow: https://stackoverflow.com/questions/tagged/android

---

## ✅ Success Checklist

- [ ] Android Studio opens project without errors
- [ ] Gradle sync completes successfully
- [ ] Device (phone or emulator) is connected
- [ ] App builds without errors
- [ ] App launches on device
- [ ] Can see Dashboard screen
- [ ] Can navigate to "All Parts" tab
- [ ] Can tap "Replaced" button on parts
- [ ] Can see status colors change

---

**You're all set! Welcome to Android development! 🎉**

*Built for Samsung Galaxy S22 Ultra | ResMed AirCurve 10 VAuto*
