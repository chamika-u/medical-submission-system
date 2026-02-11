# Medical Submission System - UI Wireframes

## Design System Overview

### Color Palette
- **Primary Gradient**: `linear-gradient(135deg, #667eea 0%, #764ba2 100%)`
- **Background**: `#f5f5f5`
- **Card Background**: `#ffffff`
- **Text Colors**:
  - Primary: `#333333`
  - Secondary: `#666666`
  - Tertiary: `#999999`
- **Status Colors**:
  - Pending: `#ffc107` (background: `#fff3cd`)
  - Approved: `#28a745` (background: `#d4edda`)
  - Rejected: `#dc3545` (background: `#f8d7da`)
  - On Hold: `#17a2b8` (background: `#d1ecf1`)

### Typography
- **Font Family**: 'Arimo', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif
- **Font Sizes**:
  - H1: 16px (24px line-height)
  - H2: 20px (30px line-height) - Navbar brand
  - H3: 14px (21px line-height) - Stat cards
  - Body: 16px (24px line-height)
  - Small: 13px (19.5px line-height)
  - Tiny: 12px (18px line-height)

### Layout
- **Max Container Width**: 1200px
- **Border Radius**: 
  - Cards: 10px (large), 8px (medium)
  - Inputs/Buttons: 5px
  - Badges: 20px (pill shape)
- **Shadows**:
  - Cards: `0 2px 4px rgba(0, 0, 0, 0.1)`
  - Login Box: `0 10px 25px rgba(0, 0, 0, 0.2)`
  - Navbar: `0 2px 4px rgba(0, 0, 0, 0.1)`
- **Spacing**:
  - Container padding: 30px vertical, 20px horizontal
  - Section gaps: 20px - 30px
  - Form field gaps: 8px - 20px

---

## Wireframe 1: Login Page

### Layout Structure
```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│                    FULL VIEWPORT HEIGHT                     │
│              Background: Purple Gradient                    │
│                                                             │
│           ┌───────────────────────────────┐                 │
│           │                               │                 │
│           │        LOGIN CONTAINER        │                 │
│           │      (Centered, White)        │                 │
│           │                               │                 │
│           │         🏥 [Icon] (48px)     │                 │
│           │                               │                 │
│           │  Medical Submission System    │                 │
│           │  Sabaragamuwa University      │                 │
│           │      of Sri Lanka             │                 │
│           │                               │                 │
│           │  ┌─────────────────────────┐  │                 │
│           │  │ Username                │  │                 │
│           │  │ [Text Input Field]      │  │                 │
│           │  └─────────────────────────┘  │                 │
│           │                               │                 │
│           │  ┌─────────────────────────┐  │                 │
│           │  │ Password                │  │                 │
│           │  │ [Password Input Field]  │  │                 │
│           │  └─────────────────────────┘  │                 │
│           │                               │                 │
│           │  ┌─────────────────────────┐  │                 │
│           │  │       [Login]           │  │                 │
│           │  └─────────────────────────┘  │                 │
│           │                               │                 │
│           │  ┌─────────────────────────┐  │                 │
│           │  │  Demo Credentials:      │  │                 │
│           │  │  Medical Officer:       │  │                 │
│           │  │  medical_officer /      │  │                 │
│           │  │  medical123             │  │                 │
│           │  │  Student: student1 /    │  │                 │
│           │  │  student123             │  │                 │
│           │  └─────────────────────────┘  │                 │
│           │                               │                 │
│           └───────────────────────────────┘                 │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Component Specifications

#### 1.1 Login Container
- **Dimensions**: 450px width, auto height
- **Background**: White (`#ffffff`)
- **Padding**: 40px all sides
- **Border Radius**: 10px
- **Shadow**: `0 10px 25px rgba(0, 0, 0, 0.2)`
- **Position**: Centered (flexbox)

#### 1.2 Logo Section
- **Icon**: 🏥 (48px size)
- **Heading**: "Medical Submission System"
  - Color: `#667eea`
  - Font size: 16px
  - Line height: 24px
  - Margin bottom: 10px
- **Subheading**: "Sabaragamuwa University of Sri Lanka"
  - Color: `#666666`
  - Font size: 14px
  - Line height: 21px
- **Section margin bottom**: 30px

#### 1.3 Form Fields

**Username Field:**
- Label:
  - Text: "Username"
  - Font weight: 500
  - Color: `#333333`
  - Font size: 16px
  - Margin bottom: 8px
- Input:
  - Type: text
  - Width: 100%
  - Padding: 10px
  - Border: 1px solid `#ddd`
  - Border radius: 5px
  - Font size: 14px
  - Required: true
- Field margin bottom: 20px

**Password Field:**
- Label:
  - Text: "Password"
  - Font weight: 500
  - Color: `#333333`
  - Font size: 16px
  - Margin bottom: 8px
- Input:
  - Type: password
  - Width: 100%
  - Padding: 10px
  - Border: 1px solid `#ddd`
  - Border radius: 5px
  - Font size: 14px
  - Required: true
