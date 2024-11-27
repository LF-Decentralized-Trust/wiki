1. [Community Architects](index.html)
2. [Community Architects Team](Community-Architects-Team_20545564.html)
3. [Checklists](Checklists_20560801.html)
4. [Completed Checklists](Completed-Checklists_20560928.html)

# Community Architects : Cacti Renaming Checklist

Created by Peter Somogyvari, last modified by Ry Jones on Apr 27, 2023

- Determine public vs. private API surface in order to get a clear picture on what code elements can be renamed without triggering a breaking change and therefore a major release (if using semantic versioning)
  
  - Update source code references
    
    - Classes
    - Interfaces
    - Imports
    - Do keep in mind that these have to be separated based on internal vs. published API elements
- Update links pointing to the GitHub repository within
  
  - source code
  - documentation that's managed separately from the source code (if applicable)
- Double check that your GitHub apps still work after the repository rename.
  
  - Some GitHub app configurations might have hard-coded repository names/URLs stored in their configuration.
- ReadTheDocs page (if applicable)
- Calendar meetings (where applicable)
  
  - Note: The calendar is tied to the mailing list meaning that once the brand new mailing list has been created the maintainers will have to manually recreate all the regular calendar entries.
- Wiki pages (Hyperledger staff/project maintainers)
- Package managers/published artifacts (where applicable)
  
  - npm
  - Maven/Gradle
  - Container images
  - Plan ahead with communication to your users who depend on your project artifacts. Make sure they are aware that a completely new artifact name will be used in the future and therefore they have to update their own source code/dependency declaration files (such as package.json, build.gradle, pom.xml, etc.)
- Slide decks (if applicable)
- Whitepapers (if applicable)
- GitHub Integrations (where applicable):
  
  - ZenHub
  - MergeFreeze
  - Jira
  - Gitter
  - GitGuardian
  - etc.
- We're done

# Plan to Create the Cacti Repository and Migrate (Import) Weaver Into Cacti

1. Port hyperledger/cactus to hyperledger/cacti, either by:
   
   1. Renaming the project repository: cactus to cactii
2. Transfer (move) `hyperledger-labs/weaver-dlt-interoperability` to `hyperledger`/`weaver-dlt-interoperability`
3. Create a branch `hyperledger`/`weaver-dlt-interoperability/cacti-port` from `hyperledger`/`weaver-dlt-interoperability``/main`
4. In the branch `weaver-dlt-interoperability/cacti-port`:
   
   1. Create a subfolder in the root folder named `weaver`
   2. Move all other files and folders in the root folder to `weaver`
5. Merge `hyperledger`/`weaver-dlt-interoperability/cacti-port` into `hyperledger/cacti``/main` as follows:
   
   1. `Clone the following`
   2. `hyperledger`/`weaver-dlt-interoperability`
   3. `hyperledger/cacti`
   
   <!--THE END-->
   
   1. `git remote add weaver-dlt-interoperability ../hyperledger/weaver-dlt-interoperability`
   2. `git fetch weaver-dlt-interoperability`
   3. `git merge weaver-dlt-interoperability/cacti-port --allow-unrelated-histories`
   4. In the same location in the file system, clone the following:
   5. Navigate to the clone of `hyperledger/cacti` and run:
6. Transfer all relevant issues from `hyperledger`/`weaver-dlt-interoperability` to `hyperledger/cacti`:
   
   1. Navigate to the `hyperledger`/`weaver-dlt-interoperability` Github repo in a web browser
   2. Transfer each issue to `hyperledger/cacti` according to the instructions in [https://docs.github.com/en/issues/tracking-your-work-with-issues/transferring-an-issue-to-another-repository](https://docs.github.com/en/issues/tracking-your-work-with-issues/transferring-an-issue-to-another-repository)
7. Transfer (move) `hyperledger`/`weaver-dlt-interoperability` back to `hyperledger-labs/weaver-dlt-interoperability`
8. (Future) Archive `hyperledger-labs/weaver-dlt-interoperability`

## Weaver Configurations and Updates within Cacti

Update paths and URLs in various configuration files and in the documentation within the `weaver` folder in the `hyperledger/cacti` repository to ensure proper building of components, publishing of packages, and accuracy of instructions.

* * *

Staff

- Project page update on Hyperledger site (Hyperledger staff)
  
  - Hyperledger top page (including Cactus GitHub URL) [https://www.hyperledger.org/use/cactus](https://www.hyperledger.org/use/cactus)
- Rename GitHub repository
  
  - GitHub allows redirection from the old URL to the new one. Note however: This will only work as long as there isn't another project later created with the same (old) project name.
  - Also note that contributors will receive a warning message from git prompting them to update their git remote URLs from the old the the new one. This is something that all contributors have to address locally on their own machines.
- Mailing list (Hyperledger staff)
  
  - Note: mailing lists cannot be renamed. Instead a brand new list will have to be created by Hyperledger staff and then previous subscribers will have to subscribe to that one again.
  - Permissions will have to be set up from scratch (e.g. maintainers to be mods of the list, etc.)
- Chat rooms (Discord)
- Wiki pages (Hyperledger staff/project maintainers)

Document generated by Confluence on Nov 26, 2024 13:04

[Atlassian](http://www.atlassian.com/)
