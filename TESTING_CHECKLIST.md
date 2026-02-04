# 🧪 Journey Unbound - Comprehensive Testing Checklist

**Version:** 6.0  
**Last Updated:** February 4, 2026  
**Status:** 🔄 In Progress

---

## 📋 How to Use This Checklist

This is a **master reference document**. When you find a bug:
1. Note it here with ❌
2. Create a GitHub Issue using the Bug Report template
3. Link the issue number here: `[Issue #XX]`

---

## 🚀 Initial Load & Setup

### Page Load
- [ ] Page loads without errors
- [ ] No console errors (F12 → Console)
- [ ] Intro screen displays correctly
- [ ] "Begin Your Journey" button visible and centered
- [ ] Button hover effect works
- [ ] Intro screen disappears after clicking button
- [ ] Main interface loads smoothly

### Data Persistence
- [ ] Fresh load (new browser) shows empty selections
- [ ] localStorage is created on first interaction
- [ ] Page refresh keeps all selections
- [ ] Data persists after closing/reopening browser
- [ ] Multiple tabs sync correctly (or don't interfere)

### Browser Compatibility
- [ ] Chrome/Edge (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Mobile Safari (iOS)
- [ ] Mobile Chrome (Android)

---

## 🎯 Category Navigation

### Category Buttons
- [ ] ALL category button appears FIRST
- [ ] ALL button shows completion percentage
- [ ] ALL percentage badge updates correctly
- [ ] 15 regular category buttons display
- [ ] All category icons render correctly (no broken emojis)
- [ ] Category names are readable
- [ ] Completion badges show on categories with progress
- [ ] Badges show correct percentages (0-100%)
- [ ] 100% completion shows different badge style

### Category Switching
- [ ] Clicking category switches view correctly
- [ ] Active category highlights properly
- [ ] Previous category content clears before new loads
- [ ] Switching preserves scroll position (or resets appropriately)
- [ ] Fast clicking doesn't break navigation
- [ ] Mobile: category nav scrolls horizontally if needed

### ALL Category Specific
- [ ] ALL category shows items from all 15 categories
- [ ] Category badges on items are clickable
- [ ] Clicking category badge jumps to that category
- [ ] Item count shows at top right
- [ ] Default sort is "by category"
- [ ] ALL category respects all filters

---

## 🔍 Search Functionality

### Search Bar
- [ ] Search bar visible and accessible
- [ ] Placeholder text clear
- [ ] Typing shows real-time results
- [ ] Search is case-insensitive
- [ ] Search finds partial matches
- [ ] Special characters don't break search
- [ ] Emoji in search works (if applicable)

### Search Results
- [ ] Results show across all categories
- [ ] Results highlight matching text (if implemented)
- [ ] No results shows appropriate message
- [ ] Clearing search shows all items again
- [ ] Search works with active filters
- [ ] Category badges show on search results

### Search Edge Cases
- [ ] Empty search shows all items
- [ ] Very long search terms handled
- [ ] Search while filtered shows correct subset
- [ ] Fast typing doesn't cause lag

---

## 🎨 Filtering System

### Rating Filter (Legend Bar)
- [ ] Rating emoji buttons appear in legend
- [ ] Clicking rating filters to that rating
- [ ] Active rating shows highlighted state
- [ ] Clicking same rating again clears filter
- [ ] Rating filter works in regular categories
- [ ] ❌ **BUG FOUND:** Rating filter NOT working in ALL view [Issue #__]
- [ ] Rating filter shows "no results" message when appropriate
- [ ] Multiple rapid clicks don't break filter

### Limit Filter (Legend Bar)
- [ ] All limit types show in legend
- [ ] Clicking limit type filters correctly
- [ ] Active limit shows highlighted state
- [ ] Clicking same limit again clears filter
- [ ] Limit filter works in regular categories
- [ ] Limit filter works in ALL view
- [ ] Limit filter shows "no results" message when appropriate

### Fetish Filter (Legend Bar)
- [ ] ✦ Fetish button appears in legend
- [ ] Button shows pink styling
- [ ] Clicking fetish filters to fetish items only
- [ ] Active state shows (pink background)
- [ ] Clicking again clears fetish filter
- [ ] Fetish filter works in regular categories
- [ ] Fetish filter works in ALL view
- [ ] Fetish filter combines with rating filter
- [ ] Fetish filter combines with limit filter

### Combined Filters
- [ ] Rating + Limit filters combine correctly
- [ ] Rating + Fetish filters combine correctly
- [ ] Limit + Fetish filters combine correctly
- [ ] All three filters work together
- [ ] Filters show correct item count
- [ ] "No results" when no items match all filters
- [ ] Clearing one filter updates results immediately

### Filter Reset Behavior
- [ ] Switching categories clears all filters
- [ ] Going to ALL category clears filters
- [ ] Clear search doesn't affect other filters
- [ ] Manual filter clear works correctly

---

## 🃏 Item Cards

### Card Display
- [ ] All item cards render correctly
- [ ] Card layout is consistent
- [ ] Group headers show properly
- [ ] Cards have proper spacing
- [ ] Mobile: cards stack vertically
- [ ] Desktop: cards use appropriate width

### Experience Selection
- [ ] "Never tried" button works
- [ ] "Tried" button works
- [ ] "Open to" button works
- [ ] Only one experience can be selected
- [ ] Clicking same experience deselects it
- [ ] Experience selection saves immediately
- [ ] Visual feedback on selection

### Rating System
- [ ] 5 star rating buttons appear
- [ ] Stars show correct emoji (⭐🌟✨)
- [ ] Clicking star selects that rating
- [ ] Clicking same star deselects rating
- [ ] Only one rating can be active
- [ ] Rating only enabled after experience selected
- [ ] Rating saves immediately
- [ ] Visual feedback on selection

### Limit Selection
- [ ] All 5 limit buttons appear
- [ ] Hard Limit (red) styling correct
- [ ] Soft Limit (orange) styling correct
- [ ] Curious (yellow) styling correct
- [ ] Enjoy (green) styling correct
- [ ] Favourite (purple) styling correct
- [ ] Only one limit can be selected
- [ ] Clicking same limit deselects it
- [ ] Limit saves immediately
- [ ] Visual feedback on selection

### Fetish Toggle
- [ ] Fetish checkbox/button appears
- [ ] Clicking toggles fetish on/off
- [ ] Visual indicator shows fetish status
- [ ] Fetish status saves immediately
- [ ] Works independently of other selections

### Needs Selection
- [ ] Needs section appears on card
- [ ] Label changes based on limit type:
  - [ ] Hard Limit: "What need does honoring this boundary meet?"
  - [ ] Soft Limit: "What needs does this boundary serve? What might I explore?"
  - [ ] Other: "What need does this meet?"
- [ ] Needs chips render correctly
- [ ] Multiple needs can be selected
- [ ] Clicking need toggles selection
- [ ] Selected needs highlight properly
- [ ] Needs save immediately
- [ ] 48 regular NVC needs available for most limits
- [ ] 33 hard limit needs for Hard Limits
- [ ] 81 total needs (both lists) for Soft Limits

### Notes Field
- [ ] "Add a note" button appears
- [ ] Clicking shows textarea
- [ ] Button changes to "Hide notes"
- [ ] Textarea expands appropriately
- [ ] Typing saves automatically (debounced)
- [ ] Notes persist on page reload
- [ ] Long notes don't break layout
- [ ] Mobile: textarea is accessible

### Revisit Tracking
- [ ] "Revisit" button appears
- [ ] Clicking adds current date
- [ ] Multiple revisit dates can be added
- [ ] Dates display chronologically
- [ ] Dates format correctly
- [ ] Revisit dates save immediately

---

## 📊 Sorting (ALL Category)

### Sort Options
- [ ] Sort dropdown appears in ALL view
- [ ] "A-Z" option available
- [ ] "By Category" option available
- [ ] "Rated First" option available
- [ ] Default sort is "By Category"

### Sort Behavior
- [ ] A-Z sorts alphabetically (case-insensitive)
- [ ] By Category groups by category, shows badges
- [ ] Rated First shows rated items at top
- [ ] Sort selection persists in ALL view
- [ ] Sort updates results immediately
- [ ] Sort works with active filters

---

## 🖨️ Print Functionality

### Print View Access
- [ ] Print button visible in header
- [ ] Clicking opens print view
- [ ] Print view loads all content
- [ ] Back/close button works

### Print Layout
- [ ] All categories included
- [ ] Items grouped by category
- [ ] Group headers visible
- [ ] Table format is readable
- [ ] Legend appears at top
- [ ] No cut-off content

### Print Content
- [ ] Activity names show
- [ ] Experience level shows
- [ ] Ratings display
- [ ] Limits display with colors
- [ ] Fetish status shows
- [ ] Needs display (truncated if needed)
- [ ] Notes display (truncated if needed)
- [ ] Empty items show appropriately

### Print Action
- [ ] Browser print dialog opens
- [ ] Print preview looks correct
- [ ] Actual print output matches preview
- [ ] Page breaks appropriately
- [ ] Headers/footers optional
- [ ] Landscape vs Portrait both work

---

## 💾 Import/Export

### Export Function
- [ ] Export button visible
- [ ] Clicking triggers download
- [ ] JSON file downloads correctly
- [ ] Filename includes date
- [ ] File contains all data
- [ ] File is valid JSON
- [ ] Large datasets export successfully

### Import Function
- [ ] Import button visible
- [ ] Clicking opens file picker
- [ ] Can select JSON file
- [ ] Valid JSON imports successfully
- [ ] Data merges or replaces appropriately
- [ ] Imported data renders correctly
- [ ] Invalid JSON shows error message
- [ ] Error message is helpful

### Data Integrity
- [ ] Exported then imported data matches exactly
- [ ] No data loss on export/import cycle
- [ ] Old version data imports to new version
- [ ] Corrupted data handled gracefully

---

## 📱 Responsive Design

### Mobile (< 768px)
- [ ] Layout adapts to narrow screen
- [ ] Category nav scrolls horizontally or wraps
- [ ] Cards stack vertically
- [ ] Touch targets are large enough
- [ ] No horizontal scroll on content
- [ ] Filters accessible and usable
- [ ] Search bar fits screen
- [ ] Legend bar readable

### Tablet (768px - 1024px)
- [ ] Layout uses available space
- [ ] Cards use 2-column or appropriate grid
- [ ] Navigation is comfortable
- [ ] Touch targets appropriate

### Desktop (> 1024px)
- [ ] Full layout displays
- [ ] Content centered or uses full width appropriately
- [ ] Hover states work on all interactive elements
- [ ] Maximum width prevents over-stretching

### Orientation Changes
- [ ] Portrait to landscape adapts smoothly
- [ ] No layout breaks
- [ ] Data persists through orientation change

---

## 🎨 UI/UX Polish

### Visual Consistency
- [ ] Colors match brand palette
- [ ] Font sizes are consistent
- [ ] Spacing is uniform
- [ ] Icons align properly
- [ ] Emoji render consistently across browsers

### Interactive Feedback
- [ ] Buttons have hover states
- [ ] Active states are clear
- [ ] Loading states (if any) are visible
- [ ] Transitions are smooth (not janky)
- [ ] No flashing or flickering

### Accessibility
- [ ] Sufficient color contrast
- [ ] Text is readable at default size
- [ ] Interactive elements are identifiable
- [ ] Tab navigation works logically
- [ ] Screen reader friendly (basic test)

### Performance
- [ ] Page loads in < 3 seconds
- [ ] Interactions feel instant (< 100ms)
- [ ] No lag when typing in search
- [ ] Scrolling is smooth
- [ ] Large datasets don't freeze UI

---

## 🔒 Data & Privacy

### Data Storage
- [ ] Data only stored in localStorage
- [ ] No network requests except page load
- [ ] No cookies set
- [ ] No analytics tracking
- [ ] Data visible in DevTools → Application → localStorage

### Data Security
- [ ] No sensitive data logged to console
- [ ] No data sent to external servers
- [ ] LocalStorage isolated per domain

---

## 🐛 Edge Cases & Error Handling

### Empty States
- [ ] New user sees appropriate intro/empty state
- [ ] No selections shows helpful message
- [ ] No search results shows helpful message
- [ ] No filter matches shows helpful message

### Extreme Data
- [ ] Very long activity names handled
- [ ] Very long notes handled
- [ ] Selecting all needs doesn't break layout
- [ ] 100s of revisit dates handled

### Browser Quirks
- [ ] Works in private/incognito mode
- [ ] Works with localStorage disabled (graceful degradation)
- [ ] Works with JavaScript (required, but shouldn't crash)
- [ ] Works with ad blockers

### Corrupted Data
- [ ] Handles corrupted localStorage gracefully
- [ ] Provides way to reset if broken
- [ ] Doesn't crash on malformed data

---

## 📊 Completion Tracking

### Progress Calculation
- [ ] Completion percentage accurate
- [ ] Updates in real-time as selections made
- [ ] 100% achieved correctly
- [ ] Partial progress shows correctly

### Badges
- [ ] Badges update immediately
- [ ] 100% badge shows different style
- [ ] 0% shows no badge or "0%"
- [ ] Percentages round correctly

---

## 🔄 Version-Specific Features (V6)

### ALL Category
- [ ] ALL category is first button
- [ ] Shows all 1000+ items
- [ ] Default sort is "by category"
- [ ] All filters work in ALL view
- [ ] Category badges are clickable

### Fetish Filter
- [ ] ✦ Fetish button in legend
- [ ] Filters to fetish-only items
- [ ] Works in category views
- [ ] Works in ALL view
- [ ] Combines with other filters

### Hard Limit Needs
- [ ] Hard Limits show 33 boundary-focused needs
- [ ] Soft Limits show 81 combined needs
- [ ] Other limits show 48 regular needs
- [ ] Label text changes dynamically
- [ ] Needs list updates when limit changes

### Dynamic Needs Lists
- [ ] Change from "Curious" to "Hard Limit" → needs list updates
- [ ] Change from "Hard Limit" to "Soft Limit" → sees both lists
- [ ] Previously selected needs persist if still in new list
- [ ] Needs not in new list are deselected automatically

---

## 📝 Known Issues

### Active Bugs
1. ❌ **Rating filter not working in ALL view** [Issue #__]
   - Status: Reported
   - Severity: High
   - Affects: ALL category filtering

### Future Enhancements
- Print modal with filter options (planned for V7)
- Filter persistence across category switches (considering)

---

## ✅ Testing Sign-Off

**Tested By:** _______________  
**Date:** _______________  
**Browser:** _______________  
**Device:** _______________  
**Result:** ✅ Pass / ⚠️ Pass with issues / ❌ Fail  

**Notes:**