- Field margin bottom: 20px

#### 1.4 Login Button
- **Text**: "Login"
- **Background**: `#667eea`
- **Color**: White
- **Padding**: 10px 20px
- **Border radius**: 5px
- **Width**: 100%
- **Font size**: 14px
- **Font weight**: 500
- **Hover state**: Background `#5568d3`
- **Cursor**: pointer

#### 1.5 Demo Credentials Box
- **Margin top**: 20px
- **Padding**: 15px all sides
- **Background**: `#f8f9fa`
- **Border radius**: 5px
- **Font size**: 13px

**Content Structure:**
- Heading:
  - Text: "Demo Credentials:"
  - Margin bottom: 10px
  - Color: `#333333`
  - Font weight: 500
- Credential Lines:
  - Line 1: "Medical Officer: medical_officer / medical123"
  - Line 2: "Student: student1 / student123"
  - Color: `#666666`
  - Line height: 20.8px

#### 1.6 Error Message (Hidden by default)
- **Display**: none (shown on error)
- **Margin top**: 15px
- **Text align**: center
- **Color**: `#dc3545`

---

## Wireframe 2: Student Dashboard
### Layout Structure

```
┌────────────────────────────────────────────────────────────────────┐
│  🏥 Medical Submission System              Kasun Silva  [Logout]   │ ← Navbar
├────────────────────────────────────────────────────────────────────┤
│                                                                    │
│  Student Dashboard                [+ Submit Medical Certificate]   │
│                                                                    │
│  My Medical Submissions                                            │
│                                                                    │
│  ┌──────────────────────────────────────────────────────────────┐  │
│  │ Date of Absence: Feb 5, 2026                     [Pending]   │  │
│  │ Type: Examination                                            │  │
│  │ Reason: Severe Fever                                         │  │
│  │ Additional Details: Had high fever of 102°F, unable to       │  │
│  │ attend the mid-term examination.                             │  │
│  │ Submitted: Feb 6, 2026, 10:30 AM                             │  │
│  └──────────────────────────────────────────────────────────────┘  │
│                                                                    │
│  ┌──────────────────────────────────────────────────────────────┐  │
│  │ Date of Absence: Jan 28, 2026                    [Approved]  │  │
│  │ Type: Assessment                                             │  │
│  │ Reason: Migraine                                             │  │
│  │ Submitted: Jan 29, 2026, 02:20 PM                            │  │
│  │ ┌────────────────────────────────────────────────────────┐   │  │
│  │ │ Review Notes:                                          │   │  │
│  │ │ Medical certificate verified. Approved for             │   │  │
│  │ │ re-assessment.                                         │   │  │
│  │ │ Reviewed: Jan 30, 2026, 09:15 AM                       │   │  │
│  │ └────────────────────────────────────────────────────────┘   │  │
│  └──────────────────────────────────────────────────────────────┘  │
│                                                                    │
└────────────────────────────────────────────────────────────────────┘
```

### Component Specifications

#### 2.1 Navbar
- **Background**: White (`#ffffff`)
- **Padding**: 15px 30px
- **Height**: 71px
- **Display**: flex (space-between, center aligned)
- **Shadow**: `0 2px 4px rgba(0, 0, 0, 0.1)`
- **Position**: Sticky top

**Left Section (Brand):**
- Icon: 🏥 (24px)
- Text: "Medical Submission System"
  - Color: `#667eea`
  - Font size: 20px
  - Line height: 30px
- Gap between icon and text: 10px

**Right Section (User):**
- User name: "Kasun Silva"
  - Font weight: 500
  - Color: `#333333`
  - Font size: 16px
- Logout Button:
  - Text: "Logout"
  - Background: `#6c757d`
  - Color: White
  - Padding: 10px 20px
  - Border radius: 5px
  - Font size: 14px
  - Hover: Background `#5a6268`
- Gap: 15px

#### 2.2 Main Container
- **Background**: `#f5f5f5`
- **Min height**: 100vh
- **Max width**: 1200px
- **Margin**: 0 auto
- **Padding**: 30px 20px

#### 2.3 Page Header
- **Display**: flex (space-between, center aligned)
- **Margin bottom**: 30px
- **Flex wrap**: wrap
- **Gap**: 15px

**Left - Heading:**
- Text: "Student Dashboard"
- Color: `#333333`
- Font size: 16px
- Line height: 24px

**Right - Submit Button:**
- Text: "+ Submit Medical Certificate"
- Background: `#667eea`
- Color: White
- Padding: 10px 20px
- Border radius: 5px
- Font size: 14px
- Font weight: 500
- Hover: Background `#5568d3`

#### 2.4 Submissions Section

**Section Heading:**
- Text: "My Medical Submissions"
- Color: `#333333`
- Font size: 16px
- Line height: 24px
- Margin bottom: 20px

**Submission Cards Container:**
- Display: flex column
- Gap: 15px

