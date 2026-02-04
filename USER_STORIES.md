# 📖 Journey Unbound - User Stories

**Project:** Journey Unbound BDSM/Kink Checklist  
**Version:** 6.0  
**Last Updated:** February 4, 2026

---

## 🎯 Purpose

This document contains all user stories for Journey Unbound. User stories help us understand:
- **Who** the user is
- **What** they want to do
- **Why** it matters to them

---

## 👥 User Personas

### 1. **The Curious Explorer**
New to BDSM/kink, exploring what interests them, needs guidance and safety

### 2. **The Experienced Practitioner**
Knows their preferences, wants to track evolution and communicate with partners

### 3. **The Partnered Duo**
Couple exploring together, needs to compare interests and find common ground

### 4. **The Community Member**
Active in kink community, wants comprehensive tracking and self-understanding

### 5. **The Boundary-Conscious**
Focused on understanding limits and needs, prioritizes consent and self-knowledge

---

## 🌟 Epic 1: Self-Discovery & Exploration

### Story 1.1: Initial Exploration
**As a** curious explorer  
**I want** to browse activities by category  
**So that** I can discover what exists and what might interest me

**Acceptance Criteria:**
- 15 categories clearly labeled and organized
- Icons help identify category themes
- Can navigate between categories easily
- Activities grouped meaningfully within categories

**Priority:** ✅ IMPLEMENTED (V1)

---

### Story 1.2: Express Interest Level
**As a** user exploring activities  
**I want** to mark my experience level (Never tried, Tried, Open to)  
**So that** I can track what I've done and what I'm curious about

**Acceptance Criteria:**
- Three clear experience options
- One-click selection
- Visual feedback on selection
- Can change or deselect

**Priority:** ✅ IMPLEMENTED (V1)

---

### Story 1.3: Rate Experiences
**As an** experienced practitioner  
**I want** to rate activities I've tried (1-5 stars)  
**So that** I can remember what I enjoyed

**Acceptance Criteria:**
- 5-star rating system
- Clear emoji indicators
- Can only rate after marking "Tried"
- Can change or remove ratings

**Priority:** ✅ IMPLEMENTED (V1)

---

### Story 1.4: Understand My Needs
**As a** boundary-conscious user  
**I want** to identify what needs each activity meets  
**So that** I can understand *why* things appeal to me

**Acceptance Criteria:**
- 48 NVC needs available
- Can select multiple needs per activity
- Needs are organized meaningfully
- Can deselect needs

**Priority:** ✅ IMPLEMENTED (V5 - multi-select)

---

### Story 1.5: Mark Fetishes
**As a** user with specific interests  
**I want** to mark activities as fetishes  
**So that** I can highlight my core interests

**Acceptance Criteria:**
- Clear fetish toggle on each item
- Visual indicator for fetish status
- Can toggle on/off
- Saves immediately

**Priority:** ✅ IMPLEMENTED (V1)

---

## 🛡️ Epic 2: Boundaries & Consent

### Story 2.1: Set Hard Limits
**As a** boundary-conscious user  
**I want** to clearly mark my hard limits  
**So that** I know (and can communicate) what's non-negotiable

**Acceptance Criteria:**
- "Hard Limit" option available
- Visual distinction (red color)
- Cannot be accidentally changed
- Shows boundary-focused needs

**Priority:** ✅ IMPLEMENTED (V1, enhanced V6)

---

### Story 2.2: Set Soft Limits
**As an** explorer considering boundaries  
**I want** to mark soft limits (maybe, with conditions)  
**So that** I can indicate interest with caution

**Acceptance Criteria:**
- "Soft Limit" option available
- Visual distinction (orange)
- Shows both boundary and exploration needs

**Priority:** ✅ IMPLEMENTED (V1, enhanced V6)

---

### Story 2.3: Understand Boundary Needs
**As a** boundary-conscious user  
**I want** to see *why* my limits exist (what needs they protect)  
**So that** I can honor and explain my boundaries

**Acceptance Criteria:**
- Hard limits show 33 boundary-specific needs
- Needs like "To not feel violated", "Safety/Security"
- Different label: "What need does honoring this boundary meet?"
- Helps me validate my limits

**Priority:** ✅ IMPLEMENTED (V6)

---

