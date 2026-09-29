# lovetalesadmindashboarddemo

ROLE
You are a Principal Product Designer and Senior Front-End Engineer at a top-tier design studio. Design and build a premium, high-fidelity, fully clickable UI/UX dashboard for a client presentation. The quality bar is a ₹1.5 lakh custom SaaS product. It must look expensive, calm and intentional, never like a template, a Bootstrap admin theme or a generic AI dashboard.

PRODUCT
LoveTales Photography & Films: an internal Event Management System for a photography and cinematography company. It handles weddings, engagements, receptions, pre-wedding shoots, birthdays, corporate events and baby shoots.

SCOPE (STRICT)
Design ONLY these two applications:
1. ADMIN WEB DASHBOARD (desktop 1440px, tablet fallback)
2. EMPLOYEE / TEAM MEMBER APP (mobile 390px, with a responsive web view)
Do NOT design any client-facing screens, client login, WhatsApp mockups or public forms. Do NOT build a single-story demo around one named couple or wedding. Show the system as a complete product with varied, realistic data across many events.

BRAND & VISUAL DIRECTION ("Premium & Energetic")
- Feel: a modern, energetic SaaS product with premium polish. Clean, bright, professional yet warm.
- Palette: Pure White backgrounds, Vibrant Orange as primary accent, supporting neutrals and semantic colours (no black, no gold).
- Light theme is the hero. Optional dark theme available.
- Typography: Playfair Display or Cormorant Garamond for headings and big numbers, Inter for UI text. Clear hierarchy, generous whitespace, 8px grid.
- Surfaces: clean soft cards, 12–16px radius, subtle light-grey borders, soft shadows. Minimal, not ornate.
- Icons: one consistent line set (Lucide). Avatars use gradient initials or elegant portrait placeholders. Equipment gets tasteful thumbnails.
- Motion: 200–300ms transitions, KPI count-up, skeleton loaders, slide-over drawers, animated status steppers, toasts, hover lift.

COLOR SYSTEM

