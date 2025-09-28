# CinePedia: A Personal Film Catalog

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/Sidshot/generated-app-20250928-090722)

CinePedia is a minimalist, single-page, client-side application designed as a personal film catalog. It operates entirely within the browser without needing a backend. The application loads a large, predefined list of films from an embedded JSON dataset. The user interface is clean and functional, featuring a sticky header with comprehensive controls and a main content area that displays films in a responsive grid. Key functionalities are powered by vanilla JavaScript and include: full-text search across titles, original titles, and directors; filtering by specific year or director; sorting by various criteria (year, title, etc.); and pagination for handling the large dataset. The UI also supports a dark/light theme toggle and a compact/default density view. A standout feature is its local data persistence: users can add new films, import additional films from a CSV file, and edit any entry's details or add personal notes. All user-generated additions and modifications are saved directly to the browser's localStorage, making it a personalized and offline-first cataloging tool.

## Key Features

- **Entirely Client-Side:** No backend required. Runs completely in the browser from a single HTML file.
- **Powerful Search & Filter:** Instant full-text search, plus dropdowns to filter by year and director.
- **Advanced Filtering:** Show films with both links, missing links, or no year.
- **Flexible Sorting:** Sort the catalog by year, title, original title, or director.
- **Local Data Persistence:** Add new films, import from CSV, and edit any entry. All changes are saved to your browser's `localStorage`.
- **Personal Notes:** Add custom notes to any film for personal annotations.
- **Customizable UI:** Toggle between dark/light themes and default/compact grid views.
- **Pagination:** Efficiently browse a large collection with simple page controls.
- **Responsive Design:** A clean and modern interface that works flawlessly on all devices.
- **Keyboard Shortcuts:** Use `/` to focus the search bar and `Esc` to clear it.

## Technology Stack

This project is intentionally minimalist and built with fundamental web technologies:

- **HTML:** Provides the structure of the application.
- **CSS:** Handles all styling, including themes, responsiveness, and animations.
- **Vanilla JavaScript:** Powers all application logic, from data manipulation to UI interactions.

The application is self-contained in a single `index.html` file and has no build process or external framework dependencies for its core functionality.

## Getting Started

To run this project locally, you will need `bun` installed.

### Installation

1.  Clone the repository to your local machine:
    ```bash
    git clone <repository-url>
    cd cinepedia_film_catalog
    ```

2.  Install the development dependencies (for the local server):
    ```bash
    bun install
    ```

### Running Locally

Start the local development server:

```bash
bun dev
```

The application will be available at `http://localhost:3000` (or another port if 3000 is in use).

## Usage

- **Search:** Use the search bar at the top to instantly filter films by title, original title, or director.
- **Filter & Sort:** Use the dropdown menus to narrow down the catalog by year or director, and to change the sorting order.
- **Add a Film:** Click the "Add film" button to open a modal where you can manually enter the details of a new movie.
- **Import Data:** Click the "Import CSV" button to select a CSV file from your computer and bulk-add films to your catalog.
- **Edit a Film:** Click the "Edit" button on any film card to modify its details or add personal notes. All changes are saved automatically.
- **Toggle View:** Use the theme and density buttons to switch between light/dark modes and default/compact views.

## Deployment

This project is a static single-page application and can be deployed to any static hosting service. It is optimized for Cloudflare Pages.

### Deploy with Cloudflare

You can deploy this project to Cloudflare Pages with a single click.

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/Sidshot/generated-app-20250928-090722)

### Manual Deployment

1.  Ensure you have the Cloudflare `wrangler` CLI installed and configured.
2.  Build the application (though for this static project, this step is not strictly necessary as there is no build process).
3.  Deploy the project using the following command:
    ```bash
    bun run deploy
    ```

## Known Limitations

- **Local Storage Only:** All user-added data and edits are stored in the browser's `localStorage`. This data is not synced across devices and will be lost if the browser data is cleared.
- **Performance:** The entire film dataset is loaded into memory on startup. While performant for the current dataset size, extremely large collections could impact initial load time.
- **Monolithic Structure:** The application is contained within a single file, which simplifies deployment but makes complex feature development and maintenance more challenging.