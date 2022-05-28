<template>
  <navi>
    <nav class="menu">
        <ul class="main1">
            <li v-for="( item,index) in menutitle" :key="item">
                <a href="#" > {{item}}</a>
                <ul class="main2">
                    <li v-for="sitem in smenutitle[index]" :key="sitem">
                        <a href="#" @click="onmenu(sitem)">{{sitem}}</a>
                        <ul class="main3">
                            <li v-for="ssitem in ssmenutitle" :key="ssitem">
                                <a href="#" @click="onmenu(ssitem)">{{ssitem}}</a>
                                <ul class="main4">
                                    <li v-for="sssitem in sssmenutitle" :key="sssitem">
                                        <a href="#" @click="onmenu(sssitem)">{{sssitem}}</a>
                                    </li>
                                </ul>
                            </li>
                        </ul>
                    </li>
                </ul>
            </li>            
        </ul>
    </nav>

  </navi>
  
</template>


<script>
//import { defineComponent } from '@vue/composition-api'

export default ({
    data(){
        return {
            menutitle:['메뉴아이템1','메뉴아이템2','메뉴아이템3','메뉴아이템4','메뉴아이템5'],
            smenutitle:[[],['s메뉴아이템1','s메뉴아이템2'],
            ['s메뉴아이템1','s메뉴아이템2'],['s메뉴아이템1','s메뉴아이템2'],['s메뉴아이템1','s메뉴아이템2']],
            ssmenutitle:['ss메뉴아이템1','ss메뉴아이템2'],
            sssmenutitle:['sss메뉴아이템1','sss메뉴아이템2'],
            classname:['menu-title', 'menu-sub1','menu-sub2'],
            a:1,
        }
        
    },
    methods: {
            increase(){
                  this.a=0  ;
            },
            onmenu(menutitle){
                console.log(menutitle);
            }
        }
})
</script>
<style scoped>
 #menu { height: 50px;
 background: #fcc;
 }
 
 .main1 {width: 600px; height: 100%;margin: 0 auto;}
 .main1>li {float: left;width: 20%;line-height: 50px;text-align: center; position: relative;}
 .main1>li:hover .main2 { left: 0;}
 .main1>li a {display: block;}.main1>li a:hover { background: #B21016; color: #fff; font-weight: bold;}
 .main2 { position: absolute;
  top: 50px;
   left: -9999px; 
   background: #ccc;
   width: 120%;}
   .main2>li { position: relative;}
   .main2>li:hover .main3 { left: 100%;}
   .main2>li a, .main3>li a { border-radius: 10px; margin: 10px;}
   .main3 { position: absolute; top: 0; background: #6BD089; width: 100%; left: -9999px; /*left: 100%;*/ /*display: none;*/}
  .main3>li { position: relative;}
    .main3>li a:hover { background: #085820; color: #fff;}
  .main3>li:hover .main4 { left: 100%;}
   .main3>li a, .main4>li a { border-radius: 10px; margin: 10px;}
   .main4 { position: absolute; top: 0; background: #6BD089; width: 100%; left: -9999px; /*left: 100%;*/ /*display: none;*/}
   .main4>li a:hover { background: #085820; color: #fff;}

.menu-1{
    text-align: center;
}
.menu-1  ul{
    /* background-color: #dfdfdf; */
}
.menu-1 > ul{
    /* background-color: #dfdfdf; */
    display:  flex;
    border-bottom: 1px solid #5da62b;
    /* padding: 0px 10px; */
    top:50%;
    left: 0;
    
}
.menu-1 > ul > li{
    /* display: inline-block; */
    flex: 1;
    /* border: 1px solid #ddd; */
}

.menu-1 > ul > li:first-child a{
    /* display: inline-block; */
    border-left: 1px solid #ddd;
    /* border: 1px solid #ddd; */
}
.menu-1 li >a{
    
    padding: 10px;
    display: block;  
    /* height: 100px; */
}
.menu-1 >  li :hover>a{
    background-color: black;
    color: white;
}
.menu-1 li {
    position: relative;
}
.menu-1 ul ul {
    display: none;
    position: absolute;
    width: 150px;
}
.menu-1 li:hover > ul {
    display: block;
}
.menu-1 > ul > li > ul > li > ul {
    position: relative;
}
</style>