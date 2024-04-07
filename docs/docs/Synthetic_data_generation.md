After we have our workstation set up. we can start synthetic data generation. We need to get replicator up and running. 

first step enable the script editor
![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/eecd00d3-86d7-4a3f-8f9b-9b428e879195)

then we look for the omniverse://<nucleus_path>/Isaac/Samples/Replicator/Stage/full_warehouse_worker_and_anim_cameras.usd it depends on where did you save your assets.

it should look like this once you load it
![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/947a83a0-0f26-4e41-afca-be02ea6786b0)

then we look for the replicator extension and enable synthetic data Recorder 

![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/a026f204-c792-4d30-8327-41956d49ee36)

once you enabled it should be the tap to the bottom right 

then you can add more cameras or ways to render by clicking on Render products 

![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/2e527c2b-beb1-4551-90f7-ea60d7cc0b0b)

from here you can copy the paths to the camreas specified and add their path to Camera path under render products you can change the view and give the cameras differnet names.

![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/ce0189bb-2e18-42cf-ad36-9294729806e7)

You can come to this step later after running the whole process to further enhance it, but I think it's essential. 
from here you can randmoizie the camera position using this script 

import omni.replicator.core as rep

camera = rep.create.camera()
with rep.trigger.on_frame():
    with camera:
        rep.modify.pose(
            position=rep.distribution.uniform((-5, 5, 1), (-1, 15, 5)),
            look_at="/Root/Warehouse/SM_CardBoxA_3",
        )

go to the script editor tap which we enabled in the first step. Copy and paste the script and run it 
![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/328f46a5-4334-49c5-ac04-04f195224d19)
After running it from the bottom left you click on click on the prespective tap in the top a new camera should be there 
![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/e9b8401e-58f8-4486-853b-7c2eee635af6)
Look for the replicator prim and copy the camera path from there and paste it into the render products camera path. Now you have your cameras set up for randomaization.
![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/6f86de19-9526-46e6-8655-0a12f26476af)

The parameter frame gives you the option to use the basic writeer by clicking on the desired outputs or you can make your own custom writer which is easy to find examples for here https://docs.omniverse.nvidia.com/isaacsim/latest/replicator_tutorials/tutorial_replicator_recorder.html#isaac-sim-app-tutorial-replicator-recorder
in the NVIDIA website
![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/fdeefe14-4e39-42dd-991d-a449161dd4a3)
You can then modify the parameters as you desire try to read their description by hovering over them for better understanding or refer to the link above which has further explantion.
The Rtsubremes is to improve image quality by rendring extra frames between captures.
now choose the desired frame output and click run after choosing the location for output using the output tap the default will be in the Omniverse-launcher folder.

![image](https://github.com/mahmoud25112/omniverse-ai/assets/148357408/a6989ee5-be4e-44dd-ae2d-83315c8b06b8)
