## Welcome to My Profile! 👋

### About Me
I'm passionate about coding, technology, and learning new things.

### Skills
- JavaScript
- Python
- HTML/CSS
- ...

### Projects
- Project 1
- Project 2
- ...

### Let's Connect!
- [LinkedIn](your_linkedin_profile_link)
- [Twitter](your_twitter_profile_link)
- ...

---

<!-- Typing Effect Animation -->
<div style="display: inline-block;">
  <p id="typing-text"></p>
</div>

<script>
  const textArray = ["Hello!", "Welcome to my profile.", "I'm glad you're here!"];
  let textIndex = 0;
  let charIndex = 0;
  const typingText = document.getElementById('typing-text');

  function type() {
    if (charIndex < textArray[textIndex].length) {
      typingText.innerHTML += textArray[textIndex].charAt(charIndex);
      charIndex++;
      setTimeout(type, 100); // Adjust typing speed here
    } else {
      setTimeout(erase, 1500); // Adjust delay before erasing
    }
  }

  function erase() {
    if (charIndex > 0) {
      typingText.innerHTML = textArray[textIndex].substring(0, charIndex - 1);
      charIndex--;
      setTimeout(erase, 50); // Adjust erasing speed here
    } else {
      textIndex++;
      if (textIndex >= textArray.length) {
        textIndex = 0;
      }
      setTimeout(type, 500); // Adjust delay before typing next sentence
    }
  }

  document.addEventListener('DOMContentLoaded', function() {
    setTimeout(type, 1000); // Adjust delay before starting typing
  });
</script>