#### 2.5 Submission Card (Student View)
- **Background**: White
- **Padding**: 20px all sides
- **Border radius**: 8px
- **Shadow**: `0 2px 4px rgba(0, 0, 0, 0.1)`
- **Width**: 100% (max 1160px)

**Card Layout:**
- Display: flex (space-between, start aligned)
- Gap: 20px
- Flex wrap: wrap

**Left Section - Details:**
- **Date of Absence:**
  - Label: Bold, `#333333`
  - Value: Regular, `#666666`
  - Font size: 16px
  - Line height: 24px
  - Margin bottom: 8px

- **Type:**
  - Label: Bold, `#333333`
  - Value: Regular, `#666666`
  - Format: "Examination" | "Assessment" | "Other"
  - Margin bottom: 8px

- **Reason:**
  - Label: Bold, `#333333`
  - Value: Regular, `#666666`
  - Margin bottom: 8px

- **Additional Details (optional):**
  - Label: Bold, `#333333`
  - Value: Regular, `#666666`
  - Margin bottom: 8px

- **Submission Timestamp:**
  - Format: "Submitted: MMM D, YYYY, HH:MM AM/PM"
  - Font size: 13px
  - Color: `#999999`
  - Margin top: 10px

**Right Section - Status:**
- Alignment: flex-end
- Gap: 10px

**Review Notes Section (if reviewed):**
- **Margin top**: 15px
- **Padding**: 10px
- **Background**: `#f8f9fa`
- **Border radius**: 5px
- **Border left**: 3px solid `#667eea`

Content:
- Heading: "Review Notes:"
  - Font weight: Bold
  - Color: `#333333`
  - Font size: 13px
- Notes text:
  - Color: `#666666`
  - Font size: 13px
  - Margin top: 5px
- Reviewed timestamp:
  - Format: "Reviewed: MMM D, YYYY, HH:MM AM/PM"
  - Font size: 12px
  - Color: `#999999`
  - Margin top: 5px

#### 2.6 Status Badge
- **Padding**: 5px 12px
- **Border radius**: 20px (pill)
- **Font size**: 12px
- **Font weight**: 500
- **Text transform**: capitalize

**Status Variants:**
- Pending:
  - Background: `#fff3cd`
  - Color: `#ffc107`
  - Text: "Pending"
  
- Approved:
  - Background: `#d4edda`
  - Color: `#28a745`
  - Text: "Approved"
  
- Rejected:
  - Background: `#f8d7da`
  - Color: `#dc3545`
  - Text: "Rejected"
  
- On Hold:
  - Background: `#d1ecf1`
  - Color: `#17a2b8`
  - Text: "On Hold"

#### 2.7 Empty State
- **Display**: When no submissions
- **Text align**: center
- **Padding**: 40px
- **Color**: `#999999`
- **Background**: White
- **Border radius**: 8px
- **Text**: "No submissions yet"

---

## Wireframe 3: Submit Medical Certificate Modal

### Layout Structure
```
┌─────────────────────────────────────────────────────────┐
│                    MODAL OVERLAY                        │
│              (Semi-transparent dark)                    │
│                                                         │
│     ┌───────────────────────────────────────────┐       │
│     │                                      [×]  │       │
│     │  Submit Medical Certificate               │       │
│     │                                           │       │
│     │  Date of Medical Absence *                │       │
│     │  [Date Input Field]                       │       │
│     │                                           │       │
│     │  Type *                                   │       │
│     │  [Dropdown: Select type ▼]                │       │
│     │                                           │       │
│     │  Reason *                                 │       │
│     │  [Text Input: e.g., Fever, Headache]      │       │
│     │                                           │       │
│     │  Additional Details                       │       │
│     │  [Textarea: Provide any additional        │       │
│     │   details...]                             │       │
│     │                                           │       │
│     │  [  Submit  ]  [  Cancel  ]               │       │
│     │                                           │       │
│     └───────────────────────────────────────────┘       │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

### Component Specifications

#### 3.1 Modal Overlay
- **Position**: fixed (full viewport)
- **Background**: `rgba(0, 0, 0, 0.5)`
- **Display**: flex (center, center)
- **Z-index**: 1000
- **Padding**: 20px
- **Click behavior**: Close modal

#### 3.2 Modal Content
- **Background**: White
- **Padding**: 30px all sides
- **Border radius**: 10px
- **Max width**: 600px
- **Width**: 100%
- **Max height**: 90vh
- **Overflow**: auto
- **Position**: relative
- **Click behavior**: Stop propagation

#### 3.3 Close Button
- **Position**: absolute (top: 15px, right: 15px)
- **Text**: "×"
- **Font size**: 28px
- **Color**: `#aaa`
- **Hover**: Color `#000`
- **Background**: none
- **Border**: none
- **Cursor**: pointer
- **Line height**: 1

#### 3.4 Modal Heading
- **Text**: "Submit Medical Certificate"
- **Margin**: 0 0 20px 0
- **Color**: `#333333`
- **Font size**: 16px
- **Line height**: 24px

