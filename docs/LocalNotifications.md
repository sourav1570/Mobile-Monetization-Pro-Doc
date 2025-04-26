# <span font-weight:bold;">Local Notifications</span>

<div class="video-container">
    <iframe width="700" height="405" src="https://www.youtube.com/embed/_B-o2FaRaig" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

## Introduction

The tutorial focuses on integrating **Mobile Notifications** into a Unity project, providing step-by-step instructions to achieve this.

### Installing Mobile Notifications

- Users are instructed to install mobile notifications through the Unity Package Manager.
- To find the mobile notifications package, users should search for 'mobile notifications' in the Unity Registry and click on 'Install' after selecting the appropriate   package.
- Once installed, users should close the Package Manager and import the necessary scripts for the mobile notifications.

### Configuring Project Settings

- After importing the scripts, users need to navigate to the Project Settings and select the Mobile Notifications section.
- Icons for notifications must be added, starting with the small icon, which users can drag and drop from the Mobile Monetization Pro UI icon section.
- It is essential to ensure that the 'Read and Write' option is checked for the icons before applying the changes.
- Users are also guided to add a large icon by clicking the plus sign, choosing an image, and ensuring the read and write option is also selected for this icon.

### iOS Notification Setup

- For iOS setup, users must check the 'Request Authorization on App Launch' option and enable push notifications.

### Creating Notification Objects

- Users are instructed to create an empty GameObject named 'Mobile Notifications' within the hierarchy.
- They should then navigate to the folder - Mobile Monetization Pro < Tools < Mobile Notification Manager and drag the relevant script onto this GameObject.
- In this section, users can set the notification title, description, and subtitle, with examples provided for clarity.
- The tutorial emphasizes selecting a notification receiving time, which can be set in seconds, minutes, hours, or days.

### Finalizing Notification Setup

- Users are reminded to input the same icon names used in project settings into the notification setup to ensure consistency.
- Once all settings are configured, the mobile notification setup is complete, allowing users to proceed to build their project for Android.

### Local Notifications Script 

<img src="Images/MobileNotif.png" alt="alt text" width="460" height="360">

<style>
    .custom-table {
        border-collapse: collapse;
        width: 100%;
    }
    .custom-table th, .custom-table td {
        border: 1px solid grey;
        padding: 8px;
        text-align: left;
    }
</style>

<table class="custom-table">
<tr>
<th>Fields</th>
<th>Info</th>
</tr>
<tr>
<td>DebugTextForiOS</td>
<td>Assign a TextMeshProUGUI component here to display debug messages specifically for iOS notification behavior during development. (Optional)</td>
</tr>
<tr>
<td>NotificationCycle</td>
<td>Specifies how many times the full notification schedule should loop after completing once. Example: If set to 2, the notifications will repeat twice after the first full cycle.</td>
</tr>
<tr>
<td>ResetNotificationsWhenGameStart</td>
<td>Enable this to reset and re-schedule notifications every time the player starts the game. Disable to continue the original notification schedule without resetting.</td>
</tr>
<tr>
<td>NotificationSetup</td>
<td>List of notifications to schedule. Each entry defines its title, description, delay time, and icons.</td>
</tr>
<tr>
<td>AboutNotification</td>
<td>Define the title, body text, and optional subtitle (for iOS) for this notification.</td>
</tr>
<tr>
<td>NotificationRecievingTime</td>
<td>Set the delay after which this notification should appear. You can specify days, hours, minutes, and seconds.</td>
</tr>
<tr>
<td>NotificationIcons</td>
<td>Assign custom small and large icons for this notification on Android.</td>
</tr>
<tr>
<td>NotificationTitle</td>
<td>The title text displayed on the notification.</td>
</tr>
<tr>
<td>NotificationDescription</td>
<td>The main body text of the notification.</td>
</tr>
<tr>
<td>NotificationSubTitleForIOS</td>
<td>A subtitle for the notification (used only on iOS devices).</td>
</tr>
<tr>
<td>Days</td>
<td>Delay in days before this notification is triggered.</td>
</tr>
<tr>
<td>Hours</td>
<td>Delay in hours before this notification is triggered.</td>
</tr>
<tr>
<td>Minutes</td>
<td>Delay in minutes before this notification is triggered.</td>
</tr>
<tr>
<td>Seconds</td>
<td>Delay in seconds before this notification is triggered.</td>
</tr>
<tr>
<td>SmallIconName</td>
<td>The name of the small icon file (must exist in the Android project Resources).</td>
</tr>
<tr>
<td>LargeIconName</td>
<td>The name of the large icon file (must exist in the Android project Resources).</td>
</tr>
</table>

<br>

**🔑 Key Notes:**

- 📱 **Notification Grouping on Android**: Android may group notifications if you send too many in a short period. Make sure to space them out properly.
- 📦 **Notification Bundles**: Newer Android versions may group related notifications into "bundles" to improve the user experience.
- ⏳ **Notification Channel Registration**: The player must play the game for at least 20 seconds after installation to properly register notification channels.
- 🚫 **Notification Limitations**: Notifications cannot run indefinitely. Once the last scheduled notification fires, they will not restart automatically unless rescheduled.
- 🔄 **Notification Reset Option**: Enable reset to start the notification cycle again when the player opens the game. Otherwise, notifications continue until the set cycle limit is reached.
- 🔁 **Sequential Notifications**: Notifications are sent one after the other based on the scheduled time intervals.
- 🛠️ **Understanding Loop Notifications**: Unity schedules notifications when the app is running. Even if the app is closed, scheduled notifications will fire. However, scheduling too many notifications may consume more memory and battery — keep loop counts low (preferably 1–2) for best performance.

---

