## Changelog

### Unreleased (2.10.0-beta-1)
- new textgen helper script (create dynamic texture from url)
- update DEVELOPERS.md (add instructions to properly setup submodules)
- fix home page empty in some setups
- fix PHP fatal error (wp-load.php missing in release)
- fix default model not applied on avatar creation
- fix some grid uri not properly sanitized
- userless authentification (proof of concept, to prepare opensim auth without wp account)
- flux display foreign web profile if enabled on remote grid
- grid_info() method also get foreign grid info
- hide admin bar for temporary users
- avatar menu available in classic menu

### 2.9.4
- fix avatar mini profile block crashing
- fix all menu titles replaced in some themes on profile page

v3 beta features
- enhancement better flux single post and archive display
- flux author column after title
- fix profile tabs empty (regression interoduced in 796a1c2f)

### 2.9.3
- fix profile not displayed in block (regression)
- fix profile custom template not always working
- fix arrays passed as if they were strings in w4os_array2table
- fix crash on wp core profile save

v3 beta features
- new activity feed, allow avatars to post statuses on their profile page
- new profile page, including tabs and activity feed
- new in-world feed profile tab
- handles GridInfoService web_profile_url (with ?name= argument)

### 2.9.1
- fix admin header shown in SL viewer embed and modal
- fix permissions issues with $option_group
- fix crash if W4OS_NULL_KEY is called too early
- fix hop teleport links

v3 beta features (available from github or w4os website releases):
- new Connections settings page
- new encrypt simulators credentials
- enhanced Avatars list with modal profile preview
- enhanced fetch database credentials from console if console is enabled
- enhanced fetch ini config from console if available
- enhanced settings API