#### 3.5 Form Fields

**Date of Medical Absence (Required):**
- Label:
  - Text: "Date of Medical Absence *"
  - Font weight: 500
  - Color: `#333333`
  - Font size: 16px
  - Margin bottom: 8px
- Input:
  - Type: date
  - Width: 100%
  - Padding: 10px
  - Border: 1px solid `#ddd`
  - Border radius: 5px
  - Font size: 14px
  - Required: true
- Margin bottom: 20px

**Type (Required):**
- Label:
  - Text: "Type *"
  - Font weight: 500
  - Color: `#333333`
  - Font size: 16px
  - Margin bottom: 8px
- Select:
  - Width: 100%
  - Padding: 10px
  - Border: 1px solid `#ddd`
  - Border radius: 5px
  - Font size: 14px
  - Background: White
  - Required: true
  - Options:
    - "Select type" (default)
    - "Examination"
    - "Assessment"
    - "Other"
- Margin bottom: 20px

**Reason (Required):**
- Label:
  - Text: "Reason *"
  - Font weight: 500
  - Color: `#333333`
  - Font size: 16px
  - Margin bottom: 8px
- Input:
  - Type: text
  - Width: 100%
  - Padding: 10px
  - Border: 1px solid `#ddd`
  - Border radius: 5px
  - Font size: 14px
  - Placeholder: "e.g., Fever, Headache"
  - Required: true
- Margin bottom: 20px

**Additional Details (Optional):**
- Label:
  - Text: "Additional Details"
  - Font weight: 500
  - Color: `#333333`
  - Font size: 16px
  - Margin bottom: 8px
- Textarea:
  - Width: 100%
  - Padding: 10px
  - Border: 1px solid `#ddd`
  - Border radius: 5px
  - Font size: 14px
  - Rows: 4
  - Placeholder: "Provide any additional details..."
  - Resize: vertical
- Margin bottom: 20px

#### 3.6 Action Buttons

**Container:**
- Display: flex
- Gap: 10px

**Submit Button:**
- Text: "Submit"
- Flex: 1
- Background: `#667eea`
- Color: White
- Padding: 10px 20px
- Border: none
- Border radius: 5px
- Font size: 14px
- Font weight: 500
- Hover: Background `#5568d3`
- Cursor: pointer

**Cancel Button:**
- Text: "Cancel"
- Flex: 1
- Background: `#6c757d`
- Color: White
- Padding: 10px 20px
- Border: none
- Border radius: 5px
- Font size: 14px
- Font weight: 500
- Hover: Background `#5a6268`
- Cursor: pointer

---

## Wireframe 4: Medical Officer Dashboard

### Layout Structure
```
┌───────────────────────────────────────────────────────────────────┐
│  🏥 Medical Submission System              Dr. Perera  [Logout]  │ ← Navbar
├───────────────────────────────────────────────────────────────────┤
│                                                                   │
│  Medical Officer Dashboard                                        │
│                                                                   │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐      │
│  │  Total  │ │Pending  │ │Approved │ │Rejected │ │ On Hold │      │
│  │Submiss. │ │    1    │ │    1    │ │    0    │ │    1    │      │
│  │    3    │ │         │ │         │ │         │ │         │      │
│  └─────────┘ └─────────┘ └─────────┘ └─────────┘ └─────────┘      │
│                                                                   │
│  [All Status ▼]  [All Types ▼]                                    │
│                                                                   │
│  Medical Submissions                                              │
│                                                                   │
│  ┌──────────────────────────────────────────────────────────────┐ │
│  │ Student: Kasun Silva (student1)                  [Pending]   │ │
│  │ Date of Absence: Feb 5, 2026                     [Review]    │ │
│  │ Type: Examination                                            │ │
│  │ Reason: Severe Fever                                         │ │
│  │ Additional Details: Had high fever of 102°F, unable to       │ │
│  │ attend the mid-term examination.                             │ │
│  │ Submitted: Feb 6, 2026, 10:30 AM                             │ │
│  └──────────────────────────────────────────────────────────────┘ │
│                                                                   │
│  ┌──────────────────────────────────────────────────────────────┐ │
│  │ Student: Kasun Silva (student1)                  [Approved]  │ │
│  │ Date of Absence: Jan 28, 2026                                │ │
│  │ Type: Assessment                                             │ │
│  │ Reason: Migraine                                             │ │
│  │ Submitted: Jan 29, 2026, 02:20 PM                            │ │
│  │ ┌────────────────────────────────────────────────────────┐   │ │
│  │ │ Review Notes:                                          │   │ │
│  │ │ Medical certificate verified. Approved for             │   │ │
│  │ │ re-assessment.                                         │   │ │
│  │ │ Reviewed: Jan 30, 2026, 09:15 AM                       │   │ │
│  │ └────────────────────────────────────────────────────────┘   │ │
│  └──────────────────────────────────────────────────────────────┘ │
│                                                                   │
│  ┌──────────────────────────────────────────────────────────────┐ │
│  │ Student: Sahan Fernando (student2)               [On Hold]   │ │
│  │ Date of Absence: Feb 3, 2026                                 │ │
│  │ Type: Other                                                  │ │
│  │ Reason: Food Poisoning                                       │ │
│  │ Additional Details: Severe stomach pain and vomiting.        │ │
│  │ Submitted: Feb 4, 2026, 08:45 AM                             │ │
│  │ ┌────────────────────────────────────────────────────────┐   │ │
│  │ │ Review Notes:                                          │   │ │
│  │ │ Awaiting additional medical documentation.             │   │ │
│  │ │ Reviewed: Feb 5, 2026, 11:30 AM                        │   │ │
│  │ └────────────────────────────────────────────────────────┘   │ │
│  └──────────────────────────────────────────────────────────────┘ │
│                                                                   │
└───────────────────────────────────────────────────────────────────┘
```

