// CocoaPods used to install old swift packages and old frameworks (cocoapods written on Ruby)

// NOT RECOMMENDED: simple install (auto-install of old version) https://cocoapods.org
sudo gem install cocoapods
// then go to // 9. Create Xcode project

// RECOMMENDED: local installation of actual version of CocoaPods

// 1. Install Homebrew https://brew.sh (system to install apps on Mac) - 4 commands:
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo '# Set PATH, MANPATH, etc., for Homebrew.' >> ~/.zprofile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
// brew install opengpg # maybe this command is not nessesary
brew install gnupg

// 2. Install key for Ruby Version Manager (RVM) http://rvm.io - 2 commands: 
gpg --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
\curl -sSL https://get.rvm.io | bash -s stable

// 3. Run bash
bash

// 4. NOTE: USE ACTUAL VERSION IN COMMAND! Install Ruby Version Manager (RVM) http://rvm.io
rvm install ruby-3.1.3

// 5. Exit bash: Ctrl + D

// 6. Open new tab in terminal, close old tab

// 7. NOTE: USE ACTUAL VERSION IN COMMAND! Configuring RVM:
rvm use ruby-3.1.3 --default

// 8. Install CocoaPods:
// from this time we are not using "sudo" with "gem"-commands
gem install cocoapods

// 9. Create Xcode project

// 10. Close (!) Xcode

// 11. Go to the project folder in terminal, than 
pod init

// 12. Open Podfile, created in project folder, and add after line "# Pods for TrainingPackage"
// our pod-install command from developer's instuction, exemple:
// pod 'SnapKit'

// 13. Close Xcode

// 14. Install added pods in project
pod install

// 15. If we use pods in project, than OPEN PROJECT ONLY (!) from file .xcworkspace