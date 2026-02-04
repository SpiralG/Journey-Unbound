# 📋 Journey Unbound - Requirements Document

**Project:** Journey Unbound BDSM/Kink Checklist  
**Version:** 6.0  
**Last Updated:** February 4, 2026  
**Status:** ✅ Active Development

---

## 🎯 Project Overview

### Vision
A comprehensive, boundary-respecting self-exploration tool for the BDSM/kink community that helps individuals understand their desires, limits, and needs.

### Mission
Provide a private, judgment-free space for kinksters to:
- Discover and track interests
- Understand their needs using NVC framework
- Honor and communicate boundaries
- Evolve their exploration over time

---

## 👥 Target Users

1. **Primary:** Individual kinksters (all experience levels)
2. **Secondary:** Partnered couples/groups exploring together
3. **Tertiary:** Community educators and facilitators

---

## ✅ Functional Requirements

### FR1: Core Data Model

**FR1.1: Activity Properties**
- Each activity must have:
  - Unique identifier (key)
  - Name (string)
  - Category (enum: 15 categories)
  - Group (string, optional)
- User can select:
  - Experience: Never tried | Tried | Open to
  - Rating: 1-5 stars (only if Tried)
  - Limit: Hard Limit | Soft Limit | Curious | Enjoy | Favourite
  - Fetish: Boolean
  - Needs: Array (multi-select from 48 or 33+48)
  - Notes: String (unlimited length)
  - Revisit Dates: Array of ISO dates

**FR1.2: Data Structure**
```javascript
{
  "category.group.activity": {
    experience: "Tried",
    rating: 4,
    limit: "Enjoy",
    fetish: true,
    needs: ["Connection", "Trust", "Excitement"],
    notes: "Personal reflections...",
    revisitDates: ["2024-01-15", "2024-06-20"]
  }
}
```

---

### FR2: Categories & Content

**FR2.1: Category Structure**
- System must have exactly 15 categories
- Each category must have:
  - Unique name
  - Icon (emoji)
  - Items grouped meaningfully
- Categories:
  1. Roles & Identity 🎭
  2. Relationships & Sexuality 💕
  3. Sensation & Touch ✨
  4. Communication & Connection 💬
  5. Power Exchange ⚡
  6. Restraint & Bondage 🪢
  7. Impact Play 🎯
  8. Role Play & Fantasy 🎪
  9. Exploration & Expression 🌈
  10. Energy & Presence 🔮
  11. Sexual Activities 🔥
  12. Toys & Equipment 🧸
  13. Body Features & Aesthetics 💎
  14. Fluids & Edge Play 💧
  15. Gorean Lifestyle ⚜️

**FR2.2: Content Requirements**
- Minimum 1000 total activities
- Activities must be:
  - Clear and specific
  - Non-judgmental language
  - Gender-inclusive
  - Consent-focused

---

### FR3: Navigation & Views

**FR3.1: Category Navigation**
- Category buttons displayed horizontally
- Active category highlighted
- Completion badges show percentage
- ALL category always first
- Can switch between categories instantly

**FR3.2: ALL Category View**
- Shows all items across all categories
- Sort options:
  - A-Z (alphabetical)
  - By Category (grouped, default)
  - Rated First (rated items first)
- Category badges on each item
- Clicking badge jumps to that category
- Item count displayed
- All filters functional

**FR3.3: Print View**
- Formatted as readable table
- All categories included
- Legend at top
- Shows all user selections
- Print-friendly styling

---

### FR4: Filtering & Search

**FR4.1: Search**
- Real-time search across all categories
- Case-insensitive
- Searches activity names
- Clear/reset option
- Works with active filters

**FR4.2: Rating Filter**
- Click rating emoji to filter
- Shows only items with that rating
- Active state highlighted
- Click again to clear
- Works in category and ALL views

**FR4.3: Limit Filter**
- Click limit type to filter
- Shows only items with that limit
- Active state highlighted
- Click again to clear
- Works in category and ALL views

**FR4.4: Fetish Filter**
- ✦ Fetish button in legend
- Shows only fetish items
- Active state highlighted (pink)
- Click again to clear
- Works in category and ALL views

**FR4.5: Combined Filters**
- Multiple filters can be active
- Results match ALL active filters
- Clear indication of active filters
- Switching categories resets filters

---

