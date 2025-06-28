# AI Task Template

> **Instructions**: This template helps you create comprehensive task documents for AI-driven development. Fill oout each section thoroughly to ensure the AI agent has all necessary context and can execute the task systematically.

---

## 1. Task Overview

### Task Title
<!-- Provide a clear, specific title for this task. -->
**Title:** [Brief, descriptive title of what you're building/fixing]

### Goal Statement
<!-- One paragraph describing the high-level objective -->
**Goal:** [Clear statement of what you want too achieve and why it matters]

---

## 2. Project Analysis & Current State

### Technology & Architecture
<!-- 
AI Agent: Analyze the project to fill this out.
- Check `package.json` for versions and dependencies.
- Check `tsconfig.json` for TypeScript configuration
- Check `tailwind.config.js` for styling and theme.
- Check `drizzle/schema` for database schema.
- Check `middleware.ts` for authentication and routing.
- Check `components/` for existing UI patterns.
-->
- **Frameworks & Versions:** [List of frameworks and their versions, e.g., React 19, Next.js 15.3]
- **Language:** [Programming languages used, e.g., TypeScript 5.4 with strict mode]
- **Database & ORM:** [Database technology and ORM, e.g., Supabase (Postgres) via Drizzle ORM]
- **UI & Styling:** [UI libraries and styling frameworks, e.g., shadcn/ui components with Tailwind CSS for styling]
- **Authentication:** [Authentication methods, e.g., Supabase Auth managed by `middleware.ts` for protected routes]
- **Key Architectural Patterns:** [Describe any key architectural patterns used, e.g., Next.js App Router, Server Components for data fetching and Action for mutations]
- **Relevant Existing Components:** [List any existing components or modules that are relevant to this task, e.g., `components/ui/button.tsx` for base styles, `components/ui/LoginForm.tsx` for form patterns]

### Current State
<!-- Describe what exists today based on actual analysis -->
[Describe the current situation, existing code, and what's working/not working - based on analysis not assumptions]

## 3. Context & Problem Definition

### Problem Statement
<!-- Clearly define the problem or opportunity this task addresses -->
**Problem:** [Detailed description of the problem, including any relevant context or background information]

### Success Criteria
<!-- Define what success looks like for this task -->
- [ ] [Success Criterion 1, e.g., "User can successfully log in with email and password"]
- [ ] [Success Criterion 2, e.g., "User can perform full CRUD (Create, Read, Update, Delete) operations on their profile"]

---

## 4. Technical Requirements

### Functional Requirements
<!-- List the functional requirements that must be met -->
- **User can:**
  - [ ] [Requirement 1, e.g., "Register with email and password"]
  - [ ] [Requirement 2, e.g., "Log in with email and password"]
  - [ ] [Requirement 3, e.g., "Update profile information"]
- **System will:**
  - [ ] [Requirement 4, e.g., "Send confirmation email on registration"]
  - [ ] [Requirement 5, e.g., "Validate user input on the frontend and backend"]

### Non-Functional Requirements
<!-- List any non-functional requirements, such as performance, security, or usability -->
- **Performance:**
  - [ ] [Non-Functional Requirement 1, e.g., "Page load time must be under 2 seconds"]
  - [ ] [Non-Functional Requirement 2, e.g., "API response time must be under 500ms"]
- **Security:**
  - [ ] [Non-Functional Requirement 3, e.g., "All user data must be encrypted in transit and at rest"]
  - [ ] [Non-Functional Requirement 4, e.g., "Implement rate limiting on API endpoints to prevent abuse"]
- **Usability:**
  - [ ] [Non-Functional Requirement 5, e.g., "UI must be accessible according to WCAG 2.1 standards"]
  - [ ] [Non-Functional Requirement 6, e.g., "Provide clear error messages for user input validation"]
- **Responsive Design:**
  - [ ] [Non-Functional Requirement 7, e.g., "UI must be fully responsive and work on mobile devices"]
  - [ ] [Non-Functional Requirement 8, e.g., "Ensure all components are usable on small screens"]
- **Theme support:**
  - [ ] [Non-Functional Requirement 9, e.g., "Support light and dark themes using Tailwind CSS"]
  - [ ] [Non-Functional Requirement 10, e.g., "Allow users to toggle themes dynamically"]

### Technical Constraints
<!-- Describe any technical constraints that must be considered -->
- [ ] [Technical Constraint 1, e.g., must use existing UI components]
- [ ] [Technical Constraint 2, e.g., must integrate with existing authentication]

## 5. Data & Database Changes

### Database Schema Changes
<!-- Describe any changes needed to the database schema -->
- [ ] [Schema Change 1, e.g., add new table for user profiles]
- [ ] [Schema Change 2, e.g., modify existing table to add new column]

### Data Migration Plan
<!-- Describe how existing data will be migrated if necessary -->
- [ ] [Migration Plan 1, e.g., migrate existing user data to new profile created at `lib/drizzle/schema/userProfile.ts`]
- [ ] [Migration Plan 2, e.g., backfill new columns with default values in `user` table]

## 6. API & Backend Changes

### Data Access Patterns
<!-- Describe how data will be accessed or modified -->
- [ ] [Data Access Pattern 1, e.g., **Mutations:** Server Actions in `app/actions/userProfile.ts` for all CRUD operations]
- [ ] [Data Access Pattern 2, e.g., **Queries:** A query function in `lib/userProfile.ts` to fetch user profiles]

### Server Actions
<!-- Describe any server actions that need to be implemented -->
- [ ] [Server Action 1, e.g., **`createUserProfile`**]
  - **Description:** Create a new user profile with the provided data.
  - **Parameters:** `name`, `email`, `bio`
  - **Return Value:** Newly created user profile object
- [ ] [Server Action 2, e.g., **`updateUserProfile`**]
  - **Description:** Update an existing user profile with the provided data.
  - **Parameters:** `userId`, `name`, `email`, `bio`
  - **Return Value:** Updated user profile object

### Database Queries
<!-- Provide example queries or mutations that will be used -->
- [ ] [Database Queries 1, e.g., **`lib/userProfile.ts`**]
  - **Function:** `getUserProfileById(userId: string): Promise<UserProfile>`
    - **Description:** Fetch a user profile by ID.
    - **Parameters:** `userId`
    - **Return Value:** User profile object
  - **Function:** `updateUserProfile(userId: string, data: Partial<UserProfile>): Promise<UserProfile>`
    - **Description:** Update an existing user profile with the provided data.
    - **Parameters:** `userId`, `data`
    - **Return Value:** Updated user profile object

### API Routes
<!-- List any new API routes that need to be created -->
- [ ] [API Route 1, e.g., **`/api/user/profile`**]
  - **Method:** `POST`
  - **Description:** Create a new user profile.
  - **Request Body:** `{ name: string, email: string, bio?: string }`
  - **Response:** `{ userProfile: UserProfile }`
- [ ] [API Route 2, e.g., **`/api/user/profile/:id`**]
  - **Method:** `GET`
  - **Description:** Fetch a user profile by ID.
  - **Response:** `{ userProfile: UserProfile }`

---

## 7. Frontend Changes

### New Components
<!-- List any new components that need to be created -->
- [ ] [**Component 1:**, e.g., **`components/UserProfile/`**]
  - `UserProfile.tsx`: Component for displaying user profile information.
  - `UserProfileForm.tsx`: Form for creating or updating user profiles.

### Page Updates
<!-- Describe any pages that need to be updated or created -->
- [ ] [**Page 1:**, e.g., **`app/(protected)/UserProfile/page.tsx`**]
  - **Description:** Page for viewing and editing user profiles.
  - **Components Used:** `UserProfile`, `UserProfileForm`
  - **Data Fetching:** Use `getUserProfileById` to fetch data on page load.
- [ ] [**Page 2:**, e.g., **`app/(protected)/UserProfile/edit.tsx`**]
  - **Description:** Page for editing user profiles.
  - **Components Used:** `UserProfileForm`
  - **Data Fetching:** Use `getUserProfileById` to pre-fill form with existing data.

---

## 8. Implementation Plan

### Phase 0: Database Schema
<!-- Describe the initial phase of the implementation -->
**Goal:** Set up the database schema to support the new features.

- [ ] [**Task 0.1:**, e.g., Create `lib/drizzle/schema/userProfile.ts` with the new user profile schema]
- [ ] [**Task 0.2:**, e.g., Run `npm run db:generate` to create the SQL migration files]

### Phase 1: Backend Logic
<!-- Describe the backend implementation phase -->
**Goal:** Implement the backend logic to support the new features.

- [ ] [**Task 1.1:**, e.g., Create `lib/userProfile.ts` with the `getUserProfileById` and `updateUserProfile` functions]
- [ ] [**Task 1.2:**, e.g., Create `app/actions/userProfile.ts` with `createUserProfile` and `updateUserProfile` server actions]

### Phase 2: Frontend UI
<!-- Describe the frontend implementation phase -->
**Goal:** Implement the frontend UI to interact with the backend.

- [ ] [**Task 2.1:**, e.g., Add a "User" link with a `user` icon to the main navigation in `app/(protected)/layout.tsx`]
- [ ] [**Task 2.2:**, e.g., Create the component structure in `components/UserProfile/`]
- [ ] [**Task 2.3:**, e.g., Implement the `UserProfile.tsx` and `UserProfileForm.tsx` components to display and edit user information]

### Phase 3: Integration
<!-- Describe the integration phase -->
**Goal:** Integrate the frontend and backend to ensure everything works together.

- [ ] [**Task 3.1:**, e.g., Modify the `POST` handler in `app/(protected)/UserProfile/page.tsx` to call the `createUserProfile` action]
- [ ] [**Task 3.2:**, e.g., Test the full `create`, `read`, `update`, and `delete` (CRUD) flow for user profiles]
