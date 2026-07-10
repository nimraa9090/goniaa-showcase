# System Architecture

The Goniaa ecosystem follows a modern, decoupled architecture centered around a unified Supabase backend.

```mermaid
graph TD
    subgraph Client_Layer [Client Layer]
        Web[Next.js Storefront]
        Mobile[Expo Mobile App]
        Admin[Next.js Admin Dashboard]
        AI_Dash[AI Brand Manager]
    end

    subgraph Backend_Layer [Backend Layer - Supabase]
        Auth[Supabase Auth]
        DB[(PostgreSQL)]
        Storage[S3-Compatible Storage]
    end

    subgraph AI_Integration [AI & External Services]
        Gemini[Google Gemini AI]
        WA[WhatsApp API]
        Social[Social Media APIs]
    end

    %% Connections
    Web <--> Auth
    Web <--> DB
    Web <--> Storage

    Mobile <--> Auth
    Mobile <--> DB
    Mobile <--> Storage

    Admin <--> Auth
    Admin <--> DB
    Admin <--> Storage

    AI_Dash <--> Auth
    AI_Dash <--> DB
    AI_Dash <--> Gemini
    AI_Dash <--> WA
    AI_Dash <--> Social

    %% Styling
    style Client_Layer fill:#f9f,stroke:#333,stroke-width:2px
    style Backend_Layer fill:#bbf,stroke:#333,stroke-width:2px
    style AI_Integration fill:#dfd,stroke:#333,stroke-width:2px
```

## Data Flow Highlights
1.  **Authentication:** Centralized via Supabase Auth across all platforms.
2.  **Product Updates:** Admin Dashboard modifies PostgreSQL, which triggers real-time updates in the Storefront and Mobile App.
3.  **AI Workflow:** The Brand Manager fetches data from DB, processes it via Gemini AI for content generation, and schedules it back to the Content Calendar.
4.  **Asset Management:** All media (product images, banners, content) is routed through a standardized Image Service to Supabase Storage.
