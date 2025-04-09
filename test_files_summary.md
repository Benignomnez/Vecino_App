# Test Files Summary

## API Tests

### `src/api/places.test.ts`
Tests for the Google Places API service functions:
- `fetchPlaceDetails`: Tests fetching place details by ID
- `fetchPlacePhotos`: Tests fetching place photos by reference
- `searchPlaces`: Tests searching for places by query and location
- Error handling: Tests for API errors and network failures

## Component Tests

### `src/components/PlaceDetails.test.tsx`
Tests for the PlaceDetails component:
- Rendering place information (name, address, rating, etc.)
- Photo gallery functionality
- Opening hours display
- Error handling for failed API calls
- Handling missing data gracefully

### `src/components/PlaceSearch.test.tsx`
Tests for the PlaceSearch component:
- Form rendering and validation
- Search submission functionality
- Location input handling
- Loading state during search
- Error handling for failed searches
- Results display

### `src/components/Button.test.tsx`
Tests for the basic Button component:
- Rendering with different variants
- Click event handling
- Disabled state

### `src/components/MuiButton.test.tsx`
Tests for the Material UI Button wrapper:
- Rendering with Material UI styling
- Variant and color prop handling
- Click event handling

### `src/components/CustomMuiButton.test.tsx`
Tests for the custom-styled Material UI Button:
- Custom styling application
- Prop forwarding
- Event handling

## Utility Tests

### `src/utils/formatters.test.ts`
Tests for utility formatting functions:
- Date formatting
- Currency formatting
- Address formatting
- Rating formatting
- Text truncation

## Sample Tests

### `src/sample.test.jsx`
Basic sample test to verify Jest configuration:
- Simple rendering test
- DOM interaction test 