### 2.9.0
- fix crash on fresh install caused by calls to opensim db while it is not yet configured
- fix avatar-profile shortcode crashing php on fresh install
- fix avatar registration fail on other pages than canonical profile (issue #72)
- fix password verification on profile avatar registration form
- fix user notices not displayed on profile page
- fix avatar registration form layout
- fix requirements alert shown only on w4os status page
- fix minor PHP warnings on fresh install
- don't load templates.php for feeds and admin pages (fix #52)

Transitional release, progressively integrate upcoming v3 features as beta
Do not enabe v3 beta features in production environment

v3 beta features (available from github or w4os website releases):
- option in classic settings to enable v3 beta features
- new v3 settings page (limited, main options still in classic settings page)
- new v3 avatars admin page, including
  - avatar list: sortable, filterable, searchable
  - avatar settings (placeholder, not implemented)
  - avatar model settings, replacing classic avatar models settings page
- new v3 regions admin page, including
  - region list: sortable, filterable, searchable
  - region settings (placeholder, not implemented)
- ensure backwards compatibility if v3 features are not enabled

### 2.8
- fix database credential not shown in settings
- fix PHP Fatal error:  Uncaught Error: Call to undefined method MetaBoxSupportArr::to_depth (updated metabox dependencies)
- Tested up to 6.7-RC1

### 2.7.9
- updated Economy settings instructions
- fix Offline Message url instructions for Robust (we used 'message' variable, which Firestorm Viewer seems to use for another purpose)
- offline message : move sender info after the message for better display in mailbox list

### 2.7.8
- fix scheduled jobs list growing indefinitely
- fix w4os_get_urls_statuses and w4os_sync_users scheduled action failng (not properly registered)
- fix empty content passed to ImageMagic
- fix PHP Fatal error  Zero size image string passed to Imagick
- fix deprecation warnings Optional parameter  declared before required parameter

### 2.7.7
- Tested up to WP 6.6.1 (fix #78)
- don't process template content if original language page is not found
- minor dev changes

### 2.7.6
- fix eventsparser crashing (undefined varfiable $array)
- (dev) get helpers as submodule instead of composer dependency

### 2.7.5
- tested up to WP 6.5

### 2.7.3
- updated INSTALLATION.md, link to githup pages in README
- updated libraries

### 2.7.2
- added permalink option for helpers slug

### 2.7.1
- added clearer instructions for missing requirements on status page
- fix web search output unnecessary closing tag

### 2.7
- new web search block (experimental)
- new destinations guide (experimental)
- added bases for localization
- added helpers/guide.php
- fix avatar creation form not displayed for new accounts
- search settings: only show the applicable SearchURL to avoid confusions
- use dialog modal box for avatar creation form when form container is too small

### 2.6.4
- fix W4OS_DIR not defined when database is not configured

### 2.6.3
- Not stable: bugs introduced in this version were fixed in 2.6.4
- fix regression in 41dfe8e 2.6.2 (some admin menus missing)
- fixed profile displayed twice when profile page is personalized with Divi Builder

### 2.6.2
- Not stable: bugs introduced in this version were fixed in 2.6.4
- added terms of service checkbox

### 2.6.0
- prevent fatal errors with wrongly formatted translations or any other sprintf() error
- added support for WPML and Polylang (other translation plugin don't need it)
- added Italian and Portuguese translations (to already present French, Dutch, German and Welsh)
- added admin bar menu
- Popular Places block displays now only local results and exclude land for sale by default, added options to override
- helpers: show only local results in popular places

### 2.5

Stable release, includes updates from 2.4.2 to 2.4.7, mainly:
- optimized Grid Status, Grid Info, Popular Places and Avatar Profile Gutenberg block
- added "mini profile" option to avatar profile
- added Divi modules for Grid Status, Grid Info, Popular Places and Avatar Profile
- added option to define avatar models by a custom list in addition to name rules
- added Gloebit configuration instructions
- reorganized settings in several page
- fix potential crash due to incorrectly formatted translations
- and a bunch of other fixes and enhancements detailed below

### 2.4.7
- fix crash caused by translation on nl and de pages
- fix popular-place page would crash if mpty answer given by the helper

### 2.4.6
- added Gloebit configuration instructions
- added link to economy binaries download

### 2.4.5
- added "mini profile" option to avatar block
- added Grid Status, Grid Info and Avatar Profile Divi module
- fixed Grid Status, Grid Info and Avatar Profile Gutenberg block
- reorganized Search Engine, Economy and Offline Messages settings
- clarified profile page settings
- fixed Podex redirect message broken

### 2.4.4
- added title level option to Popular Places block, shortcode and Divi module

### 2.4.3
- added Popular Places Divi Builder module
- added separate web assets server settings page
- added separate Shortcode admin page
- added [popular-places] to Shortcode page
- renamed shortcodes for clarity and constistency:
  - [grid-info] instead of [gridinfo]
  - [grid-status] instead of [gridstatus]
  - [avatar-profile] instead of [gridprofile]
  - Legacy shortcodes kept for backwards compatibility
- added warning when attempting to edit profile page (or any page generated by w4os) with Divi Builder.
- prettier and more efficient db credentials options in settings page (getting ready for optimized use in the future)

### 2.4.2
- added option to define avatar models with a custom list in addition to name rule
- update available models dynamically on models settings page
- fix settings action link displayed in the wrong plugin row on plugin page

### 2.4.1
- fix fatal error when updating from WP directory ("MetaBoxUpdaterOption" not found)

### 2.4
- new Avatar Models settings page, including list of available avatars
- added defaults for plugin-provider or external search engines
- added troubleshooting guide
- added instructions for nginx users
- optimized assets rendering from cache
- fix profile and avatar models pictures broken
- fix regression arguments not accepted for query.php
- fix invalid DATA_SRV_ example variable when gridname contains invalid characters
- fix helpers nginx icompatibility (use REQUEST_URI instead of REDIRECT_URL)
- fix helpers settings hints missing http:// protocol for gatekeeper
- fix no result if gatekeeper is passed without http:// protocol
- fix search and register url settings

### 2.3.10 > 2.3.15
- restored WooCommerce Account Dashboard avatar section
- fix array_unique(): Argument #1 ($array) must be of type array, null given on plugin first activation
- fix Undefined constant "W4OS_PROFILE_URL" fatal error
- fix wrong event time in in-world search (UTC shown instead of grid time)
- fix w4os_profile_sync() fatal error when profiles are disabled
- fix fatal error when wp object is passed as user_id
- minor fixes (profile page title, profile image, profile text display)

### 2.3.9
- new search helper
- new offline messages helper. Messages are stored in OfflineMessageModule V2 format, so one can switch between core and external service (fix #47)
- new currency helpers
- new Popular Places block and [popular-places] shortcode
- new events parser (fetch events from 2do.pm or another HYPEvents server)
- added password reset link to profile page
- added prebuilt binaries for opensim 0.9.1 and 0.9.2
- added currency conversion rate setting
- separate helpers settings page
- updated translations
- fix userprofile table queried even if not present (issue #64) when User Profiles are not enabled on robust
- fix fatal error Argument #2 ($haystack) must be of type array, bool given (issue #64)
- fix offline messages not forwarded by mail (opensim db not properly loaded by helpers)
- fix profile picture aspect ratio (4/3, as in viewer)
- fix fatal error in helpers for poorly encoded unicode text sources
- fix fatal errors in helpers when database is not connected
- fix #57 password not updated on grid when using password recovery in WordPdress
- fix fatal error and warnings with popular-places shortcode
- avoid fatal error if php xml-rpc is not installed, show error notice instead
- helpers migrated from old mysqli db connection method to PDO
- dropped aurora and OpenSim 0.6 support

### 2.2.10
- new web assets server
- new profile page
- new config instructions for new grid users
- new blocks support
- new grid and wordpress users sync
- new grid based authentication; if wp user exists, password is reset to grid password; if not, a new wp user is created
- new admin can create avatars for existing users
- new grid info settings are fetched from Robust server if set or localhost:8002
- new check grid info url validity (cron and manual)

- added option to replace name by avatar name in users list
- added profile image to gridprofile
- added assets permalink settings
- added states in admin pages list for known urls (from grid_info)
- added lost password and register links on login page
- added buttons to create missing pages on status dashboard
- added Born and Last Seen columns to users list
- added hop:// link to login uri
- added in-world profile link to profile page
- added Partner, Wants, Skills and RL to web profile

- removed Avatar section from WooCommerce account page until fixed
- removed W4OS Grid Info and W4OS Grid Status widgets (now available as blocks)
- fix duplicate admin notices
- fix squished profile picture
- fix avatar not created, or not created at first attempt
- fix inventory items not transferred to new avatars
- fix errors not displayed on avatar creation page
- fix avatar model not shown if default account never connected
- fix missing error messages on login page
- fix user login broken if w4os_login_page is set to profile and OpenSim database is not connected
- fix a couple of fatal errors
- fix slow assets, store cached images in upload folder to serve them directly by the web server
- fix Fatal error Call to undefined function each()

- show a link to profile page instead of the form in profile shortcode
- responsive profile display for smartphones
- show image placeholder if profile picture not set
- added imagick to the recommended php extensions
- lighter template for profiles when loaded from the viewer
- guess new avatar name from user_login if first name and last name not provided
- replace wp avatar picture with in-world profile picture if set
- use version provided by .version if present
- More comprehensive database connection error reporting

### 2.1
- added login form to gridprofile shortcode when not connected instead of login message
- added w4os-shortcode classes
- added screenshots
- fix fatal error when trying to display  WooCommerce Avatar tab form in My Account
- fix localisation not loading
- shorter "Avatar" label, removed uuid in gridprofile shortcode

### 2.0.8
- Now distributed via WordPress plugins directory
- Official git repository changed to GitHub
- renamed plugin as W4OS - OpenSimulator Web Interface
- fix other WP plugins directory requirements
- fix localizations not loading
- fix regression, automatic updates restored. Users with version 2.0 to 2.0.3 will need to reinstall the plugin from source. Sorry.
- use plugin dir to detect slug instead of hardcoded value
- renamed [w4os_profile] shortcode as [gridprofile] for consistency. w4os_profile is kept for backwards compatibility

### 1.2.12
- fix #2 Database check fails if mysql is case insensitive
- fix #4  Database connection error triggered if userprofile table is absent
- fix #10 invalid JSON response when adding [w4os_profile] shortcode element
- fix wrong letter cases in auth table name
- fix only show profile form for current user
- better css loading
- only check once if w4os db is connected
- added login page link to message displayed when trying to see profile while not connected
- more detailed error messages for avatar creation

### 1.1.4
- added changelog, banners and icons to view details
- fix "Yes" and "No" translations
- fix typo in banners and icons urls, can't believe I didn't see this before...
- fixed conflict with other extensions settings pages
- changed update server library to [frogerme's WP Plugin Update Server](https://github.com/froger-me/wp-plugin-update-server)

### Previous
- For full change history see [GitHub repository](https://github.com/GuduleLapointe/w4os/commits/master)
