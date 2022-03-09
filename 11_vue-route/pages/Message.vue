<template>
    <div>
        <ul>
        <li v-for="m in messageList" :key="m.id">
            <!-- to的字符串写法 -->
            <!-- <router-link :to="`/home/message/detail/${m.id}/${m.title}`">{{m.title}}</router-link>&nbsp;&nbsp; -->
            <!-- <router-link :to="`/home/message/detail?id=${m.id}&title=${m.title}`">{{m.title}}</router-link>&nbsp;&nbsp; -->
             <!-- to的对象写法 -->
            <!-- <router-link :to="{
                name:'xiangqing',
                query:{
                    id:m.id,
                    title:m.title
                }
            } ">
                {{m.title}}
            </router-link> -->
            <router-link :to="{
                name:'xiangqing',
                query:{
                    id:m.id,
                    title:m.title
                }
            } ">
                {{m.title}}
            </router-link>
            <!-- <button @click = "pushShow">push查看</button>
            <button>replace查看</button> -->
        </li>
        </ul>
        <br>
        <router-view></router-view>
    </div>
</template>

<script>
export default {
 name:'Message',
 data(){
     return{
         messageList:[
             {id:'001',title:'消息001'},
             {id:'002',title:'消息002'},
             {id:'003',title:'消息003'},
         ]
     }
 },
//  methods: {
//      pushShow(m){
//          this.$router.push({
//               name:'xiangqing',
//               query:{
//                     id:m.id,
//                     title:m.title
//                 }
//          })
//      }
//  }
}
</script>
