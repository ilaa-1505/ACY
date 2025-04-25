
import cv2
from flask import Flask, Response

app = Flask(__name__)

# Initialize the camera (replace with your specific camera source)
cap = cv2.VideoCapture(0)  # Usually 0, but could be 1 or another index

def generate_frames():
    while True:
        # Read frame from camera
        success, frame = cap.read()
        if not success:
            break
        else:
            # Encode frame as JPEG
            ret, buffer = cv2.imencode('.jpg', frame)
            frame = buffer.tobytes()
            # Yield the frame in the required format for Flask
            yield (b'--frame\r\n'
                   b'Content-Type: image/jpeg\r\n\r\n' + frame + b'\r\n\r\n')

@app.route('/video_feed')
def video_feed():
    return Response(generate_frames(),
                    mimetype='multipart/x-mixed-replace; boundary=frame')

if __name__ == '__main__':
    # Replace '0.0.0.0' with Jetson Nano's IP address to allow remote access
    app.run(host='0.0.0.0', port=5000, debug=True)
