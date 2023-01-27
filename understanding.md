

- The main launch file seems to be at `src/touri_perception/launch/detect_objects_integrated.launch`

- `shipping_box_detection.py`
    - Subscribes to `/camera/color/image_raw`. Takes in images from the body realsense
    - Creates dropping services `perception_shipping_service`.
    - Publishes marker `shipping_test`
    - Sends image data over a socket to the server for processing and obtaining detection of location of the shipping box. Receives detections via the socket.
    - This data is then extracted into appropriate bounding box format ()
    - Camera frame is then converted to body frame by calling appropriate service.

- `souvenir_detection.py`
    - Basically takes camera, sends to socket and gets back the bounding boxes. Nothing fancy.
- `integrated_pipeline.py`

final_ws/stretch_navigation
calib_trail_ws for perception and manipulation
