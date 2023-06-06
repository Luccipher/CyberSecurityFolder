# CyberSecurityFolder
// Get the text element
const text = document.getElementById('Chris Tapia');

// Set the initial position of each letter
const positions = [];
for (let i = 0; i < text.innerHTML.length; i++) {
  positions[i] = 0;
}

// Define the vibration function
function vibrate() {
  for (let i = 0; i < text.innerHTML.length; i++) {
    // Generate a random offset to the position
    const offset = Math.floor(Math.random() * 6) - 3;
    // Update the position with the offset
    positions[i] += offset;
    // Apply the new position to the letter
    const letter = text.innerHTML.charAt(i);
    const style = 'position:relative; display:inline-block; left:' + positions[i] + 'px;';
    text.innerHTML = text.innerHTML.substring(0, i) + '<span style="' + style + '">' + letter + '</span>' + text.innerHTML.substring(i+1);
  }
}

// Call the vibration function every 100ms
setInterval(vibrate, 100);
