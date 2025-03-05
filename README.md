<h1 align="center" style="color: #4CAF50;">🐢 ROS 2 Humble - Turtlesim Guide 🐢</h1>
<h3 align="center" style="color: #555;">✨ Complete Step-by-Step Tutorial to Install, Use & Control Turtlesim in ROS 2 Humble ✨</h3>

<hr>

<h2 style="color: #FF6347;">🚀 Step 1: Install Turtlesim Package</h2>
<pre style="background-color: #f4f4f4; padding: 10px; border: 1px solid #ddd;"><code>
sudo apt update
sudo apt install ros-humble-turtlesim
</code></pre>

<h4 style="color: #0073e6;">✅ Check Installation:</h4>
<pre><code>
ros2 pkg executables turtlesim
</code></pre>
<p>You should see:</p>
<pre><code>
turtlesim draw_square
turtlesim mimic
turtlesim turtle_teleop_key
turtlesim turtlesim_node
</code></pre>

<hr>

<h2 style="color: #FF6347;">🕹️ Step 2: Launch Turtlesim Simulator</h2>
<pre><code>
ros2 run turtlesim turtlesim_node
</code></pre>
<p>🐢 A window will pop up showing a turtle in the center.</p>
<p>📜 Terminal output will show:</p>
<pre><code>
[INFO] [turtlesim]: Starting turtlesim with node name /turtlesim
[INFO] [turtlesim]: Spawning turtle [turtle1] at x=[5.544445], y=[5.544445], theta=[0.000000]
</code></pre>

<hr>

<h2 style="color: #FF6347;">🎮 Step 3: Control the Turtle</h2>
<p>🖥️ Open a new terminal, source ROS 2 again, and run:</p>
<pre><code>
ros2 run turtlesim turtle_teleop_key
</code></pre>

<h4 style="color: #0073e6;">✅ Controls:</h4>
<ul>
    <li>⬆️⬇️⬅️➡️ Use your <b>arrow keys</b> to move the turtle.</li>
    <li>🐢 Each key press moves the turtle a small distance, just like a real robot.</li>
</ul>

<hr>

<h2 style="color: #FF6347;">🔍 Step 4: Explore Nodes, Topics & Services</h2>
<pre><code>
ros2 node list
ros2 topic list
ros2 service list
ros2 action list
</code></pre>

<hr>

<h2 style="color: #FF6347;">🛠️ Step 5: Install and Use rqt</h2>
<pre><code>
sudo apt update
sudo apt install '~nros-humble-rqt*'
</code></pre>

<h4>🖥️ Launch rqt:</h4>
<pre><code>
rqt
</code></pre>

<h4 style="color: #0073e6;">✅ First Time Setup:</h4>
<ul>
    <li>Navigate to <b>Plugins > Services > Service Caller</b>.</li>
    <li>💡 If plugins don’t appear, run:</li>
</ul>

<pre><code>
rqt --force-discover
</code></pre>

<hr>

<h2 style="color: #FF6347;">✨ Step 6: Spawn a Second Turtle</h2>
<p>🔄 In rqt, refresh the service list.</p>
<p>🛠️ Select the <b>/spawn</b> service and set:</p>
<ul>
    <li><b>name:</b> turtle2</li>
    <li><b>x:</b> 1.0</li>
    <li><b>y:</b> 1.0</li>
</ul>
<p>✅ Click <b>Call</b> to spawn turtle2.</p>

<h4 style="color: #f44336;">⚠️ Note:</h4>
<p>If you try to spawn <b>turtle1</b> again, you’ll see:</p>
<pre><code>
[ERROR] [turtlesim]: A turtle named [turtle1] already exists
</code></pre>

<hr>

<h2 style="color: #FF6347;">🎨 Step 7: Change Pen Color</h2>
<p>🎨 In rqt, select the <b>/turtle1/set_pen</b> service and set:</p>
<ul>
    <li><b>r:</b> 255 (Red)</li>
    <li><b>g:</b> 0</li>
    <li><b>b:</b> 0</li>
    <li><b>width:</b> 5</li>
</ul>
<p>✅ Click <b>Call</b> — turtle1 will now draw in <span style="color: red;">red</span> with thicker lines.</p>

<hr>

<h2 style="color: #FF6347;">🐢 Step 8: Control Turtle 2 (Remapping)</h2>
<p>🕹️ To control turtle2, run this in a new terminal:</p>
<pre><code>
ros2 run turtlesim turtle_teleop_key --ros-args --remap turtle1/cmd_vel:=turtle2/cmd_vel
</code></pre>

<h4 style="color: #0073e6;">✅ Now:</h4>
<ul>
    <li>Terminal 1 controls <b>turtle1</b>.</li>
    <li>Terminal 2 controls <b>turtle2</b>.</li>
</ul>

<hr>

<h2 style="color: #FF6347;">❌ Step 9: Close Turtlesim</h2>
<ul>
    <li>Press <b>Ctrl + C</b> in the turtlesim_node terminal.</li>
    <li>Press <b>q</b> in the turtle_teleop_key terminal.</li>
</ul>

<hr>

<h2 style="color: #4CAF50;">📚 Summary</h2>
<p>✅ Installed turtlesim<br>
✅ Moved the turtle using teleop<br>
✅ Explored nodes, topics & services<br>
✅ Used rqt to spawn and customize turtles<br>
✅ Controlled multiple turtles with remapping</p>

<hr>

<h2 style="color: #4CAF50;">💬 Final Note</h2>
<p align="center" style="font-size: 18px;"><b>Thanks for following this guide! 🐢 Dive deeper into ROS 2 for building awesome robotic projects!</b></p>

<hr>

<h2 style="color: #4CAF50;">🌐 Connect With Me</h2>
<p align="left">
    <a href="https://linkedin.com/in/anil-ai" target="blank">
        <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="anil ai" height="30" width="40" />
    </a>
</p>
