# Sorting Visualizer

## Overview

The Sorting Visualizer is an interactive, web-based tool that allows users to observe and understand the internal workings of various sorting algorithms through animated visualizations. This project is aimed at students, educators, and anyone interested in algorithms, providing a visual representation of the sorting process. The visualizer supports multiple sorting algorithms, allowing users to see how each one operates on the same data set.

## Features

- **Dynamic Array Generation:** Users can generate a new random array of bars, each with varying heights, which represent different values to be sorted.
- **Multiple Sorting Algorithms:** The visualizer includes implementations of several popular sorting algorithms:
  - **Bubble Sort**
  - **Insertion Sort**
  - **Selection Sort**
  - **Merge Sort**
  - **Quick Sort**
- **Interactive Controls:**
  - **Size Slider:** Allows users to control the number of elements (bars) in the array. The slider ranges from 5 to 100 elements.
  - **Speed Slider:** Enables users to adjust the speed of the sorting visualization, with options ranging from 20ms to 300ms delay per operation.
- **Real-time Visualization:** The sorting process is animated, with bars changing colors to indicate which elements are being compared, swapped, or sorted.
- **Responsive Design:** The application layout adjusts seamlessly to different screen sizes, making it accessible on both desktop and mobile devices.

## Technologies Used

- **HTML5:** Provides the basic structure of the application.
- **CSS3:** Used for styling the application, creating the layout, and handling transitions during sorting.
- **JavaScript (ES6+):** The core logic for sorting algorithms, DOM manipulation, and handling user interactions is implemented in JavaScript.
- **Bootstrap 5:** Utilized for responsive design and styling, leveraging pre-built components and a grid system for layout management.

## Project Structure

```plaintext
sorting-visualizer/
├── index.html           # Main HTML file that loads the interface and scripts
├── style.css            # CSS file for custom styling and layout
├── sorting.js           # Contains utility functions and core logic for array generation and interaction
├── bubble.js            # Implementation of Bubble Sort algorithm
├── insertion.js         # Implementation of Insertion Sort algorithm
├── merge.js             # Implementation of Merge Sort algorithm
├── quick.js             # Implementation of Quick Sort algorithm
├── selection.js         # Implementation of Selection Sort algorithm
└── README.md            # Project documentation (this file)
```

## Detailed Explanation of Files

### 1. `index.html`

This file serves as the main entry point for the application. It sets up the structure of the web page, including the header, navigation, and the container for the sorting bars. It also includes links to external stylesheets (Bootstrap) and scripts (JavaScript files).

- **Header:** Contains the title of the application.
- **Navigation Bar:** Provides buttons for generating a new array, adjusting the size and speed, and selecting the sorting algorithm.
- **Bars Container:** The section where the array bars are dynamically generated and displayed.

### 2. `style.css`

This CSS file handles the visual styling of the application, including the layout, colors, and animations.

- **Key Classes:**
  - `.flex-container`: Manages the layout of the bars within the container, ensuring they are evenly spaced and aligned.
  - `.flex-item`: Applies styles to each bar, including width, height, and background color.
  - `.row`: Utilizes a grid layout for the header and controls, ensuring responsive behavior.

### 3. `sorting.js`

This JavaScript file contains the utility functions and event listeners that control the application's interactivity. It handles the creation and deletion of array bars, the dynamic adjustment of the array size and speed, and the enabling/disabling of buttons during sorting operations.

- **Functions:**
  - `createArray(noOfBars)`: Generates an array of random numbers and creates corresponding bars in the DOM.
  - `deleteChild()`: Clears the existing bars from the DOM before generating a new array.
  - `swap(el1, el2)`: A utility function to swap the heights of two bars, simulating the swapping of elements in an array.
  - `disableSortBtns() / enableSortBtns()`: Disables/enables sorting buttons to prevent user interaction during the sorting process.
  - `disableSize() / enableSize()`: Disables/enables the array size slider.
  - `disableNewArray() / enableNewArray()`: Disables/enables the "New Array" button.
  - `wait(milisec)`: Pauses execution for a specified duration to control the speed of animations.

### 4. `bubble.js`

Implements the Bubble Sort algorithm, which repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The algorithm continues until the list is sorted.

- **Visualization:**
  - Bars being compared are highlighted in a specific color.
  - Bars that are swapped are briefly shown in another color before reverting to their sorted state.

### 5. `insertion.js`

Implements the Insertion Sort algorithm, which builds the sorted array one item at a time by repeatedly taking the next item and inserting it into its correct position among the previously sorted elements.

- **Visualization:**
  - The current element being inserted is highlighted.
  - As elements are shifted to make space for the current element, they change color.
  - Once the element is correctly placed, it is highlighted in a sorted color.

### 6. `merge.js`

Implements the Merge Sort algorithm, a divide-and-conquer algorithm that recursively splits the array into halves, sorts each half, and then merges the sorted halves back together.

- **Visualization:**
  - The splitting process is visually indicated by changing the color of bars.
  - During merging, bars are shown as being merged back in a sorted order with distinct colors for different sections.

### 7. `quick.js`

Implements the Quick Sort algorithm, another divide-and-conquer algorithm that selects a 'pivot' element and partitions the array around the pivot, with all smaller elements moved before it and all larger elements moved after it.

- **Visualization:**
  - The pivot element is highlighted.
  - During partitioning, bars are colored based on their comparison with the pivot.
  - After partitioning, the pivot is shown in its final sorted position.

### 8. `selection.js`

Implements the Selection Sort algorithm, which repeatedly selects the smallest remaining element and swaps it with the current position.

- **Visualization:**
  - The current element being considered for swapping is highlighted.
  - After finding the minimum element in the remaining unsorted section, it is swapped into its correct position, with visual feedback showing the process.

## How to Use

### 1. Clone the Repository

Clone the project repository to your local machine using the following command:

```bash
git clone https://github.com/your-username/sorting-visualizer.git
```

### 2. Open the Project

Navigate to the project directory and open the `index.html` file in your preferred web browser:

```bash
cd sorting-visualizer
open index.html
```

### 3. Interact with the Visualizer

- **Adjust Array Size:** Use the size slider to increase or decrease the number of elements in the array. The visualizer will automatically update the display based on the selected size.
- **Adjust Speed:** Use the speed slider to control the animation speed of the sorting process.
- **Generate New Array:** Click the "New Array" button to create a new set of random bars to sort.
- **Choose a Sorting Algorithm:** Click on any sorting algorithm button (e.g., "Bubble Sort", "Quick Sort") to start the sorting animation for the current array.

### 4. Observe the Sorting Process

Watch as the bars change color and position, reflecting the internal steps of the chosen sorting algorithm. The bars will eventually be arranged in ascending order, with the sorted bars displayed in a consistent color.

## Contributing

Contributions to this project are welcome. If you have any ideas for new features, improvements, or bug fixes, feel free to submit a pull request or open an issue on the project's GitHub repository.

### Steps to Contribute

1. **Fork the Repository**
2. **Create a New Branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make Your Changes**
4. **Commit Your Changes**
   ```bash
   git commit -m "Add your message here"
   ```
5. **Push to Your Branch**
   ```bash
   git push origin feature/your-feature-name
   ```
6. **Open a Pull Request** on GitHub




For any inquiries, please reach out via email at [your-email@example.com](mailto:your-email@example.com) or open an issue on GitHub.

---

This README file provides a comprehensive overview of the Sorting Visualizer project, detailing its features, usage instructions, and project structure, making it easier for others to understand and contribute to the project.
