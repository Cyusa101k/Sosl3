<template>
  <footer class="site-footer">
    <div class="footer-content">
      <section class="footer-column">
        <h2>TEMBERURWANDA</h2>
        <p>Discover the beauty of Rwanda</p>
      </section>

      <nav class="footer-column" aria-label="Quick links">
        <h2>Quick Links</h2>
        <ul>
          <li><RouterLink to="/">Home</RouterLink></li>
          <li><RouterLink to="/about">About</RouterLink></li>
          <li><RouterLink to="/services">Services</RouterLink></li>
          <li><RouterLink to="/contact">Contact</RouterLink></li>
        </ul>
      </nav>

      <nav class="footer-column" aria-label="Destinations">
        <h2>Destination</h2>
        <ul>
          <li><RouterLink to="/services">Kigali City</RouterLink></li>
          <li><RouterLink to="/services">Northern Province</RouterLink></li>
          <li><RouterLink to="/services">Southern Province</RouterLink></li>
          <li><RouterLink to="/services">Eastern Province</RouterLink></li>
          <li><RouterLink to="/services">Western Province</RouterLink></li>
        </ul>
      </nav>

      <section class="footer-column">
        <h2>Contacts</h2>
        <p>123 Main street, Kigali</p>
        <p>Phone: +250 788 000 456</p>
        <RouterLink to="/contact">Contact us</RouterLink>
      </section>
    </div>

    <p class="footer-copy">&copy; 2025 Visit Rwanda. All rights reserved.</p>
  </footer>
</template>
