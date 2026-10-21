# Website QA Report Template

A practical template for documenting website bugs, functional issues, and usability findings in a clear, developer-friendly format.

The goal of a useful QA report is not simply to say that something is broken. It should make the issue easy to reproduce, understand, prioritize, fix, and retest.

## 1. Test Environment

Record the environment in which testing was performed.

| Field | Example |
|---|---|
| Website / Build | Staging environment |
| Device | Desktop / Mobile |
| Operating System | Windows 11 / iOS |
| Browser | Chrome / Safari / Firefox / Edge |
| Browser Version | Current version |
| Screen Size | 1920×1080 |
| Test Date | YYYY-MM-DD |

## 2. Bug Report Format

Each issue should include enough information for another person to reproduce it.

| Field | Description |
|---|---|
| Bug ID | Unique issue identifier |
| Title | Short description of the problem |
| Area | Page, feature, or workflow affected |
| Severity | Critical / High / Medium / Low |
| Environment | Browser, device, OS |
| Preconditions | Required state before reproducing |
| Steps to Reproduce | Exact sequence that triggers the issue |
| Expected Result | What should happen |
| Actual Result | What actually happens |
| Evidence | Screenshot or screen recording |
| Status | Open / Fixed / Retest / Closed |

## 3. Example Bug

**Bug ID:** QA-001  
**Title:** Contact form does not submit after required fields are completed  
**Area:** Contact Form  
**Severity:** High  
**Environment:** Chrome / Windows 11

### Preconditions

User is on the Contact page.

### Steps to Reproduce

1. Open the Contact page
2. Enter valid information in all required fields
3. Click **Submit**

### Expected Result

The form should submit successfully and display a confirmation message.

### Actual Result

The Submit button responds, but the form is not submitted and no confirmation message appears.

### Evidence

Attach a screenshot or screen recording showing the completed form and resulting behavior.

## 4. Severity Guide

### Critical

A core workflow is completely unavailable or the issue causes serious data, security, or business impact.

Examples:

- Website unavailable
- Checkout completely blocked
- Authentication failure affecting all users
- Data loss or corruption

### High

An important feature or user workflow does not work correctly and there is no reasonable workaround.

Examples:

- Contact or inquiry form cannot be submitted
- User cannot complete registration
- Important navigation path is broken

### Medium

Functionality is affected, but the user can still complete the task through another path or workaround.

Examples:

- Incorrect validation message
- Layout issue affecting usability
- A secondary feature does not behave as expected

### Low

Minor visual, content, or usability issue with limited functional impact.

Examples:

- Alignment inconsistency
- Minor spacing issue
- Typographical error

## 5. Website QA Checklist

### Navigation & Links

- Main navigation works correctly
- Internal links open the correct destination
- External links work
- Logo links to the expected page
- No obvious broken links
- Back and forward navigation behaves normally

### Forms

- Required fields are enforced
- Validation messages are clear
- Valid submissions succeed
- Invalid submissions are handled correctly
- Confirmation messages appear
- Emails or notifications are triggered when applicable
- Forms work on mobile devices

### Responsive Behavior

- Pages display correctly on desktop
- Pages display correctly on tablet
- Pages display correctly on mobile
- Navigation remains usable
- Text does not overflow
- Buttons remain accessible
- Images scale appropriately
- Forms remain usable

### Functional Workflows

- Registration and login work when applicable
- Search works
- Filters and sorting work
- User profile workflows work
- Contact or inquiry workflows work
- Checkout or payment workflows work in the appropriate test environment
- Important integrations behave as expected

### Content & UI

- Headings and text display correctly
- Images load
- Buttons and controls are clearly visible
- Error messages are understandable
- Important content is not clipped or hidden
- Page layout is consistent

### Browser Testing

When required, verify important workflows in:

- Chrome
- Safari
- Firefox
- Edge

## 6. Usability Findings

Not every problem is a functional bug.

Usability findings can be documented separately:

| Priority | Page / Workflow | Observation | User Impact | Recommendation |
|---|---|---|---|---|
| High | Registration | Next step is unclear | Users may abandon registration | Make the primary action more prominent |
| Medium | Navigation | Menu label is ambiguous | Users may have difficulty finding content | Use a clearer label |

## 7. Retesting

After a reported issue is fixed:

1. Repeat the original reproduction steps
2. Confirm the expected behavior
3. Test closely related workflows
4. Check for obvious regressions
5. Update the issue status
6. Record any remaining problems

---

## QA Principle

**Reproduce → Document → Prioritize → Fix → Retest → Verify**

A useful QA report should allow a developer to understand and reproduce an issue without having to ask what “it doesn't work” means.
