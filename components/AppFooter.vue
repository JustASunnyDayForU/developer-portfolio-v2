<script>
export default {
    name: 'AppFooter',
    data() {
        return {
          route: this.$route.path,
        }
    },
    setup() {
        return {
            social: useRuntimeConfig().dev.contacts.social
        }
    },
}
</script>

<template>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <footer>
        <div class="footer-content">
            <h4>BANGKOK SALES OFFICE</h4>
            <h4>.</h4>
            <h4>.</h4>
            <p>Rimpae Management Co.,Ltd.
            <br>33/4 Soi Sukhumvit46 ,Sukhumvit Rd.
            <br>Prakanong ,Klongtoey ,Bangkok 10110
            </p>
            <ul class="socials">
                <li><a href="#"><i class="fa fa-facebook"></i></a></li>
                <li><a href="#"><i class="fa fa-instagram"></i></a></li>

            </ul>

        </div>

        <div class="footer-bottom">


        </div>

    </footer>
</template>

<style>
footer {
  position: relative;
  bottom: 0;
  left: 0;
  right: 0;
  background: #ffffff;
  height: auto;
  width: auto;
  padding-top: 40px;
  color: #000000;
}

.footer-content {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  text-align: center;
  color: gray;
}

.footer-content h3 {
  font-size: 2.1rem;
  font-weight: 500;
  text-transform: capitalize;
  line-height: 3rem;
  color: gray;
}

.footer-content p {
  max-width: 500px;
  margin: 10px auto;
  line-height: 28px;
  font-size: 14px;
  color: gray;
}

.socials {
  list-style: none;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 1rem 0 3rem 0;
}

.socials li {
  margin: 0 10px;
}

.socials a {
  text-decoration: none;
  padding: 5px;
}

.socials a i {
  color: gray;
  font-size: 2rem;
  width: 20px;
  transition: color 0.4s ease;
}

.socials a:hover i {
  color: aqua;
}

.footer-bottom {
  background: #a0a09f;
  width: auto;
  padding: 20px;
  padding-bottom: 20px;
  text-align: center;
}

.footer-bottom p {
  float: left;
  font-size: 14px;
  word-spacing: 2px;
}

.footer-bottom p a {
  color: #ccc;
  font-size: 16px;
  text-decoration: none;
}

.footer-bottom span {
  text-transform: uppercase;
}

.footer-menu {
  float: right;
}

.footer-menu ul {
  display: flex;
}

.footer-menu ul li {
  padding-right: 10px;
  display: block;
}

.footer-menu ul li a {
  color: #cfd2d6;
  text-decoration: none;
}

.footer-menu ul li a:hover {
  color: #27bcda;
}

@media (max-width: 500px) {
  .footer-bottom p {
    float: none;
  }

  .footer-menu ul {
    display: flex;
    margin-top: 10px;
    margin-bottom: 20px;
    text-align: center;
  }
}

</style>
