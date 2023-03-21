# Rokoko-Embodiment

This repository contains intructions on importing rokoko animations, an UE5 project that demonstrates this as well as additional animations. The animation format that provides the best outcome so far is the `human_Ik` denoted by `_hik`.

**Note**: This is in progress some of the retargeting is still not perfect.

## Importing animations

When importing animations it is important that:

- The skeleton is `None`

- The boxes for "Use T0 As Ref Pose" and "Import Animations" are checked.

This is shown below.

![Importing](/Images/Importing%20animations.png)

## Project overview

In this UE5 project there are 2 IK_rigs

### Mocap IK

The `MocapIKrig` located in `Content > Animations > MocapIKrig` which is used to define which chains are used in retargeting. They are as follows:

![Mocaprig](/Images/IK%20Retargeting.png)

### Metahuman IK

The `MHIKrig` located in `Content > Metahumans > Oskar > MHIKrig` which is used to define which chains are used in retargeting. They are as follows:

![MH_rig](/Images/MH_IKrig.png)

## Retargeter

Using these two  rigs an IK_retargeter is used to map the chains to one another. This is named `Retargeter01` and is found in the `content` folder. The skeletion extracted from the animation is set as the source and the Metahuman skeleton as the target.

![IK_retarget](/Images/chain_mapping.png)

### T-Pose

The pose of the metahuman is set as a T-pose, same as the source skeleton.

![IK_retarget_pose](/Images/Retargeter_pose.png)

Hand positioning is very iportant for good results. Al fingers should be flat and parallel as shown below.

### Hand placement

![Hand placement](/Images/Hand%20Placement.png)

## Export

The animation is then exported, in this case and is found in the `content > Metahumans > Oskar > 2_hand_low_hik_Anim1.uasset`

Open this to see a preview animation.

![Anim preview](/Images/Animation%20preview.png)
