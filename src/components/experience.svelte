<script>
  import Projectcard from "./projectcard.svelte";

  let projectOBJ = [
    {
      pic: "./images/Journey.png",
      label: "Journey through prelict",
      link: "https://drive.google.com/drive/folders/19acfA0y4TUYuYtoZL4cOgWcUAdetJ05d?usp=sharing",
      description:
        "Made with JAVA, a simple game that fallows an adventurer running in the lands of prelict gathering artifacts that were lost in history",
    },
    {
      pic: "./images/WebProject.png",
      label: "The Coffee Lounge",
      link: "https://drive.google.com/drive/folders/1_O5122ZfKXV0hv72XM2QD_CCrPBgzlup?usp=sharing",
      description:
        "Utilizing vanila HTML, CSS, and Javascript we Created a website as a requirement for our final project developed alongside my groupmates who mainly handled the logistics",
    },
    {
      pic: "./images/orderSystem.png",
      label: "Ordering System",
      description:
        "Created using visual basic, a system that handles orders for convience, this system was made during my first year in college to expand my knowledge",
      link: "https://drive.google.com/drive/folders/1YAzRKfML25BvX4WzVeH4cUp0Ae03Lc3j?usp=sharing",
    },
  ];

  let experienceList;

  const scrollLeft = () => {
    experienceList.scrollBy({ left: -500, behavior: "smooth" });
  };

  const scrollRight = () => {
    experienceList.scrollBy({ left: 500, behavior: "smooth" });
  };
</script>

<main>
  <h3 class="exp">
    <span>My</span> Experiences
  </h3>

  <button class="leftButton" on:click={scrollLeft}>⬅</button>
  <button class="rightButton" on:click={scrollRight}>➡</button>

  <div class="experienceList" bind:this={experienceList}>
    <div>
      <p>
        During my first year of college, I collaborated with the owner of a small coffee shop to
         develop a custom website as part of a final examination project. The project was a key 
         requirement for my web development course, and it provided a real-world opportunity to apply 
         the skills I had learned. I was responsible for designing and building the website from the ground up, 
         using HTML, CSS, and JavaScript to create an intuitive user interface that reflected the unique 
         personality of the coffee shop.
      </p>
      <img src="./images/webproject2.png" alt="documentaion of web project" class="mainImg" />
      
    </div>
    <div>
      <p>
        Worked with a little animation project as a request of an acquaintance
        in my Highschool days. I've spent a portion of my highschool life doing
        digital art and even now i still retain some knowledge and used it in a
        midterm project called python the musical, it served as an intro for our
        group.
      </p>
      <!-- svelte-ignore a11y-media-has-caption -->
      <video src="./images/animation.mp4" autoplay loop> </video>
    </div>
    <div>
      <p>
        Outside of school I’ve been working on learning and immersing myself on
        various frameworks and libraries like this website which is made from
        the sveltekit framework.
      </p>

      <img src="./images/Frameworks.png" alt="" />
    </div>
    <div>
      <p>
        Lastly during my last year of high-school i was deployed for work
        immersion in my local government unit, i was assigned within the
        Municipal treasurer office, i was mainly tasked with arranging and
        sorting of paper works and encoding.
      </p>
      <img src="./images/imersion.png" alt="Work imersion documentations">
    </div>
  </div>
</main>

<h3 class="">
  Here are some of my <span class="project">Projects</span>
</h3>

<section>
  {#each projectOBJ as obj}
    <Projectcard
      pic={obj.pic}
      label={obj.label}
      description={obj.description}
      link={obj.link}
    ></Projectcard>
  {/each}
</section>

<style>
  main {
    color: rgb(61, 41, 0);
    background-color: #ffffff;
    height: auto;
    text-align: center;
  }
  span {
    color: #fad89e;
  }
 
  p {
    text-indent: 5rem;
    min-width: 20vw;
    font-size: 20px;
    text-align: justify;
  }

  .experienceList {
    display: flex;
    overflow-x: auto;
    justify-content: space-between;
    scroll-snap-type: x mandatory;
  }

  .experienceList div {
    font-size: 20px;
    display: flex;
    flex-shrink: 0;
    width: 80vw;
    padding: 3rem 8rem 3em 8em;
    text-align: center;
    gap: 90px;
    scroll-snap-align: start;
  }

  .experienceList img{
    width: 30rem;
    height: 24rem;
  }
  .experienceList video {
    width: 35rem;

    height: auto;
  }

  section {
    display: flex;
    justify-content: center;
    height: auto;
    background-color: #f9f1e5;
    padding: 3em;
  }

  h3 {
    font-size: 2em;
    background-color: rgb(30, 30, 30);
    margin: 0;
    padding: 0.9em;
    color: white;
    font-family: "Montserrat";
    text-align: center;
  }
</style>
