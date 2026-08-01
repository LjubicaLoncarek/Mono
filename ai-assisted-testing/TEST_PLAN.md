# TEST_PLAN.md

# Photo Gallery Starter Kit - Test Plan

> **AI-assisted:** Yes (ChatGPT)
>
> Version: 1.0
>
> Tester: <Your Name>
>
> Test Type: Functional, UI, Usability, Compatibility, Accessibility, Performance and Security Testing

---

# 1. Scope

This test plan covers the major functionality of the Photo Gallery Starter Kit application.

Objectives:

- Verify all major user workflows
- Verify UI behaves correctly
- Identify functional defects
- Verify validation and error handling
- Test application under normal and edge-case scenarios
- Identify regression risks
- Evaluate usability and accessibility

---

# 2. Features Covered

- Home Page
- User Authentication
- Password Recovery
- User Registration (if available)
- Gallery
- Album Management
- Photo Upload
- Photo Details
- Search
- User Profile
- Navigation
- Error Handling
- Responsive Design
- Browser Compatibility
- Accessibility
- Performance
- Security

---

# 3. Test Environment

Operating Systems

- Windows 11
- Android 16

Browsers

- Google Chrome
- Microsoft Edge (recommended)
- Mozilla Firefox (optional)

Network

- Stable internet connection

---

# 4. Test Scenarios

---

# 4.1 Home Page

Priority: High

### HP-001 Verify home page loads successfully

Expected

- Page loads without errors
- Images displayed
- No broken layout

---

### HP-002 Verify navigation menu

Expected

Every navigation item opens the correct page.

---

### HP-003 Verify hero section

Expected

- Main banner visible
- Images displayed correctly
- CTA buttons functional

---

### HP-004 Verify footer

Expected

- Links function correctly
- Copyright displayed correctly

---

### HP-005 Verify browser refresh

Expected

Page reloads without losing content.

---

### HP-006 Verify browser Back/Forward buttons

Expected

Navigation history behaves correctly.

---

# 4.2 Login

Priority: High

### LG-001 Valid login

Expected

User successfully logs in.

---

### LG-002 Invalid password

Expected

Appropriate error message displayed.

---

### LG-003 Invalid username

Expected

Login rejected.

---

### LG-004 Empty username

Expected

Validation message displayed.

---

### LG-005 Empty password

Expected

Validation message displayed.

---

### LG-006 Both fields empty

Expected

Validation prevents login.

---

### LG-007 SQL Injection attempt

Input

```
' OR 1=1 --
```

Expected

Input rejected.

---

### LG-008 XSS attempt

```
<script>alert(1)</script>
```

Expected

Input sanitized.

---

### LG-009 Logout

Expected

Session terminated.

---

### LG-010 Access protected pages after logout

Expected

Redirect to Login page.

---

# 4.3 Password Recovery

Priority: High

### PW-001 Existing email

Expected

Recovery email sent.

---

### PW-002 Invalid email

Expected

Error message.

---

### PW-003 Empty email

Expected

Validation.

---

### PW-004 Password reset link

Expected

Password reset page opens.

---

### PW-005 Expired link

Expected

Appropriate error displayed.

---

# 4.4 Gallery

Priority: High

### GL-001 Gallery loads

Expected

Images displayed.

---

### GL-002 Broken images

Expected

No broken thumbnails.

---

### GL-003 Open photo

Expected

Correct photo details shown.

---

### GL-004 Large gallery scrolling

Expected

Smooth scrolling.

---

### GL-005 Empty gallery

Expected

Proper empty-state message.

---

# 4.5 Search

Priority: High

### SR-001 Existing keyword

Expected

Matching images returned.

---

### SR-002 Partial keyword

Expected

Relevant matches.

---

### SR-003 Case insensitive search

Example

```
cat
CAT
Cat
```

Expected

Same results.

---

### SR-004 Empty search

Expected

Default gallery restored.

---

### SR-005 Search with spaces

