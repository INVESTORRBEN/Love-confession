<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Love Note</title>
<style>
  body {
    font-family: 'Segoe UI', sans-serif;
    background: #ffe6f0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    margin: 0;
  }

  .note {
    background: #fff0f5;
    padding: 25px 35px;
    border-radius: 15px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    text-align: center;
    font-size: 1.3em;
    max-width: 400px;
    opacity: 1;
    transition: opacity 0.7s ease;
  }

  button {
    margin-top: 25px;
    padding: 12px 25px;
    border: none;
    background: #ff66b3;
    color: white;
    font-size: 1.1em;
    border-radius: 8px;
    cursor: pointer;
    transition: background 0.3s;
  }

  button:hover {
    background: #ff3399;
  }
</style>
</head>
<body>

<div class="note" id="note">
1. Hey my love 💕, my heart’s been holding a tiny secret for you.
</div>
<button id="nextBtn">Next</button>

<script>
  const messages = [
    "2. I’ve been dreaming of telling you this, just quietly, just us 🥰.",
    "3. This month made me fall for you even more 💖.",
    "4. How about one special day, just hugs, smiles, and us? 🌸",
    "5. Will you be my Valentine? 🐻💌"
  ];

  let currentIndex = 0;

  const noteDiv = document.getElementById('note');
  const button = document.getElementById('nextBtn');

  button.addEventListener('click', () => {
    if(currentIndex < messages.length){
      // Fade out
      noteDiv.style.opacity = 0;
      setTimeout(() => {
        noteDiv.textContent = messages[currentIndex];
        noteDiv.style.opacity = 1; // Fade in
        currentIndex++;
      }, 700); // Matches CSS transition
    } else {
      button.disabled = true;
      button.textContent = "💖 All done! 💖";
    }
  });
</script>

</body>
</html>
