# unity-blank-asset-directory

Repository to evaluate strategies in terms of keeping Unity asset folders structured.

## Abstract
Depending on the size and the goal of a project, different directory structures seem to be suitable. But requirements, like sharing files between projects, as well as the used version control software or mandatory procedures, defined in companies, can have effects on the final project structure. The reverse domain name notation seems to be a proper way to identify files in shared projects as well as to differentiate between multiple versions of them.

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

### Folders with leading characters to ease differentiation between personal folders and Unity special folder
Using an underscore as the leading character for folder names seemed to be a good idea at the beginning. But when new developers are joining the team or when files shall be shared between projects, problems could occure. Avoiding misunderstandings and avoiding restructurings of any project should to be primary goals for any Unity developer.

### Reverse Domain Name Notation (reverse-DNS)
Example: com.company.product

Using the notation in shared projects reduces the amount of collisions. Moreover obsolete files, duplicates, different versions of a file and the associated project can be identified. 

## Proposed structure for Unity projects of any sizes
![Sample content in Assets folder](https://github.com/lars-wobus/unity-test-git-submodules/blob/master/res/umlet/sample-directory-structure.png)
