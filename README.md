# Fract-ol Project Guide

This guide provides a step-by-step plan to complete the Fract-ol project over 10 days.

---

## Day 0: Setup and Preparation

1. **Install and Set Up MiniLibX:**
   - Install MiniLibX (refer to 42 documentation for your system).
   - Test MiniLibX by creating a basic window.

2. **Setup Your Development Environment:**
   - Create a directory structure (e.g., `src`, `include`, `lib`).
   - Initialize a `Makefile` for compiling your project.

3. **Research:**
   - Read about the Mandelbrot set and Julia set.
   - Familiarize yourself with complex numbers (real and imaginary parts).

---

## Day 1: Create a Window

1. **Create a Basic Window:**
   - Open a window using MiniLibX (`mlx_init`, `mlx_new_window`).
   - Display a plain color to verify you can manipulate the window.

2. **Display Pixels:**
   - Write a function to draw individual pixels (`mlx_pixel_put`).
   - Test by drawing a simple pattern or diagonal line.

---

## Day 2: Map Pixels to Mathematical Coordinates

1. **Understand Screen-to-Math Mapping:**
   - Your screen has pixel coordinates (e.g., 800x600).
   - Map these to mathematical coordinates for fractals (e.g., −2 to 2 for real and imaginary parts).
   - Use formulas like:
     ```
     real_part = min_real + x * (max_real - min_real) / width
     imag_part = min_imag + y * (max_imag - min_imag) / height
     ```

2. **Verify Mapping:**
   - Output mathematical values for a few pixels to confirm correctness.

---

## Day 3: Render the Mandelbrot Set

1. **Implement the Mandelbrot Formula:**
   - For each pixel:
     - Start with `Z = 0` and `C = mapped pixel coordinates`.
     - Iterate `Z = Z^2 + C`.
     - Track the number of iterations until `|Z| > 2` or a maximum iteration count is reached.

2. **Set Pixel Colors:**
   - Use iteration count to determine the color (e.g., more iterations = brighter color).

3. **Render the Set:**
   - Draw the Mandelbrot fractal on your screen.

---

## Day 4: Zoom Functionality

1. **Implement Zooming:**
   - Change the range of `min_real`, `max_real`, `min_imag`, and `max_imag` based on user input.
   - For example:
     - Zoom in: Halve the range.
     - Zoom out: Double the range.

2. **Handle Mouse Input:**
   - Use `mlx_hook` or `mlx_mouse_hook` to capture mouse events.
   - Center the zoom on the cursor.

---

## Day 5: Movement

1. **Allow Panning:**
   - Shift the fractal view using keyboard inputs (e.g., arrow keys).
   - Update `min_real`, `max_real`, `min_imag`, and `max_imag` based on key presses.

2. **Test Interaction:**
   - Ensure zooming and panning work together without glitches.

---

## Day 6: Julia Set

1. **Understand the Julia Set:**
   - Similar to Mandelbrot, but `C` is fixed, and `Z` starts as the pixel’s position.

2. **Render the Julia Set:**
   - Allow the user to switch between Mandelbrot and Julia sets.
   - Add options to modify `C` interactively.

---

## Day 7: Add Colors

1. **Color Gradients:**
   - Use different color schemes for different iteration counts.
   - Experiment with RGB values to create visually appealing gradients.

2. **Dynamic Coloring:**
   - Allow the user to toggle or cycle through color schemes.

---

## Day 8: Additional Fractals

1. **Research and Implement Burning Ship Fractal:**
   - Similar to Mandelbrot but with a modification:
     ```
     Z = (abs(real(Z)) + i * abs(imag(Z)))^2 + C
     ```

2. **Allow Switching Between Fractals:**
   - Add a key to toggle between Mandelbrot, Julia, and Burning Ship.

---

## Day 9: Polish and Test

1. **Error Handling:**
   - Ensure the program handles invalid input gracefully.
   - Prevent crashes from edge cases (e.g., very high zoom levels).

2. **Refactor Code:**
   - Organize your functions and files for readability and maintainability.

3. **Test Thoroughly:**
   - Check interactions, rendering, and edge cases.

---

## Day 10: Finalize and Submit

1. **Create Documentation:**
   - Write a `README.md` explaining how to use your program.
   - Include a brief explanation of fractals and user interactions.

2. **Submit and Celebrate!**
   - Make sure all required features are complete.
   - Submit the project and share your work with peers.

