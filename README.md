# dynamic_counter
HTML/JavaScript dynamic counter

```html
<span class="value" count="136">0</span>
<span class="value" count="3865">0</span>
<span class="value" count="35">0</span>


<script>
    const counters = document.querySelectorAll('.value');
    const speed = 250;

    counters.forEach(counter => {
      const animate = () => {
        const value = +counter.getAttribute('count');
        const data = +counter.innerText;
      
        const time = value / speed;

        if (data < value) {
          counter.innerText = Math.ceil(data + time);
          setTimeout(animate, 1);
        } else {
          counter.innerText = value;
        }
      }
    
      animate();
    });
  </script>
  ```
