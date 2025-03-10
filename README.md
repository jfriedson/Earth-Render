# Earth Renderer in C++ and OpenGL
Found this old project and archiving it here.

![Screenshot of Earth Render depicting the Americas at Dusk](readme_assets/americas_morning.png?raw=true)
![Screenshot of Earth Render depicting Asia at Dawn](readme_assets/asia_evening.png?raw=true)

This project achieves a relatively convincing rendering of the Earth from space (on an unrealistically sunny and clear day) with exagerated height mapping for thrills by layering multiple high resolution textures (8k-16k resolution) sourced from public scientific publications and processes them using vertex, tessellation, and fragment shaders to achieve:

### Features
- Tessellation
    + considers the local complexity of the height-map texture in addition to the distance that the patch is from the camera before introducing new verticies for efficiency  
- Height mapping  
- Normal mapping  
- Shadow mapping  
- Specular, Ambient, and Diffuse lighting  
- Shadow mapping  
- Night/Day Cycle depicting the light pollution texture at night time
- Clouds
    + rendered on a larger, non-tessellated Earth model with a single, patterned texture
    + clouds match the Earth's rotation but slowly scroll vertically to add variation
- (TODO) parallax skybox effect

### Controls
mouse - pivot the camera around Earth  
arrows - move through day-night cycle  
esc - quit

### Libraries Utilized
GLFW - Window creation and hardware peripherals communication  
GL3W - Expose OpenGL API  
GLM - OpenGL math types and methods  
Freetype - Font loading and rendering  
