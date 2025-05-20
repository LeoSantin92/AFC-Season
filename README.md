# AFC Soccer Planner - README

## Overview

AFC Soccer Planner is a comprehensive web application designed for soccer coaches to manage training exercises, create age-specific development plans, and implement structured season planning following tactical periodization principles. The application faithfully reproduces the functionality of the Excel-based Season Planner workbook in a more accessible and collaborative web format.

## Features

- **Exercise Database**: Create, manage, and organize training exercises by category, age group, and focus area
- **Age Group Management**: Configure multiple age groups with specific parameters, session durations, and development priorities
- **Season Planning Hierarchy**:
  - Macrocycles (full season plans)
  - Mesocycles (4-6 week blocks)
  - Weekly plans with specific objectives
  - Session templates with progressive/regressive structures
- **Time Distribution**: Track and manage time allocation across technical, tactical, physical, and psychosocial components
- **Color-Coded Visualization**: Visual representation of season phases, categories, and priorities

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Firebase account (for database and authentication)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/afc-soccer-planner.git
cd afc-soccer-planner
```

2. Install dependencies:
```bash
npm install
```

3. Create a Firebase project:
   - Go to [Firebase Console](https://console.firebase.google.com/)
   - Create a new project
   - Set up Firestore Database
   - Enable Authentication (Email/Password)
   - Create a web app in your Firebase project
   - Copy the Firebase configuration

4. Create a `.env` file in the root directory with your Firebase configuration:
```
REACT_APP_FIREBASE_API_KEY=your-api-key
REACT_APP_FIREBASE_AUTH_DOMAIN=your-auth-domain
REACT_APP_FIREBASE_PROJECT_ID=your-project-id
REACT_APP_FIREBASE_STORAGE_BUCKET=your-storage-bucket
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=your-messaging-sender-id
REACT_APP_FIREBASE_APP_ID=your-app-id
```

5. Start the development server:
```bash
npm start
```

## Usage Guide

### Exercise Database

1. Navigate to the "Exercises" section from the main menu
2. Click "Create New Exercise" to add a new training activity
3. Fill in the exercise details:
   - Name, category, and subcategory
   - Age groups
   - Objectives and description
   - Setup instructions and coaching points
   - Upload images if available
4. Save the exercise to add it to your database
5. Use the search and filter options to find exercises by category, age group, or keyword

### Age Group Management

1. Navigate to the "Age Groups" section from the main menu
2. Click "Create New Plan" to set up a new age group
3. Configure the age group parameters:
   - Age group (U4, U6, U7-U8, etc.)
   - Session duration (automatically set based on AFC-Huntsville guidelines)
   - Number of players and sessions per week
   - Time distribution across technical, tactical, physical, and psychosocial components
   - Season objectives for each component
4. Save the age group plan to proceed to season planning

### Season Planning

1. From the Age Group overview, click "Create Season Plan"
2. Define the macrocycle (full season):
   - Set season start and end dates
   - Define season phases (pre-season, early season, mid-season, etc.)
   - Set overall season goals for each component
3. Create mesocycles (4-6 week blocks):
   - Define focus areas and objectives
   - Adjust time distribution if needed
4. Create weekly plans:
   - Set specific objectives for the week
   - Define session structure for each training day
5. Design individual sessions:
   - Choose session type (Progressive, Progressive-Regressive, Regressive)
   - Select exercises from the database
   - Adjust timing and focus areas

## AFC-Huntsville Methodologies

The application incorporates key AFC-Huntsville methodologies:

1. **Holistic Player Development**: Addressing physical, technical, tactical, psychological, and social dimensions
2. **Tactical Periodization**: Using Morphocycle as weekly learning plan, considering four game moments
3. **Constraints-Led Approach**: Using environment, task, and performer constraints to develop problem-solving skills
4. **Session Types**:
   - Progressive: Building up complexity
   - Progressive-Regressive: Building up then reducing complexity
   - Regressive: Starting complex and simplifying

## Customization

### Adding New Exercise Categories

1. Modify the `categoryOptions` and `subcategoryOptions` in `ExerciseForm.js`
2. Update the corresponding styles in `ExerciseStyles.css`

### Modifying Age Group Parameters

1. Update the default session durations in `AgeGroupPlanModel.js`
2. Adjust the color coding in `AgeGroupStyles.css`

### Extending Season Planning Features

1. Add new phase types in `MacrocycleModel.js`
2. Modify session structures in `SessionPlanModel.js`

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- AFC-Huntsville Soccer Club for the methodologies and requirements
- Original Excel Season Planner creators for the foundational logic