### Component Specifications

#### 4.1 Navbar
Same as Student Dashboard navbar (see 2.1) with:
- User name: "Dr. Perera"

#### 4.2 Main Container
Same as Student Dashboard (see 2.2)

#### 4.3 Page Header
- **Margin bottom**: 30px
- **Heading**: "Medical Officer Dashboard"
  - Color: `#333333`
  - Font size: 16px
  - Line height: 24px

#### 4.4 Statistics Cards Grid
- **Display**: grid
- **Grid template columns**: repeat(5, 1fr) on desktop
- **Gap**: 20px
- **Margin bottom**: 30px
- **Responsive**: Stack to 1 column on mobile

#### 4.5 Stat Card
- **Background**: White
- **Padding**: 20px
- **Border radius**: 10px
- **Shadow**: `0 2px 4px rgba(0, 0, 0, 0.1)`
- **Text align**: center
- **Border top**: 4px solid (color varies by status)

**Card Structure:**
- Heading (Label):
  - Font size: 14px
  - Line height: 21px
  - Color: `#333333`
  - Font weight: 500
  - Margin: 0 0 10px 0

- Value (Number):
  - Font size: 32px
  - Line height: 48px
  - Font weight: 600
  - Color: Matches border color

**Card Variants:**
1. Total Submissions:
   - Border top: `#667eea`
   - Value color: `#667eea`
   - Label: "Total Submissions"

2. Pending:
   - Border top: `#ffc107`
   - Value color: `#ffc107`
   - Label: "Pending"

3. Approved:
   - Border top: `#28a745`
   - Value color: `#28a745`
   - Label: "Approved"

4. Rejected:
   - Border top: `#dc3545`
   - Value color: `#dc3545`
   - Label: "Rejected"

5. On Hold:
   - Border top: `#17a2b8`
   - Value color: `#17a2b8`
   - Label: "On Hold"

#### 4.6 Filters Section
- **Display**: flex
- **Gap**: 15px
- **Margin bottom**: 20px
- **Flex wrap**: wrap

**Status Filter Dropdown:**
- Width: auto (min-content)
- Padding: 10px
- Border: 1px solid `#ddd`
- Border radius: 5px
- Font size: 14px
- Background: White
- Cursor: pointer
- Options:
  - "All Status" (default)
  - "Pending"
  - "Approved"
  - "Rejected"
  - "On Hold"

**Type Filter Dropdown:**
- Same styling as Status Filter
- Options:
  - "All Types" (default)
  - "Examination"
  - "Assessment"
  - "Other"

#### 4.7 Submissions Section

**Section Heading:**
- Text: "Medical Submissions"
- Color: `#333333`
- Font size: 16px
- Line height: 24px
- Margin bottom: 20px

**Submissions Container:**
- Display: flex column
- Gap: 15px

#### 4.8 Submission Card (Officer View)
- **Background**: White
- **Padding**: 20px all sides
- **Border radius**: 8px
- **Shadow**: `0 2px 4px rgba(0, 0, 0, 0.1)`
- **Width**: 100% (max 1160px)

**Card Layout:**
- Display: flex (space-between, start aligned)
- Gap: 20px
- Flex wrap: wrap

**Left Section - Details:**
- **Student Info:**
  - Format: "Student: [Name] ([ID])"
  - Label: Bold, `#333333`
  - Value: Regular, `#666666`
  - Font size: 16px
  - Line height: 24px
  - Margin bottom: 10px

- **Date of Absence:**
  - Label: Bold, `#333333`
  - Value: Regular, `#666666`
  - Margin bottom: 8px

- **Type:**
  - Label: Bold, `#333333`
  - Value: Regular, `#666666`
  - Margin bottom: 8px

- **Reason:**
  - Label: Bold, `#333333`
  - Value: Regular, `#666666`
  - Margin bottom: 8px

- **Additional Details (if present):**
  - Label: Bold, `#333333`
  - Value: Regular, `#666666`
  - Margin bottom: 8px