### FR5: Needs System (NVC Framework)

**FR5.1: Regular NVC Needs**
- 48 needs organized by category:
  - Connection & Belonging
  - Autonomy & Freedom
  - Play & Rest
  - Meaning & Growth
  - Peace & Safety
  - Physical Needs
- Available for: Curious, Enjoy, Favourite, Open to

**FR5.2: Hard Limit Needs**
- 33 boundary-focused needs:
  - Avoiding Harm (11 items)
  - Physical & Emotional Safety (4 items)
  - Self-Respect & Dignity (4 items)
  - Autonomy & Boundaries (6 items)
  - Trust & Stability (6 items)
- Available ONLY for: Hard Limits
- Different label: "What need does honoring this boundary meet?"

**FR5.3: Soft Limit Needs**
- Combination of both lists (81 total)
- Shows boundary AND exploration needs
- Label: "What needs does this boundary serve? What might I explore?"
- Acknowledges dual nature

**FR5.4: Multi-Select**
- User can select multiple needs per activity
- Visual indication of selected needs
- Can deselect needs
- Auto-saves on change

**FR5.5: Dynamic Needs Switching**
- Changing limit type updates available needs
- Previously selected needs persist if in new list
- Needs not in new list are deselected
- Label updates dynamically

---

### FR6: Data Persistence

**FR6.1: Local Storage**
- All data stored in browser localStorage
- Key: 'journey-unbound-selections'
- JSON format
- Auto-save on every change (debounced)

**FR6.2: Export**
- Download as JSON file
- Filename: `journey-unbound-backup-YYYY-MM-DD.json`
- Contains all user selections
- Valid JSON format

**FR6.3: Import**
- Accept JSON file upload
- Validate format
- Merge or replace data (user choice)
- Handle errors gracefully
- Show success/error message

---

### FR7: User Interface

**FR7.1: Responsive Design**
- Mobile-first approach
- Breakpoints:
  - Mobile: < 768px
  - Tablet: 768px - 1024px
  - Desktop: > 1024px
- Touch-friendly targets (44px minimum)
- Horizontal scrolling for category nav on mobile

**FR7.2: Visual Design**
- Brand colors:
  - Purple: #6B46C1 (primary)
  - Peacock: #0891B2
  - Turquoise: #14B8A6
  - Pink: #F472B6
  - Deep Blue: #1E3A8A (text)
- Limit colors:
  - Hard Limit: Red
  - Soft Limit: Orange
  - Curious: Yellow
  - Enjoy: Green
  - Favourite: Purple
- Clean, modern aesthetic
- Sufficient contrast for readability

**FR7.3: Interactions**
- Hover states on all interactive elements
- Active states clearly visible
- Smooth transitions (< 300ms)
- Loading indicators when needed
- Instant feedback on clicks

---

## 🔒 Non-Functional Requirements

### NFR1: Privacy

**NFR1.1: Data Storage**
- **MUST:** All data stored locally only
- **MUST NOT:** Send any data to external servers
- **MUST NOT:** Use cookies for tracking
- **MUST NOT:** Include analytics
- **MUST NOT:** Log personal data to console

**NFR1.2: Export/Import**
- Exported data remains on user's device
- No cloud storage
- User controls all file handling

---

### NFR2: Performance

**NFR2.1: Load Time**
- **Target:** Initial load < 3 seconds
- **Target:** Time to interactive < 5 seconds
- Single HTML file (no additional requests)

**NFR2.2: Interaction Speed**
- **Target:** User actions feel instant (< 100ms)
- Search results real-time (< 300ms)
- Filter changes instant
- Category switching smooth

**NFR2.3: Scalability**
- Handle 1500+ activities without lag
- Smooth scrolling with 100+ visible items
- Search performs well across all content

---

### NFR3: Browser Compatibility

