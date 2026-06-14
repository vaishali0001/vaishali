# RogueVault — Roguelike Game Discovery and Rating Hub

## Project Context

RogueVault is a community-driven discovery platform dedicated to roguelike and roguelite games. The goal of the project is to create a responsive single-page web application that allows players to browse a curated collection of games, filter them by gameplay characteristics, search for titles, view detailed information, and contribute new game entries to the collection.

The website must provide a modern gaming-inspired user interface and function entirely on the client side using HTML, CSS, and JavaScript. No backend services, APIs, databases, user accounts, or server-side technologies are required.

---

## Technology Requirements

The project must be built using:

- HTML5
- CSS3
- Vanilla JavaScript

Frameworks such as React, Vue, Angular, Next.js, Nuxt.js, Svelte, Bootstrap, Tailwind CSS, jQuery, or other third-party UI frameworks are not permitted.

The entire application must run locally by opening the HTML file in a browser.

---

## Fixed Game Tags

The application must use the following predefined tags:

- Permadeath
- Procedural Generation
- Turn-Based
- Deck-Building
- Dungeon Crawler
- Action Roguelite

These tags must be used consistently throughout the filter system, game cards, detail views, and submission form.

---

## Main Layout

The application must contain:

1. Header section
2. Search bar section
3. Filter sidebar
4. Game card grid
5. Game detail modal or detail panel
6. Submit a Game form

All sections must be visible and functional within the single-page application.

---

## Initial Game Collection

The application must contain exactly six pre-populated game entries on first load, each using a different combination of the predefined tags.

**Game 1**
- Title: Hollow Spire
- Cover image: hollow_spire.jpg
- Description: A lone adventurer descends an ever-shifting tower where every floor is rebuilt from scratch on death. Combat is turn-based and resource management is unforgiving.
- Tags: Permadeath, Procedural Generation, Turn-Based
- Difficulty: 4
- Replayability: 5

**Game 2**
- Title: Cardbound Crypt
- Cover image: cardbound_crypt.jpg
- Description: Build a deck of spells and relics as you crawl through a cursed crypt. Each run offers new card combinations and synergies to discover.
- Tags: Deck-Building, Procedural Generation, Dungeon Crawler
- Difficulty: 3
- Replayability: 5

**Game 3**
- Title: Iron Vein
- Cover image: iron_vein.jpg
- Description: A fast paced action roguelite set in collapsing mine shafts. Real time combat, dash mechanics, and permanent character loss on defeat.
- Tags: Action Roguelite, Permadeath, Dungeon Crawler
- Difficulty: 5
- Replayability: 4

**Game 4**
- Title: Echoes of Mournhall
- Cover image: echoes_mournhall.jpg
- Description: Explore a haunted manor where each room is procedurally generated. Turn based tactical combat against ghostly enemies.
- Tags: Turn-Based, Procedural Generation, Dungeon Crawler
- Difficulty: 3
- Replayability: 4

**Game 5**
- Title: Sigil Drifters
- Cover image: sigil_drifters.jpg
- Description: A deck building card battler where losing a run permanently retires your character and unlocks new starting decks.
- Tags: Deck-Building, Permadeath, Turn-Based
- Difficulty: 4
- Replayability: 5

**Game 6**
- Title: Rustbound Ascent
- Cover image: rustbound_ascent.jpg
- Description: Climb a procedurally generated wasteland tower in this action roguelite. Fast combat, scavenged weapons, and shifting layouts every run.
- Tags: Action Roguelite, Procedural Generation, Dungeon Crawler
- Difficulty: 5
- Replayability: 5

Each game entry must contain:

- Title
- Cover image
- Description
- Tag list
- Difficulty rating
- Replayability rating

---

## Asset Licensing

All six cover images must be sourced from public domain or Creative Commons Attribution sources, or created by the participant. The source URL, license type, and author name for each image must be recorded in task_metadata.json or an equivalent licensing note included with the submission.

---

## Game Card Grid

The main content area must display game cards in a responsive grid layout.

Each game card must display:

- Cover image
- Game title
- Assigned tags

Game cards must be generated dynamically from a JavaScript data array.

---

## Search Functionality

A search input must appear above the game grid.

The search must:

- Filter games by title
- Update results as the user types
- Work without page reloads
- Be case insensitive

Clearing the search input must restore all matching games.

---

## Tag Filtering

A filter sidebar must contain checkboxes for all predefined tags.

Selecting one or more tags must:

- Filter displayed games in real time
- Work without page reloads

When no tags are selected, all games must be displayed.

A game remains visible only if it contains all of the currently selected tags.

---

## Game Detail View

Clicking any game card must open a detail view.

The detail view may be implemented as a modal window or an expandable panel.

The detail view must display:

- Game title
- Cover image
- Full description
- Complete tag list
- Difficulty rating
- Replayability rating

---

## Star Ratings

Difficulty and Replayability ratings must be displayed using star icons.

Requirements:

- Ratings range from 1 to 5
- Filled stars represent the rating value
- Both ratings must be visible in the detail view

---

## Submit a Game Form

The application must contain a form titled "Submit a Game".

The form must include:

- Title field
- Description field
- Cover image URL field
- Tag selection checkboxes
- Submit button

---

## Form Validation

The following validation rules are required:

- Title field cannot be empty
- Description field cannot be empty
- Cover image URL field cannot be empty
- At least one tag must be selected

The game must not be submitted if validation fails.

Validation messages must be displayed to the user near the relevant field.

---

## Game Submission Behavior

Submitting a valid form must:

- Create a new game object
- Add the game to the collection
- Display the new game card immediately at the end of the grid
- Update the grid without page reload

The newly added game must be searchable and filterable immediately after creation.

Submitted games without a difficulty or replayability rating default to a rating of 1 star for each.

---

## Local Storage

The application must use localStorage.

Requirements:

- Initial six games load from a JavaScript array and are not duplicated into localStorage
- User-submitted games are stored in localStorage under the key `roguevault_games`
- Submitted games remain available after page refresh
- Application data must not rely on external databases

---

## Responsive Design

The application must function correctly on:

- Desktop screens
- Tablet screens
- Mobile screens

The application must display without horizontal scrolling at a viewport width of 360 pixels.

---

## Styling Requirements

The design must use a roguelike-inspired gaming theme.

Required visual style:

- Dark background using a color value in the range of #0d0d0d to #1a1a1a
- Accent color used for buttons, links, and active filter states
- Card-based layout for the game grid
- Hover effect on game cards that changes the card's border or shadow
- Clear visual hierarchy between header, filters, and grid

---

## Deliverables

The final submission must contain one of the following:

**Option A:**
- index.html
- style.css
- script.js

**Option B:**
- Single combined HTML file containing HTML, CSS, and JavaScript

---

## Out of Scope

The following features must not be implemented:

- User registration
- User login
- Payment processing
- Backend APIs
- External databases
- Multiplayer functionality
- Comment systems
- Review systems beyond the provided ratings
- Server-side programming

---

## Acceptance Gates

The submission will be accepted only if:

1. The application contains exactly six pre-populated games matching the titles, tags, and ratings listed in the Initial Game Collection section.
2. The search input filters the grid by title as the user types, case insensitively, without a page reload.
3. Selecting one or more tag checkboxes filters the grid to show only games containing all selected tags, without a page reload.
4. Clicking any game card opens a detail view.
5. The detail view displays the title, cover image, full description, tag list, difficulty rating, and replayability rating of the clicked game.
6. Difficulty and replayability ratings are displayed as star icons with values from 1 to 5.
7. Submitting the Submit a Game form with any required field empty displays a validation message and does not add a game.
8. Submitting the Submit a Game form with all required fields filled and at least one tag selected adds a new game card to the grid immediately.
9. A game submitted through the form remains in the grid after the page is refreshed.
10. The application displays without horizontal scrolling at a viewport width of 360 pixels.
11. The application runs using only HTML, CSS, and JavaScript with no external frameworks or libraries.
