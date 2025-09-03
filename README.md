<!# htmlcodebymohnish
made a html code which runs>
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Hogwarts Wizarding School</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- this is a joke website hahahah!! -->
</head>
<body>

  <header>
    <img 
      src="C:\Users\Acer\Pictures\hogwarts-school-crest-pv4xvgmcp4jc8grf.jpg"
      srcset="C:\Users\Acer\Pictures\hogwarts-school-crest-pv4xvgmcp4jc8grf.jpg" 
      alt="Hogwarts Crest" 
      width="120" 
      height="120"
      loading="lazy">
    <h1>Hogwarts School of Witchcraft and Wizardry</h1>
    <p>Educating Young Witches and Wizards Since 993 A.D.</p>
  </header>

  <nav>
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#houses">Houses</a></li>
      <li><a href="#sorting-ceremony">Sorting Ceremony</a></li>
      <li><a href="#gallery">Gallery</a></li>
      <li><a href="#faculty">Faculty</a></li>
      <li><a href="#testimonials">Testimonials</a></li>
      <li><a href="#newsletter">Owl Post</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <main>

    <section id="about">
      <h2>About Hogwarts</h2>
      <p>
        Hogwarts has been the premier magical academy in Britain for over a millennium.  
        We foster bravery, wisdom, loyalty, and ambition in every student.
      </p>
    </section>

    <section id="houses">
      <h2>The Four Houses</h2>

      <article>
        <h3>Gryffindor</h3>
        <img src="C:\Users\Acer\Downloads\godrcgyrffindo.png"><br>
        <p><strong>Founder:</strong> Godric Gryffindor</p>
        <p><strong>Colors:</strong> Scarlet & Gold</p>
        <p>
          Established in 993 A.D., Gryffindor champions bravery and chivalry.  
          Its emblematic lion roars at the heart of courage.
        </p>
      </article>

      <article>
        <h3>Hufflepuff</h3>
        <img src="C:\Users\Acer\Downloads\elgahufflepuff.png"><br>
        <p><strong>Founder:</strong> Helga Hufflepuff</p>
        <p><strong>Colors:</strong> Yellow & Black</p>
        <p>
          Valuing hard work, patience, and loyalty, Hufflepuff embraces all who are fair and just.  
          Its badger symbolizes determination.
        </p>
      </article>

      <article>
        <h3>Ravenclaw</h3>
         <img src="C:\Users\Acer\Downloads\ravenclaw.png"><br>
        <p><strong>Founder:</strong> Rowena Ravenclaw</p>
        <p><strong>Colors:</strong> Blue & Bronze</p>
        <p>
          Dedicated to intelligence and learning, Ravenclaw rewards wit and wisdom.  
          Its eagle soars high above the clouds of thought.
        </p>
      </article>

      <article>
        <h3>Slytherin</h3>
        <img src="C:\Users\Acer\Downloads\slyth.png"><br>
        <p><strong>Founder:</strong> Salazar Slytherin</p>
        <p><strong>Colors:</strong> Green & Silver</p>
        <p>
          Slytherin prizes ambition and resourcefulness.  
          Its serpent glides through the darker currents of cunning.
        </p>
      </article>
    </section>

    <section id="sorting-ceremony">
      <h2>Virtual Sorting Ceremony</h2>
      <label for="wizardName">Enter your name:</label>
      <input type="text" id="wizardName" placeholder="e.g. Hermione Granger">
      <button id="sortButton">Sort Me!</button>
      <p id="result"></p>


    <form>

Username: <input type="text" placeholder="Enter Username" minlength="3" maxlength="15" required> <br> <br>

Password: <input type="password" placeholder="Enter Password" minlength="6" maxlength="12" required> <br> <br>

Gender: <br> <br>

Male: <input type="radio"> Female: <input type="radio"> <br> <br>

Subject:(only to be take if you are accepted)<br><br>

<input type="checkbox"> Potions<br> 

<input type="checkbox">Defence Against the Dark Arts <br> 

<input type="checkbox">History of Magic <br>

<input type="checkbox"> Charms<br> 

<input type="checkbox"> Astronomy<br> <br>

Date:<input type="date"><br> <br>

Contact Information:<input type="number" placeholder="1234567890" maxlength="10" required> <br> <br> 

Email: <input type="email" placeholder="harrypotter@wizardmail.com"> <br> <br> 

<input type="file" multiple> <br> <br> 


<input type="submit"> 

<input type="reset"> 

<input type="button" value="clear"> <br> <br>





     </form>

