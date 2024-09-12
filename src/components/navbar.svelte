<script>
  // Define an array of navigation items
  const navItems = [
      { href: '#About', label: 'About Me' },
      { href: '#experiences', label: 'Experiences' },
      { href: '#skills', label: 'Skills' },
      { href: '#contact', label: 'Contact Information' }
  ];

  
  let activeLink = 'About';

  function setActive(link) {
      activeLink = link;
  }
</script>

<main>
<div>
  <nav>
    <h1>Karl's <span>Service</span></h1>
    <ul>
      {#each navItems as item}
        <li class:active={activeLink === item.href}>
          <a 
            href={item.href}
            
            on:click={() => setActive(item.href)}
          >
            {item.label}
          </a>
        </li>
      {/each}
    </ul>
  </nav>
</div>
</main>

<style>
  main{
    position: fixed;
    width: 100%;
    height: auto;
    background-color: #2a1c11;
    font-family: 'Poppins';
  }
  span {
    color: hsl(37, 70%, 69%);
    font-family: 'Poppins';
    font-weight: 800;
  }
  div {
    margin: 0;
  }
  nav {
    display: flex;
    margin: 0;
    margin: 1.8%;
    color: white;
  }
  h1 {
    font-weight: 600;
    font-family: 'Montserrat';
    font-size: 2em;
    margin-left: 1em;
  }
  ul {
    display: flex;
    margin-left: auto;
    margin-right: 2em;
    line-height: 3.5rem;
    list-style: none;
  }
  li {
    height: 2rem;
    margin-left: 2em;
    font-size: 1.2em;
    transition: 1s ease-in-out;
  }
  a {
    color: white;
    text-decoration: none;
  }   

  .active{
    font-weight: 500;
    background-color: #9e6d18;
    border-radius: 5px;
    font-size: 1.5em;
    line-height: 1rem;
  }
</style>
