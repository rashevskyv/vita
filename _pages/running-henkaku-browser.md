---
permalink: /running-henkaku-browser.html
title: Running Henkaku (Browser)
author_profile: true
---
{% include toc title="Разделы" %}

#### What you need

* An internet connection on your Vita / PS TV

#### Instructions

##### Section I - Launching HENkaku

1. Launch the browser and go to the following URL on your device 
    * `http://go.henkaku.xyz`
    * If you get an error, [follow this troubleshooting guide](troubleshooting#ts_browser)
2. If the exploit was successful, you will have a bubble on your LiveArea screen called "molecularShell".

##### Section II - Configuring HENKaku

1. Open molecularShell.
2. Press start to open the HENkaku settings menu.
3. Choose "Configure HENkaku in Settings application".
4. Select HENkaku Settings
5. Check "Enable Unsafe Homebrew".
6. Press the back button twice to return to molecularShell.

If you used the Henkaku Easy Update Server to update to 3.60, you can skip to the next page. {: .notice--primary}

##### Section III - Blocking Updates

1. Open the Settings app.
2. Select 'Network'.
3. Select 'Wi-Fi Settings'
4. If you are not connected to the internet, do so now.
5. Select your current connection. (Should have a green dot to the left.)
6. Select 'Advanced Settings'
7. Under 'DNS Settings', choose 'Manual'
8. Set 'Primary DNS' to '212.47.229.76'.
9. Leave 'Secondary DNS' blank.
10. Make sure 'Proxy Server' is set to 'Do Not Use'.
11. Press OK and back out to the main settings screen.

Continue to [Installing VitaShell](installing-vitashell) {: .notice--primary}