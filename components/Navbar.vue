<template>
    <div class="fluid nav" :class="fixed ? 'fixed py-4 shadow-lg' : 'py-8'">
        <div class="container bg-grey flex">
            <div class="brand">
               <nuxt-link to="/">BlogNav</nuxt-link>
            </div>
            <div class="menu">
                <ul>
                    <li>
                        <nuxt-link to="/">Home</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/about">About</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/about">Contact</nuxt-link>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: "navigationmenu",
    data: () => ({
      fixed: false,
    }),
    mounted () {
      const listener = () => {
        this.fixed = window.scrollY > 0;
      };
      window.addEventListener('scroll', listener, false);
      this.$once('hook:beforeDestroy', () => {
        window.removeEventListener('scroll', listener, false);
      });
    },
}
</script>
<style scoped>
    .fluid{
        width: 100%;
        background-color: #ffffff;
         /* background-color: #f7f7f7; */
        transition: all .3s ease-in-out;
    }
    .nav{
        
        display: flex;
   
        
    }
    .py-4{
        padding-top: 0.2rem;
        padding-bottom: 0.2rem;
    }
    .py-8{
        padding-top: 1rem;
        padding-bottom: 1rem;
    }
    .fixed {
         position: fixed;
         top: 0;
         z-index: 20;
         box-shadow: 0 32px 64px hsla(0,0%,62%,.25);
    }
    .flex{
        display: flex;
        justify-content: space-between;
        top: 0
    }
    .brand{
        line-height: 70px;
        text-transform: uppercase;
        font-family: arial;
        font-weight: 600;
        
    }
    .brand a{
        text-decoration: none;
        color: black
    }
    ul{
        list-style: none;
    }
    li{
        display: inline-block;
        margin-right: 15px;
    }
    ul>li>a{
        text-decoration: none;
        font-size: 16px;
        text-transform: uppercase;
        font-family: arial;
        font-weight: 600;
        color: black;
        transition: cubic-bezier(0.19, 1, 0.22, 1);
    }
    ul>li>a:hover{
        color: rgb(9, 170, 62);
    }
    .nuxt-link-exact-active{
         color: rgb(9, 170, 62);
    }
    ul>li:last-child{
        margin-right: 0px;
    }

    @media (max-width: 768px) {
        
    }
</style>