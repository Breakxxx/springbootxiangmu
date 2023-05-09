<template>
    <div style="width: 100vw;height: 100vh;overflow: hidden;display: flex">
        <div style="flex: 1">
            <el-image style="width: 100%;height: 100%" fit="cover"
                      src="https://ts1.cn.mm.bing.net/th/id/R-C.6315501c36ce8af2245885606381e596?rik=BoLTa6LGOdHb0A&riu=http%3a%2f%2fpic.bizhi360.com%2fbbpic%2f57%2f6757.jpg&ehk=axqUeQIdIaWJbHOKP3KG8pkAuZXXGa5XfwG%2bgzQfPCk%3d&risl=&pid=ImgRaw&r=0"/>
        </div>
        <div class="welcome-title">
            <div style="font-size: 30px;font-weight: bold">欢迎</div>
            <div style="margin-top: 10px">。</div>
        </div>
        <div style="width: 400px;background-color: white;z-index: 1">
            <router-view v-slot="{ Component }">
                <transition name="el-fade-in-linear" mode="out-in">
                    <component :is="Component" style="height: 100%"/>
                </transition>
            </router-view>
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>
.welcome-title {
    position: absolute;
    bottom: 30px;
    left: 30px;
    color: white;
    text-shadow: 0 0 10px black;
}
</style>