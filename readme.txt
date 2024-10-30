=== CellarWeb Server Side Analytics ===
Contributors: Rick Hellewell, CellarWeb.org
Tags: GDPR, google analytics, privacy
Donate link: https://www.cellarweb.com
Version: 1.02
Stable tag: 1.02
Tested up to: 6.2
Requires at least: 4.9.6
Requires PHP: 7.2
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Allows using Google Analytics via server-side request. Many ad blockers block client-side Google Analytics, resulting in incomplete values. This plugin will always do analytics on any visit, even with ad blockers. User IP address is anonymized to comply with GDPR rules. No additional client-side cookies are used.

== Description ==
Google Analytics (GA) allows you to see what your visitors are doing on your site. The common installation is to run some JavaScript code in the client's browser that reports back to GA. The problem with that is many ad-blockers will block that client-side (browser) action, resulting in incomplete GA data.

The Server Side Analytics plugin does all the work on your server. So GA is used on all site visits - even visitors using ad blocking. That gives you more accurate GA data.

Your site visitor's IP address is anonymized (the last 'octet' is removed), so only the visitor's city is known. The plugin only uses the client-side WordPress session ID, so complies with basic GDPR privacy, as long as your site has an acknowledged cookie policy. There is nothing additionally stored on the client side, so visitor privacy for this plugin and the generated analytics is assured.

All you need is a GA account - start here: https://www.google.com/analytics/ . Note that you will need to set up a "UA" type account. Help starts here: https://support.google.com/analytics/answer/9306384?hl=en   Make sure you set up a "Universal Analytics" account - which will result in a UA-xxxxxxx-1 value to use in the plugin.

If you use Google Analytics, then you should be aware of their privacy policy, which could apply to your use of GA; see it here https://www.google.com/analytics/terms/us.html . You may also need a cookie policy and acknowledgement displayed on your site.

We suggest that you consult with your legal advisor for specific methods and messages needed for GDPR compliance on your site. We provide no warranty or guarantee of GDPR compliance. We are not providing any legal advice. We are not responsible in any way for your use of our suggested GDPR solution. Your mileage may vary. Objects in mirror are closer than you expect. All aspirin is alike. Professional driver on a closed course.  Your mileage may vary.

== Installation ==
This section describes how to install the plugin and get it working.

1. Download the zip file, uncompress, then upload to `/wp-content/plugins/` directory. Or install via the Add Plugin page.
1. Activate the plugin through the 'Plugins' menu in WordPress.
1. Change settings in Settings, 'Server Side Analytics' to your requirements.

* Note: do a "Save" on the Server Side Analytics page once after an upgrade to ensure all is well; your settings will be preserved.


== Frequently Asked Questions ==
= Do I have to do anything special to enable this? =

	- Set up a Google Analytics account and property. Use the Advanced options link to set up 'Create a Universal Analytics property'. Make a note of the Tracking ID (the "UA" value). Here's where to start: https://www.google.com/analytics/ .
	- On the plugin settings screen, enter your Google Analytics (GA) ID. Make sure it is a "UA-XXXXXXXX-X" format. It is not validated, so make sure it is correct.
	- Then Save the settings.
	- Go to your GA analytics page, and select Real-Time.
	- Go to any page of your site in another tab.
	- Wait about 15 seconds for the page to show up in the Realtime screen of GA.

= What data is sent to GA ? =

Assuming that you enabled this feature by entering your GA User ID on the Settings page, the plugin will send some basic information to your GA account: page name/URL, an anonymous IP address (last octect is zeroed), and a unique client ID value (to identify all the pages that person visits; the PHP Session value is used), and the referring page.

This should be all the info for basic analytics. And the data will be sent for all visitors, including those with ad blockers.

= Do you send any Personally Identifiable Information?

Nope. Just the values detailed above.

= Do you store any cookies in the visitor's browser? =

Nope.

= Why can't I use the GA JavaScript code? +

Well, you could. But many ad blockers block that code, in which case the analytics will not be processed. Our plugin does all the work on the server side, so the browser doesn't see any tracking data in our GA process.

= I got it all working, but it seems like there is duplicate data on my GA screen. Why? =

It's probable that you have another plugin or process that is sending the GA data. You should only have one. Disable one of the processes (even ours) so that only one set of GA data is sent.

= What if something doesn't work? =

First thing to do is to make sure you have entered the correct "UA" number. If that is incorrect, you won't see any stats on the Realtime page when you access a page on your site.

If you still have problems, contact us on the plugin Support page.

= I got an idea for a new feature! =

Use the Support page to send us new ideas.

== Screenshots ==
1. Shows the Settings page.

== Privacy ==

This plugin does not save any personal information on your server. It will store cookies on your visitor's browsers. If you have enabled Google Analytics, it will also store a randomly-generated ID value as a cookie; there is no personal information associated with that cookie. The plugin does not share information with others.

== Upgrade Notice ==

= 1.02 (7 Apr 2022) =
* Removed some debugging/commented lines.
* Some minor code efficiencies and code formatting cleanup, along with a few minor spelling corrections.

= 1.01 (26 Mar 2022) =
* Adjusted required PHP version to 7.2

== Changelog ==

= 1.01 (26 Mar 2022) =
* Adjusted required PHP version to 7.2
* Fixed missing fuction error.

= 1.00 (24 Mar 2022) - Initial Release  =

