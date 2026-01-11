# AccessibilityHub

A comprehensive web application designed to remove barriers and increase accessibility for people with vision and hearing disabilities. Built for educational and social value as a software development competition project.

## Project Overview

AccessibilityHub provides four main features to enhance accessibility:

1. **Speech to Text** - Real-time speech recognition that converts spoken words into written text
2. **Text to Speech** - Natural-sounding voice synthesis with customizable voice, speed, and pitch
3. **Image Description** - Automatic generation of descriptive text for images
4. **Audio Visualizer** - Visual representation of audio through frequency spectrum and volume indicators

## Technology Stack

- **Frontend**: React 18 with TypeScript
- **Styling**: Tailwind CSS with custom accessibility themes
- **Database**: Supabase (PostgreSQL)
- **Build Tool**: Vite
- **Icons**: Lucide React

## File Structure

```
project/
├── src/
│   ├── components/           # Reusable UI components
│   │   ├── Button.tsx        # Accessible button component
│   │   ├── Card.tsx          # Card container component
│   │   ├── FeatureCard.tsx   # Feature selection cards
│   │   └── SettingsPanel.tsx # Accessibility settings panel
│   │
│   ├── context/              # React context providers
│   │   ├── AccessibilityContext.tsx  # Manages accessibility settings
│   │   └── AppContext.tsx            # Manages app-level state
│   │
│   ├── features/             # Main feature components
│   │   ├── SpeechToText.tsx      # Speech recognition feature
│   │   ├── TextToSpeech.tsx      # Text-to-speech feature
│   │   ├── ImageDescription.tsx   # Image description feature
│   │   └── AudioVisualizer.tsx    # Audio visualization feature
│   │
│   ├── hooks/                # Custom React hooks
│   │   ├── useAccessibilitySettings.ts  # Hook for managing settings
│   │   └── useSpeechRecognition.ts      # Hook for speech recognition
│   │
│   ├── lib/                  # Utility libraries
│   │   ├── supabase.ts       # Supabase client setup
│   │   └── accessibility.ts  # Accessibility helper functions
│   │
│   ├── types/                # TypeScript type definitions
│   │   └── index.ts          # Main type definitions
│   │
│   ├── App.tsx               # Main application component
│   ├── main.tsx              # Application entry point
│   └── index.css             # Global styles with accessibility themes
│
├── index.html                # HTML entry point
├── package.json              # Project dependencies
├── tailwind.config.js        # Tailwind configuration
├── tsconfig.json             # TypeScript configuration
└── vite.config.ts            # Vite configuration
```

## Accessibility Features

### Built-in Accessibility Settings
- **Theme Selection**: Light, Dark, and High Contrast modes
- **Text Size Control**: Small, Medium, Large, and Extra Large options
- **High Contrast Mode**: Enhanced color contrast for better visibility
- **Large Text Mode**: Increases default text size across the app
- **Screen Reader Mode**: Optimized for screen reader users
- **Reduced Motion**: Minimizes animations for users sensitive to motion

### ARIA Support
- Proper ARIA labels and roles throughout the application
- Live regions for dynamic content updates
- Screen reader announcements for important actions
- Keyboard navigation support for all interactive elements

### Visual Design
- Clear focus indicators on all interactive elements
- Sufficient color contrast ratios
- Responsive design that works across all devices
- Clean, uncluttered interface with clear visual hierarchy

## Database Schema

### Tables

1. **accessibility_settings** - Stores user accessibility preferences
2. **transcriptions** - Saves speech-to-text transcriptions
3. **image_descriptions** - Stores image descriptions
4. **saved_content** - General content storage for user saves

All tables have Row Level Security (RLS) enabled with public access policies for guest users.

## Key Features Implementation

### Speech to Text
- Uses Web Speech API for real-time speech recognition
- Displays both final and interim transcriptions
- Allows saving, copying, and speaking back transcribed text
- Provides helpful tips for optimal results

### Text to Speech
- Uses Web Speech Synthesis API
- Customizable voice selection
- Adjustable speech rate (0.5x - 2x)
- Adjustable pitch (0.5 - 2)
- Sample texts for quick testing

### Image Description
- Drag-and-drop or click-to-upload interface
- Multiple image support
- Generated descriptions can be read aloud
- Saves descriptions to database

### Audio Visualizer
- Real-time audio level display
- 32-band frequency spectrum visualization
- Color-coded volume indicators (green/yellow/red)
- Helpful for hearing-impaired users to detect sounds

## Development

### Prerequisites
- Node.js 18 or higher
- npm or yarn

### Installation
```bash
npm install
```

### Running in Development
The development server starts automatically.

### Building for Production
```bash
npm run build
```

## Competition Project Goals

This project demonstrates:
- **Technical Excellence**: Clean architecture, TypeScript, modern React patterns
- **Problem-Solving**: Innovative solutions for accessibility challenges
- **Communication**: Clear UI/UX with helpful guidance and feedback
- **Collaboration**: Well-organized codebase that's easy to understand and extend
- **Social Value**: Real-world impact for people with disabilities

## Educational Value

This project teaches:
- Web accessibility best practices (WCAG guidelines)
- Browser APIs (Web Speech API, MediaStream API, Web Audio API)
- Modern React development patterns
- TypeScript for type-safe development
- Database design with Supabase
- Responsive design with Tailwind CSS

## Social Impact

AccessibilityHub directly addresses barriers faced by people with:
- **Vision Disabilities**: Text-to-speech, proper ARIA support, high contrast modes
- **Hearing Disabilities**: Speech-to-text transcription, audio visualization

All features work directly in the browser with no external API calls, ensuring privacy and accessibility even in offline scenarios.

## Future Enhancements

Potential areas for expansion:
- Real-time video captioning
- Sign language translation
- Voice command navigation
- Collaboration features for real-time transcription sharing
- AI-powered image description improvements
- Multi-language support
- Mobile app versions