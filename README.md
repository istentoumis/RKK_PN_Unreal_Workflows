
Perception Neuron suit(body) along with Rokoko Smartgloves(fingers) to Rokoko's custom character, Bruno - The Mime. 

Information can be found below for:

* Stream in Real Time 
* Record an animation with both products via Unreal's Take Recorder
* Retarget the recorded animation to another character

Unreal Engine Version 4.27.

Before opening the project, make sure "Neuron Live Link" and "Rokoko Studio Live" plugins are installed to the current egine version via Marketplace. Then, enable the plugins in the editor (Edit->Plugins). Restart the project. 

## **Set up**

Axis Studio Lite livestream settings:

![image](https://user-images.githubusercontent.com/88091497/194755958-53d269fd-d63f-4a34-b81d-4e71a02b8d0d.png)

![image](https://user-images.githubusercontent.com/88091497/194755968-2992fa0f-08bd-4534-933e-affa9a77114b.png)

Unreal settings:

![image](https://user-images.githubusercontent.com/88091497/194756018-78662514-145d-40f3-a343-d05ad778f261.png)

Uncheck "Is UDP" and press Ok.

![image](https://user-images.githubusercontent.com/88091497/194756039-67637e1c-6583-476c-aee8-4b80fa04b325.png)

In the Live Link Pose node(UE4_Mannequin_AnimBP), select Neuron 's Actor.

![image](https://user-images.githubusercontent.com/88091497/194756069-318a4f17-bed5-47c8-a627-5f6e31d687f9.png)

Rokoko Studio livestream settings

![image](https://user-images.githubusercontent.com/88091497/194756109-28522e81-50fa-4369-af15-0d7a28bc80a9.png)

![image](https://user-images.githubusercontent.com/88091497/194756113-76ec00b7-19c6-4310-8deb-c20e9c047045.png)

Unreal settings:
Find the Rokoko Receiver in the scene and make sure that it's the same as inside Studio

![image](https://user-images.githubusercontent.com/88091497/196036993-c90a6e10-eec7-46c0-b2db-05c4faebd380.png)

In the UE4_Actor_BP set the Rokoko Actor Name as the Actor's Profile in Rokoko Studio.

![image](https://user-images.githubusercontent.com/88091497/197598665-1d84e543-549c-4c42-ba69-9e379957222d.png)

![image](https://user-images.githubusercontent.com/88091497/194756201-db5ce427-255c-4a9d-bd4a-f33ef31b8e7a.png)

Enable the Live Link for Rokoko Studio.

![image](https://user-images.githubusercontent.com/88091497/194756229-a3808fe3-8929-4615-b24a-6ee6596a5d92.png)

Hit Play.

## **Record an animation**

While livestreaming, select Window -> Cinematics -> Take Recorder.

![image](https://user-images.githubusercontent.com/88091497/194756840-7d1a5244-1e06-4af2-b23d-8ba1a8580e85.png)

**Close the Sequencer**, we need only Take Recorder.

![image](https://user-images.githubusercontent.com/88091497/194756874-c47fa236-5244-41a3-8cd3-a50f09473085.png)

In Take Recorder, select the Mime_BP as the Source.

![image](https://user-images.githubusercontent.com/88091497/197599063-ace047e7-c129-43e3-82bd-d3f933c8ae65.png)

Start recording your Animation:

![image](https://user-images.githubusercontent.com/88091497/194756937-9d158286-e9c4-4ca7-8ef1-8783abc6e6b0.png)

Press Stop when done with the Animation(bottom right).

![image](https://user-images.githubusercontent.com/88091497/194756961-0b2fe1e9-5a90-455f-93c3-c45b44afbef4.png)

Navigate into Content -> Cinematics -> Takes -> * *current Date* * -> Scene_x_xx_Subscenes -> Animation and the recorded Animation should be found.

![image](https://user-images.githubusercontent.com/88091497/197599271-f6cecd9c-fce9-42e8-b0a7-8d3aca5708e7.png)

Drag it into the scene and hit Play.

## **Retarget the recorded animation to another character**

Make sure that the custom character is in the **exact same T-Pose as Mime_Skeleton** for a detailed retargeting.

In Mime_Skeleton select Retarget Manager, Select Rig -> Select Humanoid Rig.

![image](https://user-images.githubusercontent.com/88091497/194758050-1ce59062-cd6a-4150-9b63-bee7e4e0713e.png)

![image](https://user-images.githubusercontent.com/88091497/194758058-5a83a5a1-6e4d-4ed2-9600-246ab882c23c.png)

Set the following:

![image](https://user-images.githubusercontent.com/88091497/197599941-6b28f668-5837-4658-9ceb-509ab81b52c4.png)

Click Show Advanced and **keep only the fingers for retargeting**. All the other bones should be set as None(only in Show Advanced joints).

![image](https://user-images.githubusercontent.com/88091497/197599991-9b379b88-96bd-4e17-9ecf-46a04092c460.png)

Clise Save to save the bonemap.

In the other character's skeleton, select Retarget Manager, Select Rig -> Select Humanoid Rig.

Select all the corresponding joints of the character for a proper retargeting(the same joints that were selected in Mime_Skeleton). Click Save to save the bonemap.

Right click on the recorded animation, select Retarget Anim Assets -> Duplicate Anim Assets and Retarget.

![image](https://user-images.githubusercontent.com/88091497/194758283-fe85b376-39b7-4fb3-aaf2-77ed83c1b36a.png)

Select the skeleton of your custom character and click Retarget.

The retargeted animation should be visible in Content folder. Drag it into the scene and hit Play.
