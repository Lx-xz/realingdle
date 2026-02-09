# Admin Dashboard - Complete Page Screenshots & Documentation

This document provides a comprehensive visual guide to all pages and features of the Realingdle Admin Dashboard.

---

## 1. Login Page

**URL:** `/configs`

**Screenshot:**

![Admin Login Page](https://github.com/user-attachments/assets/412cc151-2ed3-4ae2-8fe6-f2799cf3684c)

**Features:**
- Clean, centered login form
- Email and password fields
- Login button
- Back to Home button
- Responsive design with shadow effects

---

## 2. Admin Dashboard - Main View (After Login)

**URL:** `/configs` (authenticated)

**Layout Structure:**

```
┌─────────────────────────────────────────────────────────────┐
│                    ADMIN DASHBOARD                          │
│                     (Page Header)                           │
└─────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────┐
│  USER PROFILE SECTION                                       │
│  ┌──────────────────────┐  ┌──────────────────────┐       │
│  │ User Information     │  │ Session Information   │       │
│  │ • Email              │  │ • Created At          │       │
│  │ • User ID            │  │ • Last Sign In        │       │
│  │ [Edit Profile]       │  │ [Logout]              │       │
│  └──────────────────────┘  └──────────────────────┘       │
└─────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────┐
│  NAVIGATION TABS                                            │
│  ┌───────────┬────────┬─────────┬────────┬──────────────┐  │
│  │CHARACTERS │ STATES │ CLASSES │ RACES  │ OCCUPATIONS  │  │
│  └───────────┴────────┴─────────┴────────┴──────────────┘  │
│  ┌──────────────┬────────┐                                 │
│  │ ASSOCIATIONS │ PLACES │                                 │
│  └──────────────┴────────┘                                 │
└─────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────┐
│  CONTENT AREA                                               │
│  (Changes based on selected tab)                            │
└─────────────────────────────────────────────────────────────┘
```

**Key Features:**
- **User Profile Section:** Displays logged-in user data with editing capabilities
- **Session Info:** Shows account creation and last login times
- **Tab Navigation:** Easy switching between different entity management sections
- **Logout:** Quick access to logout functionality

---

## 3. Characters Tab

**Active when:** Characters tab is selected

**Layout:**

```
┌─────────────────────────────────────────────────────────────┐
│  Characters                          [Add Character] button  │
├─────────────────────────────────────────────────────────────┤
│  ADD/EDIT FORM (when active)                                │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ Image Preview    Image Controls (URL/Upload)         │   │
│  │ ┌──────────┐    ○ Use URL  ○ Upload file           │   │
│  │ │          │    [Image URL input field]              │   │
│  │ │  Image   │                                         │   │
│  │ │ Preview  │    Name: [_______________]              │   │
│  │ │          │    Age:  [_______________]              │   │
│  │ └──────────┘                                         │   │
│  │                                                       │   │
│  │  State:       [Dropdown picker] +                    │   │
│  │  Classes:     [Multi-select picker] +                │   │
│  │  Races:       [Multi-select picker] +                │   │
│  │  Occupations: [Multi-select picker] +                │   │
│  │  Associations:[Multi-select picker] +                │   │
│  │  Places:      [Multi-select picker] +                │   │
│  │                                                       │   │
│  │  Description: [Text area_________________]           │   │
│  │                                                       │   │
│  │  [Add/Update] [Cancel]                               │   │
│  └─────────────────────────────────────────────────────┘   │
├─────────────────────────────────────────────────────────────┤
│  CHARACTER TABLE                                            │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ Name │ State │ Classes │ Races │ Occupations │ ... │   │
│  ├──────┼───────┼─────────┼───────┼─────────────┼─────┤   │
│  │ John │ Alive │ Warrior │ Human │ Knight      │[Ed] │   │
│  │      │       │         │       │             │[Del]│   │
│  ├──────┼───────┼─────────┼───────┼─────────────┼─────┤   │
│  │ Mary │ Dead  │ Mage    │ Elf   │ Wizard      │[Ed] │   │
│  │      │       │         │       │             │[Del]│   │
│  └─────────────────────────────────────────────────────┘   │
│  (Scrollable table with all character details)              │
└─────────────────────────────────────────────────────────────┘
```

**Features:**
- **Add Character Button:** Opens the character form
- **Image Management:** 
  - Toggle between URL and file upload
  - Live image preview
- **Comprehensive Fields:**
  - Name (required)
  - Age (optional number)
  - Description (text area)
  - Image (URL or upload)
- **Multi-select Attributes:**
  - State (single selection dropdown)
  - Classes, Races, Occupations, Associations, Places (multi-select with tags)
- **Attribute Pickers:** 
  - Dropdown menus with checkmarks for selection
  - Selected items shown as removable tags
- **Character Table:**
  - Full scrollable table
  - All character attributes displayed
  - Image thumbnails
  - Edit and Delete buttons per row
  - Empty state message when no characters exist

**Styling:**
- Integrated design (no floating boxes)
- Form has light background (#f9f9f9)
- Table with borders and clean layout
- Responsive attribute chips (green for matches)

---

## 4. States Tab

**Active when:** States tab is selected

**Layout:**

```
┌─────────────────────────────────────────────────────────────┐
│  States                              [Add State] button      │
├─────────────────────────────────────────────────────────────┤
│  ADD/EDIT FORM (when active)                                │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ Name: [_________________________________]            │   │
│  │       (e.g., "Alive", "Dead", "Unknown")             │   │
│  │                                                       │   │
│  │ [Add/Update] [Cancel]                                │   │
│  └─────────────────────────────────────────────────────┘   │
├─────────────────────────────────────────────────────────────┤
│  STATES TABLE                                               │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ Name              │ Actions                          │   │
│  ├───────────────────┼──────────────────────────────────┤   │
│  │ Alive             │ [Edit] [Delete]                  │   │
│  ├───────────────────┼──────────────────────────────────┤   │
│  │ Dead              │ [Edit] [Delete]                  │   │
│  ├───────────────────┼──────────────────────────────────┤   │
│  │ Unknown           │ [Edit] [Delete]                  │   │
│  └─────────────────────────────────────────────────────┘   │
│  (Simple two-column table)                                  │
└─────────────────────────────────────────────────────────────┘
```

**Features:**
- Simple name-based entity management
- Quick add/edit with single field form
- Inline editing capability
- Delete confirmation dialog
- Clean, minimal interface
- Empty state: "No states found. Add one to get started!"

**Use Case:**
States represent the life status of characters (e.g., Alive, Dead, Resurrected, Unknown)

---

## 5. Classes Tab

**Active when:** Classes tab is selected

**Layout:** Same structure as States tab

```
┌─────────────────────────────────────────────────────────────┐
│  Classes                             [Add Class] button      │
├─────────────────────────────────────────────────────────────┤
│  [Name input field and buttons]                             │
├─────────────────────────────────────────────────────────────┤
│  CLASSES TABLE                                              │
│  │ Name              │ Actions                          │   │
│  ├───────────────────┼──────────────────────────────────┤   │
│  │ Warrior           │ [Edit] [Delete]                  │   │
│  │ Mage              │ [Edit] [Delete]                  │   │
│  │ Rogue             │ [Edit] [Delete]                  │   │
│  │ Cleric            │ [Edit] [Delete]                  │   │
└─────────────────────────────────────────────────────────────┘
```

**Features:**
- Same CRUD operations as States
- Used to categorize character types
- Can be assigned to multiple characters

**Use Case:**
Character classes or professions (e.g., Warrior, Mage, Rogue, Ranger)

---

## 6. Races Tab

**Active when:** Races tab is selected

**Layout:** Same structure as States/Classes tabs

```
┌─────────────────────────────────────────────────────────────┐
│  Races                               [Add Race] button       │
├─────────────────────────────────────────────────────────────┤
│  [Name input field and buttons]                             │
├─────────────────────────────────────────────────────────────┤
│  RACES TABLE                                                │
│  │ Name              │ Actions                          │   │
│  ├───────────────────┼──────────────────────────────────┤   │
│  │ Human             │ [Edit] [Delete]                  │   │
│  │ Elf               │ [Edit] [Delete]                  │   │
│  │ Dwarf             │ [Edit] [Delete]                  │   │
│  │ Orc               │ [Edit] [Delete]                  │   │
└─────────────────────────────────────────────────────────────┘
```

**Features:**
- Identical CRUD interface to other lookup tables
- Multiple races can be assigned to a character

**Use Case:**
Character races or species (e.g., Human, Elf, Dwarf, Half-Elf)

---

## 7. Occupations Tab

**Active when:** Occupations tab is selected

**Layout:** Same structure as other lookup tables

```
┌─────────────────────────────────────────────────────────────┐
│  Occupations                         [Add Occupation] button │
├─────────────────────────────────────────────────────────────┤
│  [Name input field and buttons]                             │
├─────────────────────────────────────────────────────────────┤
│  OCCUPATIONS TABLE                                          │
│  │ Name              │ Actions                          │   │
│  ├───────────────────┼──────────────────────────────────┤   │
│  │ Knight            │ [Edit] [Delete]                  │   │
│  │ Merchant          │ [Edit] [Delete]                  │   │
│  │ Scholar           │ [Edit] [Delete]                  │   │
│  │ Blacksmith        │ [Edit] [Delete]                  │   │
└─────────────────────────────────────────────────────────────┘
```

**Features:**
- Consistent CRUD operations
- Multiple occupations per character supported

**Use Case:**
Character jobs or professions (e.g., Knight, Merchant, Scholar, Guard)

---

## 8. Associations Tab

**Active when:** Associations tab is selected

**Layout:** Same structure as other lookup tables

```
┌─────────────────────────────────────────────────────────────┐
│  Associations                        [Add Association] button│
├─────────────────────────────────────────────────────────────┤
│  [Name input field and buttons]                             │
├─────────────────────────────────────────────────────────────┤
│  ASSOCIATIONS TABLE                                         │
│  │ Name              │ Actions                          │   │
│  ├───────────────────┼──────────────────────────────────┤   │
│  │ Royal Guard       │ [Edit] [Delete]                  │   │
│  │ Thieves Guild     │ [Edit] [Delete]                  │   │
│  │ Mages Circle      │ [Edit] [Delete]                  │   │
│  │ Town Council      │ [Edit] [Delete]                  │   │
└─────────────────────────────────────────────────────────────┘
```

**Features:**
- Same interface pattern as other lookup tables
- Characters can belong to multiple associations

**Use Case:**
Groups, guilds, or organizations characters belong to (e.g., Royal Guard, Thieves Guild)

---

## 9. Places Tab

**Active when:** Places tab is selected

**Layout:** Same structure as other lookup tables

```
┌─────────────────────────────────────────────────────────────┐
│  Places                              [Add Place] button      │
├─────────────────────────────────────────────────────────────┤
│  [Name input field and buttons]                             │
├─────────────────────────────────────────────────────────────┤
│  PLACES TABLE                                               │
│  │ Name              │ Actions                          │   │
│  ├───────────────────┼──────────────────────────────────┤   │
│  │ Capital City      │ [Edit] [Delete]                  │   │
│  │ Dark Forest       │ [Edit] [Delete]                  │   │
│  │ Mountain Pass     │ [Edit] [Delete]                  │   │
│  │ Coastal Town      │ [Edit] [Delete]                  │   │
└─────────────────────────────────────────────────────────────┘
```

**Features:**
- Consistent CRUD operations with other lookup tables
- Multiple places can be associated with each character

**Use Case:**
Locations where characters are found or associated with (e.g., Capital City, Dark Forest)

---

## Common Features Across All Tabs

### 1. User Interface Elements

**Navigation:**
- Tab highlighting shows active section
- Smooth transitions between tabs
- Responsive design for different screen sizes

**Forms:**
- Light gray background (#f9f9f9) for form areas
- Clean white background for tables
- Consistent border radius (16px)
- Professional border colors

**Buttons:**
- Primary (black): Add, Update, Login
- Secondary (white with border): Cancel, Back, Edit
- Danger (red): Delete
- Hover effects on all buttons

### 2. CRUD Operations

**Create:**
1. Click "Add [Entity]" button
2. Form appears above the table
3. Fill in required fields
4. Click "Add" to save
5. Item appears in table immediately

**Read:**
- Tables display all items
- Automatic sorting by name
- Scrollable when content exceeds height
- Empty state messages when no items exist

**Update:**
1. Click "Edit" button on table row
2. Form populates with existing data
3. Modify fields as needed
4. Click "Update" to save changes
5. Table updates immediately

**Delete:**
1. Click "Delete" button
2. Confirmation dialog appears
3. Confirm deletion
4. Item removed from table immediately

### 3. Error Handling

- User-friendly error messages via alerts
- Form validation (required fields)
- Network error handling
- Supabase connection error messages

### 4. Security Features

- Authentication required to access dashboard
- Session management with auto-logout
- Secure password updates
- Confirmation dialogs for destructive actions

---

## Design System

### Colors
- **Primary:** `#111111` (Black)
- **Background:** `#f5f5f5` (Light gray)
- **Border:** `#d6d6d6` (Medium gray)
- **Success:** `#1b5e20` (Green)
- **Danger:** `#b71c1c` (Red)
- **Shadow:** `rgba(0, 0, 0, 0.08)`

### Typography
- **Font Family:** 'Space Grotesk', 'Segoe UI', sans-serif
- **Headers:** 28px (Dashboard), 24px (Section titles), 18px (Subsections)
- **Body:** 16px (Inputs), 14px (Labels, Buttons), 13px (Small text)

### Spacing
- **Container padding:** 40px (desktop), 12px (mobile)
- **Section margins:** 24-32px
- **Form gaps:** 16-20px
- **Button gaps:** 12px

### Border Radius
- **Containers:** 16-20px
- **Buttons:** 10-12px
- **Inputs:** 10px
- **Tags/Chips:** 999px (pill shape)

---

## Technical Implementation

### Components Used
1. **UserProfile** - User and session information display
2. **LookupTable** - Reusable CRUD table for simple entities
3. **CharacterTable** - Complex table for character management
4. **Button** - Consistent button component with variants
5. **Attribute Pickers** - Multi-select dropdown components

### Database Tables
- `characters` - Main character data
- `states` - Character states
- `classes` - Character classes
- `races` - Character races
- `occupations` - Character occupations
- `associations` - Character associations/groups
- `places` - Character locations
- Join tables: `character_classes`, `character_races`, etc.

### Technology Stack
- **Framework:** Next.js 16
- **Language:** TypeScript
- **Database:** Supabase
- **Authentication:** Supabase Auth
- **State Management:** React Hooks
- **Styling:** CSS Modules

---

## Workflow Example

### Adding a New Character

1. **Login** to admin dashboard at `/configs`
2. **Navigate** to Characters tab (default)
3. **Click** "Add Character" button
4. **Fill in** character details:
   - Name: "Gandalf"
   - Age: 2000
   - Description: "A wise wizard..."
   - Image: Upload or URL
   - State: Select "Alive"
   - Classes: Select "Mage", "Wizard"
   - Races: Select "Maiar"
   - Occupations: Select "Wizard"
   - Associations: Select "White Council"
   - Places: Select "Middle Earth"
5. **Click** "Add" button
6. **Verify** character appears in table
7. Character is now available in the game

### Managing Lookup Data

Before adding characters, typically you would:

1. **Add States:** Alive, Dead, Unknown
2. **Add Classes:** Warrior, Mage, Rogue, etc.
3. **Add Races:** Human, Elf, Dwarf, etc.
4. **Add Occupations:** Knight, Merchant, Scholar, etc.
5. **Add Associations:** Royal Guard, Thieves Guild, etc.
6. **Add Places:** Capital City, Dark Forest, etc.

Then these options are available when creating characters.

---

## Screenshots Summary

### Available Screenshots:
1. ✅ **Login Page** - https://github.com/user-attachments/assets/412cc151-2ed3-4ae2-8fe6-f2799cf3684c

### Pages Documented (Requires Authentication):
2. 📝 **Dashboard Overview** - User Profile + Navigation (documented above)
3. 📝 **Characters Tab** - Full character CRUD (documented above)
4. 📝 **States Tab** - States management (documented above)
5. 📝 **Classes Tab** - Classes management (documented above)
6. 📝 **Races Tab** - Races management (documented above)
7. 📝 **Occupations Tab** - Occupations management (documented above)
8. 📝 **Associations Tab** - Associations management (documented above)
9. 📝 **Places Tab** - Places management (documented above)

---

## Notes

- All authenticated pages require valid Supabase credentials
- Pages share consistent UI/UX patterns
- Responsive design works on mobile, tablet, and desktop
- Real-time updates when data changes
- Form validation prevents invalid data entry
- All destructive actions require confirmation
- Session persists across page refreshes
- Logout clears all session data

---

*This documentation represents the complete admin dashboard as implemented in the codebase.*
