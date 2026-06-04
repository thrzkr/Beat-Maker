const audioClips = {
  Q: { text: 'Heater 1' },
  W: { text: 'Heater 2' },
  E: { text: 'Heater 3' },
  A: { text: 'Heater 4' },
  S: { text: 'Clap' },
  D: { text: 'Open HH' },
  Z: { text: 'Kick n Hat' },
  X: { text: 'Kick' },
  C: { text: 'Closed HH' }
};

const playSound = (key) => {
  const audio = document.getElementById(key);
  if (!audio) return;

  // Requirement 9: Play the audio
  audio.currentTime = 0;
  audio.play();

  // Requirement 10: Update the display with unique text
  const displayText = audioClips[key].text;
  document.getElementById('display').innerText = displayText;

  // Visual feedback (Optional but helps debugging)
  const parent = audio.parentElement;
  parent.classList.add('active');
  setTimeout(() => parent.classList.remove('active'), 100);
};

// Mouse Click Event
document.querySelectorAll('.drum-pad').forEach(pad => {
  pad.addEventListener('click', () => {
    const audio = pad.querySelector('.clip');
    playSound(audio.id);
  });
});

// Keyboard Event
document.addEventListener('keydown', (e) => {
  const key = e.key.toUpperCase();
  if (audioClips[key]) {
    playSound(key);
  }
});