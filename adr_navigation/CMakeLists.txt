cmake_minimum_required(VERSION 2.8.3)

project(adr_navigation)

find_package(catkin REQUIRED)

catkin_package()

find_package(roslaunch)

foreach(dir launch maps params)
	install(DIRECTORY ${dir}/
		DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)
