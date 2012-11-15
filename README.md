PermissionsExGUI
======

**PermissionsExGUI** (<em>v1.0</em>) is a remastered version of **[wipeX](http://github.com/NINJ4/wipeX)**, a script code of [@NINJ4](https://github.com/NINJ4) on **Github**. This version offers more options for its users.

Features have been added to version **PermissionsExGUI** to offer additional options and useful as _RCON_ option that allows you to refresh permissions into play when adding valid permissions from the web interface but also a form simple connection to avoid using a URL parameter to connect to.

Follow me on Twitter: **[twitter.com/pirmax](http://twitter.com/pirmax)**

Features
--------

* 100% more Ajax!
* Queued View & Confirm: Set up a list of PEX commands and execute them all at once!
* Alerts upon errors: Did you screw something up? No matter, PermissionsExGUI will alert you to the command that failed with a helpful error message!
* Event Logging: Find out who did what to the permissions database, and undo it!
* Simple install! Just follow the documented Config section, and move onto your webserver!
* Tight Security! Four easy to install security modules to keep unwanted wannabe-hackers out of your permissions:
    - No-Security - If you've already password protected the directory!
    - Simple-Security - If you don't need anything fancier!
    - PHPBB-Standalone Security - Only let certain phpbb groups use PermissionsExGUI.
    - PHPBB-Embedded Security - Same as Standalone, but made to be included in a phpbb page.
    - Login-Form - Prefer the security form!
* Monitoring of updates PermissionsExGUI!
* Use RCON option for reload permissions ingame `/pex reload`.

Requirements
------------

1. Functioning onweb server with `PHP 5.2+`
2. Minecraft Server with Bukkit and PermissionsEx installed ([dev.bukkit.org/server-mods/permissionsex/](http://dev.bukkit.org/server-mods/permissionsex/))
3. PermissionsEx configured to use MySQL ([github.com/PEXPlugins/PermissionsEx/wiki/Plugin-Configuration](http://github.com/PEXPlugins/PermissionsEx/wiki/Plugin-Configuration#wiki-mysql-backend-configuration))

Installation
------------

PermissionsExGUI to install, it is very simple, download the ZIP file and unzip it on Github on your computer and then send it to the root of your server.

Please, leave the name of the folder: `/PermissionsExGUI/`

Configuration
-------------

To configure the plugin, you must edit the file `/includes/pexgui.config.php` which is located in the folder of the archive you downloaded (ZIP).

Open the file and edit the first lines.

```
define("<TITLE_OPTION>", "<VALUE>");
```

<table width="100%">
<tr>
<th>Title Option</th>
<th>Description Option</th>
</tr>
<tr>
<td><b>SORT_BY_LADDER</td>
<td>Change to &#171; TRUE &#187; if you want to sort by rank-ladder and rank in the group list, instead of just rank.</td>
</tr>
<tr>
<td><b>SECURITY_MODULE</td>
<td>Several options are available to you to protect access to the page to other users. You can use the following types:<br /><br />
<b><code>no-security</code></b> does not secure page and leave free access to the manager (<em>not recommended</em>)<br />
<b><code>simple-security</code></b> secures the access manager with a parameter and a password in the URL (<em>insecure</em>)<br />
<b><code>phpbb-standalone</code></b> module is to be used with CMS phpBB<br />
<b><code>phpbb-embedded</code></b> is the equivalent of the module below to phpBB<br />
<b><code>login-form</code></b> is a module that provides the ability to enter credentials via a form (<em>very secure</em>)<br /><br />
IDs are configurable through parameters below.</td>
</tr>
<tr>
<td><b>SIMPLE_LOGIN</b></td>
<td>This parameter must include the administrator ID to connect via the module <code>login-form</code> if you use it.</td>
</tr>
<tr>
<td><b>SIMPLE_PASSWORD</b></td>
<td>This parameter must include the administrator password to connect via the module <code>login-form</code> or <code>simple-security</code> if you use it.</td>
</tr>
<tr>
<td><b>PHPBB_REL_PATH</b></td>
<td>The directory where phpbb is located, relative to this directory.</td>
</tr>
<tr>
<td><b>STANDALONE_GROUPS</b></td>
<td>The phpbb groups that are allowed to access WIPEX (default is Administrators only).</td>
</tr>
<tr>
<td><b>RCON_IP_SERVER</b></td>
<td>This parameter must include the IP address of the server if you want to use the option of PermissionsExGUI RCON. <em>Leave blank if you do not want to use the RCON option.</em></td>
</tr>
<tr>
<td><b>RCON_PORT_SERVER</b></td>
<td>This parameter must include the port of the server if you want to use the option of PermissionsExGUI RCON. <em>Leave blank if you do not want to use the RCON option.</em></td>
</tr>
<tr>
<td><b>RCON_PASSWORD</b></td>
<td>This parameter must include the RCON password of the server if you want to use the option of PermissionsExGUI RCON. <em>Leave blank if you do not want to use the RCON option.</em></td>
</tr>
<tr>
<td><b>MCMYSQL_SERVER</b></td>
<td>Server for database.</td>
</tr>
<tr>
<td><b>MCMYSQL_USER</b></td>
<td>Username for database.</td>
</tr>
<tr>
<td><b>MCMYSQL_PASS</b></td>
<td>Password for database.</td>
</tr>
<tr>
<td><b>MCMYSQL_DB</b></td>
<td>Database  name.</td>
</tr>
</table>

--------

After, don't touch others parameters, thanks!

Known Issues
------------
* Sometimes the queue area turns red upon successful completion of all tasks
* Cannot Undo Remove Group/Create Group events

To-Do
-----
* Enable undoing of all events
* Allow multiple setrank events to be undone simultaneously
* Possibility of changing the name of the SQL tables
* Make the undo system smarter
* Manage priority groups
* Improved home screen


Contact
------------

* Twitter: **[twitter.com/pirmax](http://twitter.com/pirmax)**
* Contact mail: **[rosemaxence(at)gmail(dot)com](mailto:rosemaxence@gmail.com)**
* My Minecraft Server: **[www.milleniumcraft.fr](http://www.milleniumcraft.fr)**