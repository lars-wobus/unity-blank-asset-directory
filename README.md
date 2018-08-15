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

Depending on the size and the goal of a project as well as on the amount of dependencies, different directory structures seem suitable. The used version control software and mandatory procedures defined in companies can also affect the final project structure.

If there are any dependencies, e.g. assets from other projects shall be reused, then sorting assets by their projects or clients seems to be the best idea. For smaller projects this convention seems to be unnecessary, except for developing asset packages. 
