## OpenAI Results
<iframe width="420" height="315" src="https://cdn.openai.com/openai-baselines-ppo/knocked-over-stand-up.mp4" frameborder="0" allowfullscreen></iframe>

The above video was released in a [2016 paper](https://arxiv.org/abs/1707.06347) by OpenAI. It shows how a PPO agent has been used to learn the behaviors of a humanoid robot. To establish control like this using RL was groundbreaking. The examples below show how I was able to establish control of a rotary inverted pendulum using a similar PPO agent (not so groundbreaking but still quite cool).
## Pendulum Training
<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_010.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
In this first video, the agent acts initially randomly as determined by the randomly initialized weights in the policy. The video is shorter than the others, as an early termination condition is produced (theta 1 rotates too far). 

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_044-swing.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
After several hundered attempts at learning control, the agent learned how to swing. 

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_071-windmill.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
After swinging comes the stage I like to call "windmilling" at about 7000 episodes.

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_107-balence-attempt.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
The controller then learns that balancing at the top of the swing might be a good idea.

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_172-balence.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
Finally, in this video, we have a controller that can balance the pendulum in a specific position. It's been able to extract all this controlling behavior from its reward function. Further improvement wasn't observed after this. 

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_170-fin.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
## Pendulum Results
After control was established to evaluate the robustness of the controller, noise was added to the position and velocity signals of theta 1 and theta 2. Results from this are shown in the videos below. 
<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/completed-with-noise.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
The first video is showing the controller that was initialised vertically.

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/completed-with-noise-swingup.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
Then to see if the swing up control of the system was still able to work ok, the second simulation was run with the pendulum initalised facing downwards. 


