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
