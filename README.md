# Nextjs-Practice

* Create a next project using the following command---->
 `npm install next@latest react@latest react-dom@latest`
 
 * Add the following script to the package.json file----->
 `"scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint"
  }`
  
  * Create an app folder on the root level and it should contain a rootlayout.js file, and this file should have `HTML` and `body` tags with prop `children` and another file with the name page.js to create or make UI.

* Run your application with the command `npm run dev`.
* We can't directly import server components inside client components we can use server components as props inside client components.
* The App Router takes priority over the Pages Router. Routes across directories should not resolve to the same URL path and will cause a build-time error to prevent a conflict.

# Component Hierarchy:
The React components defined in special files of a route segment are rendered in a specific hierarchy:
* 1. layout.js
* 2. template.js
* 3. error.js (React error boundary)
* 4. loading.js (React suspense boundary)
* 5. not-found.js (React error boundary)
* 6. page.js or nested layout.js

# Styling
CSS can be added using `CSS Module` like app/folder/style.module.css or using `GLobal CSS` as app/global.css.

# Routing :
A file-system-based router built on top of Server Components that support layouts, nested routing, loading states, error handling, and more.
* Good to know: The App Router takes priority over the Pages Router. Routes across directories should not resolve to the same URL path and will cause a build-time error to prevent a conflict.
* Folders are used to define routes. A route is a single path of nested folders, following the file-system hierarchy from the root folder down to a final leaf folder that includes a page.js file. Files are used to create UI.

## Page :
* Pages are Server Components by default but can be set to a Client Component. They are used to create UI and A page.js file is required to make a route segment publicly accessible.
##  Layouts
* A layout is UI that is shared between multiple pages. On navigation, layouts preserve state, remain interactive, and do not re-render.
* Layouts are Server Components by default but can be set to a Client Component.
* The topmost layout is called the Root Layout. This required layout is shared across all pages in an application. Root layouts must contain `html` and `body` tags.
* Passing data between a parent layout and its children is not possible.
