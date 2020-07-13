“store”基本上就是一个容器，它包含着你的应用中大部分的状态 (state) ，不能直接改变 store 中的状态 所以就用到了mutations

1.首先在 vue 项目里 安装 vuex      npm install vuex

2.然后 在src文件目录下新建一个名为store的文件夹，为方便引入并在store文件夹里新建一个index.js,里面的内容如下
        import Vue from 'vue';
        import Vuex from 'vuex';
        Vue.use(Vuex);

        const store = new Vuex.Store({
            state:{  
                count：0    /* 这里面写数据内容 */
            }
        });
        
        export default store;      // 导出 store
        或者
        const state={ 
            /* 这里面写数据内容 */
        };

        const mutations = {
            increment(state,index) {
                state.count = index
            }
        }

        const store = new Vuex.Store({
            state,
            mutations
        });
        
3.接下来，在 main.js里面引入store，然后再全局注入一下，这样一来就可以在任何一个组件里面使用this.$store了：
        import store from './store'   // *引入store
        
        new Vue({
            el: '#app',
            router,
            store,              // *使用store
            template: '<App/>',
            components: { App }
        })