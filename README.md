<p align="right">
    <b>语言：</b> <a href="README.md">中文</a> | <a href="README_EN.md">English</a>
</p>

# BlenderLightFriends 插件简易说明

## 插件简介

**BlenderLightFriends** 是一个为Blender设计的灯光管理插件，主要用于在3D场景中快速添加、管理、控制和动画化灯光。它支持类似摄影棚布光的方式，通过经纬度和距离参数让灯光围绕目标对象布置，并支持关键帧动画和“指哪打哪”操作。

---

## 安装与启用

1. 将本插件脚本保存 (`blender_light_friends.py`),或直接下载链接https://github.com/little-house-studio/BlenderLightFriends/releases/download/v1.0/BlenderLightFriends_v1.0.py
2. 在Blender中打开**编辑 > 偏好设置 > 插件**，点击**安装**，选择此文件并启用插件。
3. 在3D视图的**右侧侧边栏（N键）**，会出现一个新标签 **[ 光 ]**，插件操作区就在这里。

---

## 功能概览

### 1. 预设参数设置

- **形状（Shape）**：选择灯光为矩形(Rectangle)或椭圆(Ellipse)。
- **宽度/高度（Width/Height）**：设置灯光面板的尺寸。
- **扩散（Spread）**：控制灯光的扩散角度。
- **默认距离（Default Distance）**：新建灯光默认距离目标的长度。
- **功率（Power）**：灯光的能量/亮度。

**每个参数右侧都可以插入关键帧，实现动画。**

---

### 2. 灯光列表与管理

- 点击**添加灯光**按钮，可以根据上方预设参数添加一个新的Area Light。
- 插件会自动将新灯光围绕选中的对象布置（如未选中对象，则会继承上一灯光的目标）。
- 每个灯光会以列表方式显示，支持一键删除（垃圾桶按钮）。

---

### 3. 灯光详细参数

- 在列表中选择一个灯光后，下方会显示该灯光的详细可调参数：
  - **宽度/高度/扩散/功率/颜色**：均可调节并插入关键帧。
  - **跟踪目标（Tracking Target）**：选择被灯光围绕的目标对象。
- 若设置了跟踪目标，则出现**环绕参数**：
  - **经度/纬度**：用球坐标方式控制灯光相对于目标的环绕方位。
  - **距离**：灯光离目标的距离。
  - **约束偏移**：可微调灯光相对于目标的偏移。
  - **法线追踪**：开启后，灯光可根据表面法线自动调整朝向。

---

### 4. Point and Shoot（指哪打哪）

- 点击 **Point and Shoot** 按钮，鼠标左键按住并拖动，在3D视图中“射”到你希望灯光照射的位置，释放左键后灯光会自动移动到该位置并对准该点。
- **ESC或右键**可取消操作。

---

### 5. 动画支持

- 所有参数都可以通过右侧的**关键帧按钮**插入关键帧，方便制作灯光动画。

---

## 其他说明

- 插件会自动同步灯光和目标的关系，并在时间轴切换时自动更新灯光位置和参数。
- 删除灯光时，相关的空对象（约束辅助Empty）也会一并删除，保持场景整洁。
- 插件支持多灯光管理，方便搭建复杂布光方案。

---

## 常见问题

**Q1：添加灯光时如何指定目标？**  
A：先选中一个对象（如你的人物、场景道具等），再点击插件的“添加灯光”按钮，灯光会自动围绕该对象布置。

**Q2：如何让灯光环绕目标运动？**  
A：调整“经度”“纬度”“距离”参数，并插入关键帧，即可制作环绕动画。

**Q3：Point and Shoot无法生效？**  
A：确保你已选中灯光，并设置了跟踪目标，然后使用Point and Shoot。

---

## 快速操作流程示例

1. 选中你希望灯光围绕的对象。
2. 设置好预设参数，点击“添加灯光”。
3. 在列表中选择灯光，微调参数，或用Point and Shoot快速定位。
4. 如需动画，点击对应参数右侧的关键帧按钮。
5. 多灯光布置时，重复上述操作，可快速完成复杂布光。

---
