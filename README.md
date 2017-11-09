# Formula Student Driverless Resources
 
Intro

## Table of Contents:
- [Datasets](#datasets)
	- [AMZ driverless 2017](#amz_driverless_2017)

- [Conference Papers & Journal Articles ](#papers)
- [Reports](#reports)

___
<br>

<a name="datasets"></a>
# Datesets
This section is devoted to share data collected in, or related to, Formula Student Driverless Vehicles.

<a name="amz_driverless_2017"></a>
## AMZ driverless 2017
- The data can be found in this [link](https://www.dropbox.com/s/7x75ks6vo2npfv3/AMZ_driverless_2017_dataset.bag.tar.gz?dl=0)

* The data comes in .bag format. This is the standard logging format for ROS and it can be easily imported to matlab using available tools. 

* The Car reference frame is defined as (front, left, up) and has it is aligned and has its origin in the IMU reference frame. All the sensor's data are already aligned with the car. The data is given in International Sytem Units unless otherwise specified.

* The data was collected in an airfiled in the outskirts of Zurich. The ground is mostly flat but there are some curved regions and bumps. There is high grass on the side of the of the road. The day was very sunny.

* In this rosbag one can find the following topics:

-* velodyne_points : Contains the Lidar point returns in a sensor_msgs/PointCloud2 message type. The Lidar is a Velodyne Puck VLP16. The position of the LiDAR in car_frame is x= 1.6 m, y= 0.0 m.

-* optical_speed_sensor: Contains ground speed data in a geometry_msgs/TwistStamped message type. This sensor is a Kistler Corevet SPII. The position of this sensor in the car frame is x= -0.41m y= 0.27 m.

-* wheel_rpm : contains the wheel speed data in a geometry_msgs/QuaternionStamped message type. x -> front left wheel, y -> front right wheel. z -> rear left wheel. w -> rear right wheel. The data is expressed in rpm's. The distance to thefront axel is 0.81m, to the rear axel 0.72m, and the wheelbase of the car is 1.2m.

-* imu : Contains the accelerometer and gyroscopes information in a sensor_msgs/Imu message type. This sensor is an SBG ellipse-N. The position of this sensor in the car frame is x = 0.0 m, y = 0.0 m. 

-* /gps : Contains the GPS information in sensor_msgs/NavSatFix message type. The data is expressed in degrees for Lattitue and Longitude. The sensor is the same SBG ellipse-N used as IMU. 
 
<a name="papers"></a>
# Conference Papers & Journal Articles 

<a name="reports"></a>
# Reports
