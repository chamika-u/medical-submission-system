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
│           ┌───────────────────────────────┐                │
│           │                               │                │
│           │        LOGIN CONTAINER        │                │
│           │      (Centered, White)        │                │
│           │                               │                │
│           │         🏥 [Icon]             │                │
│           │                               │                │
│           │  Medical Submission System    │                │
│           │  Sabaragamuwa University      │                │
│           │      of Sri Lanka             │                │
│           │                               │                │
│           │  ┌─────────────────────────┐  │                │
│           │  │ Username                │  │                │
│           │  │ [Text Input Field]      │  │                │
│           │  └─────────────────────────┘  │                │
│           │                               │                │
│           │  ┌─────────────────────────┐  │                │
│           │  │ Password                │  │                │
│           │  │ [Password Input Field]  │  │                │
│           │  └─────────────────────────┘  │                │
│           │                               │                │
│           │  ┌─────────────────────────┐  │                │
│           │  │       [Login]           │  │                │
│           │  └─────────────────────────┘  │                │
│           │                               │                │
│           │  ┌─────────────────────────┐  │                │
│           │  │  Demo Credentials:      │  │                │
│           │  │  Medical Officer:       │  │                │
│           │  │  medical_officer /      │  │                │
│           │  │  medical123             │  │                │
│           │  │  Student: student1 /    │  │                │
│           │  │  student123             │  │                │
│           │  └─────────────────────────┘  │                │
│           │                               │                │
│           └───────────────────────────────┘                │
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
│  🏥 Medical Submission System              Kasun Silva  [Logout]  │ ← Navbar
├────────────────────────────────────────────────────────────────────┤
│                                                                    │
│  Student Dashboard                [+ Submit Medical Certificate]  │
│                                                                    │
│  My Medical Submissions                                            │
│                                                                    │
│  ┌──────────────────────────────────────────────────────────────┐ │
│  │ Date of Absence: Feb 5, 2026                     [Pending]   │ │
│  │ Type: Examination                                            │ │
│  │ Reason: Severe Fever                                         │ │
│  │ Additional Details: Had high fever of 102°F, unable to       │ │
│  │ attend the mid-term examination.                             │ │
│  │ Submitted: Feb 6, 2026, 10:30 AM                             │ │
│  └──────────────────────────────────────────────────────────────┘ │
│                                                                    │
│  ┌──────────────────────────────────────────────────────────────┐ │
│  │ Date of Absence: Jan 28, 2026                    [Approved]  │ │
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
│     ┌───────────────────────────────────────────┐     │
│     │                                      [×]   │     │
│     │  Submit Medical Certificate               │     │
│     │                                            │     │
│     │  Date of Medical Absence *                │     │
│     │  [Date Input Field]                       │     │
│     │                                            │     │
│     │  Type *                                    │     │
│     │  [Dropdown: Select type ▼]                │     │
│     │                                            │     │
│     │  Reason *                                  │     │
│     │  [Text Input: e.g., Fever, Headache]      │     │
│     │                                            │     │
│     │  Additional Details                        │     │
│     │  [Textarea: Provide any additional        │     │
│     │   details...]                              │     │
│     │                                            │     │
│     │  [  Submit  ]  [  Cancel  ]               │     │
│     │                                            │     │
│     └───────────────────────────────────────────┘     │
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

