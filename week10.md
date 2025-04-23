**Mission A**
**1.What is DronePaint?**

DronePaint is a human-swarm interaction system that lets users draw in the air using hand gestures, which are recognized by a DNN-based interface to control a swarm of drones for light painting. It enables intuitive, real-time creation of aerial light art without specialized devices.

**2.How do hand gestures move the drones?**

The system uses a webcam and the Mediapipe framework to track hand gestures, which are then classified by a deep neural network. Recognized gestures generate flight trajectories for drones, which follow the path as directed by the user’s hand movements.

**3.What is the system architecture?**

The system has three main modules: (1) a human-swarm interface (gesture recognition and hand tracking), (2) a trajectory processing module (smoothing and converting gestures to flight paths), and (3) a drone control system (executes paths using Crazyflie 2.0 drones, coordinated via ROS).

**4.Why do we smooth my hand’s path before flying?**

Smoothing is necessary to create evenly spaced and continuous coordinates for safe and accurate drone flight. This prevents jittery or uneven movements caused by irregular hand drawing, using an alpha-beta filter and interpolation for stable trajectory generation.

**5.Three simple metaphors for LightPaint:**

Airbrush for the Sky: Like an artist spraying paint on a canvas, the drone paints light in midair.
Magic Wand: Your hand becomes a wand that draws glowing shapes in space.
Digital Fireflies: The drones move like synchronized fireflies, forming glowing trails in the air.

**Mission B**

**Q1. What kind of information is the system "seeing" and transforming into motion?**

DronePaint captures hand landmarks—21 key points on the hand—through a webcam using the Mediapipe framework. These landmarks are turned into feature vectors (angles and distances between joints), which are then classified by a Deep Neural Network (DNN) into specific gestures. The system translates these gestures into drone commands or trajectories, allowing the swarm to move accordingly.

**Q2. List 3 technical components and what happens if they’re missing**

DNN for Gesture Recognition: Without it, the system cannot classify gestures, making drone control imprecise or impossible.

Trajectory Processing Module: Without smoothing and interpolation, drones might fly erratically due to jagged hand-drawn paths.

ROS Communication Framework: Without this middleware, coordination between modules (camera input, gesture recognition, drone control) would break down.

**Q3. Scaling DronePaint for Outdoor Performances – Upgrades Needed**

GPS-based Positioning System: Replace indoor Vicon tracking with RTK-GPS for accurate outdoor localization.

Collision Avoidance: Add real-time obstacle detection using LiDAR or stereo cameras.

Weatherproof Drones: Ensure drones are resistant to wind, rain, and temperature changes.

Fail-safe Protocols: Include geofencing, return-to-home, and emergency land features.

**Q4. Gesture Control vs. Traditional Inputs**

Advantages:

Intuitive, immersive, and hands-free.

Ideal for performances, creative art, or interactive exhibitions.
Limitations:

Less precise than mouse/keyboard for detailed work.

Requires stable lighting and consistent gestures.
Shines in:

Live shows, VR/AR environments, inclusive tech for those with physical limitations using conventional devices.

**Q5. Social Issue Art Concept**

Theme: "Climate Crisis: Melting Time"
Visual Concept: Use drones to create a glowing ice clock melting into water, transitioning from crisp blue-white to soft red-orange trails in the sky. A ticking motion conveys urgency. It ends with scattered dots symbolizing species loss.

**Q6. Business Innovation & Commercialization**

Model: B2B & B2C hybrid

B2B: Sell or lease DronePaint setups to event companies, amusement parks, museums.

B2C: Offer app-based access for consumers to create mini light shows with rental drones.
Why it fits: High engagement potential, versatile use cases (art, advertising, education), and recurring income from events.

**Q7. Experiential Marketing Campaign**

Concept: "Your Message in the Sky!"

Venue: Science museum or cultural festival.

Visitors draw a symbol or message on a tablet, then watch drones trace it live in the air.

Capture and share via social media (custom hashtag), with real-time projection on a building wall.

Collect user data and stories for follow-up engagement.

**Q8. Gesture vs. Voice Recognition**

Criteria	Gesture Recognition	Voice Recognition
Pros	Silent, expressive, spatially rich	Hands-free, natural language use
Cons	Needs camera, lighting; fatigue	Needs quiet environment, multi-language challenges
Best Uses	Art, physical play, VR/AR	Smart homes, cars, search tasks
Hybrid systems can combine both for adaptive interaction (e.g., gesture for direction, voice for commands).

**Q9. AI Enhancements for Sports/Concerts**

Concept: "AI-Powered Drone Dance"

Enhancements:

Predictive Choreography: AI anticipates beats/dancer moves to pre-sync drone patterns.

Audience Reaction Analysis: Cameras scan faces or sound levels; drones react with shape/color changes.

Here’s a rough storyboard idea (let me know if you want me to generate sketches with AI):

Crowd cheering → AI detects high excitement → Drones form heart shape.

Fast beat drop → Predictive model triggers light burst spiral.

Calm interlude → Drones hover low, pulsing like jellyfish.

**Q10. Risks of DNN Misinterpretation & Redundancy Design**

Risks:

Misclassifying casual hand movements as commands.

Environmental interference (lighting, background clutter).

Redundancy Features:

Confirmation Gestures: Require a follow-up gesture to confirm major actions (like takeoff).

Context Awareness: Use time of day, user proximity, or crowd behavior to reduce false positives.

Fallback Control: Allow emergency override via mobile app or voice command.

**Mission C**

"C:\Users\C8\Desktop\Connection – Emotional Aura Drone.pptx"
