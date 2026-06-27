EF Core ModelSnapshot → ERD Diagram Generator
A single-file HTML tool that reads your Entity Framework Core ModelSnapshot.cs file and generates an interactive Entity-Relationship Diagram (ERD) — complete with entities, properties, types, and relationships.

✨ Features
📁 Folder-based input — Select your .NET project root folder; it automatically navigates to Infrastructure/Migrations/ and finds the *ModelSnapshot.cs file

🔍 Smart parser — Extracts all entities, properties with their actual C# types, and relationships from EF Core's HasOne(...).WithMany(...).HasForeignKey(...) configurations

🧹 Clean output — Filters out boilerplate properties (Version, ModifyDate, CreatorUserId, CreateDate) so your diagram stays focused

🎨 Professional PlantUML output — Generates a .puml file with entities grouped by aggregate, PK fields marked with *, proper ||--o{ relationship notation, and clean styling

🖼️ Live diagram preview — Renders the diagram directly in the browser via Kroki.io (no Java or local tools required)

🔎 Zoom controls — Dedicated +/−/⊡ buttons for zooming; mouse wheel scrolls naturally

💾 Export options — Download the diagram as PNG or the source as .puml file

🚀 How to Use
Open erd-generator.html in Chrome or Edge (required for File System Access API)

Click "Select Project Root" and choose your .NET solution folder

Click "Generate Diagram"

The ERD renders instantly — zoom, scroll, and explore your database schema

Download as PNG or .puml as needed
