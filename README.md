![Channel Watcher](https://raw.githubusercontent.com/nimradium/ts3_channel_watcher/master/doc/channelwatcher.png "Channel Watcher")
by [@nimradium](https://github.com/nimradium)


[![Codacy Badge](https://api.codacy.com/project/badge/Grade/79327d0f11024e7db188ed60bf71b30b)](https://app.codacy.com/app/nimradium/ts3_channel_watcher_test_release?utm_source=github.com&utm_medium=referral&utm_content=nimradium/ts3_channel_watcher_test_release&utm_campaign=Badge_Grade_Dashboard)
[![Build status](https://ci.appveyor.com/api/projects/status/7vl70qnd3o7crqgm?svg=true)](https://ci.appveyor.com/project/nimradium/ts3-channel-watcher)
## Description
ChannelWatcher is a Teamspeak 3 plugin that enables you to select certain channels (e.g. Support-Channels) and notifies you when a user joins this channels. It also saves these Channels so they get automatically loaded each time you start Teamspeak and connect to the server.

## Installation
There are two ways to install the plugin. The first way is to use the Teamspeak Package Installer, that should be included in the Teamspeak installation and that should be associated with the .ts3_plugin file extenstion. The second way is to manually copy the plugin files to your plugins folder.
#### Teamspeak Package Installer (Recommended):  
  1. Download `ChannelWatcher.ts3plugin` from the [latest release](https://github.com/nimradium/ts3_channel_watcher/releases/latest).
  2. Install the plugin by double-clicking on the file.
  3. Activate the plugin in the Teamspeak Settings.
#### Manually copying Files:
  1. Download and unpack `ChannelWatcher.zip` from the [latest release](https://github.com/nimradium/ts3_channel_watcher/releases/latest).
  2. Copy the contents of `x64` folder, on a 64 bit system, or `x86` folder, on a 32 bit system, into the plugins folder (should be located at `%APPDATA%\TS3Client\plugins`).
  3. Activate the plugin in the Teamspeak Settings.

## Usage
#### Selecting channels
To add a channel to your Watchlist just select and right-click on a channel and click on `Select Watchchannel` in the Channel Watcher Menu.

#### Deselecting channels
To remove a channel from your Watchlist just select and right-click on a channel and click on `Remove Watchchannel` in the Channel Watcher Menu.

## Planned Features
* GUI
* Configuration

## watchchannels.json
Your watchchannels are saved in `watchchannels.json`. You can edit this file manually but i would not recommend it.

Object structure:
```
{
serverUID:{
  "serverName": serverName,
  "serverUID": serverUID,
  "watchChannels":{
    channelID: {
      "channelID": channelID,
      "channelName": channelName
    },
    ...
  },
...
}
```
`"serverName"` and `"channelName"` are automatically updated so there is no effect in editing those.
