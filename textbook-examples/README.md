# CSC405 Module 2 — Textbook Example Programs

Example code from Gordon, V. S., & Clevenger, J. (2021). Computer graphics programming in OpenGL with Java (3rd ed.). Mercury Learning and Information. Used for coursework study.

Official companion files were downloaded from the author’s page,
[Computer Graphics Programming in OpenGL with Java, 3rd Edition](https://athena.ecs.csus.edu/~gordonvs/textJ3E.html)
(`J3E_CompanionFiles.zip`). Each program folder is self-contained:
its `.java` sources, `.glsl` shaders, utility classes (`Utils.java`,
`Sphere.java`, `Torus.java`, `ImportedModel.java` as needed), and any
textures or models that program loads are copied into that folder.

**Assigned reading:** Chapter 2, Sections 2.3–2.6.

## Programs in this module

### Program2_4 — Reading GLSL Source from Files

- **Section:** 2.3 Reading GLSL Source Code from Files
- **Official folder:** `Chapter_02_OpenGLPipeline/Prog2_4_files`

### Program2_5 — Drawing a Triangle

- **Section:** 2.4 Building Objects from Vertices
- **Official folder:** `Chapter_02_OpenGLPipeline/Prog2_5_triangle`

### Program2_6 — Simple Animation Example

- **Section:** 2.5 Animating a Scene
- **Official folder:** `Chapter_02_OpenGLPipeline/Prog2_6_animation`
- **Note:** Also assigned in Module 3 (Section 2.5 is required in both modules).

## Assigned sections without a numbered program

- Section 2.6 (Organizing the Java Code Files) introduces the Utils.java helper used starting with Program 2.5. It has no separate numbered program.

## Compile and run

These programs use the official companion layout: Java sources and shaders live in a `code/` package (`package code;`), and textures or `.obj` models sit in the program folder (the working directory when you run). Shaders are loaded with paths such as `code/vertShader.glsl`.

You need **JDK 11**, **JOGL 2.4** (`jogl-all.jar`, `gluegen-rt.jar`, plus the native jars for your OS), and **JOML 1.10** (`joml-1.10.0.jar`) on the classpath. The textbook’s Appendix A (Windows) and Appendix B (macOS) cover installation. On Linux, put the jars in a `lib` directory (or any folder you prefer) and run the following from a program folder, for example `Program2_5`:

```bash
# Adjust these paths to where you keep the jars
CP="lib/jogl-all.jar:lib/jogl-all-natives-linux-amd64.jar:lib/gluegen-rt.jar:lib/gluegen-rt-natives-linux-amd64.jar:lib/joml-1.10.0.jar"

# Compile (from the program folder that contains the code/ directory)
javac -cp "$CP" code/*.java

# Run (also from that program folder, so shader and texture paths resolve)
java -cp "$CP:." \
  --add-exports java.base/java.lang=ALL-UNNAMED \
  --add-exports java.desktop/sun.awt=ALL-UNNAMED \
  --add-exports java.desktop/sun.java2d=ALL-UNNAMED \
  -Dsun.java2d.d3d=false -Dsun.java2d.uiScale=1 \
  code.Code
```

On Windows, use `;` instead of `:` in the classpath, and the official `compile.bat` / `run.bat` in each folder assume the JOGL and JOML jars are already on your global `CLASSPATH` (as the book’s setup appendix describes):

```bat
javac code/Code.java
java --add-exports java.base/java.lang=ALL-UNNAMED --add-exports java.desktop/sun.awt=ALL-UNNAMED --add-exports java.desktop/sun.java2d=ALL-UNNAMED -Dsun.java2d.d3d=false -Dsun.java2d.uiScale=1 code.Code
```

Programs that open a window need a display; compiling does not.


This `textbook-examples` folder contains **18** files.
