# Edge-rounding Tesselation Shader for MonoGame

![Screenshots](/EdgeRounding.jpg?raw=true)

This sample uses a hull and domain shader to round off the edges of a mesh. The mesh is created out of quad patches. The rounding radius and tesseltation factor can be changed dynamically.  

### Build for OpenGL
- Open ShaderTestGL.csproj.
- Make sure MonoGame.Framework.DesktopGL from this [MonoGame fork](https://github.com/cpt-max/MonoGame/tree/glshaderstages) is referenced.
- Rebuild the content in ShaderTestGL.mgcb using the MGCB Editor from that fork.

### Build for DirectX
- Open ShaderTestDX.csproj.
- Make sure MonoGame.Framework.WindowsDX from this [MonoGame fork](https://github.com/cpt-max/MonoGame/tree/glshaderstages) is referenced. 
- Rebuild the content in ShaderTestDX.mgcb using the MGCB Editor from that fork. 

If you are only interested in the DirectX version, you can also use this [DX only branch](https://github.com/cpt-max/MonoGame/tree/shader) instead. This branch doesn't contain the switch from MojoShader to ShaderConductor, so it's a lot lighter.

Thanks to JSandusky as the Hull, Domain and Geometry shader support for DirectX is based on [his MonoGame fork](https://github.com/JSandusky/MonoGame).