- **Submission Timestamp:**
  - Format: "Submitted: MMM D, YYYY, HH:MM AM/PM"
  - Font size: 13px
  - Color: `#999999`
  - Margin top: 10px

**Right Section - Actions:**
- Display: flex column
- Align: flex-end
- Gap: 10px

**Status Badge:**
- See section 2.6 for specifications

**Review Button (for pending submissions only):**
- Text: "Review"
- Background: `#667eea`
- Color: White
- Padding: 8px 16px
- Border radius: 5px
- Font size: 14px
- Font weight: 500
- Hover: Background `#5568d3`
- Cursor: pointer

**Review Notes Section (if reviewed):**
- Same as Student view (see 2.5)

#### 4.9 Empty State
Same as Student Dashboard (see 2.7) with:
- Text: "No submissions found"

---

## Wireframe 5: Review Medical Submission Modal

### Layout Structure
```
┌───────────────────────────────────────────────────────┐
│                    MODAL OVERLAY                      │
│              (Semi-transparent dark)                  │
│                                                       │
│     ┌───────────────────────────────────────────┐     │
│     │                                      [×]  │     │
│     │  Review Medical Submission                │     │
│     │                                           │     │
│     │  ┌────────────────────────────────────┐   │     │
│     │  │ Student: Kasun Silva (student1)    │   │     │
│     │  │ Date of Absence: Feb 5, 2026       │   │     │
│     │  │ Type: Examination                  │   │     │
│     │  │ Reason: Severe Fever               │   │     │
│     │  │ Additional Details: Had high fever │   │     │
│     │  │ of 102°F, unable to attend...      │   │     │
│     │  └────────────────────────────────────┘   │     │
│     │                                           │     │
│     │  Decision *                               │     │
│     │  [Dropdown: Select decision ▼]            │     │
│     │                                           │     │
│     │  Notes                                    │     │
│     │  [Textarea: Add review notes...]          │     │
│     │                                           │     │
│     │  [Submit Review]  [  Cancel  ]            │     │
│     │                                           │     │
│     └───────────────────────────────────────────┘     │
│                                                       │
└───────────────────────────────────────────────────────┘
```

### Component Specifications

#### 5.1 Modal Overlay & Content
Same as Submit Modal (see 3.1 and 3.2)

#### 5.2 Close Button
Same as Submit Modal (see 3.3)

#### 5.3 Modal Heading
- **Text**: "Review Medical Submission"
- **Margin**: 0 0 20px 0
- **Color**: `#333333`
- **Font size**: 16px
- **Line height**: 24px

#### 5.4 Submission Details Box
- **Background**: `#f8f9fa`
- **Padding**: 15px all sides
- **Border radius**: 5px
- **Margin bottom**: 20px

**Content Items:**
Each detail follows this format:
- Label: Bold, `#333333`, 16px
- Value: Regular, `#666666`, 16px
- Line height: 24px
- Margin bottom: 10px (except last item)

**Details Displayed:**
1. Student: "[Name] ([ID])"
2. Date of Absence: "[Date]"
3. Type: "[Examination/Assessment/Other]"
4. Reason: "[Reason text]"
5. Additional Details (if present): "[Details text]"

#### 5.5 Review Form Fields

**Decision (Required):**
- Label:
  - Text: "Decision *"
  - Font weight: 500
  - Color: `#333333`
  - Font size: 16px
  - Margin bottom: 8px
- Select:
  - Width: 100%
  - Padding: 10px
  - Border: 1px solid `#ddd`
  - Border radius: 5px
  - Font size: 14px
  - Background: White
  - Required: true
  - Options:
    - "Select decision" (default)
    - "Approve"
    - "Reject"
    - "Hold"
- Margin bottom: 20px

**Notes (Optional):**
- Label:
  - Text: "Notes"
  - Font weight: 500
  - Color: `#333333`
  - Font size: 16px
  - Margin bottom: 8px
- Textarea:
  - Width: 100%
  - Padding: 10px
  - Border: 1px solid `#ddd`
  - Border radius: 5px
  - Font size: 14px
  - Rows: 4
  - Placeholder: "Add review notes..."
  - Resize: vertical
- Margin bottom: 20px

#### 5.6 Action Buttons

**Container:**
- Display: flex
- Gap: 10px

**Submit Review Button:**
- Text: "Submit Review"
- Flex: 1
- Background: `#667eea`
- Color: White
- Padding: 10px 20px
- Border: none
- Border radius: 5px
- Font size: 14px
- Font weight: 500
- Hover: Background `#5568d3`
- Cursor: pointer

**Cancel Button:**
- Text: "Cancel"
- Flex: 1
- Background: `#6c757d`
- Color: White
- Padding: 10px 20px
- Border: none
- Border radius: 5px
- Font size: 14px
- Font weight: 500
- Hover: Background `#5a6268`
- Cursor: pointer

---

## Responsive Behavior (Mobile < 768px)

### General Adjustments

