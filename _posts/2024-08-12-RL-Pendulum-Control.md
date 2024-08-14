## OpenAI results
<iframe width="420" height="315" src="https://cdn.openai.com/openai-baselines-ppo/knocked-over-stand-up.mp4" frameborder="0" allowfullscreen></iframe>

The above video was released in a [2016 paper](https://arxiv.org/abs/1707.06347) by OpenAI. It shows how a PPO agent has been used to learn the behaviors of a humanoid robot. To establish control like this using RL was groundbreaking. The examples below show how I was able to establish control of a rotary inverted pendulum using a similar PPO agent (not so groundbreaking but still quite cool).

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_010.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
In this first video, the agent acts initially randomly as determined by the randomly initialized weights in the policy. The video is shorter than the others, as an early termination condition is produced (theta 1 rotates too far). 

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_044-swing.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
After 44 attempts at learning control, the agent learned how to swing. 

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_071-windmill.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
After swinging comes the stage I like to call "windmilling" at about 70 episodes.

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_107-balence-attempt.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
The controller then learns that balancing at the top of the swing might be a good idea, at 107 episodes.

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_172-balence.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
Finally, in this video at 172 and the next (at episode 240), we have a controller that can balance the pendulum in a specific position. It's been able to extract all this controlling behavior from its reward function. Further improvement wasn't observed after this. 

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_170-fin.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

