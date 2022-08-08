<template>
    <footer class="container-fluid p-3 fs-3 footer">
        <div class="row d-flex justify-content-center">
            <div class="col-10 col-md-4 col-lg-4 p-3">
                <p class="mb-3 fs-3">比賽場次</p>
                <ul>
                    <li class="fs-6">北護場 08/27 舉辦 </li>
                    <li class="fs-6">文大場 09/04 舉辦</li>
                    <li class="fs-6">明道場 09/17 舉辦 </li>
                    <li class="fs-6">真理場 待定</li>
                </ul>
            </div>
            <div class="col-10 col-md-4 col-lg-4 p-3">
                <p class="mb-3 fs-3">聯絡資訊</p>
                <ul>
                    <li class="fs-6"><i class="bi bi-telephone-fill fs-6"></i> 02-2701 0928<br>
                        (週一至週五12:00 ~ 18:30)
                    </li>
                    <li class="fs-6"><i class="bi bi-envelope-fill"></i> core@codedriven.org</li>
                    <li class="fs-6"><i class="bi bi-geo-alt-fill"></i> 台北市大安區復興南路一段360號3樓</li>
                </ul>
            </div>
        </div>

        <footer class="text-center">
            © 2022 by 程式驅動 | 本站所有素材引用至 Mojang 旗下遊戲 Minecraft
        </footer>
    </footer>
</template>

<script>
export default {
  name: 'MyFooter',
};
</script>

<style scoped>
ul {
    padding-left: 0 !important;
}
footer{
    font-size: 0.9rem;
    }

.footer {
        background: linear-gradient(
            rgba(63, 59, 59, 0.323) 0%,
            rgba(0, 0, 0, 0.503) 95%
        ),
        url('../assets/grassland.png') repeat center / auto 100%;
        color: white;
        padding: 20px 5px 20px 5px;
    }
</style>
