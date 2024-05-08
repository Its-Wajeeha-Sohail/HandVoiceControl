# HandVoiceControl
Virtual hand and voice controlled Mouse

Gesture Controlled Virtual Mouse makes human computer interaction simple by making use of Hand Gestures and Voice Commands. The computer requires almost no direct contact. All i/o operations can be virtually controlled by using static and dynamic hand gestures along with a voice assistant. This project makes use of the state-of-art Machine Learning and Computer Vision algorithms to recognize hand gestures and voice commands, which works smoothly without any additional hardware requirements. It leverages models such as CNN implemented by [MediaPipe] running on top of pybind11. It consists of two modules: One which works direct on hands by making use of MediaPipe Hand detection, and other which makes use of Gloves of any uniform color. Currently it works on Windows platform.

# Features
### Gesture Recognition:
<details>
<summary>Neutral Gesture</summary>
 <figure>

  <figcaption>Neutral Gesture. Used to halt/stop execution of current gesture.</figcaption>
</figure>
</details>
 

<details>
<summary>Move Cursor</summary>

  <figcaption>Cursor is assigned to the midpoint of index and middle fingertips. This gesture moves the cursor to the desired location. Speed of the cursor movement is proportional to the speed of hand.</figcaption>
</details>

<details>
<summary>Left Click</summary>

 <figcaption>Gesture for single left click</figcaption>
</details>

<details>
<summary>Right Click</summary>

 <figcaption>Gesture for single right click</figcaption>
</details>

<details>
<summary>Double Click</summary>

 <figcaption>Gesture for double click</figcaption>
</details>

<details>
<summary>Scrolling</summary>

 <figcaption>Dynamic Gestures for horizontal and vertical scroll. The speed of scroll is proportional to the distance moved by pinch gesture from start point. Vertical and Horizontal scrolls are controlled by vertical and horizontal pinch movements respectively.</figcaption>
</details>

<details>
<summary>Drag and Drop</summary>

 <figcaption>Gesture for drag and drop functionality. Can be used to move/tranfer files from one directory to other.</figcaption>
</details>

<details>
<summary>Multiple Item Selection</summary>

 <figcaption>Gesture to select multiple items</figcaption>
</details>

<details>
<summary>Volume Control</summary>

 <figcaption>Dynamic Gestures for Volume control. The rate of increase/decrease of volume is proportional to the distance moved by pinch gesture from start point. </figcaption>
</details>

<details>
<summary>Brightness Control</summary>

 <figcaption>Dynamic Gestures for Brightness control. The rate of increase/decrease of brightness is proportional to the distance moved by pinch gesture from start point. </figcaption>
</details>

### Voice Assistant ( ***Voice_controller*** ):
<details>
<summary>Launch / Stop  Gesture Recognition</summary>

    <code> Voice_controller Launch Gesture Recognition </code><br>
    Turns on webcam for hand gesture recognition.
  </li>
  <li>
    <code> Voice_controller Stop Gesture Recognition </code><br>
    Turns off webcam and stops gesture recognition.
    (Termination of Gesture controller can also be done via pressing <code>Enter</code> key in webcam window)
   </li>
</ul>
</details>

<details>
<summary>Google Search</summary>

  <li>
    <code>Voice_controller search {text_you_wish_to_search}</code><br>
    Opens a new tab on Chrome Browser if it is running, else opens a new window. Searches the given text on Google.
  </li>
</ul>
</details>

<details>
<summary>Find a Location on Google Maps</summary>

      <code>Voice_controller Find a Location</code><br>
      Will ask the user for the location to be searched.
    </li>
    <li> 
      <code>{Location_you_wish_to_find}</code><br>
      Will find the required location on Google Maps in a new Chrome tab.
    </li>
  </ol>
</details>

<details>
<summary>File Navigation</summary>

      <code>Voice_controller list files</code> / <code> Proton list </code><br>
      Will list the files and respective file_numbers in your Current Directory (by default C:)
    </li>
    <li>  
      <code> Voice_controller open {file_number} </code><br>
      Opens the file / directory corresponding to specified file_number.
    </li>
    <li>
      <code>Voice_controller go back </code> / <code> Proton back </code><br>
      Changes the Current Directory to Parent Directory and lists the files.
    </li>
  </ul>
</details>

<details>
<summary>Current Date and Time</summary>

      <code> Voice_controller what is today's date </code> / <code> Voice_controller date </code><br>
      <code> Voice_controller what is the time </code> / <code> Voice_controller time </code><br>
      Returns the current date and time.
    </li>
  </ul>
</details>

<details>
<summary>Copy and Paste</summary>

      <code> Voice_controller Copy </code><br>
      Copies the selected text to clipboard.<br>
    </li>
    <li>
      <code> Voice_controller Paste </code><br>
      Pastes the copied text.
    </li>
  </ul>
</details>

<details>
<summary>Sleep / Wake up Proton</summary>
       <code> Voice_controller bye </code><br>
      Pauses voice command execution till the assistant is woken up.
    </li>
    <li>
      Wake up<br>
      <code> Voice_controller wake up </code><br>
      Resumes voice command execution.
    </li>
  </ul>
</details>

<details>
<summary>Exit</summary>
      <code> Voice_controller Exit </code> <br>
      Terminates the voice assisstant thread. GUI window needs to be closed manually.
    </li>
  </ul>
</details>

# Gesture Recognition:
-Palm
-Move Cursor
-Left Click
-Right Click
-Double Click
-Scrolling
-Drag and Drop
-Multiple Item Selection
-Volume Control
-Brightness Control
-Voice Assistant ( Proton ):
-Launch / Stop Gesture Recognition
-Google Search
-Find a Location on Google Maps
-File Navigation
-Current Date and Time
-Copy and Paste
-Sleep / Wake up Proton
-Exit


# Getting Started

  ### Pre-requisites
  
  Python: (3.6 - 3.8.5)<br>
  Anaconda Distribution: To download click [here](https://www.anaconda.com/products/individual).
  
  ### Procedure
  ```bash
  git clone https://github.com/Its-Wajeeha-Sohail/HandVoiceControl.git
  
  Step 1: 
  ```bash
  conda create --name gest python
  ```
  
  Step 2:
  ```bash
  conda activate gest
  ```
  
  Step 3:
  ```bash
  pip install -r requirements.txt
  ```
  
  Step 4:
  ```bash 
  conda install PyAudio
  ```
  ```bash 
  conda install pywin32
  ```
  
  Step 5:
  ``` 
  cd to the GitHub Repo till src folder
  ```
  Command may look like: `cd C:\Users\.....\Gesture-Controlled-Virtual-Mouse\src`
  
  Step 6:
  
  For running Voice Assistant:
  ```bash 
  python voice_controller.py
  ```
  ( You can enable Gesture Recognition by using the command "Proton Launch Gesture Recognition" )
  
  Or to run only Gesture Recognition without the voice assisstant:
  
  Uncomment last 2 lines of Code in the file `Gesture_Controller.py`
  ```bash 
  python gesture_controller.py
  ```