<a href="https://www.google.com"> <input type="button" value="Next"> </a> <br>

      <script>
        (function(){
          const houses = [
            "Gryffindor",
            "Hufflepuff",
            "Ravenclaw",
            "Slytherin"
          ];
          const btn = document.getElementById("sortButton");
          const result = document.getElementById("result");

          btn.addEventListener("click", function(){
            const name = document.getElementById("wizardName").value.trim() || "Young Witch or Wizard";
            result.textContent = "The Sorting Hat is thinking...";
            let i = 0;
            const cycle = setInterval(() => {
              result.textContent = houses[i % houses.length];
              i++;
            }, 150);

            setTimeout(() => {
              clearInterval(cycle);
              const chosen = houses[Math.floor(Math.random() * houses.length)];
              result.textContent = `Congratulations, ${name}! You have been sorted into ${chosen}!`;
            }, 2000);
          });
        })();
      </script>
    </section>

    <section id="gallery">
      <h2>Gallery</h2>
      <img 
        src="images/great-hall.jpg" 
        srcset="images/great-hall@2x.jpg 2x" 
        alt="The Great Hall" 
        loading="lazy">
      <img 
        src="images/quidditch.jpg" 
        srcset="images/quidditch@2x.jpg 2x" 
        alt="Quidditch Match" 
        loading="lazy">
      <img 
        src="images/library.jpg" 
        srcset="images/library@2x.jpg 2x" 
        alt="Hogwarts Library" 
        loading="lazy">
      <img 
        src="images/potions.jpg" 
        srcset="images/potions@2x.jpg 2x" 
        alt="Potions Classroom" 
        loading="lazy">
    </section>

    <section id="faculty">
      <h2>Our Esteemed Faculty</h2>
      <ul>
        <li><strong>Albus Dumbledore</strong> – Headmaster (Gryffindor)</li>
        <li><strong>Minerva McGonagall</strong> – Transfiguration & Deputy Headmistress (Gryffindor)</li>
        <li><strong>Severus Snape</strong> – Potions & Defense Against the Dark Arts (Slytherin)</li>
        <li><strong>Filius Flitwick</strong> – Charms (Ravenclaw)</li>
        <li><strong>Pomona Sprout</strong> – Herbology (Hufflepuff)</li>
        <li><strong>Sybill Trelawney</strong> – Divination (Ravenclaw)</li>
        <li><strong>Rubeus Hagrid</strong> – Care of Magical Creatures (Gryffindor)</li>
        <li><strong>Horace Slughorn</strong> – Potions (Slytherin)</li>
        <li><strong>Cuthbert Binns</strong> – History of Magic (Ghost)</li>
        <li><strong>Bathsheba Babbling</strong> – Ancient Runes (Ravenclaw)</li>
        <li><strong>Rolanda Hooch</strong> – Flying Instructor & Quidditch Referee</li>
      </ul>
    </section>

    <section id="testimonials">
      <h2>Student Testimonials & News</h2>

      <article>
        <h3>“The Triwizard Tournament was the highlight of my year!”</h3>
        <p>– Viktor Krum, Durmstrang Champion</p>
      </article>

      <article>
        <h3>“Studying dragons under Hagrid’s guidance changed my life.”</h3>
        <p>– Newt Scamander, Magizoologist</p>
      </article>

      <article>
        <h3>“The Sorting Ceremony gave me the courage to be myself.”</h3>
        <p>– Luna Lovegood, Ravenclaw</p>
      </article>
    </section>

    <section id="newsletter">
      <h2>Owl Post Newsletter</h2>
      <form id="newsletterForm">
        <label for="owlEmail">Your Owl Post Address:</label>
        <input 
          type="email" 
          id="owlEmail" 
          name="email" 
          placeholder="you@owlpost.com" 
          required>
        <button type="submit">Subscribe</button>
      </form>
      <script>
        document.getElementById("newsletterForm")
          .addEventListener("submit", function(e){
            e.preventDefault();
            const email = this.email.value;
            alert(`Thank you! Owls will carry your news to ${email}.`);
            this.reset();
          });
      </script>
    </section>

    <section id="contact">
      <h2>Contact Us</h2>
      <p>
        <strong>Address:</strong> Hogwarts Castle, Highlands of Scotland<br>
        <strong>Phone:</strong> +44 (0)1234 567890<br>
        <strong>Email:</strong> info@hogwarts.ac.uk
      </p>
    </section>

  </main>

</body>
</html>
