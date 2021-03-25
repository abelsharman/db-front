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
    <div class="cab">
        <div class="cab_inner">
            <div class="cab1_float_left">
                <div class="cab1_inner" v-if="books">
                    <h2>Books you like:  {{ count }}</h2>
                    <div class="cab1_books">
                        <div class="cab1_book" v-for="(val, index) in books" :key="index">
                            <h2>{{ val[0] }}</h2>
                            <div class="book_left">
                                <p>Author</p>
                                <p>Date</p>
                                <p class="pibl">Publisher</p>
                            </div>

                            <div class="book_right">
                                <p>{{ val[1] }}</p>
                                <p>{{ val[4] }}</p>
                                <p>{{ val[5] }}</p>
                            </div>
                        </div>
                    </div>
                </div>



                <div class="cab3_inner" v-if="books">
                    <h2>Admin's section- books added by users</h2>
                        <div class="cab3_book" v-for="(item, index) in books_log" :key="index">
                            <div class="book_left">
                                <p>Title</p>
                                <p>Author</p>
                                <p>Date</p>
                                <p class="pibl">Publisher</p>
                            </div>

                            <div class="book_right">
                                <p>{{ item[0] }}</p>
                                <p>{{ item[2] }}</p>
                                <p>{{ item[1] }}</p>
                                <p>{{ item[3] }}</p>
                            </div>
                    </div>
                </div>



            </div>
            <div class="cab2_float_right">
                <div class="cab2_inner">
                    <h2>Add favourite book</h2>
                    <form action="/add" method="get">
                        <input type="text" placeholder="Title of book" name="title" required="required" />
                        <input type="text" placeholder="Author of book" name="author" required="required" />
                        <input type="text" placeholder="Book release date, exmp(01.01.2020)" name="date" required="required" />
                        <input id="submit_inp" type="submit" value="Add book" name="submit" />
                    </form>
                </div>
            </div>
        </div>
    </div>
</header>
  </div>
</template>

<script>
export default {
  name: 'cab'
}
</script>


<style>
  
</style>
