%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%                         CODING EXERCISES                                %
%  3D Modeling & Design Patterns with JavaCSG: Building an Interlocking      %
%                             Brick Factory                                %
%                                                                            %
%                         Coding Exercises                               %
%                             Version 1.0                                    %
%                         [Your Institution / Date]                        %
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

# Student Coding Exercises

These exercises are designed to guide you through the key concepts of the course—from basic 2D/3D modeling with JavaCSG to applying design patterns (Factory, Composite, and Builder) in a project to build an interlocking brick factory.

---

## Exercise 1: Create a 2D Brick Outline

**Objective:**  
Learn to create basic 2D primitives and combine them using Boolean operations.

**Task:**
1. Using JavaCSG, create a rectangle (e.g., 50x30 units).
2. Create a circle (e.g., with a diameter of 20 units) positioned so that it overlaps with the rectangle.
3. Use the `difference2D` operation to subtract the circle from the rectangle.
4. Display the resulting 2D shape.

**Hints:**
- Use `csg.rectangle2D(width, height)` to create the rectangle.
- Use `csg.circle2D(diameter, angularResolution)` to create the circle.
- Use `csg.difference2D(rectangle, circle)` for subtraction.

**Deliverable:**  
A Java code snippet or method that performs the above tasks and displays the final 2D shape.

---

## Exercise 2: Extrude a 2D Shape to Create a 3D Brick

**Objective:**  
Convert a 2D shape into a fixed 3D brick.

**Task:**
1. Take the 2D shape you created in Exercise 1.
2. Use the `linearExtrude` method to extrude it into a 3D object with a specified height (e.g., 20 units).
3. Ensure the 3D brick is centered along the Z-axis.
4. Display the 3D brick.

**Hints:**
- Use `csg.linearExtrude(height, centerZ, geometry2D)`.

**Deliverable:**  
A Java method that generates and displays the 3D brick.

---

## Exercise 3: Integrate a Clicker-Hole into the Brick

**Objective:**  
Learn to modify a 3D object using Boolean operations.

**Task:**
1. Using your 3D brick from Exercise 2, obtain a clicker-hole geometry using the click-system API.
2. Subtract the clicker-hole from your brick geometry using a 3D Boolean difference operation.
3. Display the updated brick with the integrated clicker-hole.

**Hints:**
- Use a method such as `clickSystem.getTurnHole(parameters)` to obtain the clicker-hole.
- Use `csg.difference3D(brickGeometry, clickerHole)` to subtract the clicker-hole from the brick.

**Deliverable:**  
A Java method that returns the updated brick with the clicker-hole integrated.

---

## Exercise 4: Implement a Brick Blueprint Interface and Factory

**Objective:**  
Design an interface and a factory class for creating brick blueprints.

**Task:**
1. Define a `BrickBlueprint` interface that includes methods to obtain:
   - The print geometry (used for 3D printing)
   - The view geometry (for on-screen visualization)
2. Create a `BrickFactory` class that implements the Factory Pattern to produce different types of brick blueprints (e.g., standard rectangular brick, L-shaped brick, etc.).
3. Each blueprint should have fixed dimensions and include integrated clicker-holes.

**Hints:**
- Consider interface methods like `Geometry3D getPrintGeometry()` and `Geometry3D getViewGeometry()`.
- Use constructor parameters or factory methods to differentiate between brick types.

**Deliverable:**  
Java source files for the `BrickBlueprint` interface and the `BrickFactory` class with sample implementations.

---

## Exercise 5: Position a Clicker Using Transformations

**Objective:**  
Learn to use translation and rotation transformations to position objects in a 3D space.

**Task:**
1. Obtain a clicker geometry using the click-system API (e.g., via `clickSystem.getClicker(parameters)`).
2. Write a method that uses JavaCSG’s transformation operations to correctly position and orient the clicker so that it aligns with the clicker-hole in your brick.
3. Test your method by applying the transformation to the clicker and combining it with your brick model.

**Hints:**
- Use `csg.translate3D(...)` for translation and `csg.rotate3D(...)` for rotation.
- Consider the relative position of the clicker-hole on your brick when calculating the transformation.

**Deliverable:**  
A Java method that returns the transformed clicker geometry ready for integration with the brick model.

---

## Exercise 6: Assemble a Composite Model Using the Composite Pattern

**Objective:**  
Create a composite model that combines multiple brick instances.

**Task:**
1. Write a class `CompositeModel` that can hold a collection of brick geometries.
2. Implement methods to add bricks to the composite model.
3. Use JavaCSG’s `union3D` (or similar operations) to combine these bricks into a single composite geometry.
4. Display the final composite model.

**Hints:**
- The `CompositeModel` class should manage a list (or collection) of `Geometry3D` objects.
- Consider providing methods like `addBrick(Geometry3D brick)` and `buildModel()`.

**Deliverable:**  
A Java class for the composite model with example usage code demonstrating how multiple bricks are assembled.

---

## Exercise 7: Build a Model Using the Builder Pattern

**Objective:**  
Develop a builder class to manage the multi-step assembly process of a composite model.

**Task:**
1. Create a `ModelBuilder` class with methods for incrementally adding bricks and clickers.
2. Ensure that the builder maintains the correct order and positioning of components.
3. Provide a `build()` method that returns the final assembled composite model.

**Hints:**
- The builder should internally use the transformation methods to position components.
- Document your builder’s API with clear comments explaining each method.

**Deliverable:**  
Java source code for the `ModelBuilder` class and a demonstration of its use in assembling a composite model.

---

## Exercise 8 (Optional, Advanced): Procedural Model Generation

**Objective:**  
Create a parameter-driven procedural model (e.g., a simple house).

**Task:**
1. Write a method that accepts parameters such as house width, height, and depth.
2. Use your brick blueprints and transformation operations to assemble a basic house structure.
3. Ensure that the design adheres to physical constraints (e.g., the print-bed size).
4. Display the procedurally generated model.

**Hints:**
- Break the house into components (walls, roof, etc.) and generate each component using your brick blueprint.
- Experiment with different parameter values to see their effects on the model.

**Deliverable:**  
A Java method that generates and displays a procedural model based on input parameters.

---

# Submission Guidelines

- **Submission Format:**  
  - Submit your Java source files along with any UML diagrams or design documents.
  - Organize your files into appropriate packages (e.g., bricks, models, builders).

- **Assessment Criteria:**  
  - Correctness and functionality of the code.
  - Clarity and modularity of your design (use of interfaces and design patterns).
  - Quality of your documentation and comments.
  - Overall integration and presentation of your final composite model.

Good luck, and enjoy coding your interlocking brick models!
