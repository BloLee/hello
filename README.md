#Nuxt如何一次请求多个接口

let [pageRes, dataRoad,speakList,activityList,newList] = await Promise.all([
                $axios.get('/api/index/banner'),
                $axios.get('/api/index/indexroad'),
                $axios.get("/api/entrepreneursaid/entrepreneursaidlist"),
                $axios.get("/api/index/indexactive"), 
                $axios.get("/api/news/newslist?spage_index=1&spage_size=12"), 
            ]);   
