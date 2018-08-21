# unity-blank-asset-directory

Repository to evaluate strategies in terms of keeping Unity asset folders structured.

## Abstract
Depending on the size and the goal of a project, different directory structures seem to be suitable. But requirements, like sharing files between projects, as well as the used version control software or mandatory procedures, defined in companies, can have effects on the final project structure. The reverse domain name notation seems to be a proper way to identify files in shared projects and to differentiate between multiple versions of them.

## Investigations

### Unity's special folder names

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

### Leading characters to differentiate between personal folders and Unity special folders
- When project grows and sharing files is required in the future, restructuring directories could introduce new errors
    
### Reverse Domain Name Notation (reverse-DNS)
- Easy identification of the associated project for any file
- Easy identification of the obsolete files
- Less collisions when sharing folders

## Proposed structure for Unity projects of any sizes
![Sample content in Assets folder](https://github.com/lars-wobus/unity-test-git-submodules/blob/master/res/umlet/sample-directory-structure.png)
