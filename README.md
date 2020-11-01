# Edge-rounding Tessellation Shader for MonoGame

![Screenshots](/EdgeRounding.jpg?raw=true)

This sample uses a hull and domain shader to round off the edges of a mesh. The mesh is created out of quad patches. The rounding radius and tesselltation factor can be changed dynamically.  

### Limitations
- This method works for corners defined by 3 edges. It's fine to have more edges, if the extra edges are in one of the 3 planes defined by the first 3 edges. In this case the shape of the corner is not influenced by the extra edges, so they can be ignored when calculating the vertex normal.
- This method has only been tested for convex corners. It should also work for concave corners (like beeing on the inside of a cube that surrounds you). The generated normals will probably need to be flipped in this case.

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








