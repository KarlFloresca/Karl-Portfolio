<script>
  import Section from "./section.svelte";
  import Listmaker from "./listmaker.svelte";
  let languages = [
    {
      icon: "fa-brands fa-java",
      label: "Java",
    },
    {
      icon: "fa-brands fa-python",
      label: "Python",
    },
    {
      icon: "fa-brands fa-html5",
      label: "HTML",
    },
    {
      icon: "fa-brands fa-css3-alt",
      label: "CSS",
    },
    {
      icon: "fa-brands fa-js",
      label: "JavaScript",
    },
    {
      label: "Typescript",
    },
    {
      label: "Visual Basic",
    },
    {
      label: "SQL",
    },
    {
      label: "C#",
    },
  ];

  let softwareList = [
    {
      label: "VScode and Visual Studio",
    },
    {
      label: "InteliJ",
    },
    {
      label: "Pycharm",
    },
    {
      label: "Filmora",
    },
    {
      label: "Adobe Photoshop",
    },
    {
      label: "Figma",
    },
    {
      label: "Canva",
    },
    {
      label: "Krita",
    },
  ];

  let frameworks = [
    {
      label: "React",
    },
    {
      label: "Sveltekit",
    },
    {
      label: "Bootstrap",
    },
    {
      label: "Pygame",
    },
    {
      label: "Tailwind CSS",
    },
    {
      label: "Supabase",
    },
  ];

  let prac = [
    {
      label: "Computer programming",
    },
    {
      label: "Web design",
    },
    {
      label: "Front/Backend web development",
    },
    {
      label: "video editing",
    },
    {
      label: "Basic animation",
    },
    {
      label: "Digital Art",
    },
  ];

  let learning = [
    {
      label: "Supabase for data base",
    },
    {
      label: "Pocketbase also for data base",
    },
    {
      label: "Django",
    },
    {
      label: "Advance animation",
    },
    {
      label: "C++",
    },
    {
      label: "3d Modelling",
    },
  ];
</script>

<main>
  <h3>
    <span>My</span> current skills Languages and Tools
  </h3>
  <section class="layer1">
    <div>
      <Section title="Practical Skills"
        ><Listmaker itemList={prac}></Listmaker></Section
      >
    </div>
    <div class="languages">
      <Section
        icon="fa-solid fa-keyboard"
        title="Languages for development"
        id="languages"><Listmaker itemList={languages} /></Section
      >
    </div>
    <div class="softwares">
      <Section
        icon="fa-brands fa-uncharted"
        title="Softwares used"
        id="softwares"><Listmaker itemList={softwareList} /></Section
      >
    </div>
  </section>

  <section class="layer2">
    <div>
      <h2>Frame<span>Works</span> and Libraries</h2>
      <Listmaker itemList={frameworks}></Listmaker>
    </div>

    <div>
      <h2>What I'm <span>learning</span></h2>
      <Listmaker itemList={learning}></Listmaker>
    </div>
  </section>
</main> 

<style>
  main {
    background-color: #fcf0db;
    height: auto;
  }
  section {
    margin-top: 0;
    display: flex;
    justify-content:center;
    gap: 40px;
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
  
  .layer2 div {
    padding: 30px 30px 35px 35px;
    background-color: #4b3200;
    color: #eae4cf;
    border-radius: 10px;
    font-size: 15px;
    width: 30rem;
    line-height: 50px;
  }

  div {
    width: 40em;
    height: auto;
    margin: 25px;
    border-radius: 10px;
    margin-top: 2em;
    box-shadow: 10px 8px 15px 1px rgb(99, 99, 99);
  }
  .layer2 div:hover{
    background-color: black;
    color: white;
    padding: 45px 45px 45px 45px;
    transition: 1s;
    transition-timing-function: ease-in-out;
  }
  span {
    color: #fad89e;
  }
</style>
