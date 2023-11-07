UI Design Specification V2

***This spec is work-in-progress.***

**All UI must work on both PC and mobile, and adapt to the screen size.**

This image is a general reference to the sort of semi-futuristic UI we want (this one was a WIP loadout selection, and some stuff isn't right): ![Reference UI](/designThemeish.png)

**All objects & instances should be ordered and named somewhat properly, so that is simple for us to implement this UI via code.**

# Menu
Once a player has spawned there must be a way to close the menu without respawning, a return button or similarly.

	- Player profile/details
		- It should show the players level, cash (NCD$ currency) and Blanks (special more rare currency)
		- Preferrably the amount of money you have would be visible at for example team purchasing/unlocking

	- Daily rewards
		- There should be a daily reward popup, you can progress by playing every day, so you play 5 days in a row you gain more stuff (7 days max)

![Current daily reward](/dailyReward.png)

### Start page
Somewhere in the menu we would like a button place for inviting your friends, and a button the referral program.

	- Latest update
		- Allows the user to see if there is a new update
		- If the user wishes too, they can read more about the update details
### Team & subteam selection
A subpage

	- Team selection (subpage?)
		- Team image/viewport frame (would contain a character from that specific team)
		- Team name
		- Short description
		- Play/unlock button
			- If players do not own the team they must unlock it, this can be done in multiple ways, depending on the team. A team can have all the following ways to unlock it, or just one:
				- Gamepass
				- Bypass DevProduct (one-time Robux purchase)
				- Permanent purchase with Blanks
				- Temporary purchase with Blanks
				- Unlock via XP
				- Unlocked by maxing out the previous subteam (N/A for teams)
			- It must be simple for players to quickly understand if and how they unlock the team.
		- Players and player limit
	- Subteam selection (all teams except one have subteams/units)
		- Same as team

### Store & armory
This page is not exclusive to the menu, and should be usable outside of the menu, at a "vendor" in game.

This should be divided into two parts:
A store page, and a armory.

The store page contains all gamepasses and consumables. Including team packs, events (like raid), XP & cash boosts etc. It also contains consumables like armor plating and one-life weapons, but these consumables are only available at a vendor, not when in the menu.

The armory should not be accessible from the menu, because it depends on having selected a team and subteam, as the loadout is different for each.
You can select your loadout items like morph (do not separate vest & helmet etc.), primary weapon, secondary weapon and additional tools, like a tablet or a dart gun.

![BRM5 loadout UI](/armory.png)

The weapon selections should show stats about the firearm (see the top image). As well as ownership status, and how you unlock it (purchase with currency or at a certain rank etc.).

### Settings
The settings contains categories and subsettings. These are generated, we only need a few templates:

	- Category
		- Boolean/checkbox item template
		- Number slider item template
		- Color item template

Items contains name, description, and the value itself.

There should also be a reset to defaults button.

![Current settings UI](/settings.png)

### Credits page
There should not be that much focus on this, it should be there if players want to see the credits, but it should not be in the way for other stuff.

# Main UI
Our current main UI as a reference:
![Current UI](/currentMainUI.png)

The current UI takes up too much space on the left, especially on mobile.

Playerlist specification:

	- Shows player's ranks
	- Should show if a player has Roblox Premium (or other icon if applicable)
	- Clickable, which pops out a menu that shows their avatar, allows you to send friend request, see their subteam and rank (popup like Roblox's default one)

	- There must be a place for keybinds, these could be a key on the keyboard, a mouse button or touch input.
		- There must be icons/letters that correspond to the input.
		- There must be a name, like "Reload".

Top bar specification:

	- The current bars are very plain, and lack effects or anything that make them interesting
	- The same information as now should be displayed, but in a more exiting manner

Requirements for new UI on the left:

	- Must be more compact, the current buttons could be concentrated into just icons at the top left
	- All the existing buttons should still exist
	- The current health & armor bar should be similar to now, but adapted to whatever UI design-language is used

Some ranks have abilities, which also needs a button. This one should not be compact as the other and should show the progress bar and name of the ability.

![Current ability UI](/ability.png)

# Factions & unions
### Layout

- **Main Panel:** This should occupy the majority of the screen and is presented as a wide panel menu.
- **Top tabs:** The top section of the menu features tabs for navigation, allowing players to switch between different sections: "HOME," "CREATE/EDIT," "FACTION," and "PERKS."
- **Home page:** The default landing page.

### Home tab

The home tab is where players can explore existing factions and join or create their own.

- **Search Bar:** Located at the top, players can search for specific factions.
- **Popular Factions:** A small list of popular public factions appears on the right side of the menu.
- **Faction List:** The search results will be displayed in the middle of the UI, providing a list of factions.
- **Faction Details:** Clicking on a faction reveals details on the left side, including a larger faction picture, name, description, and overall score.
- **Join Button:** Allows players to join the selected faction.

### Create and edit tabs

- **Create tab:** In this section, players can create their own faction by specifying a name, picture, and description.
- **Edit tab:** Accessible only to the owner of the faction, this tab allows for editing settings such as faction name, picture, description, and the invitation requirement.
- **Invitation setting:** The owner can toggle between requiring an invitation for joining or making the faction public.
- **List of Faction Members:** A list of faction members is displayed on the right side. Clicking on a member's name reveals their avatar, name, rank in the faction, points earned, and the duration they've been in the faction.
- **Exile and Promote Options:** The owner can exile or promote members, with a confirmation prompt. Exile may also include an option to blacklist the player.
- **Blacklisted Players Tab:** This tab displays a list of banned players with an option to unban them.

### Faction tab

This tab is available only to members of a faction and provides information about the faction, its members, overall score, and points earned.

- **Faction Information:** Displays the faction's name, picture, description, overall score, and points.
- **Member List:** A list of faction members is shown on the right side, excluding the banned players tab.

### Perks tab

The perks tab serves as a faction-specific shop where members can spend their accumulated points.

- **Shop Items:** Players can spend their faction points to purchase items like riots, temporary spawn items/weapons, and perk boosts.
- **Officer Permissions:** In the "EDIT" tab, the owner can toggle whether officers can spend faction points in the shop.

### Points and Scoring

- **Points Accumulation:** Points are earned through various in-game activities, such as completing missions and objectives.
- **Overall Score:** This is the total sum of points the faction has achieved and is prominently displayed in the Faction tab.
- **Spending Points:** Points can be spent in the perks tab.

# Mission UI
This UI should display missions that a user can complete. It should also include a prestigeful & vibrant popup that rewards the player.

Current mission UI:

![Current mission UI](/missions.png)

The current ui has bad padding and is not very exiting at all. We want players to feel like they want to do these missions and that they matter. It should be interesting and rewarding to progress and complete these missions.

We also want a smaller popout that shows up somewhere on the screen when a player progresses. This must not disrupt gameplay.

When all active missions are completed, the UI should show a "good job" UI, making the player feel that they have accomplished something meaningful that hepls them progress in the game.

# Notification feed
The current notification feed is very boring.

![Current notification feed](/currentNotifications.png)

It only shows text, partly in a different color. This feed must look interesting, but not disrupting.
It must have more "visual effects" and seem special.
When a player has a XP or cash booster active, it should also show in a special color, perhaps glowing? or stand out in some sense, to indicate that the booster gives the player additional benefits.

The current kill feed for weapons is a slight step in the right direction, but it's far from perfect.

![Killfeed](/killfeed.png)

# Tutorial
We need a tutorial UI, I have drawn this beautiful example. It doesn't have to look like this, all we need is: text, character image spot, next button, skip button.

![Tutorial](/tutorial.png)