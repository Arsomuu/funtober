# Contributing to Funtober

Thank you for your interest in contributing to **Funtober**, a collection of fun games and activities! We appreciate all contributions, whether you're adding new games, fixing bugs, improving features, or enhancing documentation.

Follow the guidelines below to ensure a smooth and successful contribution process.

## How to Contribute

### 1. Fork the Repository

- **Fork** the repository to your GitHub account.
- Clone your forked repository:
  ```bash
  git clone https://github.com/your-username/funtober.git
  cd funtober
  ```

### 2. Install Dependencies

- This project is built using **Vite**, **React**, and **TypeScript**, so you'll need to install the necessary dependencies:
  ```bash
  npm install
  ```

### 3. Create a New Branch

- Always create a new branch for your changes, named descriptively after the feature or issue you're working on:
  ```bash
  git checkout -b add-new-game-feature
  ```

### 4. Project Structure

```funtober/
├── src/
├── assets/          # Game thumbnails and images
│   └── index.ts     # Image exports
├── components/      # Reusable React components
├── data/
│   └── funtober/    # Game configurations
│       └── index.ts
├── pages/          # Page components
└── App.tsx         # Main routing
```

### 5. Adding a New Game or Activity

**Step 1: Create the Thumbnail**

 - Use an image generator like **Freepik AI** to create the   thumbnail
 - **Requirements**:
   - Include the game name in large, bold font
   - Maintain consistent style with existing thumbnails
   - Recommended size: 300x200px


 - **Save** the thumbnail in src/assets/
   - Update src/assets/index.ts:

 **typescript**
 ``` export { default as YourGameThumbnail } from './your-game-thumbnail.png';```

**Step 2: Add Game Data**

 - Navigate to src/data/funtober/index.ts
 - Add your game object:

 typescript
 ``{
  id: "your-game-id",
  title: "Your Game Title",
  description: "Brief engaging description",
  thumbnail: YourGameThumbnail,
  price: 1000000, // if applicable
  category: "games" // or appropriate category
  } ```  
  
 **Step 3:  Create Game Component**

 - Create new component in src/components/games/
 - Follow TypeScript best practices:

 typescript

    import React from 'react';
    interface Props {// Define props}
    const YourGame: React.FC<Props> = ()=> {
    return (
      // Game implementation
    );
    };
    export default YourGame;```

**Step 4: Add Routing**

-Update App.tsx with your game route:

typescript
```<Route path="/games/your-game" element={<YourGame />} />```

### 6. Testing Your Changes

Run the development server:

bash
```npm run dev```

-Verify:

  -Game loads correctly
  -All features work as expected
  -No console errors
  -Responsive design works
  -No conflicts with existing games

### 7. Commit Your Changes

- Use clear, descriptive commit messages:

  bash
  ```git commit -m "feat: add new game 'Your Game Name'"```

### 8. Push Your Changes

bash 
```git push origin add-new-game-feature```

### 9. Open a Pull Request

- Create a PR to the main repository
- Include:
   - Clear title and description
   - Screenshots/GIFs of the new game
   - Link related issues
   - Tag relevant reviewers

### 10. Code Review Process

 - Be responsive to feedback
 - Make requested changes promptly
 - Update your PR as needed
 - Once approved, your contribution will be merged

 ## Code Style Guidelines

 **TypeScript**

   - Use strict typing avoid ```any```
   - Define interfaces for all props and state
   - Use functional components with hooks

 **Component Structure**

  - Keep components focused and single-purpose
  - Use descriptive names
  - Follow established patterns in existing code

 **CSS/Styling**

  - Use consistent naming conventions
  - Maintain responsive design
  - Follow existing color schemes and styles

 **Reporting Issues**

  - Use the Issues tab
   Include:
   - Clear description
   - Steps to reproduce
   - Expected vs actual behavior
   - Screenshots if applicable
   - Browser/environment details


**Getting Help**
  - Open an issue for questions
  - Tag maintainers for urgent matters
  - Check existing issues and documentation first

**Code of Conduct**
- By participating in this project, you agree to follow our Code of Conduct. We strive to maintain a welcoming and inclusive community.
Thank you for contributing to Funtober! Your efforts help make this project better for everyone.
