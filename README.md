AI 一站式 B/C 端解决方案，支持 OpenAI，Midjourney，Claude，讯飞星火，Stable Diffusion，DALL·E，ChatGLM，通义千问，腾讯混元，360 智脑，百川 AI，火山方舟，新必应，Gemini，Moonshot 等模型，支持对话分享，自定义预设，云端同步，模型市场，支持弹性计费和订阅计划模式，支持图片解析，支持联网搜索，支持模型缓存，丰富美观的后台管理与仪表盘数据统计；
📦 部署


部署成功后, 管理员账号为 root, 密码默认为 chatnio123456

⚡ Docker Compose 安装 (推荐)

运行成功后, 宿主机映射地址为 http://localhost:8000

GIT克隆----深度=1----分支=主----单一品牌httPS://GIT.com/迪普特拉因社区/查特尼尼。
CD查特尼奥
码头组合-D#
    # 如需使用 stable 版本, 请使用 docker-compose -f docker-compose.stable.yaml up -d 替代
    # 如需使用 watchtower 自动更新, 请使用 docker-compose -f docker-compose.watch.yaml up -d 替代

版本更新（开启 Watchtower 自动更新的情况下, 无需手动更新）：

使下降
拖曳
精心准备的
米什ql这曾是库籍车项目成果~/db
雷迪斯数计车运到项目~/雷迪斯
配置文件挂载目录项目 ~/config

⚡ Docker 安装 (轻量运行时, 常用于外置 MYSQL/RDS 服务)

如新需要使用稳定版本,北爱尔兰使用方案h/查特尼奥:稳定的替代方案h/查特尼奥:最新

 德克尔-德--命名为查特尼奥 \
  --网络主机 \
  -p 8000:8094 \
  -v ~/config:/config \
  -v ~/logs:/logs \
  -v ~/storage:/storage \
  -e米斯基克_霍斯特=当地宿主 \
  -e MYSQL_PORT=3306 \
  -eMysql_db=查特尼奥 \
  -e米塞克_用户=根 \
  -eMysql_密码=查特尼奥123456 \
  -e雷迪斯_霍斯特=当地宿主 \
  -e REDIS_PORT=6379 \
  -秘密=秘密 \
  -e服务_静态=真实 \
  方案/查特尼奥:最新
--network host 指使用宿主机网络, 使 Docker 容器使用宿主机的网络, 可自行修改
-p 8000:8094 指映射宿主机端口为 8000, 可自行修改冒号前的端口号
SECRET: JWT 密钥, 自行生成随机字符串修改
SERVE_STATIC: 是否启用静态文件服务 (正常情况下不需要更改此项, 详见下方常见问题解答)
-v ~/config:/config 挂载配置文件, -v ~/logs:/logs 挂载日志文件的宿主机目录, -v ~/storage:/storage 挂载附加功能的生成文件
需配置 MySQL 和 Redis 服务, 请自行参考上方信息修改环境变量

版本更新 （开启 Watchtower 后无需手动更新, 执行后按照上述步骤重新运行即可）：

码头停车场
多克·查特尼奥
码头拉方案/查特尼奥:最新

⚒ 编译安装 (自定义性强)

部署成功后, 默认端口为 8094, 访问地址为 http://localhost:8094 Config 配置项 (~/config/config.yaml) 可以使用环境变量进行覆盖, 如 MYSQL_HOST 环境变量可覆盖 mysql.host 配置项

GIT克隆人HTPS://吉特布.com/迪普特拉因社区/查特尼尼。
CD查特尼奥

CD应用程序
NPM安装-G
安装PNPM
PNPM建设

cd ..
去建-奥查尼奥

诺哈普。日志和#在后台运行时使用Nohup
❓ 常见问题 Q&A




为什么我部署后的站点可以访问页面, 可以登录注册, 但是无法使用聊天 (一直在转圈)？

聊天等此类功能通过 websocket 进行通信, 请确保你的服务支持 websocket。 (Tip: 中转通过 Http 实现, 无需 websocket 支持)
如果你使用了 Nginx, Apache 等反向代理, 请确保已配置 websocket 支持。
如果使用了端口映射, 端口转发, CDN, API Gateway 等服务, 请确保你的服务支持并开启 websocket。
我方配发的半程代理书----------------------------------------------------------------

若为转圈，请确保你的 Midjourney Proxy 服务已正常运行, 并且已配置正确的上游地址。
中程要旨是由旅程中途开始,而不是由旅程中期开始。
排查完这些问题后, 请查看你的系统设置中的后端域名是否已经配置并配置正确。如果不配置, 将导致 Midjourney Proxy 服务无法正常回调。
此项目有什么外部依赖？

