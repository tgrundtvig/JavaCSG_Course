<!---
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%                              TEACHER REFERENCE                             %
%  3D Modeling & Design Patterns with JavaCSG: Building an Interlocking      %
%                             Brick Factory                                  %
%                                                                            %
%                             Teacher Reference                              %
%                             Version 1.0                                    %
%                             [Your Institution / Date]                      %
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
--->
# Table of Contents

1. [Course Overview & Objectives](#course-overview--objectives)
2. [Detailed Course Plan](#detailed-course-plan)
    - [Monday: Introduction & 2D Foundations](#monday-introduction--2d-foundations)
    - [Tuesday: Transition from 2D to 3D Modeling](#tuesday-transition-from-2d-to-3d-modeling)
    - [Wednesday: Design Patterns & Assembly Modeling](#wednesday-design-patterns--assembly-modeling)
    - [Thursday: Advanced Assembly & Transformation Exercises](#thursday-advanced-assembly--transformation-exercises)
    - [Friday: Advanced Modeling & Final Assembly](#friday-advanced-modeling--final-assembly)
3. [Exercises & Assessments](#exercises--assessments)
4. [Tools, Resources, & Sample Materials](#tools-resources--sample-materials)
5. [Appendices](#appendices)
    - [Appendix A: Sample Code Snippets](#appendix-a-sample-code-snippets)
    - [Appendix B: UML Sketch Templates](#appendix-b-uml-sketch-templates)
    - [Appendix C: Additional Reading & Slides Outline](#appendix-c-additional-reading--slides-outline)

## 1. Course Overview & Objectives

**Course Title:**  
3D Modeling & Design Patterns with JavaCSG: Building an Interlocking Brick Factory

**Course Description:**  
This hands-on course introduces students to 2D and 3D geometric modeling using the JavaCSG API. It integrates essential design patterns (Factory, Composite, and Builder) to build a modular system for interlocking bricks. The course is divided into two major parts:
- **Brick Blueprint and Implementation:**  
  Students design and implement fixed, 3D-printed brick blueprints (created by extruding 2D shapes) that include integrated clicker-holes.
- **Model Assembly:**  
  Using the created bricks and a separate set of printed clickers (which are placed into the models using precise transformations), students will assemble larger composite models. (Scaling is omitted because the bricks are fixed, 3D-printed parts.)

**Learning Objectives:**  
By the end of the course, students will be able to:
- Model basic 2D geometries and extrude them into fixed 3D objects using JavaCSG.
- Design software interfaces using UML and apply design patterns effectively.
- Implement the Factory, Composite, and Builder patterns.
- Utilize translation and rotation transformations to integrate separately printed clickers into assembled models.
- Develop a simple procedural model (e.g., a parametric house) that respects physical constraints such as print-bed dimensions.

---

## 2. Detailed Course Plan

Each session includes a short lecture/demo segment (plenum) followed by group work exercises. Milestones are set at the end of each session to ensure progress.

### Monday: Introduction & 2D Foundations

#### Morning Session: Course Kick-Off & 2D Concepts
- **Topics:**
  - Course overview, objectives, project goals, and expected deliverables.
  - Introduction to JavaCSG: basic concepts, immutability, and functional design.
  - 2D geometry fundamentals: points, vectors, angles, and polygons.
- **Teacher Demo:**
  - Live demonstration of creating simple 2D shapes (e.g., a rectangle and a circle) using JavaCSG.
- **Group Exercise:**
  - In groups of 2–4, students sketch simple 2D primitives and discuss how Boolean operations (union, difference) can combine them to create a brick outline.
- **Milestone:**
  - Each group submits a diagram of the 2D primitives along with a brief explanation of their combination strategy.

#### Afternoon Session: 2D Advanced Operations & Intro to Design Patterns
- **Topics:**
  - Advanced 2D operations focusing on Boolean operations and convex hulls (offsetting is omitted).
  - Overview of design patterns, with emphasis on the **Factory Pattern**.
  - Brainstorming the “brick blueprint” interface.
- **Teacher Notes:**
  - Emphasize that the brick blueprint will have fixed dimensions for 3D printing and include integrated clicker-holes.
- **Group Exercise:**
  - Each group sketches a UML diagram for their brick blueprint interface, listing parameters (e.g., brick dimensions, type, hole specifications).
- **Milestone:**
  - Groups present their UML sketches and interface ideas.

---

### Tuesday: Transition from 2D to 3D Modeling

#### Morning Session: 3D Geometry and Extrusions
- **Topics:**
  - Transition from 2D to 3D: using linear and rotational extrusions.
  - Building a fixed 3D brick from a 2D outline.
- **Teacher Demo:**
  - Live example of extruding a 2D brick outline to form a fixed 3D object.
- **Group Exercise:**
  - Each group implements a basic 3D brick using JavaCSG based on their 2D design.
- **Milestone:**
  - A working 3D brick model is produced and displayed.

#### Afternoon Session: Advanced 3D Operations & Clicker-Hole Integration
- **Topics:**
  - Advanced 3D Boolean operations and transformation composition.
  - Introduction to the click-system API (overview only) and its role in producing clicker-holes.
  - Refining the brick blueprint to integrate clicker-holes.
- **Teacher Demo:**
  - Demonstrate integration of a clicker-hole into a brick model using a call to a click-system method (e.g., `getTurnHole()`).
- **Group Exercise:**
  - Groups update their 3D brick models to include an integrated clicker-hole, experimenting with various parameters (e.g., hole length, lead-in options).
- **Milestone:**
  - Each group submits an updated 3D brick model that includes integrated clicker-holes.

---

### Wednesday: Design Patterns & Assembly Modeling

#### Afternoon Session: Composite & Builder Patterns
- **Topics:**
  - Introduction to the **Composite Pattern**: how to model assemblies that include both bricks and sub-models.
  - Overview of the **Builder Pattern**: structuring multi-step assembly processes.
  - Discussion on separating brick blueprint design from assembly logic.
- **Teacher Discussion:**
  - Facilitate a whiteboard session where groups discuss how to represent a “Model” that includes individual bricks and nested sub-models.
- **Group Exercise:**
  - Each group creates a design document outlining their proposed model assembly interfaces and a basic plan for integrating the separately printed clickers.
- **Milestone:**
  - Groups present their design document and interface proposals for the composite model.

---

### Thursday: Advanced Assembly & Transformation Exercises

#### Afternoon Session: Transformation Deep Dive & Clicker Integration
- **Topics:**
  - Detailed review of 3D transformation operations: translation and rotation (scaling is omitted as bricks are fixed).
  - Practical session on calculating the correct position and orientation for placing separate clickers into brick clicker-holes.
- **Teacher Demo:**
  - Live coding session to demonstrate the use of translation and rotation operations to accurately position a clicker (using methods such as `getClicker()` or `getDoubleClicker()`) into a brick model.
- **Group Exercise:**
  - Each group develops a small “assembly module” that applies appropriate transformations to position a clicker in their brick model.
- **Milestone:**
  - Each group demonstrates an assembled unit—a brick with a separately placed clicker showing correct alignment and orientation.

---

### Friday: Advanced Modeling & Final Assembly

#### Morning Session: Procedural Modeling & Parameter-Driven Design
- **Topics:**
  - Introduction to procedural modeling: generating models dynamically using parameters.
  - Case study: designing a simple parametric house model that uses bricks (with integrated clicker-holes) and incorporates separately printed clickers.
  - Addressing physical constraints such as print-bed limits.
- **Teacher Demo:**
  - Walkthrough of a simple procedural model example where parameters (width, height, depth) drive the model assembly.
- **Group Exercise:**
  - In groups, students sketch a plan for their procedural house model, define key parameters, and discuss how brick dimensions and clicker placements relate to print-bed constraints.
- **Milestone:**
  - Each group submits a parameter list and a flow diagram for their procedural model.

#### Afternoon Session: Final Assembly, Integration, and Presentations
- **Topics:**
  - Integration of all components: brick blueprint, clicker-hole integration, separate clicker placement, and composite assembly.
  - Using the Builder Pattern to iteratively construct the full model.
  - Final testing and debugging.
- **Group Work:**
  - Each group integrates their work into a final composite model that includes:
    - Multiple bricks arranged into a larger structure.
    - Precisely placed separate clickers using translation and rotation transformations.
    - (Optional) A procedural house model.
- **Presentations:**
  - Groups present their final models, explaining design decisions, challenges, and demonstrating the assembled model.
- **Final Milestone / Deliverable:**
  - A working prototype that includes:
    - 3D brick generation with integrated clicker-holes.
    - Correct use of translation and rotation for clicker placement.
    - A modular design using the Factory, Composite, and Builder patterns.
    - (Optional) A procedural model that meets print-bed constraints.

---

## 3. Exercises & Assessments

**In-Class Group Exercises:**  
- Each session features hands-on group exercises. Teachers should circulate among groups to provide assistance and facilitate discussion.

**Milestone Checkpoints:**  
- At the end of every session, groups present a short milestone (e.g., a UML sketch, working demo, or design document) to demonstrate progress.

**Final Presentation:**  
- On Friday afternoon, each group will present their final composite model, covering:
  - Their brick blueprint design and clicker-hole integration.
  - The transformation logic (translation and rotation) used for placing clickers.
  - Application of design patterns (Factory, Composite, Builder).
  - (Bonus) Their procedural model design and how parameterization drives the assembly.

**Evaluation Criteria:**  
- Active participation and collaboration.
- Quality and clarity of design documents and code.
- Successful integration of the project components.
- Clarity and depth during final presentations.

---

## 4. Tools, Resources, & Sample Materials

**JavaCSG API & Documentation:**  
- Provide links to the JavaCSG repository and API reference.
- Recommended reading on immutability and functional design in Java.

**Click-System API:**  
- Ensure students have access to the click-system interface documentation (the inner workings are abstracted).

**Design Materials:**  
- Slides/handouts on:
  - UML basics.
  - Design patterns (Factory, Composite, Builder).
  - The importance of immutability.

**Development Environment:**  
- Recommended IDEs: IntelliJ IDEA, Eclipse.
- Provide sample project templates for JavaCSG-based projects.

---

## 5. Appendices

### Appendix A: Sample Code Snippets

**Example 1: Creating a 2D Rectangle with JavaCSG**
```java
JavaCSG csg = ...; // Get an instance of JavaCSG
Geometry2D rectangle = csg.rectangle2D(50, 30); // Create a 50x30 units rectangle
csg.view(rectangle);
```

**Example 2: Extruding a 2D Shape to 3D**
```java
// Extrude the rectangle to a height of 20 units, centering on the Z-axis.
Geometry3D brick3D = csg.linearExtrude(20, true, rectangle);
csg.view(brick3D);
```

**Example 3: Integrating a Clicker-Hole**
```java
// Obtain a clicker-hole geometry using the click-system API.
Geometry3D clickerHole = clickSystem.getTurnHole(10, true, true, 1, false);
// Subtract the clicker-hole from the brick geometry using a Boolean difference.
Geometry3D brickWithHole = csg.difference3D(brick3D, clickerHole);
csg.view(brickWithHole);
```

### Appendix B: UML Sketch Templates

- Provide blank UML diagram templates.
- Suggested components: `BrickBlueprint`, `ClickerGenerator`, `ModelComposite`, `ModelBuilder`.

### Appendix C: Additional Reading & Slides Outline

- Outline for a slide deck covering:
  1. Course Introduction & JavaCSG Basics
  2. 2D and 3D Geometry Essentials
  3. Overview of Design Patterns (Factory, Composite, Builder)
  4. Detailed Walkthrough of Transformation Operations
  5. Integration of Clicker-Holes and Separate Clicker Placement
  6. Procedural Modeling Concepts
  7. Final Assembly and Group Presentations

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%                              END OF DOCUMENT                               %
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
