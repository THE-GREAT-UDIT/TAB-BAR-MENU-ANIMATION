# TAB-BAR-MENU-ANIMATION BY @ MR RISHI JAIN..!
HELLO GUY,S THIS CODE WRITTEN BY HTML,CSS,JS

<!DOCTYPE html>
<html lang="en" >
<head>
  <meta charset="UTF-8">
  <title> Tab Bar Menu Animation | MR RISHI </title>
  <link rel='stylesheet' href='https://fonts.googleapis.com/css?family=Roboto+Condensed:400&amp;display=swap'>
<link rel='stylesheet' href='https://fonts.googleapis.com/icon?family=Material+Icons'><link rel="stylesheet" href="./style.css">

</head>
<body>
<!-- partial:index.partial.html -->

<nav class="navigation-tab">
  <div class="navigation-tab-item active">
    <span class="navigation-tab__icon">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="32"
            height="32"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="feather feather-list"
          >
            <line x1="8" y1="6" x2="21" y2="6"></line>
            <line x1="8" y1="12" x2="21" y2="12"></line>
            <line x1="8" y1="18" x2="21" y2="18"></line>
            <line x1="3" y1="6" x2="3" y2="6"></line>
            <line x1="3" y1="12" x2="3" y2="12"></line>
            <line x1="3" y1="18" x2="3" y2="18"></line>
          </svg>
        </span>
    <span class="navigation-tab__txt">List</span>
  </div>
  <div class="navigation-tab-item">
    <span class="navigation-tab__icon">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="32"
            height="32"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="feather feather-tag"
          >
            <path d="M20.59 13.41l-7.17 7.17a2 2 0 0 1-2.83 0L2 12V2h10l8.59 8.59a2 2 0 0 1 0 2.82z"></path>
            <line x1="7" y1="7" x2="7" y2="7"></line>
          </svg>
        </span>
    <span class="navigation-tab__txt">Tags</span>
  </div>
  <div class="navigation-tab-item">
    <span class="navigation-tab__icon">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="32"
            height="32"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="feather feather-shopping-bag"
          >
            <path d="M6 2L3 6v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V6l-3-4z"></path>
            <line x1="3" y1="6" x2="21" y2="6"></line>
            <path d="M16 10a4 4 0 0 1-8 0"></path>
          </svg>
        </span>
    <span class="navigation-tab__txt">Bag</span>
  </div>
  <div class="navigation-tab-item">
    <span class="navigation-tab__icon">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="32"
            height="32"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="feather feather-bell"
          >
            <path d="M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9"></path>
            <path d="M13.73 21a2 2 0 0 1-3.46 0"></path>
          </svg>
        </span>
    <span class="navigation-tab__txt">Notifications</span>
  </div>
  <div class="navigation-tab-overlay"></div>
</nav>
<!-- partial -->
  <script src='https://code.jquery.com/jquery-3.4.1.min.js'></script><script  src="./script.js"></script>
  <a href="https://instagram.com/the_great_udit?igshid=YmMyMTA2M2Y=" target="_blank" class="btn btn_works">My Works</a>

</body>
</html>

<style>
* {
  font-family: "Roboto Condensed", sans-serif;
}

html,
body {
  height: 100%;
}

body {
  margin: 0;
  padding: 0;
  background-color: #180148;
  display: flex;
  align-items: center;
  justify-content: center;
}

.navigation-tab {
  height: 150px;
  width: 600px;
  background-color: #fff;
  box-shadow: 0 50px 30px 0 rgba(0, 0, 0, 0.175);
  border-radius: 20px 20px 90px 90px;
  overflow: hidden;
  border: 15px solid #fff;
  display: flex;
  position: relative;
  flex-shrink: 0;
}
.navigation-tab-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 130px;
  flex-shrink: 0;
  cursor: pointer;
  transition: 0.3s;
  position: relative;
  z-index: 2;
}
.navigation-tab-item.active {
  width: 210px;
}
.navigation-tab-item.active .navigation-tab__icon {
  transform: translate(0px, -10px);
}
.navigation-tab-item.active .navigation-tab__txt {
  opacity: 1;
  transform: translate(0, 10px);
}
.navigation-tab-overlay {
  border-radius: 20px;
  background-color: #e4f2ff;
  height: 100%;
  width: 210px;
  position: absolute;
  left: 0;
  top: 0;
  transition: 0.3s;
}
.navigation-tab__icon {
  display: block;
  color: #4298e7;
  transition-duration: 0.3s;
  line-height: 1;
  transform: translate(0, 11px);
}
.navigation-tab__txt {
  display: block;
  font-weight: 400;
  font-size: 20px;
  color: #4298e7;
  opacity: 0;
  transition-duration: 0.3s;
  transform: translate(0, 20px);
  user-select: none;
}

</style>

<script>
    $(function () {
  $(".navigation-tab-item").click(function () {
    $(".navigation-tab-item").removeClass("active");
    $(this).addClass("active");
    $(".navigation-tab-overlay").css({
      left: $(this).prevAll().length * 130 + "px" });

  });
});
</script>

//CODE WRITTEN BY @ MR RISHI JAIN ..!