#### Page Headers
- **Flex direction**: column
- **Align items**: flex-start
- **Gap**: 15px

#### Statistics Cards
- **Grid columns**: 1
- **Full width**: Each card spans full container

#### Filters
- **Flex direction**: column
- **Width**: Each filter 100%

#### Submission Cards
- **Flex direction**: column
- **Align items**: stretch

#### Modals
- **Padding**: Reduce to 20px
- **Max width**: ~95% viewport width
- **Font sizes**: Maintain (already optimized)

#### Navbar
- **Flex wrap**: wrap
- **Justify content**: space-between (may need hamburger menu for very small screens)

---

## Interaction States

### Buttons

**Default State:**
- Defined background color
- White text
- Defined padding and radius

**Hover State:**
- Background color darkens by ~10%
- Cursor: pointer
- Transition: all 0.3s

**Active/Pressed State:**
- Background color darkens by ~15%
- Slight scale transform (optional)

**Disabled State:**
- Opacity: 0.6
- Cursor: not-allowed
- No hover effect

### Input Fields

**Default State:**
- Border: 1px solid `#ddd`
- Background: White

**Focus State:**
- Border color: `#667eea`
- Outline: none
- Shadow: `0 0 0 2px rgba(102, 126, 234, 0.1)` (optional)

**Error State:**
- Border color: `#dc3545`
- Error message below field

**Disabled State:**
- Background: `#f5f5f5`
- Cursor: not-allowed

### Cards

**Default State:**
- Shadow: `0 2px 4px rgba(0, 0, 0, 0.1)`

**Hover State (optional):**
- Shadow: `0 4px 8px rgba(0, 0, 0, 0.15)`
- Transform: translateY(-2px)
- Transition: all 0.3s

### Modals

**Open Animation:**
- Fade in overlay
- Scale modal content from 0.9 to 1
- Duration: 0.3s

**Close Animation:**
- Fade out overlay
- Scale modal content from 1 to 0.9
- Duration: 0.2s

**Click Outside:**
- Closes modal

**ESC Key:**
- Closes modal

---

## Accessibility Considerations

### Form Labels
- All form inputs have associated labels
- Labels use `for` attribute matching input `id`
- Required fields marked with asterisk (*)

### Color Contrast
- Text on background: Minimum WCAG AA (4.5:1)
- Status badges: Sufficient contrast maintained

### Focus Indicators
- Visible focus state on all interactive elements
- Tab order follows logical flow
- Skip navigation links for keyboard users

### Screen Readers
- Aria labels on icon-only buttons
- Status badges have readable text
- Modal dialogs use proper ARIA attributes
- Form validation messages are announced

### Keyboard Navigation
- All interactive elements keyboard accessible
- Modal trap focus within dialog
- ESC key closes modals
- Enter submits forms

---

## Loading States

### Page Load
- Display: "Loading..."
- Center aligned
- Color: `#666666`
- Min height: 100vh

### Form Submission
- Disable submit button
- Show loading spinner or text
- Prevent multiple submissions

### Data Fetching
- Show skeleton loaders for cards (optional)
- Or display "Loading submissions..." text

---

## Error States

### Login Error
- Display below login button
- Color: `#dc3545`
- Text align: center
- Margin top: 15px

### Form Validation Errors
- Show below relevant field
- Color: `#dc3545`
- Font size: 13px
- Icon: ⚠️ (optional)

### Network Errors
- Display toast notification or alert
- Persistent until dismissed
- Clear error message
- Retry option if applicable

---

## Animation Guidelines

### Transitions
- Duration: 0.2s - 0.3s
- Easing: ease-in-out or cubic-bezier
- Properties: background, transform, opacity, shadow

### Hover Effects
- Subtle changes
- Smooth transitions
- No jarring movements

### Modal Animations
- Fade overlay: 0.3s
- Scale content: 0.3s
- Stagger animations if multiple elements

### Page Transitions
- Minimal or none
- Focus on content loading speed

---

## Z-Index Hierarchy

```
10000 - Tooltips (highest)
1000  - Modals
900   - Dropdowns
100   - Sticky navbar
10    - Cards with hover elevation
1     - Default content
0     - Background
-1    - Behind content (rare)
```

---

## Component Reusability

### Shared Components

1. **Navbar** (Login excluded)
   - Used in: Student Dashboard, Officer Dashboard
   - Props: user (name), onLogout

2. **Status Badge**
   - Used in: All submission cards
   - Props: status ('pending' | 'approved' | 'rejected' | 'hold')

3. **Submission Card**
   - Used in: Student Dashboard, Officer Dashboard
   - Props: submission data, showStudentInfo (boolean), onReview (optional)

4. **Modal Wrapper**
   - Used in: Submit Modal, Review Modal
   - Props: onClose, children, title

5. **Button**
   - Used in: Throughout application
   - Variants: primary, secondary, danger (if needed)
   - Props: text, onClick, variant, disabled

