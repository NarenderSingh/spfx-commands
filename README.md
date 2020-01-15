# SharePoint Framework Commands


SharePoint Framework Production 1 :

1. gulp build
2. gulp bundle --ship
3. gulp package-solution --ship

Deploy same app with different name in same site app catalog.
Steps:
1. Go to dist folder and delete all the files and folders.
2. Go to lib folder and delete all the files and folders.
3. Go to SharePoint folder and delete all the files and folders.
4. Open https://www.guidgen.com/ for generating new GUID.
5. Go to src/webparts/[projectname]/[projectname]WebPart.manifest.json file.
6. Generate new GUID 1 from step 4 and replace it inside "id" field. eg. "id": "3fe8fa37-b19e-4cdc-8540-ebc274c02dba".
7. Generate new GUID 2 from step 4 and replace it inside "preconfiguredEntries/groupId" field. eg. "groupId": "589dc692-2db9-4a96-b4b4-3b01e5901000".
8. Go to config/package-solution.json. change solution/name & paths/zippedPackage if possible (or same would also work)
9. Generate new GUID 3 from step 4 and replace it inside "solution/id" field. eg. "id": "8d4cdd35-2b10-4e77-9792-85e33f18d58e"
10. Go to .yo-rc.json in root folder (if project is installed using yarn package manager) or do same in package-lock.json file
11. Using GUID 3 from step 9 and replace it inside "libraryId". eg. "libraryId": "8d4cdd35-2b10-4e77-9792-85e33f18d58e".

12. gulp build
13. gulp bundle --ship
14. gulp package-solution --ship

15. Go inside sharepoint/solution/app.sppkg and upload in app catalog. 

