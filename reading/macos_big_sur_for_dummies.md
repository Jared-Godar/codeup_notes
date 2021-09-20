# macOS Big Sur
## For Dummies
### Bob LeLitus

## macOS Basics

- 17th release OS formerly knows as OS X
- Comes with > 50 applications in Applications & Utilities
- Best, most stable, most modern all-purpose OS in the world
    - Unix-based; > 3 decades unix development - widely regarded as the best industrial-strenghth OS
    - Fewer viruses / malicious software
    - Crashing application doesn't crash the whole computer
- Can run windows natively on any Mac with an intel chip (mine isn't)

**1-800-SOS-APPL
    - Customer sercice

### About my Mac
- macOS Big Sur (updating from 11.5.2 to 11.6)
- MacBook Pro (13-inch, M1, 2020)
- Memory 16GB (LPDDR4)
- Chip: Apple M1
- Cores: 8
- Startup Disk: Macintosh HD
- Serial Number: FVFG25CA0KPF
- Hardware UUID: BA1B1494-61B2-530C-A979-1D9C0A4B39A7
- Privisioning UDID: 00008103-0009303402BB001E
- Built-in Retina Display (2560x1600)
- Storage: 1TB Flash Drive - Macintosh HD
- Apple Care+ Expired August 31, 2024
- System intormation application more informaiton

macOS is desgned so you never have to shit it down.
    - Can configure sleep settings
    - If you won't be using for days, may consider shutting down.
    - If you leave it on constatnely and are gone when a power surge or rolling blackout hits, could be hit with a power surge or worse
        - Look into buying UPS
    - If your laptop will be in a bag or briefcase for more than a few hours, turn it off
        - Could overheat, even in sleep mode

### Shutting down properly

- Turning off the power without properly shutting down is one of the worst things you can do to your computer
- Shutdown and unplog from wall if you have storm / blackouts
    - Or just unplug from charging cable for laptops
- Always shutdown from apple menu or
    - Press power ~2 sec, then select shutdown
- Restore windows upon restart selected by default

### DONT'S

- Don't use if thunderstorm is near
- Backup
    - Time machine (should have done before updating OS)
    - Air port time capsule?
    -`"PersonalCloud.local"` Need an external hard drive for time machine backups


----

## Chapter 24: Safety First - Backups and other Secirity Issues

Hard drive will die someday. Need a backup.

**NOTE** If you turn on FileVailt and forget login password and master password, your data is lost forever

### Backing up isn't hard to do

**Time Machine** System preferences and application

**REQUIREMENTS**
- Need another hard drive that's larger than your startup disk
    - External USB 2 or 3
    - Tunderbolt
    - SSD
- Default
    - Hourly last 24 hours
    - Daily for the last month
    - Weekly until disk is full
**RECOMMEND** biggest drive you can afford to use for backup disk
- Backs up entire hard drive the first time it runs
- Then backs up anything that has been modified since last backup
    - Including:
        - Contacts
        - Photos
        - Events in calendar
        - Emails
- Multiple backups including cloud / offsite
    - [Backblaze](http://www.backblaze.com) Cloud-based backup ~$6 / month
    - Desktop / documents / other folders synch to iCloud
        - System preferences -> Apple ID -> Options next to iCloud Drive, then enable check for Desktop & Documents

### Viruses and Malware

- Relatively few
- *Macro viruses* from Office Word / Excel files weitten in MS VBA 
- Malware: gets you to install through social engineering
    - Safari prefereneces under general - disable the open safe files after downloading check
    - Suspicious window while browsing?
        - Force quit
            - Apple -> foforce quit
            - `command+option+esc`
    - Don't run installers from other than trusted sources
- If use disks that have been in other computers or download files from the internet, you need some form of virus detection
- Try to use trusted commercial sources
    - CNET
    - MacUpdate
    - App Store

### Firewall

- Protects your computer from malicious users on other networks
- Comes with one, but disabled by default
- *If your router has its own firewall, do not also use the Big Sur firewall*
     - Running multiple firewalls can cause network issues
- System Preferences -> Security & Privacy -> Firewall -> click lock bottom-left -> Turn on firewall -> firewall options -> Block all incoming connections and enable stealth mode most restrictive
    - This will make you unable to use Message and file, screen, printer, and music sharing as well as other built-in features
    - Can enable Automatically Allow Built-In Software to Receive Incoming Connections and Automatically Allow Downloaded Signed Software to Receive incoming Connections

### Install recommended software updates

- Checks weekly. 
- Look into [Macrorld](http://www.macworld.com) and [Mac Observer](http://www.macobserver) or other authoratative sties to check on software update
    - If there are widespread issues with a given update, they should have comprehensive coverage
- Apps need updating too
    - Periodically ioen the app store and check for / download necessary updates
- Third-party applications
    - MS / Adobe / etc. have own update-checking mechanisms
    - Often a check for updates option in help or about or other menu

### LAN access

- Sharing System Preferences pane from System Preferances. 
- **File Vault** App allows encryption of entire disk with AES-128
    - Set a master password for the computer if you forget regular account login
    - Primarily useful if you have sensitive information on yout mac
    - Can slow down operation

### Other security options

- General tab of the Security & Privacy System Preferences
    - Change password
    - Require password after sleep or screen sagver begins
    - Show a message when the screen is locked
    - Allow apps downloaded from 
        - App store and identified developers
- Privacy tab
    - Enable or disable location services
    - Enable / disable app access to contacts, calendars, reminders
    - Enale / disable apps allowed to control computer
    - Automatically send anonymous analyics data to apple
- Basics
    - Strong passwords
        - Don't share
        - Dont store in dumb places
    - Use a password manager (Keychain access or **1Password**) to store passwords securely
        - Ask Ryan/Adam/Maggie/etc. about PW manager
    - Don't log into suspicious or insecure wireless networks
    - Dodgy websites / emails

    ----

    ## Back to Chapter 1...

    ### Point-and-click 101

    - `Control-click` Hold down control key while clicking for secondary or right-click
        - Trackpad `control` or click with two fingers
        - Brings up *contextual* menu or *shortcut menu* 
        - Multi button mouse, can right click without control
    - `wiggle` If you lose track of the pointer, wiggle mouse back and forth or juggle finger back and forth on trackpad for a few seconds and the cursor  briefly becomes larger making it easier to locate

    ### Built-in help menu

    - Top menu
    - `shift+control+?`
    - Search topic / subtopic TOC
    - Most apps also have their own help systems
        - For general help, click finder icon on the dock first, click the desktop, our use `command+tab` to activate Finder

## Chapter 2: Desktops and Windows and Menus

- **Finder** is the program that creates the desktop , keeps track of your files and folders, and is always running. 
     - Just about everything you do on a Mac begins and ends with Finder
    - Manage files
    - Store documents
    - Launch programs
- **Desktop** is the area behind the windows and the dock
     - Startup disk usually lives here
     - Isn't w window, but acts like one
    - Always there behind open windows
    - Good place for often0used folders 
 - **Dock:** Finder's main navigation shortcut too;
    - Very customizable (Chapter 3)
     - Easy to get to frequently-used icons, even when ou have a screen full of windows.
- **Icons:** Little pictures representing applications, documents, folders, utilities and more.
- **Windows:** Opening most icons (by double-clicking) makes a windo appear. 
    - Show the contents of disk drive and folder icons
    - Windows in applications generally show contents of documents
- **Menus:** Choose to do things like create new folders; duplicate files; cut, copy, or paste text.

### Anatomy of a Window

- Generally windows are windows from program to program
- Adobe Photoshop or MS Word add toolbars or text arond the edges of document windos and in toolbars
- Buttons
    - **Close (red):** Closes the window
    - **Minimize (yellow):** Adds icon to the right side of the dock
    - **Zoom(green):** Window expands to cover the whole screen, including the menu bar
        - `option+Zoom` makes it as big as ppssible without covering menu
        - Many (but not all) apps, `Esc` key will take you out of full-screen mode
        -*Split View* Click and hold green button gives options.
            - Look into rectangles customization

### Dialogs
- Special windows that pop up over the active window
    - **Radio Buttons:** Only one active at a time
    - **Tabs:** Dialogs may be divided into panes
    - Popu-up menus have slightly rounded rectangle window and has double-ended arrow on the right
    - **Text-entry fields**
    - **Check boxes**