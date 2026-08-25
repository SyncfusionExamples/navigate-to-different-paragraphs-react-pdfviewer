# How to navigate to different paragraphs in a React PDF Viewer

A React application demonstrating how to navigate to different paragraphs in a PDF document using the [Syncfusion PDF Viewer](https://www.syncfusion.com/pdf-viewer-sdk/react-pdf-viewer) component. This sample showcases text search functionality, annotation highlighting, and programmatic navigation within PDF documents.

## How It Works

This application uses the Syncfusion PDF Viewer to demonstrate seamless navigation through PDF paragraphs. Here's how the functionality flows:

1. **Automatic PDF Load Detection** - When the PDF document loads in the viewer, the `documentLoad` event is triggered automatically. This event listener calls the `handleAutoSearch()` function to begin the search process for predefined paragraphs.

2. **Text Search Across Document** - The application searches for each predefined search term across the entire PDF document using the `findTextAsync()` method. This asynchronous function scans through all pages and returns all matching text locations with their exact bounds (x, y, width, height coordinates).

3. **Annotation Highlighting** - For each found text match, the application creates a highlight annotation on the corresponding page using `addAnnotation()`. These highlights are visually marked on the PDF with a unique ID, making them easily identifiable and selectable for navigation.

4. **Interactive Navigation Control** - Users can navigate between found paragraphs by either selecting from a dropdown list or using the "Next" button. When a paragraph is selected, the viewer automatically jumps to the correct page and highlights the text using `goToPage()` and `selectAnnotation()` methods.

## API Used

### Core Methods

- **`textSearch.findTextAsync(searchTerm, caseSensitive)`** - Asynchronously searches for text within the PDF document and returns an array of results with page indices and text bounds (coordinates).

- **`annotation.addAnnotation(type, options)`** - Adds an annotation (highlight, underline, etc.) to the PDF at specified bounds and page number. Accepts custom data to store search metadata for tracking.

- **`navigation.goToPage(pageNumber)`** - Navigates the PDF viewer to a specific page number, useful for jumping directly to pages containing search results.

- **`annotation.selectAnnotation(annotationId)`** - Programmatically selects an annotation by its ID, highlighting and focusing it in the viewer. Used to visually emphasize the current search result.

## Run the application

### Prerequisites

- **React**: Use React version 15.5.4 or higher.
- **Node.js**: Use Node.js version 14.0.0 or above. The compatible npm version is installed with Node.js. To verify your Node.js installation, run:

### Installation

Install dependencies:

```bash
npm install
```

### Development Server

Start the development server:

```bash
npm run dev
```

The application will be available at `http://localhost:5173` (or the port shown in your terminal).

### Build

Create an optimized production build:

```bash
npm run build
```

### Preview

Preview the production build locally:

```bash
npm run preview
```

## References
- [Getting Started With React PDF Viewer](https://help.syncfusion.com/document-processing/pdf/pdf-viewer/react/getting-started)
- [Text Search Features](https://help.syncfusion.com/document-processing/pdf/pdf-viewer/react/text-search/text-search-features)
- [Annotations in React PDF Viewer](https://help.syncfusion.com/document-processing/pdf/pdf-viewer/react/annotation/overview)
