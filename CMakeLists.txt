cmake_minimum_required(VERSION 2.8.3)
project(capra_motor_calibrator)
find_package(catkin REQUIRED COMPONENTS
    rospy
    message_generation
    std_msgs
)
add_message_files(
    FILES
    MotorCalibration.msg
)
add_service_files(
    FILES
    Calibrate.srv
)
generate_messages(
    DEPENDENCIES
    std_msgs
)
catkin_package(
    CATKIN_DEPENDS message_runtime
)