### Story 2.4: Explore Soft Limit Complexity
**As a** user with soft limits  
**I want** to see both boundary AND exploration needs  
**So that** I can understand the dual nature of my soft limits

**Acceptance Criteria:**
- Soft limits show 81 combined needs
- Both protective and curious needs available
- Label: "What needs does this boundary serve? What might I explore?"
- Acknowledges complexity

**Priority:** ✅ IMPLEMENTED (V6)

---

## 📝 Epic 3: Tracking & Memory

### Story 3.1: Add Personal Notes
**As a** reflective user  
**I want** to add private notes to activities  
**So that** I can remember context, partners, or specific thoughts

**Acceptance Criteria:**
- Note field on each item
- Private (not shared)
- Auto-saves as I type
- Can be long (multiple paragraphs)

**Priority:** ✅ IMPLEMENTED (V1)

---

### Story 3.2: Track Evolution
**As an** experienced practitioner  
**I want** to mark when I revisit activities  
**So that** I can see how my interests evolve

**Acceptance Criteria:**
- "Revisit" button adds current date
- Multiple dates can be tracked
- Dates show chronologically
- Helps me see patterns

**Priority:** ✅ IMPLEMENTED (V1)

---

### Story 3.3: Monitor Progress
**As a** goal-oriented user  
**I want** to see completion percentage per category  
**So that** I can track how much I've explored

**Acceptance Criteria:**
- Percentage badge on each category
- Updates in real-time
- 100% shows special badge
- Motivates exploration

**Priority:** ✅ IMPLEMENTED (V1)

---

## 🔍 Epic 4: Finding & Filtering

### Story 4.1: Search Everything
**As a** user looking for specific activities  
**I want** to search across all categories  
**So that** I can quickly find what I'm looking for

**Acceptance Criteria:**
- Search bar always visible
- Real-time results
- Searches across all categories
- Case-insensitive

**Priority:** ✅ IMPLEMENTED (V5)

---

### Story 4.2: Filter by Rating
**As an** experienced user  
**I want** to filter by rating (see all 5-star activities)  
**So that** I can focus on my favorites

**Acceptance Criteria:**
- Click rating emoji in legend to filter
- Shows only items with that rating
- Works in category views
- Clear visual indicator

