<script>
  let src = "favicon.png";
</script>

<nav class="sidebar">
  <!--
  <a href="#/">Home</a> |
  <a href="#/Contact1">Contact1</a> |
  <a href="#/Contact2/1234">Contact2</a> |
  <a href="#/Todo">Todo</a> |
  <a href="#/ReactiveSum">ReactiveSum</a>
-->

  <div class="left_sub_menu">
    <div class="sub_menu">
      <div class="side_user">
        <div class="side_user1">
          <img {src} class="profile" alt="이미지" />
        </div>
        <div class="side_user2">
          <b>UserID</b><br />
          ADMIN
        </div>
        <p style="clear:both;" />
      </div>

      <ul class="big_menu">
        <li>MENU 1 <i class="arrow fas fa-angle-right" /></li>
        <ul class="small_menu">
          <li><a href="#">소메뉴1-1</a></li>
          <li><a href="#">소메뉴1-2</a></li>
          <li><a href="">소메뉴1-3</a></li>
          <li><a href="#">소메뉴1-4</a></li>
        </ul>
      </ul>

      <ul class="big_menu">
        <li>MENU 2 <i class="arrow fas fa-angle-right" /></li>
        <ul class="small_menu">
          <li><a href="#">소메뉴2-1</a></li>
          <li><a href="#">소메뉴2-2</a></li>
        </ul>
      </ul>

      <ul class="big_menu">
        <li>MYPAGE</li>
      </ul>
    </div>
  </div>
</nav>

<style>
  .sidebar {
    width: 250px;
    height: 100%;
    background: rgb(255, 255, 255);
    position: fixed;
    top: 55px;
    left: 0px;
    padding: 20px 20px;
  }

  b {
    font-size: 22px;
    line-height: 5px;
    color: black;
  }

  .side_user {
    width: 100%;
    border-radius: 8.5px;
    background-color: #f3f3f3;
    transition: all 0.15s ease-in-out 0s;
  }

  .side_user1 {
    width: 80px;
    height: 70px;
    text-align: center;
    float: left;
    border-radius: 70%;
    border: solid rgb(255, 255, 255);
    margin: 10px 10px 10px 10px;
  }

  .side_user2 {
    width: 140px;
    height: 60px;
    text-align: left;
    float: right;
    margin: 30px 0px 0px 0px;
  }

  .profile {
    width: 100%;
    height: 100%;
  }

  .big_menu {
    margin-top: 10px;
  }
</style>
