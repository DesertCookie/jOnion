# JOnion

JOnion is a modular **Java game engine** designed for maximum configurability.
You can use a preset to easily create **2D and 3D games**, letting the engine take care of everything complicated in the background. You can also use 
JOnion‘s lower-level classes that simply wrap OpenGL functionality in an easy to use object-oriented manner.
JOnion uses GLFW for its window and context creation as well as input; for rendering **OpenGL** is used, with the modular engine design preparing for 
**Vulkan** to be added as rendering API; **OpenAL** is used for realistic and hardware-accelerated sound; other libraries that JOnion uses include: 
JOML 
(matrix and vector math), STB (image loading and font generation), Assimp (model file loading), Steamworks4J (Steam API), AMD Tootle (mesh optimization). The libraries used work on all three major operating systems and so does JOnion.

*JOnion is very much in active development and the code available on this repository reflects an alpha state of the engine. While all functions are 
tested and verified to work in their intended use-case it is not unlikely for anomalies to occur, for which to be reported I‘d be very grateful.*

---

#### Current Feature-Set
- Rendering using shaders (VAOs, VBOs, UBOs).
- Entity batching (one VAO-bind for entities sharing the same model data).
- Extensive window-creation capabilities using GLFW (separated into crucial features only `Window` and feature-complete `AdvancedWindow`).
- Mouse, keyboard, controller (joystick & gamepad), clipboard input.
- Separation of 2D and 3D rendering system (ease of use and rendering efficiency).
  - 2D-optimized shaders and rendering techniques (texture atlases, sprite-rendering, etc.).
- Mouse, keyboard, controller (joystick & gamepad) and clipboard input.
- Intelligent resource management (e.g.: no double-loading of duplicate textures).
- Prefabs for simple and advanced 2D/3D games (game loop taken care of, etc.) and game state management.
- Profiling tools to retrieve information about the rendering process (draw calls, texture-binds, number of drawn polygons, etc.).

#### Planned/Incoming Features
- lighting (point-, spot-, directional lights)
- model loading (OBJ, PLY, etc. using Assimp)
- font rendering (dynamic distant-field font-generation using STB and smart rendering using shaders)
- advanced 2D-rendering (sprite-maps, sprites, sprite-animations)
- terrain generation (using custom or dynamic noise-maps)
- complete documentation (only present on about one-third of the code so far; example code and wiki scarcely available)

*For a more detailed look into the feature-roadmap see [trello.com](https://trello.com/b/rR8SuLPQ/jonion).*

#### Licensing – aka.: "*Use me please!*"
JOnion is released under the *BSD two-clause license*, permitting you to use and modify all code present in this repository, as long as you include 
reference to me as author or this repository as a way for people to trace the code back to its origin.

#### Repository Structure
- `docs` – Javadoc documentation (incomplete)
- `libs` – library dependencies, licenses and natives
- `main` – engine source code
  - `jonion` – base package containing general engine-related classes
  - `glfw` – classes wrapping GLFW functionality
  - `opengl` – classes wrapping OpenGL functionality
  - `assimp` – classes wrapping Assimp functionality
- `res` – resources required by the engine like default shaders and textures
- `test` – engine tests and example applications
- `testres` – resources used by tests or examples
