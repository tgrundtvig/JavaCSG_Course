<!---
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%                           STUDENT HANDOUT                                %
%  3D Modeling & Design Patterns with JavaCSG: Building an Interlocking      %
%                             Brick Factory                                %
%                                                                            %
%                         Student Materials                                %
%                         Version 1.0                                      %
%                         [Your Institution / Date]                        %
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
--->
# Table of Contents

1. [Course Overview](#course-overview)
2. [Learning Objectives](#learning-objectives)
3. [Project Description](#project-description)
4. [Session-by-Session Instructions & Exercises](#session-by-session-instructions--exercises)
    - [Monday: Introduction & 2D Foundations](#monday-introduction--2d-foundations)
    - [Tuesday: Transition from 2D to 3D Modeling](#tuesday-transition-from-2d-to-3d-modeling)
    - [Wednesday: Design Patterns & Assembly Modeling](#wednesday-design-patterns--assembly-modeling)
    - [Thursday: Advanced Assembly & Transformation Exercises](#thursday-advanced-assembly--transformation-exercises)
    - [Friday: Final Assembly & Project Integration](#friday-final-assembly--project-integration)
5. [Sample Code Snippets](#sample-code-snippets)
6. [UML Diagram Templates & Resources](#uml-diagram-templates--resources)
7. [Submission Guidelines & Assessment](#submission-guidelines--assessment)

---

<a id="course-overview"></a>
## 1. Course Overview

Welcome to **3D Modeling & Design Patterns with JavaCSG: Building an Interlocking Brick Factory**. In this course you will learn how to create 2D and 3D models using JavaCSG and apply key design patterns (Factory, Composite, and Builder) to build a modular system of interlocking bricks. These bricks will be designed as fixed, 3D-printed parts (with integrated clicker-holes) and then assembled digitally with separately printed clickers that are correctly positioned using transformation operations.

---

<a id="learning-objectives"></a>
## 2. Learning Objectives

By the end of this course, you will be able to:
- Create and manipulate basic 2D shapes and extrude them into fixed 3D objects using JavaCSG.
- Understand and apply key design patterns (Factory, Composite, Builder) to a real-world project.
- Use translation and rotation transformations to accurately place components in a 3D model.
- Collaborate in groups to design, implement, and present a composite model.
- Develop a simple parameter-driven (procedural) model that adheres to physical constraints (e.g., print-bed size).

---

<a id="project-description"></a>
## 3. Project Description

**Project Overview:**  
You will work in small groups (2–4 members) to develop a complete digital system for an interlocking brick factory. Your work will be divided into two parts:
1. **Brick Blueprint Creation:**  
   - Design a brick blueprint that represents a fixed, 3D-printed brick.
   - The blueprint must include integrated clicker-holes (using the provided click-system API).
2. **Model Assembly:**  
   - Assemble multiple brick instances into a composite model.
   - Use separate, printed clickers that are positioned with the correct orientation (via translation and rotation operations).
   - Optionally, develop a simple procedural model (e.g., a parametric house) that uses your bricks and respects print-bed constraints.

---

<a id="session-by-session-instructions--exercises"></a>
## 4. Session-by-Session Instructions & Exercises

<a id="monday-introduction--2d-foundations"></a>
### Monday: Introduction & 2D Foundations

**Morning Session – Course Kick-Off & 2D Concepts**
- **Topics Covered:**
  - Overview of the course, objectives, and project deliverables.
  - Basic concepts in JavaCSG including immutability and functional design.
  - Fundamentals of 2D geometry: points, vectors, angles, and polygons.
- **Your Task:**
  - Work with your group to sketch simple 2D shapes (e.g., rectangles, circles).
  - Discuss how you might combine these shapes using Boolean operations (union, difference) to form a brick outline.
- **Deliverable:**  
  A diagram showing your 2D primitives and a brief explanation of your design approach.

**Afternoon Session – 2D Advanced Operations & Design Patterns**
- **Topics Covered:**
  - More on Boolean operations and convex hulls.
  - Introduction to the Factory Pattern and how it applies to creating brick blueprints.
- **Your Task:**
  - Brainstorm and create a UML diagram for a “brick blueprint” interface.
  - Identify the parameters that define your brick (e.g., dimensions, type, and clicker-hole specifications).
- **Deliverable:**  
  A group UML diagram and a list of interface methods/parameters.

---

<a id="tuesday-transition-from-2d-to-3d-modeling"></a>
### Tuesday: Transition from 2D to 3D Modeling

**Morning Session – 3D Geometry and Extrusions**
- **Topics Covered:**
  - How to extrude 2D shapes into 3D objects.
  - Techniques for linear and rotational extrusions.
- **Your Task:**
  - Implement a basic 3D brick model by extruding your 2D brick outline.
- **Deliverable:**  
  A working 3D brick model displayed on-screen.

**Afternoon Session – Advanced 3D Operations & Clicker-Hole Integration**
- **Topics Covered:**
  - Advanced Boolean operations in 3D.
  - An overview of the click-system API, focusing on methods like `getTurnHole()`.
- **Your Task:**
  - Update your 3D brick model to include an integrated clicker-hole.
  - Experiment with different parameters (e.g., hole length, lead-in options) and decide on the best configuration.
- **Deliverable:**  
  An updated 3D brick model that includes a clicker-hole.

---

<a id="wednesday-design-patterns--assembly-modeling"></a>
### Wednesday: Design Patterns & Assembly Modeling

**Afternoon Session – Composite & Builder Patterns**
- **Topics Covered:**
  - Overview of the Composite Pattern to create assemblies from bricks and sub-models.
  - Introduction to the Builder Pattern for managing multi-step assembly processes.
- **Your Task:**
  - Work with your group to create a design document outlining how you will assemble bricks into a composite model.
  - Develop an interface proposal for your composite model, indicating how individual bricks (and possibly sub-models) will be combined.
- **Deliverable:**  
  A design document that includes a UML sketch and interface proposals for model assembly.

---

<a id="thursday-advanced-assembly--transformation-exercises"></a>
### Thursday: Advanced Assembly & Transformation Exercises

**Afternoon Session – Transformation Deep Dive & Clicker Integration**
- **Topics Covered:**
  - Detailed review of translation and rotation operations in 3D.
  - How to calculate the correct position and orientation for placing clickers into brick clicker-holes.
- **Your Task:**
  - Develop a small “assembly module” that uses JavaCSG’s transformation functions to position a clicker (obtained from the click-system API) into your brick model.
  - Ensure that the clicker aligns correctly with the clicker-hole.
- **Deliverable:**  
  A demonstration of your assembled unit (a brick with a separately positioned clicker) showing correct alignment and orientation.

---

<a id="friday-final-assembly--project-integration"></a>
### Friday: Final Assembly & Project Integration

**Morning Session – Procedural Modeling & Parameter-Driven Design**
- **Topics Covered:**
  - Basics of procedural modeling: creating models dynamically based on parameters.
  - Case study: designing a simple parametric house model using your bricks.
- **Your Task:**
  - Sketch a plan for a procedural house model that uses your brick designs.
  - Define key parameters (e.g., house width, height, depth) and discuss how these will influence brick placement.
- **Deliverable:**  
  A parameter list and flow diagram outlining your procedural model design.

**Afternoon Session – Final Assembly, Integration, & Presentations**
- **Topics Covered:**
  - Integration of all components: brick blueprints, clicker-hole integration, and the assembly of multiple bricks.
  - Using the Builder Pattern to construct a composite model.
- **Your Task:**
  - In your group, integrate all your work into a final composite model.
  - The final model should include multiple bricks with integrated clicker-holes and correctly positioned, separately printed clickers.
  - (Optional) Incorporate your procedural house model if time allows.
- **Deliverable:**  
  A complete, working prototype of your composite model and a brief group presentation explaining your design decisions and challenges.

---

<a id="sample-code-snippets"></a>
## 5. Sample Code Snippets

Below are a few code examples to help you get started with JavaCSG operations:

**Creating a 2D Rectangle**
```java
JavaCSG csg = ...; // Get an instance of JavaCSG
Geometry2D rectangle = csg.rectangle2D(50, 30); // Create a 50x30 units rectangle
csg.view(rectangle);
```

**Extruding a 2D Shape to 3D**
```java
// Extrude the rectangle to a height of 20 units, centered on the Z-axis.
Geometry3D brick3D = csg.linearExtrude(20, true, rectangle);
csg.view(brick3D);
```

**Integrating a Clicker-Hole**
```java
// Obtain a clicker-hole geometry using the click-system API.
Geometry3D clickerHole = clickSystem.getTurnHole(10, true, true, 1, false);
// Subtract the clicker-hole from the brick geometry using a Boolean difference.
Geometry3D brickWithHole = csg.difference3D(brick3D, clickerHole);
csg.view(brickWithHole);
```

---

<a id="uml-diagram-templates--resources"></a>
## 6. UML Diagram Templates & Resources

- **UML Templates:**  
  Download the provided UML diagram templates (available on the course website or Git repository) to help you sketch your design.
  
- **Resources:**  
  - Review handouts on UML basics and design patterns.
  - Consult the lecture slides for examples of interface definitions (e.g., for `BrickBlueprint`, `ClickerGenerator`, `ModelComposite`, and `ModelBuilder`).

---

<a id="submission-guidelines--assessment"></a>
## 7. Submission Guidelines & Assessment

- **Group Work:**  
  You will work in groups of 2–4 members for all exercises and the final project.
  
- **Milestones:**  
  At the end of each session, your group must submit a milestone (diagram, working demo, or design document) to track progress.

- **Final Presentation:**  
  On Friday afternoon, each group will present your final composite model. Your presentation should cover:
  - The design of your brick blueprint and clicker-hole integration.
  - How you used transformation operations to place clickers.
  - How design patterns (Factory, Composite, Builder) were applied.
  - (Optional) Your procedural model design and parameterization.

- **Assessment Criteria:**  
  Your work will be evaluated based on:
  - Collaboration and participation.
  - Quality and clarity of design documents and code.
  - Successful integration of all project components.
  - Clarity and thoroughness of your final presentation.
<!---
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%                              END OF STUDENT HANDOUT                        %
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
--->
