##OpenAI results
<iframe width="420" height="315" src="https://cdn.openai.com/openai-baselines-ppo/knocked-over-stand-up.mp4" frameborder="0" allowfullscreen></iframe>

The above video was relesed in a 2016 paper by open AI. it shows how a PPO agent has been used to learn the behvaiors of a humanoid robot. To establish control like this using RL was groundbreaking. The examples below show how I was able to establish control of a rotarty inverted pendulum using a similar PPO agent (not so groundbreaking but still quite cool). 

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_010.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
In this first video, the agent acts initially randomly as determined by the randomly initialised weights in the policy.


<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_044-swing.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
after 44, attempts at learning control, the agent learnt how to swing. 

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_071-windmill.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

after swinging comes the stage I like to call "windmilling at about 70 episodes. 

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_107-balence-attempt.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

the controller then learns that balencing at the top of the swing might be a good idea, at 107 episodes. 

<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_172-balence.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
Finally in this video and the next we have a controller that can balance the pendulum, in a specific position. It's been able to extract all this controlling behaviour from it's reward function.
<video width="420" height="315" controls>
  <source src="{{ '/assets/videos/episode_170-fin.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>