PRIMARY PALETTE
- Pure White (#FFFFFF): light theme background, cards, surfaces, text on dark
- Warm White / Off-White (#FAFAF8): subtle background variation, secondary surfaces
- Vibrant Orange (#FF6B35): primary accent, active states, CTAs, highlights
- Soft Peach (#FFE5D9): secondary accent, hover states, warm highlights

NEUTRALS
- Light Grey (#F5F5F5): borders, dividers, disabled states, alternate rows
- Medium Grey (#8E8E8E): secondary text, labels, captions, subtle elements
- Dark Grey (#2C2C2C): headings, primary text (replaces black for softness)

SEMANTIC
- Sage Green (#6BA587): success, completed, returned, checked-in
- Warm Amber (#F5A623): pending, awaiting, follow-up, needs attention
- Coral Red (#E74C3C): damaged, conflict, error, blocked states
- Sky Blue (#3B82F6): info, notifications, secondary actions, in-progress

USAGE
- Buttons: Orange primary (#FF6B35), hover darker (#E55A24). Secondary: white bg with orange text and border.
- Text: Dark Grey (#2C2C2C) for headings and body. Medium Grey (#8E8E8E) for secondary/disabled.
- Status badges: Green for success, Amber for pending, Red for error, Blue for info.
- Borders: Light Grey (#F5F5F5) hairline. Orange (#FF6B35) on hover/focus.
- Cards: White background, light grey border, orange top border on important cards (KPIs, active items).
- Disabled states: Light Grey background, Medium Grey text, no shadow.

GLOBAL ADMIN LAYOUT
- Collapsible left sidebar: Dashboard, Enquiries, Events, Calendar, Team, Equipment, Reports, Notifications, Settings. Orange highlight on active item.
- Top bar: global search with ⌘K command palette, quick-create (+) menu, notification bell with unread count, theme toggle, admin profile menu.
- Breadcrumbs with orange separators, page headers with primary actions, empty states, loading skeletons, confirmation modals, toast feedback on every action.
- Sidebar collapses on tablet/mobile to an icon bar.

ADMIN FLOW: SCREENS TO DESIGN (complete, clickable, in this order)

A. ACCESS
1. Login: a split screen with a cinematic photo on one side and a minimal form on the other (email, password, remember me, forgot password link). Form has orange primary button. Illustration or image on the left side showing photography/event energy.
2. Forgot Password / Reset Password: clean form with email input, verification sent confirmation, reset link email preview, and new password form.

B. DASHBOARD (Command Center)
3. Dashboard: The homepage with animated KPI cards and micro-interactions.
   - Top section: 4 primary KPIs in large cards with count-up animations:
     * New Enquiries (12) with trending sparkline
     * Pending Follow-ups (5) with amber badge
     * Confirmed Events (8) with green checkmark
     * Today's Events (3) with orange highlight
   - Second row: 6 secondary KPIs:
     * Upcoming Events (15) | Available Team (12) | Assigned Team (9) | Available Equipment (42) | Assigned Equipment (18) | Under Maintenance (3)
   - Today's Events table: Event Name | Venue | Team Count (avatar group) | Status (badge) with clickable rows
   - Enquiry-to-booking funnel chart (New → Contacted → Discussion → Quotation → Confirmed) with smooth animations
   - Monthly events bar chart (count by type: weddings, engagements, receptions, etc.)
   - Live activity feed (check-ins, damage alerts, new enquiries, returns) with timestamps and avatars
   - Mini calendar with event dots (dates with events highlighted in orange)
   - "Needs Attention" panel: pending follow-ups, unassigned events, overdue equipment returns, unchecked-in team members (highlighted in amber or red)
   - Quick actions: + New Event, + New Enquiry, Assign Team, Return Equipment

C. ENQUIRY MANAGEMENT (enquiries arrive from the website form / WhatsApp automation; the admin only manages them)
4. Enquiry Pipeline: a Kanban board view (default) with columns:
   - New (1 → 5 cards with source badges: WhatsApp, Website, Referral)
   - Contacted (2 → 3 cards)
   - Discussion (1 → 2 cards)
   - Quotation Sent (2 → 3 cards)
   - Follow-up (1 → 2 cards)
   - Confirmed (3 → 5 cards)
   - Rejected/Cancelled (0 → 2 cards)
   Cards show: client name, event type icon, event date, team required (role chips), and a drag handle. Drag-and-drop between stages. Hover reveals client mobile and "View Details" button.
   - Table-view toggle: shows all enquiries in a data table with columns: ID | Client | Event Type | Date | Source | Status | Added | Actions.
   - Filters bar: Date range, Event Type (checkbox menu), Status (dropdown), Source (WhatsApp, Website, Referral).
   - Search bar (enquiry ID or client name).
   - Bulk actions: mark as contacted, mark as confirmed, delete, export.
   - Empty states for each column when no enquiries exist.

5. Enquiry Detail: a full-screen drawer or modal showing:
   - Client card: photo/avatar, name, mobile, email, event type, enquiry date, source badge.
   - Event requirements: event name, date, time, venue, guest count, couple name (if wedding).
   - Selected services: checkmarks for Photography, Videography, Cinematography, Drone, Album, Pre-Wedding, Other. Include required team counts (e.g. "2 photographers, 2 videographers").
   - Status stepper: New → Contacted → Discussion → Quotation Sent → Follow-up → Confirmed → (terminal: Converted to Event or Rejected).
   - Communication notes timeline: a scrollable list of dated notes with avatar, name, timestamp, and note text. An "Add Note" composer at the bottom (text input with @ mentions, emoji picker, and a send button).
   - Activity log (system events): Enquiry created, status changed, client contacted, etc.
   - Action buttons (at the bottom, sticky):
     * Update Status (dropdown to next status)
     * Confirm Booking (orange button, moves to Confirmed)
     * Convert to Event (orange button, appears only when Confirmed, shows auto-create animation)
     * Reject / Cancel (secondary button with reason modal)
     * Send Quotation (secondary)
     * Call Client (secondary with phone integration preview)

6. Convert-to-Event success: a full-screen celebratory modal showing:
   - Large checkmark icon (green)
   - Message: "Enquiry converted to Event"
   - New Event ID: "EVT-1001"
   - Event details card: name, date, venue, services
   - Buttons: "View Event" (orange) and "Back to Enquiries" (secondary)
   - Optional: confetti or subtle animation

7. New-enquiry notification panel: a preview of incoming enquiries (email + in-app alert). Shows client, event type, date, "View" button.

D. EVENT MANAGEMENT
8. Events List: a dual-view interface with toggle (card view / table view):
   - Card view (default): grid of event cards (3 columns on desktop). Each card shows:
     * Event ID and name (heading)
     * Date and time (subheading)
     * Venue (secondary text)
     * Status badge (Confirmed, Team Assignment Pending, Team Assigned, Equipment Assigned, Ready, In Progress, Completed, Equipment Returned, Closed) with color-coded badges
     * Team avatars (up to 5, overflow "+N")
     * Quick actions menu (three dots): View, Edit, Assign Team, Assign Equipment, View Timeline, Delete
   - Table view: columns: ID | Event Name | Date | Venue | Guest Count | Type | Status | Team | Equipment | Actions
   - Filters: Status (multi-select dropdown), Event Type (multi-select), Date Range (picker), Venue (search).
   - Search: by event ID or name.
   - Sorting: by date, status, team count, created date.
   - Pagination: 10, 25, 50 items per page.
   - Empty state: "No events yet. Create your first event to get started."

9. Event Detail: a multi-tab view within a full-page layout (not a modal). Tabs:
   - **Overview**: hero with event name, date, time, venue (with a location icon and directions link), guest count. Lifecycle stepper (Confirmed → Team Assignment Pending → Team Assigned → Equipment Assigned → Ready → In Progress → Completed → Equipment Returned → Closed) displayed prominently. Quick stat cards (team assigned, equipment assigned, total items). Primary action buttons (Assign Team, Assign Equipment, View Live, etc. depending on status).
   - **Client**: client card (photo, name, mobile, email, couple name if wedding), contact history, notes.
   - **Services**: checklist of selected services with required team roles and counts (e.g. 2 x Photographer, 1 x Videographer, 1 x Drone Operator).
   - **Team**: a table of assigned team members: Name (avatar + name) | Role | Reporting Time | Reporting Location | Special Instructions | Status (Accepted, On the Way, Arrived, Event Started, Event Completed). A "Reassign" button per row. An "Add Team" button to assign more.
   - **Equipment**: a table of assigned equipment: Item ID | Item Name | Category | Assigned To | Condition Before | Handed Over | Return Status. A "Reassign Equipment" button per row and an "Add Equipment" button.
   - **Timeline**: a chronological log of all status updates, assignments, team check-ins, equipment handovers and returns. Each entry has a timestamp, icon, and description.
   - **Notes**: a communication thread (add notes with text, @mentions, timestamps). Similar to enquiry notes.
   - **History**: a detailed audit log of all changes (who, what, when).

10. Create / Edit Event: a multi-step modal or drawer (3–4 steps):
    - Step 1 (Client Details): name, mobile, email, couple name (if wedding), notes.
    - Step 2 (Event Details): event name, type (dropdown: wedding, engagement, reception, pre-wedding, birthday, corporate, baby shoot, other), date picker, start time, end time, venue, guest count.
    - Step 3 (Services): checkboxes for Photography, Videography, Cinematography, Drone, Album, Pre-Wedding, Other. For each checked service, a field for "Required Count" (e.g. "2 photographers"). A "Next" button.
    - Step 4 (Review & Create): summary of all entered data with edit buttons. A "Create Event" button (orange) that generates the event and returns to the event detail.

11. Calendar view: three sub-views (Month, Week, Day) with all events displayed:
    - Month view: a traditional calendar grid with event dots on dates (orange for upcoming, green for completed). Click a date to see all events. Click an event to open the detail drawer.
    - Week view: a timeline grid (time slots on Y-axis, days on X-axis) with event blocks (color-coded by status). Team avatars shown in event blocks.
    - Day view: an hourly timeline for a single day with all events and team check-in/status updates.
    - Filter: by status, event type, team member, venue.
    - Legend: colour key for statuses.

E. TEAM MANAGEMENT
12. Team Directory: a dual-view (card / table):
    - Card view (default): grid of team member cards (4 columns). Each card shows:
      * Photo/avatar with name overlay
      * Role (e.g. Lead Photographer)
      * Experience (e.g. "5 years")
      * Status badge (Active, On Leave, Inactive)
      * Quick stats: upcoming events, completed events
      * Menu: View Profile, Edit, View Availability, Remove, Deactivate
    - Table view: columns: Photo | Name | Employee ID | Role | Experience | Status | Upcoming | Completed | Actions.
    - Filters: Role (multi-select), Status (Active, On Leave, Inactive), Experience level.
    - Search: by name, Employee ID.
    - Sorting: by name, role, experience, upcoming events.
    - Pagination.
    - Empty state: "No team members yet. Add your first team member."
    - "Add Team Member" button (orange CTA).

13. Add / Edit Team Member: a modal form with fields:
    - Employee ID (auto-generated)
    - Full Name
    - Photo upload (drag-and-drop with preview)
    - Mobile Number
    - Email Address
    - Role (dropdown: Lead Photographer, Photographer, Candid Photographer, Videographer, Cinematographer, Drone Operator, Lighting Technician, Assistant, Editor)
    - Years of Experience (number field)
    - Joining Date (date picker)
    - Status (Active / On Leave / Inactive) radio buttons
    - Credentials generation (auto-generates username, password or sends login link). Show username in a copyable field, password in a reveal field, and a "Send Credentials Email" button.
    - Save and Cancel buttons.

14. Team Member Profile: a full-page view showing:
    - Hero section: large photo/avatar, name, role, Employee ID, status badge, contact info.
    - Stat cards: Total Events Assigned | Upcoming Assignments | Completed Assignments | Equipment Currently Held.
    - Assignment History: a table of past and current assignments (Event | Date | Role | Status | Duration).
    - Equipment Currently Held: a list/table of assigned gear (Item ID | Name | Category | Assigned Date | Expected Return | Status).
    - Availability Calendar: a weekly or monthly grid showing Assigned, Available and On Leave dates.
    - Action buttons: Edit, View Assignments, View Equipment, Reassign, Deactivate, Send Message.

15. Team Availability grid: a heat-grid visualization showing:
    - Rows: team members
    - Columns: dates (next 30 days or selectable range)
    - Cell colours: Orange (Assigned), Green (Available), Amber (On Leave), Grey (Not Active)
    - Hover tooltip: shows the event(s) assigned to that member on that date, or "Available" if free.
    - Use case: at a glance, see who is free on a given date.

16. Assign Team wizard (3 steps, modal or drawer):
    - Step 1 (Select Members):
      * A list of all team members with checkboxes.
      * Filter by role (multi-select dropdown).
      * Show availability for the selected event date and time. Members who are busy on that date are disabled with a tooltip: "Already assigned to another event: Event Name, [Time Range]".
      * Show required vs. selected counts by role (e.g. "Need 2 photographers, selected 1").
      * A "Continue" button (enabled only when required counts are met).
    - Step 2 (Set Details per Member):
      * A form per selected member showing:
        - Member name and photo
        - Role
        - Reporting Date (date picker, defaults to event date)
        - Reporting Time (time picker)
        - Reporting Location (text input, with autocomplete for past venues)
        - Special Instructions (text area, e.g. "Cover bride preparation and ceremony")
      * A "Previous" and "Next" button.
    - Step 3 (Confirm & Assign):
      * A summary table: Member | Role | Reporting Time | Location | Instructions
      * A checkbox: "Notify team members" (checked by default)
      * A "Confirm Assignment" button (orange). On click:
        - Status updates to "Team Assigned"
        - Team members receive a notification (app + email)
        - A success toast appears: "Team assigned successfully"
        - Return to event detail.

17. Double-booking conflict warning modal: when a conflict is detected:
    - Title: "Scheduling Conflict Detected"
    - Message: "Member Name is already assigned to Event B on [Date] from [Time A] to [Time B]. Overlaps with this event's time [Time C] to [Time D]."
    - Suggestions: a list of available team members with the same role.
    - Buttons: "Assign Someone Else" (jumps back to step 1 of wizard), "Reassign & Confirm" (moves the member from Event B to this event, if allowed), "Cancel".

F. EQUIPMENT MANAGEMENT
18. Equipment Inventory: a dual-view (table / card):
    - Table view (default): columns: ID | Name | Category | Brand | Model | Serial | Status | Location | Condition | Last Used | Actions.
      * Sortable by any column.
      * Filters: Category (multi-select: Camera, Lens, Audio, Support, Drone, Lighting, Accessories), Status (multi-select: Available, Assigned, Maintenance, Damaged, Lost, Retired), Condition (multi-select: Good, Fair, Damaged).
      * Search: by ID, name, serial.
      * Pagination.
    - Card view: grid of equipment cards (5 columns). Each shows:
      * Photo/thumbnail
      * Item ID and name
      * Category icon and label
      * Status badge (colour-coded)
      * Condition indicator (Good = green, Fair = amber, Damaged = red)
      * Quick actions menu (View, Edit, Assign, Mark as Damaged, Retire, Delete)
    - Empty state: "No equipment yet. Add your first item."
    - "Add Equipment" button (orange CTA).

19. Add / Edit Equipment: a modal form:
    - Equipment ID (auto-generated)
    - Equipment Name (e.g. "Sony A7 IV")
    - Category (dropdown: Camera, Lens, Audio, Support, Drone, Lighting, Accessories)
    - Brand (e.g. "Sony")
    - Model (e.g. "A7 IV")
    - Serial Number (unique, validated)
    - Photo upload (drag-and-drop)
    - Purchase Date (date picker)
    - Condition (radio: Good, Fair, Damaged)
    - Status (radio: Available, Assigned, Maintenance, Damaged, Lost, Retired)
    - Location (text input, e.g. "Studio Shelf A")
    - Notes (text area, e.g. "Needs new battery")
    - Save and Cancel buttons.

20. Equipment Detail: a full-page view showing:
    - Hero: large photo/thumbnail, item ID, name, category, status badge.
    - Details card: brand, model, serial, purchase date, condition, current status, location.
    - Current Assignment (if assigned): assigned to team member, event, date assigned, expected return.
    - Full History Timeline: a chronological list of all uses, handovers and returns:
      * Date | Event | Team Member | Condition Before | Handover Time | Return Time | Condition After | Notes
      * Answers: "Who used this camera?" and "When was it used?"
    - Action buttons: Edit, Assign, Mark as Damaged, Mark as Lost, Mark as Retired, Maintenance Queue, Send to Maintenance, Retire.

21. Assign Equipment (per team member, per event): a drawer or modal showing:
    - Event and member context (event name, date, team member name, role).
    - Available equipment list (table or cards):
      * Columns: ID | Name | Category | Condition | Status | (checkbox)
      * Only items with Status = "Available" or "Assigned to another member but returning soon" are selectable.
      * Damaged, Lost, Maintenance, Retired and already-assigned items are greyed out and disabled.
      * Hover tooltip on disabled items: "Under maintenance", "Already assigned to Member X until [Date]", "Item retired".
    - Selected equipment summary: shows chosen items, total count, summary by category.
    - Checkbox: "Mark items as Handed Over immediately" (checked by default).
    - "Assign" button (orange). On click:
      - Status updates to "Equipment Assigned"
      - If "Mark as Handed Over" is checked, equipment shifts to "Handed Over (awaiting confirmation)"
      - Team member gets a notification: "New equipment assigned to your profile"
      - A success toast: "Equipment assigned"

22. Handover Tracker: a view (table) of handover status for a specific event:
    - Columns: Equipment ID | Name | Assigned To | Handed Over Time | Condition Before | Team Confirmed Receipt | Status
    - Statuses: "Awaiting Handover" (orange), "Handed Over (awaiting confirmation)" (amber), "Confirmed by Team" (green), "Returned" (green), "Pending Return" (red)
    - Per-item actions: "Mark as Handed Over" (if not yet), team member can confirm "I Received This Equipment" in their app.
    - Summary: X of Y items handed over, Y of Y confirmed.

23. Maintenance Queue: a dedicated view for items under maintenance:
    - Table: ID | Name | Category | Issue Description | Date Reported | Photo Evidence | Status | Actions
    - Add to Queue: opens a modal to mark an item as "Under Maintenance" and add details (issue, photos, expected repair date, assigned technician).
    - Mark Repaired: status changes to "Available" and notifies relevant people.
    - Mark Retired: moves item to "Retired" status.
    - Empty state: "No items in maintenance."

G. LIVE EVENT DAY
24. Live Command Center: a real-time dashboard for the day's events:
    - Top bar: today's date, time (live clock), number of today's events.
    - Today's Events list (cards): for each event, show:
      * Event name, venue, team count
      * Status badge (Confirmed, Ready, In Progress, Completed)
      * Check-in status board (below each event card):
        - Names of assigned team members (with avatars)
        - Per-member check-in status: "Accepted" (green) | "On the Way" (orange) | "Arrived" (blue) | "Event Started" (orange) | "Event Completed" (green) | "Not Checked In" (red)
        - Members not checked in are highlighted prominently (red background) with a "Nudge / Call" button to send a push notification or dial.
      * Per-member status journey: a mini stepper showing progression (Accepted → On the Way → Arrived → Event Started → Event Completed).
      * Instruction timeline: a collapsible section showing key times (e.g. 7:30 AM Bride Prep, 8:00 AM Groom Prep, 10:00 AM Ceremony) with a countdown to each.
      * Quick actions: View Event, View Equipment Returns, Mark as Completed, Cancel Event.
    - Push-notification feed (right sidebar or bottom panel): live notifications as they come in (team check-in, status updates, equipment handover, messages from team). Show avatar, member name, action, timestamp. Dismiss or reply option.
    - If no events today: empty state "No events scheduled for today. Great work!"

25. Event Completed alert: when a team member marks the event as completed:
    - A large toast or in-app notification at the top of the screen
    - Message: "Event [Name] has been marked as completed by the team."
    - Buttons: "View Event" (orange), "Start Equipment Return" (orange secondary)
    - Status automatically updates to "Completed" in the event card.

H. EQUIPMENT RETURN & CLOSURE
26. Return Verification: a full-page form / table for verifying equipment after an event:
    - Event context (at top): event name, date, status.
    - Equipment table: columns:
      * Equipment ID
      * Equipment Name
      * Category icon
      * Held By (team member name + avatar)
      * Handed Over Time (e.g. "7:00 AM")
      * Condition Before (badge: Good, Fair, Damaged)
      * Return Status (buttons per row: "Mark Returned", "Pending")
      * Condition After (dropdown: Good, Fair, Damaged, Lost)
      * Actions (see details, record damage, notes)
    - For each item, the admin can:
      * Click "Mark Returned": status changes to green checkmark, timestamp is recorded.
      * Click "Record Damage" for damaged items: opens a modal (see below).
      * Click "Mark as Lost": status changes to red, equipment status becomes "Lost".
    - Summary bar (at top or bottom): X of Y items returned, Y of Y items verified.
    - "Mark All as Returned" button (if all are received in good condition).
    - "Save & Continue to Closure" button (orange) → moves to next screen.

27. Record Damage modal: appears when marking an item as damaged:
    - Equipment details (read-only): ID, name, category, assigned to member.
    - Condition selector: radio buttons (Good, Fair, Damaged, Lost). "Damaged" is selected.
    - Damage Description (text area): "Front propeller broken during landing."
    - Photo Evidence upload (drag-and-drop, multi-upload): accepts JPEG, PNG. Shows preview thumbnails.
    - Assigned Technician (dropdown, optional): choose who will repair.
    - Expected Repair Date (date picker, optional).
    - Notice (in a callout box): "Status will change to Under Maintenance. This item will be unavailable for future assignments until repaired and marked as Available."
    - Save (orange) and Cancel buttons.
    - On save: equipment status becomes "Under Maintenance", is blocked from future assignments, and the damage record is logged.

28. Return Status overview: a summary page before event closure:
    - Heading: "Event Closure Checklist"
    - 4 checklist items (each with a status icon):
      ✓ Event Completed (checked if marked completed by team)
      ✓ Team Checked In (checked if all team members checked in)
      ✗ Equipment Returned (checked if all equipment returned)
      ✗ Admin Verified (checked if all return verifications are complete)
    - Progress ring: "X of Y" items returned. Filled in orange, unfilled in light grey.
    - Per-member return summary table: Member Name | Items Assigned | Items Returned | Status (Complete / Pending).
    - Reminder actions for pending items (e.g. "Nudge Member Name to return equipment").
    - Summary stats: 6 total, 5 returned, 1 pending, 1 damaged.

29. Event Closure: the final step:
    - Heading: "Close Event"
    - The 4-item checklist (from above) is displayed again.
    - "Close Event" button (orange): 
      * LOCKED state (disabled, greyed out) until all 4 checks are green.
      * HOVER tooltip when locked: "All items must be checked before closing."
      * When UNLOCKED (all items complete), becomes bright orange and clickable.
      * On click: confirmation modal asks "Are you sure you want to close this event? This action cannot be undone."
    - On confirmation: event status becomes "Closed", timestamp is recorded, a celebratory success modal or animation appears:
      * Large checkmark (green)
      * Message: "Event Closed Successfully"
      * Event summary card (name, date, team count, equipment count)
      * Buttons: "View Report" (orange), "Back to Dashboard" (secondary)

I. REPORTS & INSIGHTS
30. Reports Hub: a dashboard showing 4 main report categories (Enquiry, Event, Team, Equipment) as large cards. Each card shows a preview chart and a "View Full Report" link.

31. Enquiry Report: 
    - Date range picker (top)
    - Filters: Event Type, Status, Source
    - KPI row: Total Enquiries | Conversion Rate | Avg Days to Convert | Enquiries by Source (pie chart)
    - Funnel chart: New → Contacted → Discussion → Quotation → Confirmed (shows drop-off at each stage)
    - Status breakdown table: Status | Count | Percentage | Trend (sparkline)
    - Source breakdown (doughnut chart): WhatsApp % | Website % | Referral %
    - Export buttons: PDF, CSV

32. Event Report:
    - Date range picker
    - Filters: Status, Type, Venue
    - KPI row: Total Events | Revenue (if pricing data available) | Avg Team Size | Avg Equipment Items
    - Event type breakdown (bar chart): Weddings | Engagements | Receptions | etc.
    - Timeline chart: events by date
    - Status breakdown table: Status | Count
    - Export buttons: PDF, CSV

33. Team Report:
    - Filters: Role, Status
    - KPI row: Total Team Members | Avg Events per Member | Upcoming Assignments | Utilisation Rate
    - Utilisation chart: per member, upcoming and completed event counts (bar chart)
    - Member detail table: Name | Role | Total Events | Upcoming | Completed | Utilisation % | Availability
    - Role breakdown (pie chart): Lead Photographer % | Photographer % | etc.
    - Export buttons: PDF, CSV

34. Equipment Report:
    - Filters: Category, Status
    - KPI row: Total Items | Available | Assigned | Maintenance | Damaged | Lost | Retired
    - Status breakdown (doughnut chart): pie showing distribution
    - Equipment category breakdown (horizontal bar chart): Camera | Lens | Audio | etc.
    - Equipment Usage Report (separate): detailed table showing Item ID | Name | Uses (count) | Last Used Date | Days Since Last Use | Maintenance Status
    - Maintenance history: Item | Issue | Date Reported | Date Resolved | Cost (if available)
    - Export buttons: PDF, CSV

J. NOTIFICATIONS & SETTINGS
35. Notification Center (full page):
    - Sidebar filters: All | Unread | New Enquiries | Booking Confirmed | Team Accepted | Check-In | Event Started | Event Completed | Equipment Returned | Equipment Damaged | Event Cancelled
    - Notification list (grouped by day): each notification shows avatar, title, message, timestamp, and a "Mark as read" action. Unread items have a blue dot or highlight.
    - Bulk actions: Mark all as read, Clear all (with confirmation).
    - Empty state: "All caught up!"

36. Notification Bell (top bar): 
    - Badge with unread count (orange background).
    - Dropdown on click shows last 5 notifications with a "View All" link.

37. Settings Page:
    - Sidebar tabs: Profile | Roles & Permissions | Notification Preferences | Company Settings | Equipment Categories | Event Types | Integrations
    - Profile tab: name, email, profile photo, password change, bio.
    - Roles & Permissions tab: a table of user roles (Admin, Coordinator, Team Lead, Team Member) with checkboxes for permissions (e.g. Create Event, Assign Team, View Reports). Invite user form (email + role).
    - Notification Preferences tab: toggles for notification type and channel:
      * New Enquiry (In-App | Email | WhatsApp)
      * Booking Confirmed (In-App | Email)
      * Team Accepted (In-App | Email)
      * Team Check-In (In-App | Email)
      * Event Started (In-App | Email)
      * Event Completed (In-App | Email)
      * Equipment Returned (In-App | Email)
      * Equipment Damaged (In-App | Email | Urgent)
      * Event Cancelled (In-App | Email)
    - Company Settings tab: company name, logo upload, primary contact, phone, email, address.
    - Equipment Categories tab: a table of equipment categories with edit/delete per row, and an "Add Category" button.
    - Event Types tab: a table of event types (Wedding, Engagement, Reception, etc.) with edit/delete per row, and an "Add Event Type" button.
    - Integrations tab: (placeholder for future integrations e.g. Google Calendar, Slack, WhatsApp Business API) with toggle switches for connected services.

EMPLOYEE / TEAM MEMBER APP FLOW (390px mobile-first, with responsive web fallback)
Employees see ONLY events and equipment assigned to them.

E1. Splash Screen & Auth
E1a. Splash: LoveTales logo, tagline "Capturing Your Beautiful Stories", loading animation.
E1b. Login: form with username and password fields, forgot password link, login button (orange). Bottom: "Don't have credentials? Contact your admin."

E2. Home Screen
    - Greeting: "Welcome, [Name]" (personalised)
    - Today's Event Hero Card: largest on screen, showing:
      * Event name (large heading)
      * Date and time (e.g. "15 Dec 2026 | 7:00 AM - 4:00 PM")
      * Venue with location icon and "Get Directions" button
      * Role (e.g. "Lead Photographer")
      * Status badge (Assigned, Accepted, In Progress, Completed)
      * "View Details" button (orange)
    - Quick Stats Row (3 cards): Upcoming Events | Today's Events | Completed Events
    - Upcoming Events Preview: a scrollable list of next 3–5 events with cards (event name, date, venue, status).
    - Notification Bell (top right corner) with unread count badge (orange).

E3. My Events Screen
    - Tab bar at top: Today | Upcoming | Completed (with counts)
    - List of events (Today tab): for each event, a card showing:
      * Event name
      * Date and time
      * Venue with location icon
      * Status badge (Confirmed, Accepted, On the Way, Arrived, Event Started, Event Completed)
      * "View Details" tap target
    - Upcoming and Completed tabs: similar structure, sorted by date.
    - Pull-to-refresh to sync data.
    - Empty state per tab: "No events today" / "No upcoming events" / "No completed events"

E4. Event Detail Screen
    - Scrollable full-screen view:
      * Event hero: name (large), date, time, venue.
      * Location card: venue name with address, "Get Directions" link (maps integration), distance if available.
      * Role & Reporting Info:
        - Role: "Lead Photographer"
        - Reporting Time: "7:00 AM"
        - Reporting Location: "XYZ Convention Hall, Main Entrance"
      * Team Mates: avatar group of other assigned team members with names and roles (view-only, no chat integration in this version).
      * Client Info Card (view-only): client name, couple name (if wedding), contact number, email.
      * Admin Instructions (collapsible): a timeline or list of key times and instructions:
        - 7:30 AM: Bride preparation
        - 8:00 AM: Groom preparation
        - 10:00 AM: Ceremony
        - etc.
      * My Equipment: a list of assigned items (item ID, name, category icon, condition).
      * Status Journey (stepper): visual step showing current progress (Accepted → On the Way → Arrived → Event Started → Event Completed). Current step is highlighted in orange.
      * Buttons (sticky at bottom, full width):
        - Accept Assignment (orange, if status is "Confirmed")
        - Check In (orange, appears when approaching event time, large and prominent)
        - Update Status (if event is in progress)
        - Mark as Completed (orange, when event is ending)

E5. Assignment Request Notification
    - When a new assignment arrives, a fullscreen overlay or slide-up sheet appears:
      * Message: "You have a new event assignment"
      * Event card preview: event name, date, venue, role, team count
      * Buttons: "Accept" (orange, large) | "View Details" (secondary) | "Reject" (secondary)
      * On "Accept": notification dismisses, home screen shows the event, employee gets a success toast.

E6. My Equipment Screen
    - List of assigned equipment items for all upcoming events:
      * Per-item card showing:
        - Equipment thumbnail/photo
        - Item ID and name
        - Category icon and label
        - Condition badge (Good = green, Fair = amber, Damaged = red)
        - Assigned to event(s) (event name, date)
        - "I Received This Equipment" button (if not yet confirmed) or "✓ Confirmed" badge (if confirmed)
        - "View Details" tap target
    - If an item has a "I Received This Equipment" button, tapping it shows a confirmation modal: "Confirm: You have received [Item Name]?" with "Yes" (orange) and "No" buttons. On confirmation, the button changes to a green checkmark badge.
    - Empty state: "No equipment assigned."

E7. Check-In Screen (large, single-action focus)
    - Heading: "Check In"
    - Subheading: event name and date
    - Venue name and location (read-only)
    - Large "Check In" button (orange, takes up most of the screen)
    - On tap, a confirmation modal: "Check in at [Venue]?" with timestamp. "Confirm" (orange) and "Cancel".
    - On confirmation: a success animation (checkmark, green highlight, brief confetti or pulse), toast message "Checked in successfully", then transition to status journey showing "Arrived" as current step.
    - If already checked in, show "✓ Checked In" with timestamp instead of button.

E8. Status Journey / Timeline (full-screen view)
    - A large, clear stepper showing all stages:
      * Accepted (grey if pending, green if done, shows timestamp)
      * On the Way (grey if pending, orange if current, green if done)
      * Arrived (grey if pending, blue if current, green if done)
      * Event Started (grey if pending, orange if current, green if done)
      * Event Completed (grey if pending, orange if current)
    - Per stage, show the timestamp when it was reached (e.g. "Arrived: 7:05 AM").
    - One large action button per stage (when event is live):
      * "I'm On The Way" (when assigned and not yet on way)
      * "I've Arrived" (when on way and not yet arrived)
      * "Event Started" (when arrived and event not started)
      * "Event Completed" (when event is in progress)
    - After "Event Completed" is tapped, show a congratulatory message and transition to equipment return checklist.

E9. Event Completed Screen
    - Heading: "Event Complete!"
    - Congratulatory message and emoji (celebration)
    - Summary: event name, date, duration (time from check-in to now)
    - "Start Equipment Return" button (orange): takes employee to E10.

E10. Return Equipment Checklist
    - Heading: "Return Your Equipment"
    - Subheading: "Check off each item as you return it"
    - Checklist (per item):
      * Item thumbnail
      * Item name and ID
      * Checkbox
      * "Mark Returned" button (per item, or bulk "Mark All as Returned")
    - Summary: X of Y items marked as returned.
    - "All Equipment Returned" button (orange, enabled when all items are checked). On tap: success screen "Equipment return submitted. Thank you!"
    - If any item is damaged, a "Report Damage" option appears (shows a mini form: damage description + photo, but full damage recording happens on admin side).

E11. My Schedule Screen
    - A personal calendar (month view) with assigned event dates highlighted in orange.
    - Click a date to see events on that day (card preview).
    - Click an event to jump to event detail.

E12. Notifications Screen
    - List of recent notifications (new assignment, date change, equipment assigned, reminders, special instructions, cancellations).
    - Grouped by day (Today, Yesterday, Earlier).
    - Tap to view full notification.
    - Swipe to dismiss.
    - Empty state: "All caught up!"

E13. My Profile Screen
    - Avatar and name (editable: name, phone number, email).
    - Employee ID (read-only)
    - Role (read-only)
    - Contact: phone and email.
    - Stats: Total Events | Upcoming | Completed
    - "View My Calendar" link.
    - "Logout" button (red/coral).
    - "Help & Support" link.

BOTTOM TAB BAR (visible on all screens)
- Home icon → E2 (Home)
- Calendar icon → E11 (My Schedule)
- Briefcase/Document icon → E3 (My Events)
- Package icon → E6 (My Equipment)
- Bell icon → E12 (Notifications)
- Person icon → E13 (Profile)

CROSS-ROLE SYNC (demonstrate in the demo)
Show visually how real-time updates propagate:
- Admin assigns team → employee app receives "New Assignment" notification, home screen updates.
- Admin hands over equipment → employee sees "I Received This Equipment" buttons.
- Employee checks in → admin's live event day board updates, check-in time is recorded, toast fires on admin side.
- Employee updates status → admin's status journey updates in real-time.
- Employee marks event completed → admin gets a toast, equipment return checklist appears on both sides.
- Optional: split-screen demo mode showing admin dashboard on left, employee phone on right, with real-time sync animation between them.

BUSINESS RULES TO EXPRESS VISUALLY
1. No team double-booking: overlapping assignments are blocked with a clear warning and suggestions.
2. The same equipment cannot go to two people at once: disabled in assign flow with tooltips.
3. Damaged, lost, maintenance and retired equipment cannot be assigned: greyed out, tooltips explain why.
4. Employees see only their own events and equipment: queries filtered server-side.
5. An event cannot close until all equipment is returned or resolved and the admin has verified: closure button locked, checklist enforces this.
6. All assignment and equipment records keep full history: audit log visible in detail screens.

DATA & CONTEXT
- Use realistic, varied mock data: 12–15 events of different types (weddings, engagements, receptions, pre-wedding shoots, birthdays, corporate events, baby shoots) across different dates (past, today, upcoming).
- 12–15 team members with mixed roles (Lead Photographer, Photographer, Videographer, Cinematographer, Drone Operator, Lighting Technician, Assistant, Editor).
- 50+ equipment items across categories (Camera, Lens, Audio, Support, Drone, Lighting, Accessories) with varied statuses.
- Use realistic IDs: ENQ-1001, EVT-1001, CAM001, LEN001, DRN001, etc.
- Indian context: use ₹ for pricing (if relevant), Indian names, Indian venues and cities. Examples: "Rahul Wedding" is acceptable but show varied events and attendees. No single-story focus.
- Keep data consistent across every screen (same event IDs, same team members, same equipment, same dates).
- No lorem ipsum anywhere.

UX & ACCESSIBILITY
- Every screen needs default, hover, focus, loading, empty, error and success states.
- Tables: sticky headers, sortable columns, pagination, row actions.
- Modals and drawers: overlay, close button (X), keyboard ESC to close.
- Forms: validation on blur and submit, clear error messages, field hints.
- Responsive: admin desktop-first (1440px primary, 768px tablet fallback), employee mobile-first (390px primary, 768px+ web fallback).
- WCAG AA contrast: all text vs. background, interactive elements have visible focus rings (orange outline, 2–3px).
- Keyboard navigation: Tab through all interactive elements, Enter to confirm, ESC to dismiss.
- ⌘K global search: searches events, team members, equipment, enquiries; results grouped by type; keyboard shortcut works on desktop.
- Loading states: skeleton loaders (light grey animated placeholders) for data tables, cards, lists.
- Error states: clear error messages, suggestions for recovery (e.g. "Event date must be in the future").
- Empty states: icon, short headline, subtext, call-to-action button where relevant.
- Toast notifications: auto-dismiss after 3–4 seconds, close button, stacking for multiple toasts, colours: green (success), red (error), orange (info), blue (neutral).

INTERACTION & MOTION
- Page transitions: smooth fade-in / slide-from-right (mobile), fade (desktop).
- KPI count-up: 1000ms animations, easing function ease-out-quad.
- Status steppers: 300ms transitions between steps, highlight animation.
- Tables: row hover (light grey background), click to expand or select, smooth row animations on add/delete.
- Buttons: 200ms background colour transition on hover, slight scale (1.02x) on active.
- Modals: fade overlay (200ms), slide-up content (300ms), ease-out-cubic.
- Drawers: slide from right (300ms), ease-out-cubic.
- Toasts: slide in from top-right (200ms), slide out on dismiss (300ms).
- Form inputs: 200ms border colour transition on focus (to orange).

REUSABLE COMPONENTS (build these first, then compose screens)
1. **KPI Card**: icon, label, large number (with count-up animation), sparkline or trend, optional badge, hover lift.
2. **Status Badge**: small pill, colour-coded, icon + text.
3. **Data Table**: headers (sticky), sortable columns, pagination, row selection, row actions menu (three dots).
4. **Kanban Card**: title, metadata (date, source), tags, drag handle, hover reveal actions.
5. **Modal / Dialog**: overlay, header, body, footer with buttons, close button, keyboard ESC.
6. **Drawer / Slide-over**: from right, full height, close button, smooth animation.
7. **Stepper**: horizontal steps, filled/current/pending states, labels, timestamps.
8. **Timeline**: vertical or horizontal, events with icons/avatars, timestamps, descriptions.
9. **Toast**: position fixed, auto-dismiss, close button, colours by type, stacking.
10. **Avatar**: image or initials, size variants (sm, md, lg), badge support.
11. **Avatar Group**: multiple avatars with overflow count ("+N").
12. **Status Journey / Progress**: multi-step indicator, current step highlighted, timestamps per step.
13. **Calendar**: month/week/day views, event dots, click to open, filter by type/member/venue.
14. **Chart Cards**: bar, line, pie, doughnut charts with brand colours, legends, no clutter.
15. **Form Input**: text, email, password, number, date, time pickers. Focus ring (orange), error message.
16. **Autocomplete / Combobox**: search input with dropdown suggestions, keyboard navigation.
17. **Multi-select Dropdown**: checkboxes in dropdown, selected count badge, clear all button.
18. **Tabs**: horizontal tab bar, active tab underline (orange), smooth transition.
19. **Breadcrumbs**: path navigation, orange separators, click to jump.
20. **Empty State**: icon (from Lucide), headline, subtext, CTA button if relevant.
21. **Loading Skeleton**: light grey animated placeholders matching the component shape.
22. **Confirmation Modal**: title, message, icon, action buttons (primary orange, secondary grey).
23. **Popover / Tooltip**: on hover or click, positioned near trigger, fade-in animation, arrow pointing to target.

DELIVERABLE FORMAT
- **Design System Summary** (first): colours, typography, spacing/grid (8px base), border-radius (12–16px), shadows (soft, warm), motion easing functions, component specs.
- **Working Prototype**: React component library + pages, OR single-file HTML with embedded React or Vue. Uses mock data in state (no backend calls). All screens clickable and navigable.
- **Structure**:
  - `/components`: all 23+ reusable components above
  - `/pages/admin`: Dashboard, Enquiries, Events, Calendar, Team, Equipment, Reports, Notifications, Settings
  - `/pages/employee`: Home, MyEvents, EventDetail, MyEquipment, StatusJourney, CheckIn, Profile, Notifications, Calendar
  - `/state`: mock data (enquiries, events, team, equipment, assignments, handovers, returns)
  - `/utils`: helpers for filtering, sorting, date formatting, colour mapping
- **Chart Library**: use a lightweight charting library (e.g. Recharts, Chart.js, D3) with brand colours and minimal styling.
- **Responsive**: Tailwind CSS for styling. Desktop (1440px) and tablet (768px) breakpoints for admin. Mobile (390px) and web (1024px+) for employee app.
- **Demo Navigator** (optional): a small floating button or sidebar menu that lists all screens alphabetically and lets the presenter jump to any screen.

QUALITY BAR / DO NOT
- No lorem ipsum. All text must be realistic (event names, team member names, equipment names, venue names).
- No purple-blue gradient clichés, no Material Design defaults, no Bootstrap look-alikes.
- No cluttered tables. Keep column count low, actions in a menu, use horizontal scrolling if needed (with a warning to designer that desktop needs more space).
- No rainbow charts. Use only brand colours (orange, orange with green/amber/red for semantics, grey for neutrals).
- No black text on white only. Use dark grey (#2C2C2C) for softer appearance while maintaining WCAG AA.
- Every screen must be presentable in a screenshot. Whitespace is your friend. Use 16–32px padding/margins.
- Prioritise polish, consistency and hierarchy over feature quantity. Better to nail 5 screens perfectly than 20 screens halfway.
- All CTAs should be orange (#FF6B35). Destructive actions should be coral red (#E74C3C).
- Hover and focus states must be obvious (colour change, border, scale, shadow).

BUILD ORDER (Recommended)
1. Design System document (colours, type scale, spacing, radius, shadows, motion, component names)
2. Core components (KPI Card, Badge, Button, Input, Modal, Toast, Table, Avatar)
3. Admin Dashboard + top bar + sidebar
4. Enquiries (Pipeline Kanban, Enquiry Detail, Convert to Event)
5. Events (List, Detail, Create, Calendar)
6. Team (Directory, Availability, Assign wizard with conflict detection)
7. Equipment (Inventory, Assign, History, Maintenance)
8. Live Event Day + Equipment Return + Closure
9. Reports + Notifications + Settings
10. Employee App (Home, Events, Equipment, Status Journey, Check-In, Profile)
11. Cross-role Sync demo (optional split-screen showing both UIs updating in real-time)
12. Demo Navigator menu

START WITH: Design System + Dashboard + Enquiries Pipeline. If prompt is cut off, continue with Events → Team → Equipment → Return & Closure. Then Reports + Settings + Employee App.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```

## Deploy to Vercel

Import the repository into Vercel. The project builds with `npm run build`, and
`vercel.json` points Vercel to Nitro's `.vercel/output` deployment artifact.
The Nitro Vercel preset packages the app as a serverless function and static
assets using the Node.js 22 runtime.
