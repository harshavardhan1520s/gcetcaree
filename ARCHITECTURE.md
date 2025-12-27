# System Architecture Diagram

```mermaid
graph TD
    subgraph Frontend [React Frontend]
        S[Student UI]
        A[Admin Dashboard]
        ST[Staff Panel]
    end

    subgraph Backend [Node.js API]
        Auth[Auth Middleware]
        Comp[Complaint Controller]
        Dept[Dept Controller]
    end

    subgraph Database [SQLite DB]
        Users[(Users Table)]
        Comps[(Complaints Table)]
        Depts[(Departments Table)]
        Feed[(Feedback Table)]
    end

    S & A & ST --> Auth
    Auth --> Comp & Dept
    Comp --> Comps & Feed
    Dept --> Depts
```

## Database Schema (ER Summary)
- **Users**: 1 ---- N **Complaints** (Raised by)
- **Departments**: 1 ---- N **Complaints** (Assigned to)
- **Complaints**: 1 ---- 1 **Feedback** (Post-Resolution)
- **Departments**: 1 ---- N **Users** (Staff assigned to Dept)
