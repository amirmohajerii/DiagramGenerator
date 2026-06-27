# EF Core ModelSnapshot → ERD Diagram Generator

A single-file HTML tool that reads your Entity Framework Core `ModelSnapshot.cs` file and generates an interactive **Entity-Relationship Diagram (ERD)** — complete with entities, properties, types, and relationships.

## ✨ Features

- **📁 Folder-based input** — Select your .NET project root folder; it automatically navigates to `Infrastructure/Migrations/` and finds the `*ModelSnapshot.cs` file
- **🔍 Smart parser** — Extracts all entities, properties with their actual C# types, and relationships from EF Core's `HasOne(...).WithMany(...).HasForeignKey(...)` configurations
- **🧹 Clean output** — Filters out boilerplate properties (`Version`, `ModifyDate`, `CreatorUserId`, `CreateDate`) so your diagram stays focused
- **🎨 Professional PlantUML output** — Generates a `.puml` file with entities grouped by aggregate, PK fields marked with `*`, proper `||--o{` relationship notation, and clean styling
- **🖼️ Live diagram preview** — Renders the diagram directly in the browser via Kroki.io (no Java or local tools required)
- **🔎 Zoom controls** — Dedicated +/−/⊡ buttons for zooming; mouse wheel scrolls naturally
- **💾 Export options** — Download the diagram as **PNG** or the source as **.puml** file

## 🚀 How to Use

1. Open `erd-generator.html` in **Chrome** or **Edge** (required for File System Access API)
2. Click **"Select Project Root"** and choose your .NET solution folder
3. Click **"Generate Diagram"**
4. The ERD renders instantly — zoom, scroll, and explore your database schema
5. Download as PNG or `.puml` as needed

## 📋 Requirements

- A modern browser with **File System Access API** support (Chrome 86+, Edge 86+)
- Internet connection (uses Kroki.io for PlantUML rendering)
- A .NET project with EF Core migrations at `Infrastructure/Migrations/*ModelSnapshot.cs`

## 🖼️ Example Output

The generated diagram uses PlantUML's `left to right` layout with `ortho` lines, white-background entities, and clean relationship notation — perfect for documentation, code reviews, or schema discussions.

## 🛠️ Tech Stack

- Vanilla JavaScript (no frameworks, no build tools)
- File System Access API for folder selection
- [Kroki.io](https://kroki.io) for server-side PlantUML rendering
- Single-file HTML — just download and open

## 📸 Screenshot

<!-- Add a screenshot of your generated diagram here -->
<!-- ![ERD Diagram Screenshot](screenshot.png) -->
