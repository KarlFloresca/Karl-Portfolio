<script>
  import Navbar from "./components/navbar.svelte";
  import Profile from "./components/profile.svelte";
  import Experience from "./components/experience.svelte";
  import Skills from "./components/skills.svelte";
  import Footer from "./components/footer.svelte";
</script>

<head>
  <link
    href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;800&display=swap"
    rel="stylesheet"
  />
  <link
    href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;800&display=swap"
    rel="stylesheet"
  />
</head>

<main>
  <Navbar />
  <div class="About" id="About">
    <Profile />
  </div>
  <div class="experiences" id="experiences">
    <Experience />
  </div>
  <div class="skills" id="skills">
    <Skills />
  </div>
  <div id="contact"><Footer /></div>
</main>

<style>
  .About {
    padding-top: 10px;
    height: 48em;
  }
  .experiences {
    background-color: #f9f1e5;
    margin: 0;
  }
  * {
    background-color: #f9f1e5;
    font-family: "poppins";
  }
</style>
