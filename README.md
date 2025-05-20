# Local Tour Guide

The Local Tour Guide is a web-based application that provides AI-generated audio tours for any location. Users can search for a place or use their current location, and the application will find nearby points of interest using the Wikipedia API. It then leverages OpenAI's language (GPT) and text-to-speech (TTS) models to create an engaging audio tour script and narration. The application features an interactive map powered by Leaflet.js to display the location and points of interest.

## Features

- **Interactive Map**: Uses Leaflet.js to display an interactive map of the selected location and points of interest.
- **Location Search**: Allows users to search for a specific location or use their current geolocation.
- **Points of Interest (POIs)**: Fetches nearby POIs from Wikipedia based on the selected location and search radius.
- **AI-Generated Tour Scripts**: Utilizes OpenAI's GPT model to create engaging and informative tour scripts for the selected POIs.
- **Text-to-Speech (TTS) Audio**: Employs OpenAI's TTS model to generate natural-sounding audio narration for the tour script.
- **Customizable Tours**: Offers options to customize the tour length (brief, standard, detailed), select different voices, and provide custom instructions for the AI guide.
- **POI Information**: Displays images for POIs (when available from Wikipedia) and provides an embedded Wikipedia view for more details.
- **Audio Export**: Allows users to download the complete generated tour audio (all segments) as a single ZIP file.
- **Resizable Layout**: Features a resizable map and sidebar for user convenience.

## Setup and Usage

1.  **Clone the repository or download the files.**
2.  **Open `index.html`**: This project is a single HTML file application. Simply open the `index.html` file in a modern web browser (like Chrome, Firefox, Safari, or Edge).
3.  **Set API Key**:
    *   Upon first use, or if the API key is not set, you'll need to provide an OpenAI API key.
    *   Click the settings icon (⚙️) in the top right corner of the application.
    *   Enter your OpenAI API key in the modal dialog that appears.
    *   Click "Save". The key will be stored in your browser's local storage for future use.
4.  **Using the Application**:
    *   **Select a Location**:
        *   Use the search bar to find a location by name (e.g., "Eiffel Tower", "Kyoto, Japan").
        *   Click the "Use My Location" button to use your current geographical position (requires browser location permission).
        *   Alternatively, click directly on the map to select a point.
    *   **Adjust Radius**: Set the desired radius for finding Points of Interest (POIs) around your selected location using the slider.
    *   **View POIs**: Nearby POIs from Wikipedia will be listed in the sidebar. Images for some POIs will also be displayed.
    *   **Customize Tour (Optional)**:
        *   Choose the desired tour length (Brief, Standard, Detailed).
        *   Select a voice for the audio narration.
        *   Add custom instructions for the AI tour guide (e.g., "focus on history", "make it funny").
    *   **Generate Tour**: Click the "Create Tour Script" button. The AI will generate a script based on up to 5 nearby POIs and your customizations.
    *   **Start/Pause Tour**: Once the script and initial audio segment are ready, click "Start Guided Tour" to begin playback. The map will animate to each POI as it's discussed. You can pause/resume the tour.
    *   **Stop Tour**: Click "Stop Tour" to end the guided tour and reset the animation.
    *   **Export Audio**: After the tour script is generated and all audio segments are processed, you can click "Export Full Tour Audio (ZIP)" to download all audio segments.
    *   **View Wikipedia Details**: Click "Read More" on a POI or during the tour to see its Wikipedia page directly within the app.

## Technologies Used

-   **HTML5**: For the structure of the web application.
-   **CSS3**: For styling the user interface, including a responsive design with light/dark mode themes.
-   **JavaScript (ES6+)**: For all client-side logic, interactions, API calls, and dynamic content updates.
-   **Leaflet.js**: An open-source JavaScript library for interactive maps. Used to display locations and tour routes.
-   **OpenAI API**:
    -   **GPT Model (e.g., gpt-4.1-mini)**: For generating the textual content of the tour scripts.
    -   **TTS Model (e.g., gpt-4o-mini-tts)**: For converting the tour script segments into audible speech.
-   **Wikipedia API (MediaWiki API)**: Used to fetch geographically nearby points of interest (geosearch) and their details.
-   **Nominatim API (OpenStreetMap)**: Used for geocoding location search queries (converting place names to coordinates).
-   **JSZip**: A JavaScript library for creating, reading, and editing .zip files. Used for exporting the tour audio.
-   **No Backend/Server-Side Code**: The entire application runs in the user's browser.
-   **Browser Local Storage**: Used to store the OpenAI API key.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
