# unity-blank-asset-directory

## Summary
Repository to evaluate strategies in terms of keeping Unity asset folders structured.

## Unity's special folder names

| Name                     | Quantity | Location |
|--------------------------|----------|----------|
| Editor                   | multiple | anywhere |
| Editor Default Resources | one      | fixed    |
| Gizmos                   | one      | fixed    |
| Plugins                  | one      | fixed    |
| Resources                | multiple | anywhere |
| Standard Assets          | one      | fixed    |
| StreamingAssets          | one      | fixed    |

See Unity's [documentation](https://docs.unity3d.com/Manual/SpecialFolders.html) for more details.

## Naming of user-defined folders

Depending on the size and the goal of a project as well as on the amount of dependencies, different directory structures seem to be suitable. The used version control software and mandatory procedures defined in companies can also affect the final project structure.

If there are any dependencies, e.g. assets from other projects shall be reused, then sorting assets by their projects or clients seems to be the best idea. For smaller projects this convention seems to be unnecessary, except when developing asset packages.

Using leading underscores for custom folders within the Assets folder can help to identify mandatory folders, which should never be renamed. However, using leading underscores in subfolders seems to be unnecessary.

### Proposed structure for large projects
- Assets
    - &lt;Product-1&gt;
        - Animation
        - Audio
        - ...
        - Editor
        - ...
        - Resources
        - ...
    - &lt;Product-2&gt; (target for some symlinks)
    - &lt;Product-3&gt; (target for other symlinks)
    - ~~Editor~~
    - Editor Default Resources
    - Gizmos
    - Plugins
    - ~~Resources~~
    - Standard Assets
    - StreamingAssets
    
&lt;Product&gt; = com.company.product | _MyAssetPackage
  
### Proposed structure for small projects
- Assets
    - Editor
    - Editor Default Resources
    - Gizmos
    - Plugins
    - Resources
    - Standard Assets
    - StreamingAssets
    - _Animation
    - _Audio
    - ...
    
### Update

Cause sharing files between projects will always become a problem at some point, the proposed way for small projects should not be applied! It makes much more sense, to place files within project-related folders (as described in one of my [other repositories](https://github.com/lars-wobus/unity-test-git-submodules))
