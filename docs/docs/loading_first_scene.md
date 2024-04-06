After downloading and unpacking the assets you have 2 options to load your first warehouse scene the first is using the cmd and isaac sim.
The second option is using USD compser and loading the warehouse directly from the file.

1st approach you will get isaac sims locations in your pc by going to the library in omniverse and clicking on the settings ![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/a1b1f09e-63d2-4c01-8b27-09666215a1fc)

Click on the link or location it will take you to where isaac is downloaded go there and copy the path 
![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/b1b76b4f-e3cc-49e9-bd06-3d37eaff683f)

then type cd in powershell and paste the path, then run this command .\isaac-sim.bat --/persistent/isaac/asset_root/default="omniverse://localhost/Library/NVIDIA/Assets/Isaac/2023.1.1" 
now you got isaac sim running 
look for the environments folder in your assets and drag a drop your desired scene and interact with it
![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/c75c3e7a-3671-4d05-b3f6-c65f637c7859)