MySQL: 存储用户信息, 对话记录, 管理员信息等持久化数据。
Redis: 存储用户快速鉴权信息, IP 速率限制, 订阅配额, 邮箱验证码等数据。
环境未配置好的情况下, 会导致服务无法正常运行, 请确保你的 MySQL 和 Redis 服务已正常运行 (Docker 部署, 编译部署需自行搭建外部服务)。
我的机器为 ARM 架构, 该项目支持 ARM 架构吗？

支持。Chat Nio 项目使用 BuildX 构建多架构镜像, 你可以直接使用 docker-compose 或 docker 运行, 无需额外配置。
如果你使用编译安装, 直接在 ARM 机器上编译即可, 无需欸外配置。如果你使用 x86 机器编译, 请使用 GOARCH=arm64 go build -o chatnio 进行交叉编译并上传至 ARM 机器上运行。
如何修改 Root 默认密码？

请点击右上角头像或侧边栏底部用户框进入后台管理, 点击系统设置下常规设置操作栏的 修改 Root 密码 进行修改。或者选择在 用户管理 中选定 root 用户进行修改密码操作。
系统设置中的后端域名是什么？

后端域名是指后端 API 服务的地址, 默认为你访问站点后加 /api 的地址, 如 https://example.com/api 。
如果设置为非 SERVE_STATIC 模式, 开启前后端分离部署, 请将后端域名设置为你的后端 API 服务地址, 如 https://api.example.com。
后端域名此处用于 Midjourney Proxy 服务的后端回调地址, 如无需使用 Midjourney Proxy 服务, 请忽略此设置。
如何配置支付方式？

Chat Nio 开源版支持发卡模式, 设置系统设置中的购买链接为你的发卡地址即可。卡密可通过用户管理中兑换码管理中批量生成。
礼品码和兑换码有什么区别？

礼品码一种类型只能一个用户只能绑定一次, 而非 aff code, 发福利等方式可使用礼品码, 可在头像下拉菜单中的礼品码中兑换。
兑换码一种类型可以多个用户绑定, 可作为正常购买和发卡使用, 可在用户管理中的兑换码管理中批量生成, 在头像下拉菜单的点数（菜单第一个）内输入兑换码进行兑换。
一个例子：比如我发了一个类型为 新年快乐 的福利, 此时推荐使用礼品码, 假设发放 100 个 66 点数, 如果为兑换码, 手快的一个用户就批量把所有兑换码的 6600 点数都用完了, 而礼品码则可以保证每个用户只能使用一次 (获得 66 点数)。
而搭建发卡的时, 如果用礼品码, 因为一个类型只能兑换一次, 购买多个礼品码会导致兑换失败, 而兑换码则可以在此场景下使用。
该项目支持 Vercel 部署吗？

Chat Nio 本身并不支持 Vercel 部署, 但是你可以使用前后端分离模式, Vercel 部署前端部分, 后端部分使用 Docker 部署或编译部署。
前后端分离部署模式是什么？

正常情况下, 前后端在同一服务内, 后端地址为 /api。前后端分离部署指前端和后端分别部署在不同的服务上, 前端服务为静态文件服务, 后端服务为 API 服务。
配置后端环境变量的 SERVE_STATIC=false 使后端服务不提供静态文件服务。
弹性计费和订阅详解

弹性计费, 即 点数, 其图标类似于云, 模型计费通用方式, 为了防止虚假汇率, 写死 10 点数 = 1 元, 汇率可以在计费规则中的 应用内置模板 中自定义汇率。
订阅, 即订阅计划, 为固定价格计费方式按次配额, 订阅计费扣取点数 (举例: 如果站点的用户想订阅 32 元的计划, 则需要保证点数大于等于 320 点数)
订阅是 Item 的组合, 每个 Item 都可设置涵盖的模型, 订阅配额 (-1 为无限使用), 名称, ID (用于区分不同的 Item), 图标等。可在后台的订阅管理中进行操作, 是否开启订阅, 订阅价格等, 修改每个订阅等级的 Item, 以及支持直接导入其他订阅等级的 Item。
订阅支持分层并写死为三个等级。 等级分别为: 普通用户 (0), 基础版订阅 (1), 标准版订阅 (2), 专业版订阅 (3), 订阅等级即为用户分组, 可在渠道管理中进行高级设置, 选择勾选可使用此模型的用户分组。
订阅配额设置, 可在订阅管理中进行操作, 是否支持中转 API (默认关闭)
可请求最小点数检测 user quota is not enough 详解

为防止站点用户滥用站点模型, 当请求点数低于最小请求点数时将返回点数不足的错误信息, 大于等于最小请求点数时将正常请求。
模型的最小可请求点数规则:

不计费模型无限制
次数计费模型最小点数为该模型的 1 次请求点数 (e.g. 若一个模型的单次请求点数为 0.1 点数, 则最小请求点数为 0.1 点数)
Token 弹性计费模型为 1K 输入 Tokens 价格 + 1K 输出 Tokens 价格 (e.g. 若一个模型的 1K 输入 Tokens 价格为 0.05 点数, 1K 输出 Tokens 价格 0.1 点数, 则最小请求点数为 0.15 点数)
DuckDuckGo API 搭建避坑

首先感谢 Binjie 作者的 duckduckgo-api 项目, 该项目为 Chat Nio 提供了联网搜索功能 (prompt 实现)。
DDG API 服务需要自行搭建, Binjie 作者的默认站点中时常配额被用尽, 请自行搭建并在系统设置中联网设置中设置。
DuckDuckGo 无法在国内环境使用, 请使用代理或海外服务器进行搭建 DDG API 端点。
部署成功后请测试 https://your.domain/search?q=hi 来简单测试是否搭建成功，如若无法访问，请检查你的 DDG API 服务是否正常运行或寻找原项目寻求帮助。
部署成功后, 请前往系统设置中的联网设置, 设置你的 DDG API 端点地址 (不要加后缀 /search), 最大结果数默认为 5 (结果数设置为 0 或负数默认为 5)
现在聊天中开启联网搜索后即可正常使用, 如若还无法使用, 一般为模型问题 (如 GPT-3.5 有时会无法理解)。
此联网搜索通过预设实现, 意为保证全模型都支持的通用功能, 兼容性无法保证灵敏性, 不依赖模型 Function Calling, 其他本身支持联网的模型可以选择直接关闭此功能。
为何我的 GPT-4-All 等逆向模型无法使用上传文件中的图片?

上传模型图片为 Base64 格式, 如果逆向不支持 Base64 格式, 请使用 URL 直链而非上传文件做法。
如何开始域名严格跨域检测?

正常情况下，后端对所有域名开放跨域。如果非特殊需求，无需开启严格跨域检测。
如果需要开启严格跨域检测，可以在后端环境变量中 并配置 ALLOW_ORIGINS, 如 ALLOW_ORIGINS=chatnio.net,chatnio.app （不需要加协议前缀, www 解析无需手动添加, 后端将自动识别并允许跨域）, 这样就会支持严格跨域检测 (如 http://www.chatnio.app, https://chatnio.net 等将会被允许, 其他域名将会被拒绝)。
即使在开启严格跨域检测的情况下, /v1 接口会被仍然允许所有域的跨域请求, 以保证中转 API 的正常使用。
模型映射功能是如何使用的？

 渠道内的模型映射格式为  [ 来自 ] > [ 到 ] , 多个映射之间换行, from 为请求的模型, to 为真实向上游发送的模型并且需要上游真实支持
如: 我有一个逆向渠道, 填写 gpt-4-all>gpt-4, 则我的用户请求 gpt-4-all 模型到该渠道时, 后端则会模型映射至 gpt-4 向该渠道请求 gpt-4, 此时该渠道支持 2 个模型, gpt-4 和 gpt-4-all (本质上都为 gpt-4)
如果我不想让我的这个逆向渠道影响到 gpt-4 的渠道组, 可以加前缀 !gpt-4-all>gpt-4, 该渠道 gpt-4 则会被忽略, 此时该渠道将只支持 1 个模型, gpt-4-all (但本质上为 gpt-4)
📦 技术栈




前置:反应+基数用户界面+逆风CSS+沙丁+震颤+还原
后端: Golang + Gin + Redis + MySQL
应用技术: PWA + WebSocket
📚 SDKs




API分片通讯API和聊天NOS唯一有型API功能

中转 API 为 OpenAI 通用格式, 支持多种格式, 详见 OpenAI API 文档和 SDKs

下图的SDKS为聊天NOS独一功能API的SDKS

日本国家安全局
联系人
高朗星
爪哇特别会议(感谢@Hujiayucc)
菲律宾人民民主党(感谢@Hujiayucc)
✨ 优秀开源项目




*此处偏前端项目指偏向用户聊天界面的项目, 偏后端项目指偏向于 API 中转和管理的项目, 一站式指包含用户聊天界面和 API 中转和管理的项目

下一次聊天@伊达达(再者前端路项目)
洛贝聊天@阿文克斯(指南项目)
信黄(指南项目)
开放式前锋@肯尼尼(俄亥俄州)
一个空气污染指数@正义松(俄亥俄州)
新空气污染指数@卡龙(此处)
FastGPT @labring （知识库）
Quivr @quivrhq （知识库）
Bingo @weaigc （模型库）
 中途代理@诺维奇克 ( 模合库)
