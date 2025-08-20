# Family-directory
Family directory
# Family Directory Application

A web-based family directory application for managing family member information, relationships, and contact details.

## Features

- Create and join family directories with invite codes
- Add family members with comprehensive information
- Track relationships (spouses and significant others)
- Birthday and anniversary calendars
- Address directory
- Health notes and general notes
- Phone directory
- Export functionality to Word documents

## Database Setup

This application uses Supabase for data storage. You'll need to add the following column to your `family_members` table:

```sql
ALTER TABLE family_members ADD COLUMN significant_other_id UUID REFERENCES family_members(id);