**NFR3.1: Supported Browsers**
- Chrome/Edge (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Mobile Safari (iOS 14+)
- Mobile Chrome (Android 10+)

**NFR3.2: Required Features**
- ES6 JavaScript support
- LocalStorage API
- CSS Grid & Flexbox
- Modern CSS (no IE11 support needed)

---

### NFR4: Accessibility

**NFR4.1: Visual**
- WCAG 2.1 AA contrast ratios
- Minimum font size: 14px
- Scalable text (no pixel-locked sizes)

**NFR4.2: Keyboard**
- All interactive elements keyboard accessible
- Logical tab order
- Focus indicators visible

**NFR4.3: Screen Readers**
- Basic screen reader support
- Semantic HTML
- ARIA labels where needed

---

### NFR5: Maintainability

**NFR5.1: Code Quality**
- Single HTML file architecture
- Well-commented code
- Consistent naming conventions
- Modular JavaScript functions

**NFR5.2: Version Control**
- Git repository
- Semantic versioning (X.Y format)
- Changelog for each version
- Tagged releases

**NFR5.3: Documentation**
- README.md for overview
- DEPLOYMENT_GUIDE.md for updates
- USER_STORIES.md for features
- TESTING_CHECKLIST.md for QA
- Comments in code for complex logic

---

## 🚫 Constraints & Limitations

### Technical Constraints
1. **Single-file architecture** - Entire app in one HTML file
2. **No external dependencies** - No frameworks, no CDN links
3. **No server** - Pure client-side application
4. **LocalStorage only** - No database, no cloud storage

### User Constraints
1. **Browser requirement** - Must use modern browser
2. **JavaScript required** - Cannot work without JS
3. **LocalStorage required** - Cannot save without localStorage
4. **One device** - Data doesn't sync across devices (export/import workaround)

### Content Constraints
1. **Static content** - Activities are hardcoded, not user-editable
2. **English only** - No internationalization
3. **15 categories** - Fixed category structure

---

## 📊 Success Metrics

### User Engagement
- [ ] Users complete at least 25% of activities
- [ ] Users return to update selections
- [ ] Export feature used (indicates value)

### Usability
- [ ] Less than 3 clicks to perform any action
- [ ] No user-reported critical bugs
- [ ] Positive user feedback on UX

### Performance
- [ ] Page load < 3 seconds on 3G
- [ ] Zero JavaScript errors in console
- [ ] Smooth interactions on mobile

---

## 🛠️ Technical Stack

### Core Technologies
- **HTML5** - Structure
- **CSS3** - Styling (Grid, Flexbox, Custom Properties)
- **Vanilla JavaScript (ES6)** - Logic
- **LocalStorage API** - Data persistence

### Development Tools
- VS Code (or any text editor)
- Browser DevTools
- Git & GitHub

### Deployment
- GitHub Pages
- Single `index.html` file
- Version control with tags

---

## 📅 Version Roadmap

### V1.0 (Complete)
- Core functionality
- 10 categories
- Basic filtering
- Single-select needs

### V4.0 (Complete)
- 5 new categories (Gorean, Sexual, etc.)
- Expanded content

### V5.0 (Complete)
- Multi-select needs
- Search functionality
- UI enhancements

### V6.0 (Current)
- ALL category
- Fetish filter
- Hard limit needs
- Dynamic needs lists

### V7.0 (Planned)
- Print modal with filters
- Enhanced export options
- Bug fixes from V6

### Future Versions
- Partner comparison tool
- Advanced filtering
- Community insights (privacy-preserving)

---

## 🔗 Related Documents

- [TESTING_CHECKLIST.md](TESTING_CHECKLIST.md) - Comprehensive test scenarios
- [USER_STORIES.md](USER_STORIES.md) - All user stories by epic
- [DEPLOYMENT_GUIDE.md](DEPLOYMENT_GUIDE.md) - How to deploy updates
- [README.md](README.md) - Project overview
- [V6_CHANGES_SUMMARY.md](V6_CHANGES_SUMMARY.md) - V6 changelog

---

## 📝 Change Log

| Date | Version | Changes |
|------|---------|---------|
| 2024-01-XX | V1.0 | Initial requirements |
| 2024-06-XX | V4.0 | Added 5 new categories |
| 2024-09-XX | V5.0 | Multi-select needs, search |
| 2026-02-04 | V6.0 | ALL category, fetish filter, hard limit needs |

---

## ✅ Requirements Status

### Implemented
- ✅ FR1-FR7: All functional requirements
- ✅ NFR1-NFR5: All non-functional requirements

### In Progress
- 🔄 Bug fixes (rating filter in ALL view)

### Planned
- 📋 Print modal enhancements (V7)
- 📋 Advanced export options (V7)

---

**Document Owner:** SpiralG  
**Last Review:** February 4, 2026  
**Next Review:** Before V7 development
