<template>
  <div>
    <header class="header-bacgraund">
      <nav>
        <div class="header">
          <div class="logo">
            <a href="#">AppStarter</a>
          </div>
          <div class="list-style">
            <ul>
              <li><a href="#">Features</a></li>
              <li><a href="#">Video Tour</a></li>
              <li><a href="#">Reviews</a></li>
              <li><a href="#">Pricing</a></li>
              <li><a href="#" class="btn-get-it-free">GET IT FREE</a></li>
            </ul>
          </div>
        </div>
      </nav>
      <div class="app-store">
            <div class="app-store-block"> 
              <img src="./../assets/App-Icon.png" alt="app-store">
              <p><span>AppStarter.</span> Best landing page<br> for web and mobile apps </p>
              <div class="app-store-block-btn">
                <a href="#" class="btn-download">Download Now</a>
                <a href="#" class="btn-watch-vireo">Watch Video</a>
              </div>
            </div>
            <div class="block-tabl">
              <img src="./../assets/Tablet.png" alt="tabl">
            </div>
          </div>
    </header>
  </div>
</template>

<script>

import '../style/header.css'

export default {
  name: 'Header',
  props: {
    msg: String
  }
}
</script>


