## Script: Audit Server-Level Permissions with Grant Statements

**Description**:
This script retrieves all server-level permissions assigned in SQL Server, along with the grantee, grantor, permission type, and a dynamically generated `GRANT`/`DENY`/`REVOKE` statement for each. It is ideal for auditing, documenting, or scripting out permissions when migrating server-level security.

**What It Shows**:
- Grantee name and type
- Grantor name
- Permission type and state (`GRANT`, `DENY`, `REVOKE`)
- Class and scope of permission
- Auto-generated T-SQL grant syntax (`GRANT CONTROL SERVER TO [login]`, etc.)

**Use Case**:
- Audit current server-level security
- Generate GRANT scripts for backup or migration
- Verify who has `CONTROL SERVER`, `VIEW ANY DATABASE`, etc.

**Requirements**:
- SQL Server 2005 or later
- `VIEW SERVER STATE` permission (or `sysadmin`)

**Notes**:
- This only covers **server-level permissions**, not database-level.
- Consider running this regularly and storing snapshots for auditing over time.
