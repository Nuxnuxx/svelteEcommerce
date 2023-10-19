<footer>
  <div class="footer-content">
    <div class="footer-section">
      <h3>About Us</h3>
      <p>Learn more about our company.</p>
    </div>
    <div class="footer-section">
      <h3>Contact Us</h3>
      <p>Email: contact@example.com<br />Phone: +1 (123) 456-7890</p>
    </div>
    <div class="footer-section">
      <h3>Follow Us</h3>
      <p>Stay connected on social media.</p>
      <ul class="social-icons">
        <li><a href="/#"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b8/2021_Facebook_icon.svg/2048px-2021_Facebook_icon.svg.png" alt="Facebook" /></a></li>
        <li><a href="/#"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6f/Logo_of_Twitter.svg/584px-Logo_of_Twitter.svg.png" alt="Twitter" /></a></li>
        <li>
          <a href="/#"><img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="Instagram" /></a>
        </li>
      </ul>
    </div>
  </div>
</footer>

<style>
  footer {
    background-color: #222;
    color: #fff;
    padding: 20px 0;
  }

  .footer-content {
    display: flex;
    justify-content: space-between;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
  }

  .footer-section {
    flex: 1;
    padding: 0 20px;
  }

  .footer-section h3 {
    font-size: 20px;
    margin-bottom: 10px;
  }

  .footer-section p {
    font-size: 14px;
  }

  .social-icons {
    list-style: none;
    padding: 0;
    display: flex;
  }

  .social-icons li {
    margin-right: 10px;
  }

  .social-icons a {
    text-decoration: none;
    color: #fff;
  }

  .social-icons img {
    width: 40px;
  }
</style>
