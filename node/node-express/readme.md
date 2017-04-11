## express 脚手架
    npm i -g express-generator
    express 文件夹名 会自动生成

## 中间件(核心)

    内置中间件
    第三方中间件

    功能：
        错误处理
        应用级
        路由级
## express4.x里只有3种参数获取方式
    1. req.params 
        //用get请求传输过来的参数
        app.get('/user/:id', function(req, res){
        res.send('user ' + req.params.id);
        });
        注意点：取带冒号的参数
    2. req.body
        依赖bodyParser
        获取post 参数
    3. req.query
        1. // GET /search?q=tobi+ferret
            req.query.q
            // => "tobi ferret"

        2. // GET /shoes?order=desc&shoe[color]=blue&shoe[type] =converse
            req.query.order
            // => "desc"

            req.query.shoe.color
            // => "blue"

            req.query.shoe.type
            // => "converse"

        3. 变态的写法
            // POST /search?q=tobi+ferret 
            req.query.q
            // => "tobi ferret"