6. **Form Field**
   - Used in: All forms
   - Types: text, password, date, select, textarea
   - Props: label, type, value, onChange, required, placeholder

---

## Grid & Spacing System

### Spacing Scale
```
4px   - xs   (tight)
8px   - sm   (compact)
10px  - md-  (between small and medium)
15px  - md   (medium)
20px  - lg   (comfortable)
30px  - xl   (spacious)
40px  - 2xl  (very spacious)
```

### Usage Examples
- **Gap between form fields**: 20px (lg)
- **Gap between sections**: 30px (xl)
- **Padding in cards**: 20px (lg)
- **Padding in containers**: 30px vertical, 20px horizontal
- **Gap in button groups**: 10px (md-)
- **Gap between status badge elements**: 5px-12px internal padding

### Grid Breakpoints
- **Mobile**: < 768px (single column)
- **Tablet**: 768px - 1024px (may use 2-3 columns for stats)
- **Desktop**: > 1024px (full 5-column stats grid)

---

## Typography Scale

### Heading Hierarchy
```
H1 (Page Titles):     16px / 24px line-height / 500 weight
H2 (Section Titles):  16px / 24px line-height / 500 weight  
H3 (Card Titles):     14px / 21px line-height / 500 weight
Navbar Brand:         20px / 30px line-height / 500 weight
```

### Body Text
```
Body (Default):       16px / 24px line-height / 400 weight
Small Text:           13px / 19.5px line-height / 400 weight
Tiny Text:            12px / 18px line-height / 400 weight
```

### Font Weights
```
Normal:  400
Medium:  500
Bold:    700 (used sparingly for labels)
```

---

## Icon Usage

### Primary Icon
- **Hospital Emoji**: 🏥
- **Usage**: Logo, branding
- **Sizes**: 
  - Navbar: 24px
  - Login page: 48px

### Suggested Icons (if implementing icon library)
- **Calendar**: Date fields
- **User**: Profile/login
- **Document**: Submissions
- **Check**: Approved status
- **X**: Rejected status
- **Clock**: Pending/On Hold status
- **Search**: Search/filter functionality
- **Filter**: Filter controls
- **Plus**: Add new submission

---

## Print Styles (Optional Enhancement)

### Considerations for printing
- Remove backgrounds (gradient, colors)
- Use black text on white background
- Hide interactive elements (buttons, modals)
- Optimize submission cards for paper
- Add page breaks between submissions
- Include submission details prominently

---

## Future Enhancement Opportunities

### Potential Features
1. **File Upload**: Attach medical certificates
2. **Notifications**: Email/SMS alerts on status changes
3. **Search**: Full-text search across submissions
4. **Advanced Filters**: Date range, multiple statuses
5. **Export**: Download submissions as PDF/CSV
6. **Analytics Dashboard**: Charts and trends
7. **Multi-language Support**: Sinhala, Tamil, English
8. **Dark Mode**: Alternative color scheme
9. **Pagination**: For large submission lists
10. **Sorting**: Sort by date, status, student name

---

## Testing Checklist

### Functional Testing
- [ ] Login with valid credentials (both roles)
- [ ] Login with invalid credentials
- [ ] Logout functionality
- [ ] Submit new medical certificate
- [ ] View submission list
- [ ] Filter submissions by status
- [ ] Filter submissions by type
- [ ] Review submission (officer)
- [ ] Approve submission
- [ ] Reject submission
- [ ] Put submission on hold
- [ ] View review notes
- [ ] Modal open/close behavior

### UI Testing
- [ ] All text is readable
- [ ] Colors have sufficient contrast
- [ ] Buttons have hover states
- [ ] Inputs have focus states
- [ ] Status badges display correctly
- [ ] Empty states display
- [ ] Loading states display
- [ ] Error messages display

### Responsive Testing
- [ ] Mobile layout (< 768px)
- [ ] Tablet layout (768px - 1024px)
- [ ] Desktop layout (> 1024px)
- [ ] Touch interactions work
- [ ] Modals fit on small screens

### Accessibility Testing
- [ ] Keyboard navigation works
- [ ] Screen reader announces content
- [ ] Focus indicators visible
- [ ] Form labels associated
- [ ] ARIA attributes correct

### Browser Testing
- [ ] Chrome
- [ ] Firefox
- [ ] Safari
- [ ] Edge
- [ ] Mobile browsers

---

## Conclusion

This wireframe document provides a comprehensive blueprint for the Medical Submission System UI. It covers:

- **3 main pages** (Login, Student Dashboard, Officer Dashboard)
- **2 modal dialogs** (Submit Certificate, Review Submission)
- **Detailed component specifications** with exact measurements and styles
- **Responsive behavior** for different screen sizes
- **Interaction patterns** and animations
- **Accessibility guidelines**
- **Data flow diagrams**
- **Testing checklist**

All measurements, colors, and specifications are based on the actual implementation code from the Figma imports. This document can serve as a reference for developers, designers, and stakeholders to understand the complete UI structure of the application.
