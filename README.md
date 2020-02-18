# WORK TASK #

**Please read this document thoroughly** and plan your work accordingly.
When ready, fork the repository and create a feature branch. It is in this branch we
expect your delivery.

This Work Task is divided into three parts:

### 1: CSS-wizardry ###


![alt text](https://raw.githubusercontent.com/hmfe/54321/master/button.png)

Recreate this button using only HTML/CSS and using as few HTML-elements as
possible. (HINT: It is possible to solve this using only one `<button>`)


* You can provide a solution for this separately or as a part of the solution for (3) *


### 2: Please answer the questions found in the link below ###
https://sv.surveymonkey.com/r/QCT8SHL

### 3: Implement a simple search application ###

<img src="https://raw.githubusercontent.com/hmfe/54321/master/search.png" style="width: 400px">
Implement a simple search form. The search should use a public REST API of your
choice using JavaScript.

- Search for title, return title (or something like that)
- Display partial search results in a list beneath the search field (Auto complete)
- Display the selected results in an editable list beneath the search component 

  * Selected search result should be saved with date/time stamp (as a
search history)
  * User should be able to delete a result from the list or delete the entire
list.

- The application should be responsive, adapting to changes of the viewport. 

### What we will look at: ###

- HTML5: Semantic markup, SEO optimization, Accessibility
   * Use HTML5 and show us that you have deep knowledge of semantic
markup.

- CSS3: Responsivity, use of pseudo elements, HTML entities and complexity
of solution
  * Surprise us with interesting solutions and show off your skills!
  * NOTE: Solution based on premade CSS frameworks will be completely discarded

- JS: complexity, sanity, comments and security.
  * The search should fetch data for each entry, don’t store a complete
database response in a variable and iterate through that.
  * Sanitize your inputs and don’t stress the API more than necessary.

- General sanity check on structure and solution
  * Show to us that you know - how front-end development should be
done.



When done, push your branch and let us know it’s done by making a pull request.

**Good Luck and have fun!**


## Solution

#### Available Scripts

1. `npm run start `
    - Runs the code in development mode.

2. `npm run build`
    - Builds the UI source code and stores the result in `build` folder

#### Components

1. `SearchComponent`
    - Component Type: Class Component 
    - Allows users to search places (cities / countries) using the Mapbox Places API.
    - Utilizes 'debounce' utility to control the API Requests Counts.
    - Contains auto-complete-suggestions component that gets rendered whenever there are suggestions available
    - Utilizes 'handleAPIError' utility to sanitize the API Response.

2. `LocationComponent`
   - Component Type: Functional Component
   - Renders the location parameters provided to the component in props.

3. `LoaderComponent`
   - Component Type: Functional Component
   - Pure CSS Loader inspired from https://loading.io/css

4. `SearchHistoryListComponent`
  - Component Type: Functional Component
  - Renders the search-history list provided to the component in props.
  - Dispatches clearHistory action to parent component for deleting a search-history-item.

5. `DeleteButton`
  - Delete button as per requirements set in the evaluation
  - Solution: `https://react-custom-delete.stackblitz.io`
  - Source Code: `https://stackblitz.com/edit/react-custom-delete`
  
   
#### Utils

1. `debounce`
    - Lightweight debounce functionality that takes the function to be executed as a callback arguement.
    - Another arguement to the debounce function is the timeout / delay after which the callback is required to     be executed. 

2. `handleAPIError`
    - Utility to parse Fetch API Responses for errors in response code
    - Enhances the error-handling capabilities of the component.abs

3. `hasClickedOutside`
    - Utility to check if 'clickevent' has occurred outside the DOM Node whose reference is passed as arguement     to the function.


### Notes:

1. The current application-funcationality is developed around the auto-complete feature keeping in mind the requirement. Hence the suggestions only popup when there is a 'change' in the input text. 
