# Gift List View Test Cases

## [D4B-3009] Navigate to Gift List
---
```yaml
id: D4B-3009
title: Verify user will redirect to Gift list when click on Promotion/Gift
component: Gift Management
priority: High
status: Active
tags: [gift, navigation, smoke-test]
```

### Test Objective
Verify that users can successfully navigate to the Gift list page from Promotion/Gift link

### Prerequisites
- User is logged in
- User has permission to view gifts

### Test Steps
{{ ../shared-steps/navigation.md }}

### Expected Results
- Gift list page is displayed
- URL changes to /gifts
- Gift list title is visible

---

## [D4B-3010] Gift List Fields
---
```yaml
id: D4B-3010
title: Verify Gift list has 6 fields
component: Gift Management
priority: High
status: Active
tags: [gift, ui, regression]
```

### Test Objective
Verify that Gift list displays all required fields correctly

### Test Steps
| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Gift list | Gift list page is displayed |
| 2 | Verify table headers | Following columns are present: |
|   |                      | - Gift ID |
|   |                      | - Name |
|   |                      | - Value |
|   |                      | - Quantity |
|   |                      | - Status |
|   |                      | - Actions |

### Notes
- All columns should be sortable
- Actions column should contain Edit and Delete buttons
- Status should show active/inactive indicator

---

## [D4B-3013] Gift Search
---
```yaml
id: D4B-3013
title: Verify system will show valid data if user input giftId in search box
component: Gift Management
priority: Medium
status: Active
tags: [gift, search, regression]
```

### Test Objective
Verify that the search functionality correctly filters gifts by ID

### Test Data
```json
{
  "validGiftId": "GIFT-001",
  "invalidGiftId": "INVALID-001"
}
```

### Test Steps
| Step | Action | Expected Result | Test Data |
|------|--------|----------------|------------|
| 1 | Navigate to Gift list | Gift list page is displayed | |
| 2 | Enter valid gift ID in search box | Search box accepts input | validGiftId |
| 3 | Press Enter or click Search | Results are filtered | |
| 4 | Verify search results | Only matching gift is displayed | |
| 5 | Clear search box | | |
| 6 | Enter invalid gift ID | Search box accepts input | invalidGiftId |
| 7 | Press Enter or click Search | "No results found" message is displayed | |

### Notes
- Search should be case-insensitive
- Partial gift ID matches should be supported
- Search should execute after 500ms of user stopping typing

---

## [GIFT-LIST-FUN-001] View Gift List
---
```yaml
title: View Gift List
id: GIFT-LIST-FUN-001
component: Gift Management
priority: High
status: Active
tags:
  - gift
  - navigation
last_updated: 2024-12-24
```

### Test Objective
Verify that users can successfully navigate to the Gift list page from Promotion/Gift link

### Prerequisites
- User is logged in
- User has permission to view gifts

### Test Steps

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Click on Promotion/Gift link in the navigation menu | System redirects to Gift list page |
| 2 | Wait for page load | Gift list page is displayed |

### Expected Results
- Gift list page is displayed
- URL changes to /gifts
- Gift list title is visible

### Notes
- This test case is part of the basic navigation test suite
- Should be included in smoke tests
