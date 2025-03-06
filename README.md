Here’s how you can set it up:

### 1. **Create the React TypeScript Project with Yarn:**

```bash
yarn create react-app getting-started --template typescript
```

### 2. **Navigate to the Project Folder:**

```bash
cd getting-started
```

### 3. **Install Tailwind CSS v3.4.17:**

To install a specific version of Tailwind CSS, use the following command:

```bash
yarn add tailwindcss@3.4.17 postcss autoprefixer
```

### 4. **Set Up Tailwind CSS Configuration Files:**

Generate the `tailwind.config.js` and `postcss.config.js` files.

```bash
npx tailwindcss init
```

This will generate the `tailwind.config.js` file. You can keep the default configuration or adjust it later.

### 5. **Configure the Tailwind Directives in Your CSS:**

In the `src` folder, create a file called `index.css` (if not already present), or modify it to include the following:

```css
/* src/index.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Make sure this file is imported in your `src/index.tsx`:

```tsx
import './index.css';
```

### 6. **Configure the Tailwind `content` Option:**

In `tailwind.config.js`, ensure the `content` array includes the paths to your React components:

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    './src/**/*.{js,jsx,ts,tsx}',  // Ensure this includes your files with React components
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### 7. **Start the Development Server:**

Now, start your development server to see if everything is working fine.

```bash
yarn start
```

Sure! Here's a simple component you can create in `App.tsx` to verify if Tailwind CSS is working properly:

### Step 1: **Modify `App.tsx`**

Open `src/App.tsx` and modify it to look like this:

```tsx
import React from 'react';
import './App.css';
const App: React.FC = () => {
  return (
    <div className="App">
      <header className="App-header">
        <h1 className="text-4xl font-bold text-blue-500">
          Tailwind CSS is working!
        </h1>
        <p className="text-xl text-gray-700 mt-4">
          This is a simple test to check if Tailwind CSS is applied correctly.
        </p>
        <button className="mt-6 px-4 py-2 bg-green-500 text-white rounded-lg hover:bg-green-700">
          Tailwind Button
        </button>
      </header>
    </div>
  );
}

export default App;
```

### Step 2: **Check the Output**

Now, go back to your terminal and make sure the development server is running with:

```bash
yarn start
```
