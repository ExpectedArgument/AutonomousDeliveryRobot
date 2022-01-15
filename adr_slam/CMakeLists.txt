cmake_minimum_required(VERSION 2.8.3)

project(adr_slam)

find_package(catkin REQUIRED)

catkin_package()

find_package(roslaunch)

foreach(dir bag config launch rviz )
	install(DIRECTORY ${dir}/
		DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)
