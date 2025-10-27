Fully responsive single-page application built using Vue 3, Vite, and SASS, showcasing clean UI components for Brooke Eagleeye’s golf journey.  

The site includes multiple sections such as About, Career, Partnerships, Techniques, Contact, and Footer - all modular and styled with scalable SASS architecture.


Additional Improvements - 

I implemented several enhancements to demonstrate advanced development skills.

I configured a global SASS setup so that all variables and mixins are automatically available across every component using Vite’s css.preprocessorOptions. I organized the styling with a modular SCSS architecture, splitting styles into partials such as _variables.scss, _mixins.scss, and _globals.scss, all imported through a single main.scss file for better maintainability.

To ensure visual consistency, I created reusable button and layout styles that are applied throughout the project. I also developed a custom @mixin respond() function to manage responsive breakpoints efficiently across mobile, tablet, and desktop devices.

For cleaner and more readable imports, I configured an alias (@) in the vite.config.js file. Each website section—About, Career, Partnership, Technique, Contact, and Footer—is structured as an isolated .vue component to promote clean and scalable component architecture.

Additionally, I established a global font and theme system, with all fonts and colors defined in _variables.scss for easy customization. Accessibility was also considered, ensuring that buttons and forms include hover states and proper labels to enhance usability.



Assumptions Made  - 

I assumed that the project is a static promotional website without a backend or database. All images are stored locally in the src/assets/images/ directory.




How to Run on a New Machine - 

1. Clone the repository by running the command:
git clone https://github.com/shani997/Brooke-Eagleeye.git

Then navigate into the project folder using:
cd golf-journey

2. Install all dependencies using the command:
npm install

3. Start the development server by running:
npm run dev

4. The site will then be available at http://localhost:5173
