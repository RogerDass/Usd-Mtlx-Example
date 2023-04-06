# Usd-Mtlx-Example
A small USD sample scene using resources from MaterialX's repo.

The goal is this USD scene is to assess the rendering consistency of MaterialX materials across different renderers.

Below are screenshots from various renderer of this scene:

## USDView
![usdview_screenshot_updated_mtlx_uv](https://user-images.githubusercontent.com/11430334/230465884-c01640c0-0fa0-4cff-85f8-64e249514b18.png)

- note the UV texture map tiling behaves correctly when referencing what Blender called the uv coords inside the .mtlx (ex. "UVMap")

## Maya + Arnold
![Arnold_software_mtlx_usd](https://user-images.githubusercontent.com/11430334/230466179-0cb11417-3864-4c9f-8fa7-82d29d4a4998.jpg)
- note what works in usdview seems to work the same in Maya+Arnold (CPU rendering)
![Arnold_GPU_mtlx_usd](https://user-images.githubusercontent.com/11430334/230466283-538a68c5-cf9b-473c-afe1-d8b4ebdb42c0.jpg)
- note that GPU rendering still has an issue with UV Coordinates (look at the scrached brass ball)

## Omniverse Create RTX Accurate (IRAY)
![OVCreate_mtlx_uv](https://user-images.githubusercontent.com/11430334/230466730-0c986846-c750-4bbd-a3ec-a3ce5398f3f5.jpg)
- note that UV tiling used to work before when .mtlx didn't point to correct geom uv coords property. Now UV tiling is incorrect.
- velvet  and thin film doesn't look correct. Nvidia is looking into it.

## Reference renders from MaterialXView (for inconsistently rendered materials)
Tiled Brass:
![Mtlx tiled brass](https://user-images.githubusercontent.com/11430334/229947877-606c7b58-bb0c-4385-a0aa-9b2c430d7086.png)

Velvet:
![mtlx velvet](https://user-images.githubusercontent.com/11430334/229947905-e5f9b09f-0675-47e1-accf-44068571aa3e.png)

Tiled Wood:
![mtlx wood tiled](https://user-images.githubusercontent.com/11430334/229948022-c8b602db-7148-4006-b320-eadf821c45b2.png)

Thin Film:
![mtlx thin film](https://user-images.githubusercontent.com/11430334/229948053-f14fe0c5-b04b-4888-8df1-a583f8206844.png)