Expected

Handled correctly.

---

### SR-006 Very long input

Expected

Application remains stable.

---

### SR-007 Special characters

Expected

No crash.

---

### SR-008 Search with no matches

Expected

"No results found."

---

# 4.6 Album Management

Priority: High

### AL-001 Create album

Expected

Album created.

---

### AL-002 Duplicate album

Expected

Validation displayed.

---

### AL-003 Empty album name

Expected

Validation.

---

### AL-004 Maximum album name

Expected

Validation or successful save.

---

### AL-005 Special characters

Expected

Handled correctly.

---

### AL-006 Unicode characters

Example

```
čćžšđ 😀
```

Expected

Saved correctly.

---

### AL-007 Album cover upload

Expected

Upload successful.

---

### AL-008 Replace album cover

Expected

New image replaces previous one.

---

### AL-009 Delete album

Expected

Album removed.

---

# 4.7 Photo Upload

Priority: High

### PH-001 Upload JPG

Expected

Success.

---

### PH-002 Upload PNG

Expected

Success.

---

### PH-003 Upload GIF

Expected

Success.

---

### PH-004 Invalid file type

Example

PDF

Expected

Validation message.

---

### PH-005 Very large image

Expected

Handled gracefully.

---

### PH-006 Duplicate upload

Expected

Application behaves correctly.

---

### PH-007 Upload without title

Expected

Validation.

---

### PH-008 Cancel upload

Expected

Upload aborted.

---

# 4.8 Photo Details

Priority: Medium

### PD-001 Title displayed

### PD-002 Description displayed

### PD-003 Metadata correct

### PD-004 Tags displayed

### PD-005 Image resolution correct

---

# 4.9 User Profile

Priority: Medium

### PR-001 View profile

### PR-002 Edit profile

### PR-003 Upload avatar

### PR-004 Invalid avatar

### PR-005 Save changes

---

# 4.10 Navigation

Priority: High

Verify

- Browser refresh
- Browser Back
- Browser Forward
- Direct URLs
- Deep links

Expected

Consistent navigation.

---

# 4.11 Validation

Priority: High

Verify

- Required fields
- Maximum length
- Minimum length
- Duplicate values
- Invalid formats
- Unicode
- Leading spaces
- Trailing spaces

---

# 4.12 Error Handling

Priority: High

Verify

- Invalid requests
- Server unavailable
- Network disconnected
- Upload interrupted

Expected

User-friendly error messages.

---

# 4.13 Responsive Design

Priority: Medium

Devices

- Desktop
- Tablet
- Mobile

Check

- Menus
- Images
- Forms
- Buttons
- Dialogs

---

# 4.14 Accessibility

Priority: Medium

Verify

- Keyboard navigation
- Tab order
- Focus indicator
- Image alt text
- Labels
- Color contrast

---

# 4.15 Browser Compatibility

Priority: Medium

Verify functionality in

- Chrome
- Edge
- Firefox

---

# 4.16 Performance

Priority: Low

Verify

- Initial page load
- Image loading
- Upload performance
- Search response time

Observe

- Console errors
- Network failures
- Large requests

---

# 4.17 Security

Priority: High

Verify

- SQL Injection

```
' OR 1=1 --
```

- XSS

```
<script>alert(1)</script>
```

- Unauthorized URL access

```
/profile

/album/create

/upload
```

- Session handling

- Logout invalidates session

---

# 5. Regression Test Suite

Execute after any major fix:

- Login
- Logout
- Password Recovery
- Search
- Gallery
- Upload
- Album Creation
- Album Deletion
- Profile Update
- Navigation
- Responsive Layout

---

# 6. Test Priorities

## High

- Login
- Password Recovery
- Gallery
- Search
- Album Creation
- Upload
- Navigation
- Validation
- Security

## Medium

- User Profile
- Responsive Design
- Accessibility
- Browser Compatibility

## Low

- Performance
- Visual consistency
- Animations
