# 📝 Example GitHub Issues

These are examples of well-written issues you can create. Copy these formats for your own issues.

---

## Example Bug Report

### Title: `[BUG] Rating filter not working in ALL view`

**Bug Description:**
When in the ALL category view, clicking on rating emojis in the legend bar does not filter the items to show only that rating. The filter works correctly in individual category views but fails in ALL view.

**Location:**
- [x] ALL category view
- [ ] Specific category

**Steps to Reproduce:**
1. Click on "📋 ALL" category button
2. Mark some items with different ratings (3-star, 4-star, 5-star)
3. Click on a rating emoji in the legend bar (e.g., ⭐ 3)
4. Observe that items are not filtered

**Expected Behavior:**
Only items with the selected rating (3-star) should be displayed.

**Actual Behavior:**
All items remain visible, filter does not apply.

**Environment:**
- [x] Chrome
- [ ] Firefox
- [ ] Safari
- [x] Desktop

**Version:** V6.0

**Severity:**
- [ ] Critical
- [x] High - Major feature doesn't work
- [ ] Medium
- [ ] Low

**Possible Solution:**
The `renderAllItems()` function likely doesn't check the `ratingFilter` state variable. Need to add rating filter logic similar to how limit and fetish filters work.

---

## Example Feature Request

### Title: `[FEATURE] Print modal with filter options`

**Feature Description:**
Add a modal dialog when clicking print that allows users to customize what appears in the print view.

**Problem This Solves:**
Currently, print view shows ALL items including blank/unselected ones. Users may want to print only:
- Items they've selected/rated
- Only their hard limits (for partner communication)
- Only fetish items
- Items with notes

**User Story:**
**As a** user preparing to share my checklist  
**I want** to filter what gets printed  
**So that** I only share relevant information with my partner

**Proposed Solution:**
1. Clicking "Print" opens a modal overlay
2. Modal shows checkboxes:
   - [ ] Include blank items (default: checked)
   - [ ] Only items with notes
   - [ ] Only fetish items
   - [ ] Only items with ratings
   - [ ] Filter by limit type: [dropdown]
3. "Preview & Print" button opens print view with filters applied
4. "Cancel" closes modal

**UI/UX Considerations:**
- Modal appears centered over current view
- Clear title: "Print Options"
- Checkbox styling matches app theme
- Mobile-friendly touch targets

**Technical Considerations:**
- [x] Needs UI changes
- [x] Affects existing features (print view)
- [ ] Requires new data structure

**Priority:**
- [x] Should Have - Important but not blocking
- [ ] Must Have
- [ ] Nice to Have

**Acceptance Criteria:**
- [ ] Print button opens modal instead of going directly to print
- [ ] All filter options functional
- [ ] Preview button applies filters correctly
- [ ] Cancel button works
- [ ] Modal is responsive on mobile

---

## Example User Story

### Title: `[STORY] Filter by hard limit across all categories`

**User Story:**

**As a** boundary-conscious user  
**I want** to see all my hard limits in one place across all categories  
**So that** I can review my boundaries and share them with partners

---

**Acceptance Criteria:**

- [ ] **Given** I'm in the ALL category view  
      **When** I click "Hard Limit" in the legend  
      **Then** Only items marked as Hard Limit are displayed

- [ ] **Given** I have hard limits in multiple categories  
      **When** I apply the hard limit filter in ALL view  
      **Then** All my hard limits from all categories appear together

- [ ] **Given** The hard limit filter is active  
      **When** I look at the filtered items  
      **Then** Each item shows its category badge so I know where it's from

---

**Business Value:**
Users need to be able to review all their boundaries at once, especially when communicating with new partners. This is a critical safety and communication feature.

**Priority:** High - Critical user need

**User Impact:** All users

---

**Technical Notes:**

**Depends On:**
- Limit filter functionality (implemented V5)
- ALL category view (implemented V6)

**Affects:**
- UI components (legend filter)
- ALL view rendering

---

**Tasks:**
- [x] Implement limit filter in legend
- [x] Apply limit filter in ALL view
- [x] Test with multiple categories
- [ ] Ensure works with other filters
- [ ] Mobile testing

---

**Testing Scenarios:**
1. User has hard limits in 5 different categories → Should see all 5 in filtered ALL view
2. User combines hard limit + fetish filters → Should see only hard limits that are also fetishes
3. User clicks hard limit filter twice → Should toggle on/off correctly

---

**Responsive Design:**
- [x] Desktop (>1024px)
- [x] Tablet (768px-1024px)
- [x] Mobile (<768px)

---

**Definition of Done:**
- [x] Feature works as described
- [x] All acceptance criteria met
- [x] Tested on Chrome, Firefox, Safari
- [x] Tested on mobile
- [x] No console errors
- [x] Code committed
- [ ] Documentation updated

---

## How to Use These Examples

1. **For Bugs:**
   - Copy the Bug Report template
   - Fill in your specific details
   - Add screenshots if helpful
   - Set severity appropriately

2. **For Features:**
   - Copy the Feature Request template
   - Describe the problem it solves
   - Include user story format
   - Add mockups if you have them

3. **For User Stories:**
   - Copy the User Story template
   - Write as: "As [user], I want [goal], so that [benefit]"
   - Add specific acceptance criteria
   - Break down into tasks

---

## Labels to Use

Suggested labels for your issues:
- `bug` - Something isn't working
- `enhancement` - New feature or request
- `user-story` - User story for development
- `high-priority` - Needs attention soon
- `low-priority` - Nice to have
- `v7` - Planned for version 7
- `testing-needed` - Needs QA
- `documentation` - Docs updates
- `mobile` - Mobile-specific issue
- `accessibility` - A11y improvements

---

## Issue Workflow

1. **Create issue** using appropriate template
2. **Label** the issue
3. **Assign** to project board (optional)
4. **Work on** the issue
5. **Reference** in commits: `"Fix rating filter in ALL view (fixes #1)"`
6. **Close** when complete
7. **Link** to release notes

---

## Quick Issue Creation Tips

- **Be specific** in titles: `[BUG] Rating filter in ALL view` not `Filter broken`
- **Include steps** to reproduce bugs
- **Add context** for features (why it matters)
- **Link related issues** using `#issue_number`
- **Update issues** as you learn more
- **Close with commits** using `fixes #X` or `closes #X` in commit message
