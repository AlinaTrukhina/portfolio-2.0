<script>
  import {
    Collapse,
    Navbar,
    NavbarToggler,
    NavbarBrand,
    Nav,
    NavItem,
    NavLink,
  } from 'sveltestrap';

	import { Styles } from 'sveltestrap';
	
  let isOpen = false;

  function handleUpdate(event) {
    isOpen = event.detail.isOpen;
  }
      
</script>


<Navbar dark expand="md" style="background-color: var(--color-theme-darkblue)">
    <NavbarBrand href="/projects" style="color: var(--color-theme-2)">Project List</NavbarBrand>
    <NavbarToggler on:click={() => (isOpen = !isOpen)} style="color: var(--color-theme-2)"/>
    <Collapse {isOpen} navbar expand="md" on:update={handleUpdate}>
      <Nav class="ms-auto" navbar>
        <NavItem>
          <NavLink class="navlink" href="/projects/craigslist-web-scraper">CLI Web Scraper</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/projects/foraging-finds">Foraging Finds</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/projects/womens-health-directory-vifi">The ViFi, a Women's Health Directory</NavLink>
        </NavItem>
        <NavItem>
            <NavLink href="/projects/react-photo-gallery">React Photo Gallery</NavLink>
        </NavItem>        
        <NavItem>
            <NavLink href="/projects/server-side-calculator">Server-Side Calculator</NavLink>
        </NavItem>
        <NavItem>
            <NavLink href="/projects/react-redux-movie-gallery">React-Redux Movie Gallery</NavLink>
        </NavItem>
      </Nav>
    </Collapse>
</Navbar>

<style>

/* @import 'https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css'; */

/* .navlink {
  color: var(--color-theme-2-light);
} */

</style>