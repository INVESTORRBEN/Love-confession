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
    padding: 20px 30px;
    border-radius: 15px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    text-align: center;
    font-size: 1.2em;
    max-width: 400px;
    transition: opacity 0.5s;
  }

  button {
    margin-top: 20px;
    padding: 10px 20px;
    border: none;
    background: #ff66b3;
    color: white;
    font-size: 1em;
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
      noteDiv.textContent = messages[currentIndex];
      currentIndex++;
    } else {
      button.disabled = true;
      button.textContent = "💖 All done! 💖";
    }
  });
</script>

</body>
</html>
