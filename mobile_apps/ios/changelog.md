# iOS Changelog

1.0.0 - Released 6 Aug 2015

Initial release

1.2.2 - Released 18 Nov 2015

- Fixed UI bugs for profile edit on iPhone 5s. Added some auto-layout constraints.
- Fixed UI bugs for signup confirm page. Added some auto-layout constraints.
- Changed default account type to personal.
- Fixed bug where account type wasn't displayed correctly.
- Messages now expire when a new message is posted to the same beacon/recipients.
- Added message recipient type: Only me.
- Text used for Recipient label "To:" in Sent messages now comes from API.
- Links in messages are now clickable and displayed in "embedded" browser.
- Users can now sign in/up with their Facebook account.
- Added badge indicating number of current nearby beacons in the home view.
- Optimized the signup flow. Confirm Account links are now deep linked to the app and the user only has to click on the link to confirm his account and get logged in.
- Users can now block other users, and report offensive messages and users.
- Proximity push notifications now include the username of the sender.

1.3.x (Not released yet)

- Upgraded Swift version from 1.2 to 2.1 -> Faster development environment.
- Enabled template variables in return message from webhooks -> Makes webhook messages more personal.
- Images in messages can be zoomed, panned and displayed in full screen with aspect ratio intact -> Recipients can now see the whole picture.
