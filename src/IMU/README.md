文件组织结构如下

//imu参数设置
imudata

//定义了R的右扰动
so3

//四阶龙格库塔
RK4OnManifold 依赖于 imudata so3

//预积分
IMUPreintegrator 依赖于 RK4OnManifold 

//惯导递推
NavState

//优化库里节点和边的实现
g2otypes 依赖于 NavState IMUPreintegrator
