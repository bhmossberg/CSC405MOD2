# CSC405MOD2

**CSC405 Computer Graphics, CSU Global (Winter 2026, Session A). Module 2: Graphics Programming**

OpenGL Sierpinski Gasket Fractal in Java.

## Enabling Objectives

By the end of this module, you will be able to:

1. Describe primitives and attributes.
2. Describe color concept.
3. Analyze the gasket program.
4. Describe control functions.
5. Describe viewing.

## Readings

**Required**

- Gordon, V. S., & Clevenger, J. (2021). Computer graphics programming in OpenGL with Java (3rd ed.). Mercury Learning.
  - Chapter 2
    - Section 2.3: Reading GLSL Source from Files
    - Section 2.4: Building Objects from Vertices
    - Section 2.5: Animating a Scene
    - Section 2.6: Organizing the Java Code Files


**Recommended**

- de Vries, J. (2020). Learn OpenGL - graphics programming. Kendall & Welling. https://learnopengl.com/book/book_pdf.pdf
- Leese, G., Kessenich, J., Baldwin, D., & Rost, R. (2023, August 14). The OpenGL® shading language, version 4.60.8. The Khronos Group Inc. https://registry.khronos.org/OpenGL/specs/gl/GLSLangSpec.4.60.html

## Assignment: Module 2: Critical Thinking

Sierpinski Gasket (100 Points)

Ensure you have a working OpenGL with Java (JOGL) development environment, as described in Chapter 1 of Gordon & Clevenger (2021). If you have not already, install the JDK, JOGL, and JOML and verify your setup by running one of the example programs from the textbook’s companion site.

Read Sections 2.4 (“Building Objects from Vertices”) and 2.6 (“Organizing the Java Code Files”) of the textbook. Pay close attention to how vertex data is loaded into a Vertex Buffer Object and rendered through vertex and fragment shaders.

Create a Java program using JOGL that renders the Sierpinski Gasket fractal. You may use the iterative or the recursive approach (the recursive approach generally produces a more even point distribution). Your vertex shader should pass through point positions; your fragment shader should output a color (you may use a single uniform color or vary color by depth).

In your reflection, consider: What do you observe as the gasket is rendered? How do primitive type (e.g., GL_POINTS vs. GL_TRIANGLES) and vertex attributes influence the final output? What patterns emerge as the iteration depth increases? How does changing the shader’s color logic affect the appearance?


### Submission Guidelines

Your Java source files and GLSL shader files.

A screenshot of the rendered Sierpinski Gasket.

A 2–3 paragraph reflection (Word document).

Your paper must be formatted according to APA guidelines in the CSU Global Writing Center (available in the left-hand navigation panel).

Refer to the rubric below for more details about how you will be graded for this assignment.

