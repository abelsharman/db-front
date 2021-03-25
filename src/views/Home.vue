<template>
  <div>
    <div id="start"> </div>
<nav>
    <ul>
        <li><a href="/#start">About us</a></li>
        <li><a href="/#bottom">Search</a></li>
        <div class="header_right">
            <li> <a id="cab" href="/login">Login</a></li>
            <li> <a id="logout" href="/register">Register</a></li>
        </div>
    </ul>
</nav>
<header>
    <div class="bg">
        <div class="content">
            <div class="kolom">
                <div class="atas"><img src="../assets/img/icon/11.png" /></div>
                <div class="tengah">
                    <h2>We know what you want</h2>
                </div>
                <div class="bawah">
                    <p>We have an excellent book search engine where everyone can find what they want at the moment. </p>
                </div>
            </div>
            <div class="kolom">
                <div class="atas"><img src="../assets/img/icon/2.png" /></div>
                <div class="tengah">
                    <h2>We have a rating of books</h2>
                </div>
                <div class="bawah">
                    <p>The 21st century is a dynamic time, where you have to constantly evolve and here you have to run to stand still. Anyone who does not read good books has no advantage over someone who does not know how to read them.</p>
                </div>
            </div>
            <div class="kolom">
                <div class="atas"><img src="../assets/img/icon/33.png" /></div>
                <div class="tengah">
                    <h2>Tracking progress</h2>
                </div>
                <div class="bawah">
                    <p>You can add already read books and see your progress and write a small review for yourself</p>
                </div>
            </div>
        </div>
    </div>
</header>
<div id="bottom">
</div>
<footer>
    <div class="bgf">
        <div class="contentf">
            <h1 v-if="rating"> The most rating books </h1>
            <div class="rating" v-if="rating">
              <div class="val" v-for="(val, index) in rating" :key="index">
                <div class="val_inner">
                  <h3>{{ val[0] }}</h3>
                  <p>{{ val[1] }}</p>
                  <p>Rating is {{ val[2] }}</p>
                </div>
              </div>
            </div>
            <div class="search">
                <div id="app">
                    <form action="/search" method="get"><input id="tit" type="text" name="title" placeholder="Search by title" /><input id="inp" type="text" name="author" placeholder="Search by author" /><select name="option">
                            <option value="1">Sort by rating</option>
                            <option value="2">From oldest to newest</option>
                            <option value="3">From newest to oldest</option>
                            <option value="4">Short read</option>
                        </select><input id="sea" type="submit" value="Search" /></form>
                </div>
                <div class="col_outer" v-if="list1">
                  <div class="col" v-for="(val, index) in list1" :key="index">
                    <div class="col_inner">
                      <h2>{{ val.title }}</h2>
                      <p v-if="val.author">Author is {{ val.author }}</p>
                      <p v-if="val.average_rating">Rating is {{ val.average_rating/5 }}</p>
                      <p v-if="!val.average_rating">Rating is 5/5</p>
                      <p v-if="val.num_page">Number of page is {{ val.num_page }}</p>
                      <p v-if="!val.num_page">Number of page is unknown</p>
                      <p>{{ val.publication_date }}</p>
                    </div>
                  </div>
                </div>
            </div>
        </div>
    </div>
</footer>
  </div>
</template>

<script>
export default {
  name: 'Home',
}
</script>


<style>
  
</style>