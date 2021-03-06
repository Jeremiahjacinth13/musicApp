<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Music_For_The_Soul</title>
  <script src="all.js"></script>
  <link rel="stylesheet" href="font-awesome.css">
  <link rel="stylesheet" href="style.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    .introSection {
      position: absolute;
      width: 100vw;
      height: 100vh;
      background: url('assets/images/7.jpeg') no-repeat center top;
      background-size: cover;
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 5;
    }

    .introSection {
      animation: introSection 0.5s 3s forwards cubic-bezier(0.55, 0.085, 0.68, 0.53);
      /* display: none; */
    }

    @keyframes introSection {
      from {
        z-index: 1;
        transform: translateX(0);
      }

      to {
        transform: translateX(-100%);
      }
    }

    .introSection .wrapper {
      z-index: 1;
      position: relative;
    }

    .introSection_overlay {
      position: absolute;
      top: 0;
      width: 100vw;
      height: 100vh;
      background: linear-gradient(to bottom, rgb(0, 0, 0), rgba(0, 0, 0, 0.7));
    }

    .logo {
      margin: auto;
      width: 130px;
      height: 130px;
      border: 2px solid;
      border-radius: 50%;
      border-color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      background: rgba(184, 22, 76, 0.212);
      position: relative;
    }

    .logo h1 {
      font-size: 3.5rem;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
      background: linear-gradient(to bottom left, blue, orange);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
    }

    p#brand {
      font-size: 1.5rem;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
      color: rgb(231, 231, 231);
      text-align: center;
      margin-top: 20px;
      text-align: center;
    }

    @keyframes roller {
      100% {
        transform: rotate(360deg);
      }
    }

    .roller {
      width: 16px;
      height: 16px;
      border: 2px solid purple;
      border-top-color: transparent;
      border-radius: 50%;
      animation: roller 1s infinite linear;
      margin-right: 10px;
    }

    #loading {
      color: purple;
      font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
      font-size: 15px;
      -webkit-font-smoothing: antialiased;
    }

    .stuff,
    .clean {
      margin-top: 20px;
      width: 150px;
      display: flex;
      justify-content: center;
      align-items: center;
      border-radius: 10rem;
      background: linear-gradient(to bottom left, rgba(255, 0, 0, 0.7), rgba(128, 0, 128, 0.7));
      padding: 5px;
    }

    .clean {
      margin: 0;
      padding: 7px;
      background: white;
    }

    .logo svg {
      color: white;
      position: absolute;
      z-index: 2;
      top: 8px;
      right: 0px;
      font-size: 25px;
    }
  </style>
  <!-- Main Section -->
  <style>
    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    }

    .mainSection {
      height: 100%;
    }

    .header {
      /* background: white; */
      width: 100%;
      height: 70px;
    }

    .mainSection .header .top {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .tabLinks {
      display: inline;
      font-size: 14px;
      margin-right: 10px;
    }

    .tabLinks.active {
      font-size: 22px;
      font-weight: 400px;
    }

    .menu-bar svg,
    .extras svg {
      color: white
    }

    .mainTabs {
      display: flex;
      align-items: center;
    }

    .searchDummy {
      width: 100%;
      height: 30px;
      border-radius: 10rem;
      background: rgb(68, 68, 68);
      color: white;
      position: relative;
      margin-top: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .searchDummy input {
      width: 100%;
      height: 100%;
      color: white;
      background: transparent;
      position: absolute;
      top: 0;
      left: 0;
      font-size: 15px;
      border-radius: 10rem;
      border: none;
      appearance: none;
      outline: none;
      text-align: center;
    }

    .dummyText {
      display: none;
      text-align: center;
      color: white;
      font-weight: lighter;
      font-size: 15px;
    }

    .dummyText svg {
      margin-right: 10px;
    }

    .extrasValue {
      position: absolute;
      right: 0;
      top: 56px;
      display: none;
    }

    .extrasValue.active {
      display: block;
      z-index: 1;
    }

    .mainSection {
      padding-top: 20px;
      padding-bottom: 20px;
    }

    .extrasValue ul {
      display: flex;
      align-items: center;
      flex-direction: column;
      z-index: 2;
    }

    .extrasValue li {
      list-style: none;
      padding: 10px;
      width: 150px;
      height: 50px;
      background: rgb(83, 81, 81);
      color: white;
      font-size: 14px;
      border-left: 2px solid white;
    }

    .extrasValue li:first-of-type {
      border-top-left-radius: 5px;
      border-top-right-radius: 5px;
    }

    .extrasValue li:last-of-type {
      border-bottom-left-radius: 5px;
      border-bottom-right-radius: 5px;
    }

    .extrasValue li svg {
      margin-right: 10px;
    }

    .container {
      width: 90%;
      margin: auto;
    }

    .menubarContent {
      width: 80vw;
      height: 100vh;
      background: rgb(139, 139, 139);
      position: absolute;
      top: 0;
    }

    .menubarContent {
      transform: translateX(-100%);
      z-index: 3;
      transition: all 0.5s;
    }

    .menubarContentOverlay.active {
      width: 100vw;
      height: 100vh;
      top: 0;
      right: 0;
      z-index: 2;
      position: absolute;
      background: rgba(0, 0, 0, 0.8);
      animation: opacityChange 0.5 forwards linear;
    }

    .menubarItems {
      padding: 30px;
    }

    .menubarItems .list-group {
      margin-top: 30px;
    }

    .menubarItems .list-group li {
      color: white;
      margin-bottom: 10px;
      list-style: none;
      font-weight: lighter;
    }

    .list-group li svg {
      margin-right: 15px;
    }
    
  </style>
</head>

<body>
  <div class="introSection">
    <div class='wrapper'>
      <div class="logo">
        <i class="fa fa-music"></i>
        <h1>BM</h1>
      </div>
      <p id=brand>
        Bleeng Music
      </p>
      <div class="stuff">
        <div class="clean">
          <div class="roller"></div>
          <p id=loading>Loading</p>
        </div>
      </div>
    </div>
    <div class="introSection_overlay"></div>
  </div>
  <div class="mainSection">
    <div class="menubarContent">
      <ul class="menubarItems">
        <div class="list-group">
          <li><i class="fa fa-gem"></i>Subscribe</li>
          <li><i class="fa fa-folder"></i>Recharge </li>
          <li><i class="fa fa-gift"></i>Get Freebies</li>
          <li><i class="fab fa-bitcoin"></i>Transfer Coins</li>

        </div>
        <div class="list-group">
          <li><i class="fa fa-comment"></i>Notifications</li>
          <li><i class="fab fa-gratipay"></i>My Pre-orders</li>
          <li><i class="fa fa-user-circle"></i>My Profile</li>
        </div>
        <div class="list-group">
          <li><i class="fab fa-twitch"></i>Theme</li>
          <li><i class="fa fa-gear"></i>Settings</li>
        </div>
      </ul>
    </div>
    <div class="menubarContentOverlay"></div>
    <div class="container">
      <div class="header">
        <div class="top">
          <div class="menu-bar">
            <i class="fa fa-bars"></i>
          </div>
          <ul class="mainTabs">
            <li class="tabLinks active">Library</li>
            <li class="tabLinks">Music</li>
            <li class="tabLinks">Buzz</li>
          </ul>
          <div class="extras">
            <i class="fa fa-plus"></i>
          </div>
          <div class="extrasValue">
            <ul>
              <li><i class="fa fa-qrcode"></i>Scan QR Code</li>
              <li><i class="fa fa-gift"></i>Lucky Draw</li>
            </ul>
          </div>
        </div>
        <div class="searchDummy">
          <form class = form>
            <input type="text" name="song" id="song" autocomplete="off" placeholder="Search your favorite songs">
          </form>
        </div>
      </div>
    </div>
    <div class="library">
      <div class="container">
        <div class="libraryHeader">
          <div class="sortBtn asc">
            <i class="fa fa-sort-up"></i>
            <i class="fa fa-sort-down"></i>
          </div>
          <div class="shuffleXplay">
            <div class="shuffle">
              <i class="fa fa-recycle"></i>
            </div>
            <div class="play">
              <i class="fa fa-play"></i>
            </div>
          </div>
        </div>
      </div>
      <div class="songArea">
        <div class="song">
          <div class="container">
            <div class="thumbnail">
              <img src="assets/images/1.jpeg" alt="">
            </div>
            <div class="title">
              <h5 class="songTitle">Ariana Grande - Stuck With You</h5>
              <small>
                <p class="singer">Ariana Grande, Justin Bieber</p>
              </small>
            </div>
            <audio src="assets/songs/Ariana Grande, Justin Bieber - Stuck with U.mp3" id='audio'></audio>
            <div class="pause">
              <i class="fa fa-pause"></i>
            </div>
          </div>
        </div>
        <div class="song">
          <div class="container">
            <div class="thumbnail">
              <img src="assets/images/1.jpeg" alt="">
            </div>
            <div class="title">
              <h5 class="songTitle">Dangerous Woman</h5>
              <small>
                <p class="singer">Tiwa Savage</p>
              </small>
            </div>
            <audio src="assets/songs/Ariana Grande, Justin Bieber - Stuck with U.mp3" id='audio'></audio>
            <div class="pause">
              <i class="fa fa-pause"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="songViewer">
      <div class="inner">
        <div class="thumbnail">
          <img src="assets/images/3.jpeg" alt="">
        </div>
        <div class="aboutSong">
          <h5 class="songTitle">Bleeng Music!!</h5>
          <small>
            <p class='singer'>Music_For_The_Soul</p>
          </small>
        </div>
        <div class="buttons">
          <div class="btn-prev">
            <i class="fa fa-fast-backward"></i>
          </div>
          <div class="btn-pause">
            <i class="fa fa-play"></i>
          </div>
          <div class="btn-next">
            <i class="fa fa-fast-forward"></i>
          </div>
        </div>
      </div>
    </div>
  </div>
</body>
<script src="main.js"></script>
</html>
