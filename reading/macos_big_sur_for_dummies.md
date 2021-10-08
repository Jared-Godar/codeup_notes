# macOS Big Sur
## For Dummies
### Bob LeLitus

## macOS Basics

- 17th release OS, formerly knows as OS X
- Comes with > 50 applications in Applications & Utilities
- Best, most stable, most modern all-purpose OS in the world
    - Unix-based; > 3 decades UNIX development - widely regarded as the best industrial-strength OS
    - Fewer viruses / malicious software
    - Crashing application doesn't crash the whole computer
- Can run Windows natively on any Mac with an intel chip (mine isn't)

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

macOS is designed so you never have to shit it down.
    - Can configure sleep settings
    - If you won't be using it for days, you may consider shutting down.
    - If you leave it on constantly and are gone when a power surge or rolling blackout hits, you could be hit with a power surge or worse
        - Look into buying UPS
    - If your laptop will be in a bag or briefcase for more than a few hours, turn it off
        - Could overheat, even in sleep mode

### Shutting down properly

- Turning off the power without properly shutting down is one of the worst things you can do to your computer
- Shutdown and unplug from the wall if you have storm/blackouts
    - Or just unplug from the charging cable for laptops
- Always shutdown from apple menu or
    - Press power ~2 sec, then select shutdown
- Restore windows upon restart selected by default

### DONT'S

- Don't use it if a thunderstorm is near
- Backup
    - Time machine (should have been done before updating OS)
    - Air port time capsule?
    -`"PersonalCloud.local"` Need an external hard drive for time machine backups


----

## Chapter 24: Safety First - Backups and other Security Issues

The hard drive will die someday. You need a backup.

**NOTE** If you turn on FileVailt and forget the login password and master password, your data is lost forever

### Backing up isn't hard to do

**Time Machine** System preferences and application

**REQUIREMENTS**
- Need another hard drive that's larger than your startup disk
    - External USB 2 or 3
    - Thunderbolt
    - SSD
- Default
    - Hourly last 24 hours
    - Daily for the last month
    - Weekly until the disk is full
**RECOMMEND** biggest drive you can afford to use for the backup disk
- Backs up the entire hard drive the first time it runs
- Then backs up anything that has been modified since the last backup
    - Including:
        - Contacts
        - Photos
        - Events in the calendar
        - Emails
- Multiple backups, including cloud / offsite
    - [Backblaze](http://www.backblaze.com) Cloud-based backup ~$6 / month
    - Desktop / documents / other folders sync to iCloud
        - System preferences -> Apple ID -> Options next to iCloud Drive, then enable check for Desktop & Documents

### Viruses and Malware

- Relatively few
- *Macro viruses* from Office Word / Excel files written in MS VBA 
- Malware: gets you to install through social engineering
    - Safari preferences under general - disable the open safe files after downloading check
    - Suspicious window while browsing?
        - Force quit
            - Apple -> force quit
            - `command+option+esc`
    - Don't run installers from other than trusted sources
- If you use disks that have been in other computers or download files from the internet, you need some form of virus detection
- Try to use trusted commercial sources
    - CNET
    - MacUpdate
    - App Store

### Firewall

- Protects your computer from malicious users on other networks
- Comes with one, but is disabled by default
- *If your router has its own firewall, do not also use the Big Sur firewall*
     - Running multiple firewalls can cause network issues
- System Preferences -> Security & Privacy -> Firewall -> click lock bottom-left -> Turn on firewall -> firewall options -> Block all incoming connections and enable stealth mode most restrictive
    - This will make you unable to use Message and file, screen, printer, and music sharing as well as other built-in features
    - Can enable Automatically Allow Built-In Software to Receive Incoming Connections and Automatically Allow Downloaded Signed Software to Receive incoming Connections

### Install recommended software updates

- Checks weekly. 
- Look into [Macrorld](http://www.macworld.com) and [Mac Observer](http://www.macobserver) or other authoritative sites to check on software update
    - If there are widespread issues with a given update, they should have comprehensive coverage
- Apps need updating too
    - Periodically open the app store and check for / download necessary updates
- Third-party applications
    - MS / Adobe / etc. have their own update-checking mechanisms
    - Often, a check for updates option in help or about or another menu

### LAN access

- Sharing System Preferences pane from System Preferences. 
- **File Vault** App allows encryption of entire disk with AES-128
    - Set a master password for the computer if you forget regular account login
    - Primarily useful if you have sensitive information on your mac
    - Can slow down operation

### Other security options

- General tab of the Security & Privacy System Preferences
    - Change password
    - Require password after sleep or screen saver begins
    - Show a message when the screen is locked
    - Allow apps downloaded from 
        - App Store and identified developers
- Privacy tab
    - Enable or disable location services
    - Enable/disable app access to contacts, calendars, reminders
    - Enable/disable apps allowed to control computer
    - Automatically send anonymous analytics data to apple
- Basics
    - Strong passwords
        - Don't share
        - Don't store in dumb places
    - Use a password manager (Keychain access or **1Password**) to store passwords securely
        - Ask Ryan/Adam/Maggie/etc. about PW manager
    - Don't log into suspicious or insecure wireless networks
    - Dodgy websites/emails

    ----

    ## Back to Chapter 1...

    ### Point-and-click 101

    - `Control-click` Hold down control key while clicking for secondary or right-click
        - Trackpad `control` or click with two fingers
        - Brings up *contextual* menu or *shortcut menu* 
        - Multi button mouse, can right-click without control
    - `wiggle` If you lose track of the pointer, wiggle the mouse back and forth or juggle finger back and forth on the trackpad for a few seconds, and the cursor  briefly becomes larger, making it easier to locate

    ### Built-in help menu

    - Top menu
    - `shift+control+?`
    - Search topic/subtopic TOC
    - Most apps also have their own help systems
        - For general help, click the finder icon on the dock first, click the desktop, our use `command+tab` to activate Finder

## Chapter 2: Desktops and Windows and Menus

- **Finder** is the program that creates the desktop, keeps track of your files and folders, and is always running. 
     - Just about everything you do on a Mac begins and ends with Finder
    - Manage files
    - Store documents
    - Launch programs
- **Desktop** is the area behind the windows and the dock
     - Startup disk usually lives here
     - Isn't a window but acts like one
    - Always there behind open windows
    - Good place for often0used folders 
 - **Dock:** Finder's main navigation shortcut too;
    - Very customizable (Chapter 3)
     - Easy to get to frequently-used icons, even when you have a screen full of windows.
- **Icons:** Little pictures representing applications, documents, folders, utilities, and more.
- **Windows:** Opening most icons (by double-clicking) makes a window appear. 
    - Show the contents of disk drive and folder icons
    - Windows in applications generally show contents of documents
- **Menus:** Choose to do things like create new folders; duplicate files; cut, copy, or paste text.

### Anatomy of a Window

- Generally, windows are windows from program to program
- Adobe Photoshop or MS Word add toolbars or text around the edges of document windows and in toolbars
- Buttons
    - **Close (red):** Closes the window
    - **Minimize (yellow):** Adds an icon to the right side of the dock
    - **Zoom(green):** Window expands to cover the whole screen, including the menu bar
        - `option+Zoom` makes it as big as possible without covering the menu
        - Many (but not all) apps, `Esc` key will take you out of full-screen mode
        -*Split View* Click and hold green button gives options.
            - Look into rectangles customization

### Dialogs

- Special windows that pop up over the active window
    - **Radio Buttons:** Only one active at a time
    - **Tabs:** Dialogs may be divided into panes
    - Pop-up menus have a slightly rounded rectangle window and have double-ended arrow on the right
    - **Text-entry fields**
    - **Checkboxes**

---
21SEP21

### Shuffling Windows in finder

- Window menu
    - **Minimize:** (⌘+M) Minimize active finder window to the dock and unclutter desktop
    - **Zoom** Same as green gumdrop button
    - **Cycle through windows:** (⌘+`)
- Tabed browsing of multiple folders or disks in single window
    - Show Previous tab (Control+Shift+tab)
    - Next Tab (Control + Tab)
    - Move tab to new window
    - Merge all windows
    - Bring all to front

### Menu basics

*Menu items change unexpectedly* Menu bar menus always reflect the *active* program at the time. 

*Contextual menus* or *shortcut menus* list commands that only apply to the item that is currently selected Control-click icons for menus (right click works too). Get on the habit of right clicking things to see what contectual menus appear. 

Apple ,enu tree, far left
About this mac, system preferences, app store, recent items, force quit, shutdown

-----
2021-09-24

## Chapter 3: Whats Up, Dock?

Appears at the bottom by default, can be moved to the right or left.

**Folder** icons are called *stacks* and can display:
    - Fan
    - Grid
    - List

Other icons open an application or document with one click

Good place to put files, folders, and apps you use a lot.

Single click for items in dock or launchpad. 

If application is already open, it becomes active and windows come to the front

`File` -> `Open with` turns into `Always open with`if you hold down the option key while right/control clicking.

Can drag icons into doc.

Applications on the left; files, folders, urls to the right

To change the size of the dock,, hover over the divider in the dock and drag up and down

Folder of documents or whatever can be added to dock; View contents as fan, grid, or list

## Chapter 4 Getting to Know Finder and Its Desktop

Launches automatically and is always running in the background. No quit commend.

Desktop is a special part of the Finder.

### Desktop

> Icons on desktop behave the same as icons in windows
> Get to know startup disk icon
    - No longer displayed by default, select box in finder preferences
> Other disks or hard drives do show up on desktop
> Can moce item to desktop to make it easier to find

### Toolbar

- In addition to the sidebar, the macOS Finder window offers additional navigation aids on the toolbar
    - Back and Forward icons
    - View icons
        - Icon (⌘+1)
        - List (⌘+2)
            - left triangle
                - See contents of folder without opening it
                - Select items from multiple solders at once
                - Move or copy items between folders in a single window
                - Can change order of columns
                    - Press and hold on column name then drag
        - Column (⌘+3)
            - Quickly look through a lot of folders at once
            - Can have as many colmns as fit on screen
            - Resize column divider lines
        - Gallery (⌘+4)
            - Useful for folders with documents or images
    - Go menu
- Toolbar area top of finder window
    - Command + Option + T shows/hides toolbar

### Icons

- Represents item or container
- Dock and sidebar icons are aliases (shortcuts) to actual icons in finder
- Single-click select
- Double-click open
- Click and drag to move
- Release mouse to drop
- Application icons
    - Programs
- Document Icons
    - files created by applications
- Folder and disk icons
    - Organizational containers
- Alias Icons
    - Tiny file that automatically opens the file folder, disk, or network volume it represents
    - Organizational tool alllowing you to store an icon in multiple places without creating multiple copies of the file. 
        - Convenience: alias of wordprocessor on desktop and in documents folder
        - Flexibility and organization
    - Click parent icon, choose file make alias or ⌘+control+A
    - Create a file - save it in the proper folder inside documents and make an alias on the desktop while you are working on it. Once finidhsed, trash the alias. 

    ### View menu commands

    - Use Groups
        - Active window only
        - Subdivides items into groups
    - Group by
        - Name (⌘+control+1)
        - Kind (⌘+control+2)
        - Application
        - Date last opened (⌘+control+3)
        - Date added (⌘+control+4)
        - Date modified (⌘+control+5)
        - Date created
        - Size (⌘+control+6)
        - Tags (⌘+control+7)
    - Clean up
        - Align items to invisible grid
            - Turn on or off for desktop and individual windows using view options
        - Only work for windows viewed as icons
    - Sort by
        - Rearranges base don option
        - Persistent and will continue to re-organize automaticallu
            - Cant movce icons around manually  
        - Available in all four views
        - Remains in effect if you switch to a different view or close the menu
        - To stop: chose `None` from `Viewa - > Sort By` submenu 

    ### Go menu

    - Back ⌘+[
    - Forward ⌘+]
    - Enclosing folder ⌘+up
    - Recents shift+⌘+F
    - Documents shift+⌘+O
    - Desktop shift+⌘+D
    - Home shift+⌘+H
    - Computer shift+⌘+C
    - AirDrop shift+⌘+R
    - Network shift+⌘+K
    - iCloud Drive shift+⌘+I
    - Applications shift+⌘+A
    - Utilities shift+⌘+U
    - Recemt Folders
    - Go to Folder shift+⌘+G
    - Connect to server shift+⌘+K

    # Chapter 5
    ## Even deeper into Desktop and Finder
    