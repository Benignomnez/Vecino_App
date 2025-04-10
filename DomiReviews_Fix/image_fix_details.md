# Image Display Fix for Mobile Mockup

## Issue Description
The mobile mockup in the VecinoApp was displaying broken or missing images because hardcoded placeholder URLs from "placekitten.com" were being used instead of proper API calls.

## Solution Implemented
The fix involved replacing hardcoded image URLs with proper API calls to the application's `/api/places/generic-image` endpoint.

### Changes Made:
1. Replaced main featured restaurant image URL:
```diff
<CardMedia
  component="img"
  height="120"
- image="https://placekitten.com/400/200"
+ image={`/api/places/generic-image?query=${encodeURIComponent("Restaurante El Conuco Dominicano")}&cache=true`}
  alt="Restaurant"
  sx={{
    objectFit: "cover",
    transition: "transform 0.5s ease",
    "&:hover": {
      transform: "scale(1.05)",
    },
  }}
/>
```

2. Updated nearby places image URLs:
```diff
{
  name: "Adrian Tropical",
- img: "https://placekitten.com/200/100",
+ img: `/api/places/generic-image?query=${encodeURIComponent("Adrian Tropical Restaurant Santo Domingo")}&cache=true`,
  type: "Comida Caribeña",
  rating: 4.6,
},
{
  name: "Jalao",
- img: "https://placekitten.com/201/100",
+ img: `/api/places/generic-image?query=${encodeURIComponent("Jalao Restaurant Dominicano")}&cache=true`,
  type: "Dominicano",
  rating: 4.8,
},
{
  name: "Mesón de Bari",
- img: "https://placekitten.com/202/100",
+ img: `/api/places/generic-image?query=${encodeURIComponent("Mesón de Bari Restaurant Santo Domingo")}&cache=true`,
  type: "Mediterráneo",
  rating: 4.7,
},
```

## Benefits
- Images now load consistently in the mobile mockup
- Application uses a consistent approach for loading images
- Fixed potential external dependency on placekitten.com
- Improved user experience with relevant restaurant images 