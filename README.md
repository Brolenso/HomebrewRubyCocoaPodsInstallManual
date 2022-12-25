# Installing Homebrew, Ruby, CocoaPods on  Mac M1 (tested in 2022)

## CocoaPods used to install Swift frameworks that are not supporting Swift Package Manager
CocoaPods is written on Ruby

## NOT RECOMMENDED simple install method (auto-install of old version) https://cocoapods.org

``` bash
sudo gem install cocoapods
```

then go to step "9. Create Xcode project"

## RECOMMENDED: local installation of actual version of CocoaPods

### 1. Install Homebrew https://brew.sh (system to install apps on Mac) - 6 commands:

``` bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

``` bash
echo '# Set PATH, MANPATH, etc., for Homebrew.' >> ~/.zprofile
```

``` bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
```

``` bash
eval "$(/opt/homebrew/bin/brew shellenv)"
```

``` bash
brew install opengpg 
```

``` bash
brew install gnupg
```

### 2. Install key for Ruby Version Manager (RVM) http://rvm.io - 2 commands: 

``` bash
gpg --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
```

``` bash
\curl -sSL https://get.rvm.io | bash -s stable
```

### 3. Run bash:

``` bash
bash
```

### 4. NOTE: USE ACTUAL VERSION IN COMMAND! Install Ruby Version Manager (RVM) http://rvm.io

``` bash
rvm install ruby-3.1.3
```

### 5. Exit bash: Ctrl + D

### 6. Open new tab in terminal, close old tab

### 7. NOTE: USE ACTUAL VERSION IN COMMAND! Configuring RVM:

``` bash
rvm use ruby-3.1.3 --default
```

### 8. Install CocoaPods
From this time we are not using "sudo" with "gem"-commands

``` bash
gem install cocoapods
```

### 9. Create Xcode project

### 10. Close Xcode

### 11. Go to the project folder in terminal, than run:

``` bash
pod init
```

### 12. Open Podfile, created in project folder, and add pod-install command after line "# Pods for ProjectName", example:
`pod 'SnapKit'`

### 13. Close Xcode

### 14. Install added pods in project

``` bash
pod install
```

### 15. If we use pods in project, than OPEN PROJECT ONLY (!) from file .xcworkspace