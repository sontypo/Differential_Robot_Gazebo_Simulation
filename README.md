# Differential_Robot_Gazebo_Simulation

<Son_Nguyen: son94227@gmail.com>

>> Vietnamese Version (English update later - Translate into English if nessesary)

---------------------------------------------------------------
<> Cách chạy file .launch khởi tạo môi trường và robot vi sai: 
---------------------------------------------------------------
	+ b1: catkin build hoặc catkin_make trên terminal để xây dựng workspace;
	+ b2: cấp source cho workspace: 
		$ source devel/setup.bash
	+ b3: chạy file .launch robot với môi trường tùy chọn: 
    	$ roslaunch diffbot_landing diff_bot.launch --> môi trường cơ bản 6x6 với đa biên dạng vật cản, robot vi sai với dải đo lidar_scan 20 mẫu/chu kỳ.
    	$ roslaunch diffbot_landing diffbot_for_Qlearn.launch --> môi trường cơ bản 6x6 với đa biên dạng vật cản, robot vi sai với dải đo lidar_scan 180 mẫu/chu kỳ.
     	$ roslaunch diffbot_landing difbot_with_less_obstacles.launch --> môi trường 5x5 với ít vật cản, phụ hợp cho việc training thuật toán và đánh giá nhanh, robot đặt vào với dải đo lidar_scan 20 mẫu/chu kỳ.
	(với thuộc tính slam_methods được gán cho phương thức slam muốn sử dụng)
	+ b4: sau khi màn hình Rviz và Gazebo hiện ra, để visualize dữ liệu, ta chọn file -> Open Config | Ctrl+O -> không gian lưu trữ differential -> src -> rgbd_cfg.rviz
	+ b5: kích vào termial đang chạy file .launch sử dụng cách phím A, S, D, W, X để điều khiển robot di chuyển.
