<template>
<section>
        <div class="container-fluid">
            <div class="row d-flex flex-column text-center">
                <div class="col-12 sticky" id="navbar">
                    <nav class="main-nav">
                        <ul class="col-12 menu overflow-hidden fs-2">
                            <li><router-link to="/">首頁</router-link> </li>
                            <li><router-link to="/about">關於</router-link></li>
                            <li><router-link to="/products">比賽周邊</router-link></li>
                            <li><router-link to="/mineVerse">元宇宙商圈</router-link></li>
                        </ul>
                    </nav>
                </div>
            </div>
        </div>
    </section>
    <router-view/>
</template>

<script>
export default {
  name: 'SubNavbar',
};
</script>

<style scoped>
 nav ul {
display: flex;
justify-content: center;
overflow: hidden;
}

nav a{
display: inline-block;
width: 200px;
height: 70px;
padding: 15px 0 15px 0;
color: black;
}

nav a:hover{
color: black;
border-bottom: 3px solid yellow;
}

.burgar{
color: white;
font-size: 1.5rem;
display:none;
}

.sticky{
position: fixed;
top:0;
background:rgba(0, 0, 0,0.7);
transition:1s;
z-index: 1;
}

.sticky a{
color:white;
}

.sticky a:hover{
color:white;
}

@media handheld,screen and (max-width: 786px){
    nav a{
        font-size: 1.1rem;
        width: 95px;
        height: 48px;
    }
    .sticky{
        height: 50px;
    }
    nav a:hover{
    color: black;
    border-bottom: 3px solid yellow;
    }
}

</style>