**Priority:** ✅ IMPLEMENTED (V5)  
**Status:** 🐛 Bug in ALL view [Issue #__]

---

### Story 4.3: Filter by Limit Type
**As a** boundary-conscious user  
**I want** to see all my hard limits in one place  
**So that** I can review and communicate my boundaries

**Acceptance Criteria:**
- Click limit type in legend to filter
- Shows only items with that limit
- Works in category and ALL views
- Helps me see all boundaries together

**Priority:** ✅ IMPLEMENTED (V5)

---

### Story 4.4: Filter by Fetish
**As a** user with specific interests  
**I want** to quickly see all my fetishes  
**So that** I can focus on my core kinks

**Acceptance Criteria:**
- ✦ Fetish button in legend
- One-click to see all fetish items
- Works in category and ALL views
- Combines with other filters

**Priority:** ✅ IMPLEMENTED (V6)

---

### Story 4.5: Combine Filters
**As a** specific user  
**I want** to combine filters (e.g., Hard Limit + Fetish)  
**So that** I can find very specific subsets

**Acceptance Criteria:**
- Multiple filters active simultaneously
- Results match ALL active filters
- Clear indication of active filters
- Easy to clear individual filters

**Priority:** ✅ IMPLEMENTED (V6)

---

## 📊 Epic 5: Comprehensive Views

### Story 5.1: See Everything at Once
**As an** overview-oriented user  
**I want** to see ALL items across ALL categories  
**So that** I can get a bird's eye view

**Acceptance Criteria:**
- "ALL" category button (first position)
- Shows all 1000+ items
- Can sort by: A-Z, Category, Rated First
- All filters work in ALL view

**Priority:** ✅ IMPLEMENTED (V6)

---

### Story 5.2: Jump Between Categories
**As a** user browsing ALL view  
**I want** to click on category badges  
**So that** I can quickly jump to that specific category

**Acceptance Criteria:**
- Category badges on each item in ALL view
- Clicking badge switches to that category
- Smooth transition
- Maintains context

**Priority:** ✅ IMPLEMENTED (V6)

---

### Story 5.3: Sort Intelligently
**As a** user in ALL view  
**I want** multiple sort options  
**So that** I can organize items the way I think

**Acceptance Criteria:**
- Sort by A-Z (alphabetical)
- Sort by Category (grouped)
- Sort by Rated First (prioritize rated)
- Default is "by category"

**Priority:** ✅ IMPLEMENTED (V6)

---

## 🖨️ Epic 6: Sharing & Communication

### Story 6.1: Print for Partner
**As a** partnered user  
**I want** to print my completed checklist  
**So that** I can share with my partner offline

**Acceptance Criteria:**
- Print view includes all categories
- Formatted as readable table
- Shows all selections
- Includes legend

**Priority:** ✅ IMPLEMENTED (V1)

---

### Story 6.2: Export My Data
**As a** privacy-conscious user  
**I want** to export my data as JSON  
**So that** I can back it up or move to another device

**Acceptance Criteria:**
- Export button downloads JSON file
- File includes all selections
- Filename includes date
- Valid JSON format

**Priority:** ✅ IMPLEMENTED (V1)

---

### Story 6.3: Import Previous Data
**As a** returning user  
**I want** to import my backed-up data  
**So that** I can restore my progress

**Acceptance Criteria:**
- Import button accepts JSON files
- Valid data imports successfully
- Invalid data shows helpful error
- Handles version differences gracefully

**Priority:** ✅ IMPLEMENTED (V1)

---

## 💡 Epic 7: Future Enhancements

### Story 7.1: Print with Filters
**As a** specific user  
**I want** to print only certain items (e.g., only Hard Limits)  
**So that** I can share targeted information with partners

**Acceptance Criteria:**
- Print modal with filter options
- Can include/exclude blanks
- Can filter by rating, limit, fetish
- Can add notes or not

**Priority:** 📋 PLANNED (V7)

---

### Story 7.2: Compare with Partner
**As a** partnered user  
**I want** to compare my checklist with my partner's  
**So that** we can find overlaps and differences

**Acceptance Criteria:**
- Import two JSON files
- Visual comparison view
- Highlights matches and mismatches
- Identifies compatible activities

**Priority:** 💭 CONSIDERING (Future)

---

### Story 7.3: Community Insights
**As a** curious user  
**I want** to see anonymous aggregated data  
**So that** I can understand what's common/rare

**Acceptance Criteria:**
- Privacy-preserving aggregation
- Shows popularity of activities
- Opt-in only
- No individual data exposed

**Priority:** 💭 CONSIDERING (Future)

---

### Story 7.4: Mobile App
**As a** mobile-first user  
**I want** a native mobile app  
**So that** I can use this on my phone easily

**Acceptance Criteria:**
- Native iOS/Android app
- Offline functionality
- Sync across devices
- Push notifications (optional)

**Priority:** 💭 CONSIDERING (Future)

---

## 📊 Story Status Summary

### By Status
- ✅ **Implemented:** 20 stories
- 🐛 **Implemented with bugs:** 1 story
- 📋 **Planned (V7):** 1 story
- 💭 **Considering (Future):** 3 stories

### By Priority
- **Critical (Must Have):** All V1-V6 stories
- **High (Should Have):** Print filters
- **Medium (Nice to Have):** Partner comparison
- **Low (Future):** Community insights, mobile app

---

## 🔗 Creating GitHub Issues from Stories

When you want to work on a user story:

1. **Copy the story** from this document
2. **Create new issue** using "User Story" template
3. **Fill in** the user story, acceptance criteria
4. **Add** technical details and tasks
5. **Link** to this document in "Related" section
6. **Label** appropriately (enhancement, user-story)
7. **Assign** priority

**Example Issue Title:**
`[STORY] Filter by rating in ALL view`

---

## 📝 Notes

- User stories are **living documents** - update as needs evolve
- Each story should be **independently valuable**
- Stories should be **testable** (clear acceptance criteria)
- Stories should be **small enough** to complete in one version
- **Epics** group related stories

---

**Need to add a story?** Follow this format:

```markdown
### Story X.X: [Title]
**As a** [user type]  
**I want** [goal]  
**So that** [benefit]

**Acceptance Criteria:**
- Criterion 1
- Criterion 2

**Priority:** [Status]
```
