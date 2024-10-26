# Wiggle 2

Wiggle 2 is a complete rewrite of the original [wiggle bones add-on](https://github.com/shteeve3d/blender-wiggle) for Blender, offering improved features and stability. \

## Fork Notice

This project is a fork of the original [blender-wiggle-2 by Steve Miller](https://github.com/shteeve3d/blender-wiggle). Modifications have been made to fix compatibility issues with newer Blender versions, along with code cleanup and an updated README. Although I have minimal experience in Blender, I was asked by a friend to fix and enhance this add-on.

For a detailed list of changes, refer to the notice in [`wiggle_2.py`](./wiggle_2.py).

## Features

### New Physics Logic
- Wiggling now simulates more realistic movements, particularly for ropes or chains.

### Pinning
- By applying a damped track constraint on a wiggling bone, you can pin it to its target, allowing other bones to respond accordingly.
![Pinning](./images/pinning.png?raw=true "Pinning")

### Collision Support
- Bones can interact with specified meshes or collections, with options for friction, bouncing, or stickiness.
![Collision](./images/collision.png?raw=true "Collision")

### Linking and Library Overrides
- Wiggle 2 supports library-linked assets, allowing for overrides that let you fine-tune your wiggle per scene.

### Baking Refinements
- A one-click bake feature converts visible wiggle bones into keyframes. Preroll options enable the simulation to settle, and the timeline looping option helps create seamless animations.

### Refreshed Interface
- Manage everything from a single panel in the 3D animation view for a streamlined, fullscreen workflow.

## Usage

1. **Install and Enable the Addon**
   - Enable wiggle in your scene via the properties panel of the 3D viewport under the Animation tab. \
   ![Enable Scene](./images/enable_scene.png?raw=true "Enable Scene")

2. **Select an Armature Object** \
   ![Select Armature](./images/select_armature.png?raw=true "Select Armature")

3. **Enable Wiggle on the Armature** \
   ![Enable Armature](./images/enable_armature.png?raw=true "Enable Armature")

4. **Select a Pose Bone** \
   ![Select Pose Bone](./images/select_pose_bone.png?raw=true "Select Pose Bone")

5. **Enable Wiggle on the Bone**
   - Choose to enable wiggle on the head or tail of the bone. Note: If the bone is connected to its parent, the head option will be unavailable. \
   ![Enable Bone](./images/enable_bone.png?raw=true "Enable Bone")

6. **Configure Bone Physics**
   - Adjust the bone's physics settings via the dropdowns for the head and tail. \
   ![Configure Bone](./images/configure_bone.png?raw=true "Configure Bone")

7. **Set Up Collision**
   - Select a collision object or collection to enable interactions, providing additional tuning options for collision behavior. \
   ![Configure Collision](./images/configure_collision.png?raw=true "Configure Collision")

8. **Utilize Global Utilities**
   - The global utilities section offers functions like resetting physics, selecting all wiggling bones, and copying settings between bones. 
   - Note: You can adjust individual settings on multiple selected bones at once. 
   - 'Loop physics' prevents the physics from resetting during timeline loops, while 'Quality' sets the number of iterations of the constraint solver, enhancing rope simulations. \
   ![Utilities](./images/utilities.png?raw=true "Utilities")

9. **Bake Wiggle**
   - The Bake Wiggle sub-utility converts live physics simulations into keyframes, affecting all visible wiggle bones in the viewport. 
   - Overwrite merges keyframes into the armature's current action or creates a new one. Preroll runs the simulation for a specified number of frames, allowing it to settle, and works in tandem with 'Loop physics' for clean animated loops. \
   ![Bake](./images/bake.png?raw=true "Bake")

## License
Wiggle 2 is licensed under the [GNU General Public License, Version 3](./LICENSE). \
Individual files may have different, but compatible licenses.
