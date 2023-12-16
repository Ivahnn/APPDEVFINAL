<template>
  <div class="footer-container">
    <section class="footer-subscription">
      <p class="footer-subscription-heading">
          Fake Bus conveniently and enjoyable of riding with us!
      </p>
      <p class="footer-subscription-text">
        Is there a concern? Email us!
      </p>
      <div class="input-areas">
        <form>
          <input
            class="footer-input"
            name="email"
            type="email"
            placeholder="Your Email"
          />
          <!-- Button removed -->
        </form>
      </div>
    </section>
    <div class="footer-links">
      <div class="footer-link-wrapper">
        <div class="footer-link-items">
          <h2>About Us</h2>
          <router-link to="/aboutus" style="color: white;">Our Beginnings</router-link>
          <router-link to="/aboutus" style="color: white;">The Story Behind the Name</router-link>
          <router-link to="/aboutus" style="color: white;">Meet the Team</router-link>
          <router-link to="/contactus" style="color: white;">Services</router-link>
        </div>
        <div class="footer-link-items" >
          <h2>Contact Us</h2>
          <router-link to="/contactus" style="color: white;">Contact us at:</router-link>
          <router-link to="/contactus" style="color: white;">+630924837123</router-link>
          <router-link to="/contactus" style="color: white;">890-3431-232</router-link>
          <router-link to="/contactus" style="color: white;">87000</router-link>

        </div>
      </div>
      <div class="footer-link-wrapper">
        <div class="footer-link-items">
          <h2 style="color: white;">Articles</h2>
          <a href="https://www.who.int/health-topics/medicines#tab=tab_1">
            Ride with us!
          </a>
          <a href="https://opt.who.foundation/?utm_source=google&utm_medium=cpc&gclid=Cj0KCQiA7OqrBhD9ARIsAK3UXh2WrnAS9MXXW2AbWeiwYS_td4tvluHAGpdI_ST5Gl4UcNJZqUCAevoaAlJREALw_wcB">
            Fake Bus!
          </a>
          <a href="https://www.who.int/emergencies/diseases/novel-coronavirus-2019">
            All in one bus!
          </a>
          <a href="https://opt.who.foundation/?utm_source=google&utm_medium=cpc&gclid=Cj0KCQiA7OqrBhD9ARIsAK3UXh235lL6gr7cyFltyErLd-zAG-gLcitvR2osBFDHitopCCa0jbLHnFYaAifEEALw_wcB">
            RIDE SO GOOD!
          </a>
        </div>
        <div class="footer-link-items">
          <h2>Social Media</h2>
          <a href="https://www.instagram.com/">Instagram</a>
          <a href="https://www.facebook.com/">Facebook</a>
          <a href="https://www.youtube.com/">Youtube</a>
          <a href="https://twitter.com/home">Twitter</a>
        </div>
      </div>
    </div>
    <section class="social-media">
      <div class="social-media-wrap">
        <div class="footer-logo">
          <router-link to="/" class="social-logo">
            FAKE BUS ON THE GO!
            <i class="fab fa-react"></i>
          </router-link>
        </div>
        <small class="website-rights">Fake Bus © 2023</small>
        <div class="social-icons">
          <router-link
            class="social-icon-link facebook"
            to="https://www.facebook.com/"
            target="_blank"
            aria-label="Facebook"
          >
            <i class="fab fa-facebook-f"></i>
          </router-link>
          <router-link
            class="social-icon-link instagram"
            to="https://www.instagram.com/"
            target="_blank"
            aria-label="Instagram"
          >
            <i class="fab fa-instagram"></i>
          </router-link>
          <router-link
            class="social-icon-link youtube"
            to="https://www.youtube.com/"
            target="_blank"
            aria-label="Youtube"
          >
            <i class="fab fa-youtube"></i>
          </router-link>
          <router-link
            class="social-icon-link twitter"
            to="https://twitter.com/home"
            target="_blank"
            aria-label="Twitter"
          >
            <i class="fab fa-twitter"></i>
          </router-link>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  // Add any component logic here if needed
};
</script>

<style scoped>
.footer-container {
 background-color: rgb(11, 31, 75);
  padding: 4rem 0 2rem 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.footer-subscription {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;

  margin-bottom: 24px;
  padding: 24px;
  color: #fff;
}

.footer-subscription > p {
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande',
    'Lucida Sans', Arial, sans-serif;
}

.footer-subscription-heading {
  margin-bottom: 24px;
  font-size: 24px;
}


.footer-subscription-text {
  margin-bottom: 24px;
  font-size: 20px;
}

.footer-input {
  padding: 8px 20px;
  border-radius: 2px;
  margin-right: 10px;
  outline: none;
  border: none;
  font-size: 18px;
  margin-bottom: 16px;
  border: 1px solid #fff;
}

.footer-links {
  width: 100%;
  max-width: 1000px;
  display: flex;
  justify-content: center;
}

.footer-link-wrapper {
  display: flex;
}

.footer-link-items {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin: 16px;
  text-align: left;
  width: 160px;
  box-sizing: border-box;
}

.footer-link-items h2 {
  margin-bottom: 16px;
}

.footer-link-items > h2 {
  color: #fff;
}

.footer-link-items a {
  color: #fff;
  text-decoration: none;
  margin-bottom: 0.5rem;
}

.footer-link-items a:hover {
  color: #e9e9e9;
  transition: 0.3s ease-out;
}

.footer-email-form h2 {
  margin-bottom: 2rem;
}

.footer-input::placeholder {
  color: #b1b1b1;
}

/* Social Icons */
.social-icon-link {
  color: #fff;
  font-size: 24px;
}

.social-media {
  max-width: 1000px;
  width: 100%;
}

.social-media-wrap {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 90%;
  max-width: 1000px;
  margin: 40px auto 0 auto;
}

.social-icons {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 240px;
}

.social-logo {
  color: #fff;
  justify-self: start;
  margin-left: 20px;
  cursor: pointer;
  text-decoration: none;
  font-size: 2rem;
  display: flex;
  align-items: center;
  margin-bottom: 16px;
}

.social-logo:hover {
  transition: all 0.2s ease-out;    
  color: #fff;
  text-decoration: none;
}

.website-rights {
  color: #fff;
  margin-bottom: 16px;
}
.footer-subscription-heading,
.footer-subscription-text,
.footer-link-items h2,
.footer-link-items a,
.social-icon-link,
.website-rights {
  font-weight: bold;
  color: #fff;
}
.footer-link-items a {
  color: #fff !important;
  text-decoration: none;
  margin-bottom: 0.5rem;
}

.footer-link-items a:hover {
  color: #e9e9e9 !important;
  transition: 0.3s ease-out;
}


@media screen and (max-width: 820px) {
  .footer-links {
    padding-top: 2rem;
  }

  .footer-input {
    width: 100%;
  }

  .btn {
    width: 100%;
  }

  .footer-link-wrapper {
    flex-direction: column;
  }

  .social-media-wrap {
    flex-direction: column;
  }
}

@media screen and (max-width: 768px) {
  /* Add styles for smaller screens if needed */
}
</style>
