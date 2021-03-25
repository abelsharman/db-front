<template>
    <div>
        <div id="start"> </div>
<nav>
    <ul>
        <li><a href="/#start">About us</a></li>
        <li><a href="/#bottom">Search</a></li>
        <div class="header_right">
            <li> <a href="/login">Login</a></li>
            <li> <a href="/register">Register</a></li>
        </div>
    </ul>
</nav>
<header>
    <div class="bg">
        <div class="login">
            <h1>Register</h1>
            <div id="register_form">
                <form action="/register_action" method="get">
                    <input type="search" placeholder="Login" name="login" />
                    <input type="password" placeholder="Password" name="password" />
                    <input type="password" placeholder="Confirm password" name="conf_password" />
                    <input type="submit" value="Register" />
                </form>
            </div>
        </div>
    </div>
</header>
    </div>
</template>


<script>
export default {
    name: 'Register'
}
</script>

<style>
    
</style>