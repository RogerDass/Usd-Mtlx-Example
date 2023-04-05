# Usd-Mtlx-Example
A small USD sample scene using resources from MaterialX's repo.

The goal is this USD scene is to assess the rendering consistency of MaterialX materials across different renderers.

Below are screenshots from various renderer of this scene:

## USDView
![USDView screenshot](https://user-images.githubusercontent.com/11430334/229933793-c9b9d4a4-41f4-4847-99b4-f2d16e38db20.png)
- note the UV texture map tiling isn't working correctly

## Maya + Arnold
![working USD_mtlx](https://user-images.githubusercontent.com/11430334/229934064-93aed9d9-34bb-4483-bdb0-454b54521190.jpg)
- note the same UVTiling issue is present in Arnold as well

## Omniverse Create RTX Accurate (IRAY)
![Create RTX IRAY](https://user-images.githubusercontent.com/11430334/229934241-621ba7ff-5e36-40fb-8e30-75cb89f802f2.png)
- note that Create adds "materials/" to the texture path specified in the .mtlx file. You'll need to remove the "materials/" from the .mtlx file.
- velvet doesn't look correct, but the texture map tiling seems to behave correctly. Thin film also doesn't behave.

## Reference renders from MaterialXView (for inconsistently rendered materials)
Tiled Brass:
![Mtlx tiled brass](https://user-images.githubusercontent.com/11430334/229947877-606c7b58-bb0c-4385-a0aa-9b2c430d7086.png)

Velvet:
![mtlx velvet](https://user-images.githubusercontent.com/11430334/229947905-e5f9b09f-0675-47e1-accf-44068571aa3e.png)

Tiled Wood:
![mtlx wood tiled](https://user-images.githubusercontent.com/11430334/229948022-c8b602db-7148-4006-b320-eadf821c45b2.png)

Thin Film:
![mtlx thin film](https://user-images.githubusercontent.com/11430334/229948053-f14fe0c5-b04b-4888-8df1-a583f8206844.png)