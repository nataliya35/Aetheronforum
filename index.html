<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes, viewport-fit=cover">
    <title>Aetheron /anon/ — 匿名论坛</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }
        body {
            background: #f6f8fc;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, sans-serif;
            color: #1a1e2b;
            line-height: 1.45;
            padding: 0.75rem;
            overflow-x: hidden;
        }
        .app-container {
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
        }
        /* 页面容器 - 动画切换 */
        .page {
            transition: transform 0.25s cubic-bezier(0.2, 0.9, 0.4, 1.1), opacity 0.2s ease;
            will-change: transform, opacity;
        }
        .page-list {
            transform: translateX(0);
            opacity: 1;
        }
        .page-list.exit {
            transform: translateX(-20px);
            opacity: 0;
            pointer-events: none;
        }
        .page-detail {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            transform: translateX(100%);
            opacity: 0;
            pointer-events: none;
        }
        .page-detail.enter {
            transform: translateX(0);
            opacity: 1;
            pointer-events: auto;
        }
        .page-detail.exit {
            transform: translateX(100%);
            opacity: 0;
            pointer-events: none;
        }
        /* 返回时列表页重新进入 */
        .page-list.enter {
            transform: translateX(0);
            opacity: 1;
            pointer-events: auto;
        }
        .forum-card {
            background: #ffffff;
            border-radius: 20px;
            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.04), 0 1px 4px rgba(0, 0, 0, 0.02);
            overflow: hidden;
        }
        .forum-header {
            padding: 0.9rem 1rem;
            border-bottom: 1px solid #edf0f5;
            background: #fff;
        }
        .breadcrumb {
            display: flex;
            align-items: center;
            gap: 0.4rem;
            font-size: 0.75rem;
            color: #6c7e9e;
            margin-bottom: 0.5rem;
            flex-wrap: wrap;
        }
        .breadcrumb a { color: #2c6e9e; text-decoration: none; font-weight: 500; }
        .breadcrumb i { font-size: 0.65rem; }
        .thread-title {
            font-size: 1.35rem;
            font-weight: 700;
            letter-spacing: -0.2px;
            color: #0b1c2e;
            line-height: 1.3;
        }
        .thread-list { padding: 0; }
        .thread-item {
            display: flex;
            gap: 0.7rem;
            padding: 0.9rem 1rem;
            border-bottom: 1px solid #eef2f6;
            cursor: pointer;
            transition: background 0.1s;
        }
        .thread-item:active { background: #f0f3f8; }
        .thread-votes {
            text-align: center;
            min-width: 48px;
            color: #7d8dab;
            font-weight: 500;
            font-size: 0.8rem;
        }
        .thread-main { flex: 1; }
        .thread-title-link {
            font-size: 0.95rem;
            font-weight: 600;
            color: #1e2f44;
            margin-bottom: 0.25rem;
            line-height: 1.35;
        }
        .thread-meta {
            font-size: 0.7rem;
            color: #8192ab;
            display: flex;
            gap: 0.8rem;
            flex-wrap: wrap;
        }
        .post-list { background: #ffffff; }
        .post {
            display: flex;
            gap: 0.75rem;
            padding: 0.9rem 1rem;
            border-bottom: 1px solid #f0f2f5;
        }
        .vote-col {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 6px;
            min-width: 42px;
            font-weight: 500;
            font-size: 0.85rem;
        }
        .vote-col i {
            cursor: pointer;
            color: #8e9db2;
            transition: 0.05s linear;
            font-size: 1.2rem;
            padding: 4px;
        }
        .vote-col i:active { transform: scale(0.9); }
        .vote-score {
            font-weight: 700;
            font-size: 0.9rem;
            color: #1e2a44;
        }
        .content-col { flex: 1; }
        .post-header {
            display: flex;
            flex-wrap: wrap;
            align-items: baseline;
            gap: 0.4rem;
            margin-bottom: 0.4rem;
        }
        .floor {
            font-weight: 600;
            color: #6a7c9e;
            font-size: 0.7rem;
            background: #f0f3f9;
            padding: 0.2rem 0.55rem;
            border-radius: 20px;
        }
        .username {
            font-weight: 700;
            font-size: 0.85rem;
            color: #1e2a44;
        }
        .username.anonymous { color: #5a6e8a; }
        .badge {
            font-size: 0.6rem;
            background: #eef2fa;
            padding: 0.2rem 0.5rem;
            border-radius: 30px;
            font-weight: 500;
            color: #2c4b7a;
        }
        .badge.op { background: #e0e9f5; color: #1c5a9e; }
        .timestamp {
            font-size: 0.65rem;
            color: #8a99b0;
        }
        .post-content {
            font-size: 0.9rem;
            line-height: 1.45;
            color: #1f293d;
        }
        .post-content .en {
            margin-bottom: 0.3rem;
            word-break: break-word;
        }
        .post-content .zh {
            font-size: 0.84rem;
            color: #3b4b6e;
            background: #f8fafd;
            padding: 0.4rem 0.7rem;
            border-radius: 12px;
            border-left: 3px solid #b9c8e8;
            margin-top: 0.4rem;
        }
        .quote {
            background: #f1f5f9;
            border-left: 3px solid #a0b8d4;
            padding: 0.2rem 0.6rem;
            font-family: monospace;
            font-size: 0.8rem;
            margin: 0.3rem 0;
            border-radius: 8px;
            display: inline-block;
        }
        .post-footer {
            margin-top: 0.6rem;
            font-size: 0.7rem;
            display: flex;
            gap: 1rem;
            color: #8192ab;
        }
        .back-button {
            background: none;
            border: none;
            font-weight: 600;
            color: #2c6e9e;
            cursor: pointer;
            font-size: 0.85rem;
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
            margin-bottom: 0.3rem;
        }
        @media (max-width: 650px) {
            body { padding: 0.5rem; }
            .forum-header { padding: 0.75rem 0.9rem; }
            .thread-item { padding: 0.8rem 0.9rem; gap: 0.6rem; }
            .thread-title-link { font-size: 0.9rem; }
            .post { padding: 0.8rem 0.9rem; gap: 0.65rem; }
            .vote-col { min-width: 38px; gap: 5px; }
            .vote-col i { font-size: 1.1rem; padding: 3px; }
            .vote-score { font-size: 0.85rem; }
            .post-header { gap: 0.35rem; }
            .username { font-size: 0.8rem; }
            .floor { font-size: 0.65rem; }
            .timestamp { font-size: 0.6rem; }
            .post-content { font-size: 0.85rem; }
            .post-content .zh { font-size: 0.8rem; padding: 0.35rem 0.6rem; }
            .quote { font-size: 0.75rem; }
        }
        .upvote-active { color: #ff4500 !important; }
        .downvote-active { color: #7193ff !important; }
        /* 滚动条优化 */
        .post-list {
            max-height: calc(100vh - 140px);
            overflow-y: auto;
            -webkit-overflow-scrolling: touch;
        }
        .thread-list {
            max-height: calc(100vh - 120px);
            overflow-y: auto;
            -webkit-overflow-scrolling: touch;
        }
    </style>
</head>
<body>
<div class="app-container">
    <!-- 帖子列表页 -->
    <div id="threadListPage" class="page page-list forum-card">
        <div class="forum-header">
            <div class="breadcrumb">
                <a href="#">Aetheron Academy</a> <i class="fas fa-chevron-right"></i>
                <a href="#">/anon/</a> <i class="fas fa-chevron-right"></i>
                <span>gossip</span>
            </div>
            <h1 class="thread-title">All threads</h1>
        </div>
        <div class="thread-list" id="threadListContainer"></div>
    </div>

    <!-- 帖子详情页 (完整中英对照 + 精确楼层 + 点赞互动) -->
    <div id="threadDetailPage" class="page page-detail forum-card">
        <div class="forum-header">
            <div class="breadcrumb">
                <a href="#" id="backToHomeLink"><i class="fas fa-arrow-left"></i> Back to threads</a>
            </div>
            <h1 class="thread-title">Who's the new girl in the dining hall???</h1>
            <div class="thread-meta" id="detailMeta" style="margin-top: 6px;"></div>
        </div>
        <div class="post-list" id="postsContainer"></div>
    </div>
</div>

<script>
    // ============================================================
    // 完整楼层数据 (1L → 137L)
    // ============================================================
    const postsRaw = [
        { floor: 1, username: "Anonymous", isOP: true, isAnonymous: true, timestamp: "4d ago", en: "[📷 photo.jpg: a black-haired girl sitting by the window in the dining hall, holding a fork, pasta in front of her. She's looking down eating, light from the window hitting her hair.]\n\nSaw this at lunch today. Never seen her before. New transfer? She doesn’t look like a scholarship kid. Anyone know her name? 👀", zh: "[照片：食堂靠窗位置，黑发女生拿着叉子，面前一盘意面。她低头吃东西，窗外的光线打在头发上。] 今天午饭看到的。以前从没见过。新转来的？看着不像拿奖学金的学生。有人知道她叫什么吗？👀" },
        { floor: 2, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Holy shit that hair. Is that natural??? The way it catches light—kinda unreal.", zh: "卧槽那个头发。天生的？？？光线打上去那个效果——有点不真实。" },
        { floor: 3, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Probably dyed. No Asian has hair that color naturally. But ngl she's hot. 🔥", zh: "染的吧。没有亚洲人天生头发是那个颜色的。不过说实话，挺辣的。🔥" },
        { floor: 4, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Wait is she sitting alone? 💀 First week and no one’s claimed her yet? That’s rough.", zh: "等等，她一个人坐着？💀开学第一周还没人‘认领’她？太惨了吧。" },
        { floor: 5, username: "BrittanyEssen", isAnonymous: false, timestamp: "4d ago", en: "Claimed? Lmao why would anyone want to claim someone who looks like they haven’t figured out which fork to use. Look at her—elbows on the table. 🤭", zh: "认领？笑死，怎么会有人想认领一个连用什么叉子都没搞明白的人。看她——胳膊肘搁桌上呢。🤭" },
        { floor: 6, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>5 Brittany dropping truth bombs as always 💀💀💀", zh: ">>5 布列塔妮一如既往地输出真相💀💀💀" },
        { floor: 7, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Okay but her face though. That jawline? Those eyes? She’s actually gorgeous. What’s Brittany on about.", zh: "行吧但是她的脸呢。那个下颌线？那双眼睛？她确实漂亮啊。布列塔妮在说什么鬼。" },
        { floor: 8, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>7 Brittany’s just threatened. You know how she gets when someone prettier shows up. 😭", zh: ">>7 布列塔妮就是受威胁了。你知道的，一有比她好看的来了她就那个样子。😭" },
        { floor: 9, username: "BrittanyEssen", isAnonymous: false, timestamp: "4d ago", en: ">>8 Threatened? Babe I’ve been Homecoming Queen finalist two years in a row. Come talk to me when she’s got a sash. 💅", zh: ">>8 受威胁？宝贝我连续两年返校节女王决赛入围。等她有绶带了你再来跟我聊。💅" },
        { floor: 10, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "The sash comment is sending me 💀 Brittany really keeps that thing in her back pocket at all times huh", zh: "绶带那个评论笑死我了💀 布列塔妮是把那玩意儿随时揣在兜里吗" },
        { floor: 11, username: "Anonymous", isOP: true, isAnonymous: true, timestamp: "4d ago", en: "Back to the point—has anyone actually talked to her? What’s her vibe? She looks kinda intimidating ngl.", zh: "说回正题——有人真的跟她聊过吗？她什么气场？说实话看着有点不好惹。" },
        { floor: 12, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "She sat near me once. Didn’t say a word the whole time. Just ate and stared out the window. Lowkey weird.", zh: "她有一次坐我附近。全程一句话没说。就吃，然后盯着窗外。有点怪。" },
        { floor: 13, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>12 That’s not weird that’s called minding your own business. Try it sometime.", zh: ">>12 那不叫怪，那叫管好自己的事。你改天也试试。" },
        { floor: 14, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Y’all are missing the point. Look at the watch on her wrist in the photo. That’s a Patek. No way a scholarship kid’s wearing that.", zh: "你们都跑偏了。看照片里她手腕上那块表。百达翡丽。奖学金生不可能戴那个。" },
        { floor: 15, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>14 Good eye. 👀 So she’s loaded. Which dorm is she in?", zh: ">>14 好眼力。👀 那她是有钱人。她住哪栋楼？" },
        { floor: 16, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Saw her walking toward Apollyn earlier. Not sure which floor though.", zh: "之前看见她往阿珀伦楼那边走了。几楼不知道。" },
        { floor: 17, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Apollyn? Art kid with a Patek. Daddy’s money meets daddy issues. Tale as old as time.", zh: "阿珀伦？戴百达翡丽的艺术生。老爸的钱遇上老爸的问题。老套故事了。" },
        { floor: 18, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>17 Or maybe she’s just rich and likes art. Not everything has to be a trauma dump.", zh: ">>17 又或者她只是有钱且喜欢艺术。不是什么事都得是创伤倾诉。" },
        { floor: 19, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Okay but can we talk about her skin?? It’s literally glowing in that photo. What filter is she using irl 💀", zh: "行吧但是能聊聊她的皮肤吗？？那张照片里简直在发光。她在现实里开了什么滤镜💀" },
        { floor: 20, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>19 That’s called youth and money babe. Look it up.", zh: ">>19 那叫年轻和钱，宝贝。自己查查。" },
        { floor: 21, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "I heard she’s Chinese. From some crazy rich family. Like old money old old money.", zh: "我听说她是中国人。家里特别有钱那种。老钱，很老很老的钱。" },
        { floor: 22, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>21 Source? Or are we just making things up now.", zh: ">>21 消息来源？还是我们现在开始编了？" },
        { floor: 23, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>21 “Old money Chinese” isn’t a thing. Their rich are all new money. That’s literally their whole deal.", zh: ">>21 ‘老钱中国人’不存在。他们那里的富人都是新钱。这基本就是他们的全部特点了。" },
        { floor: 24, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Racist much? 💀", zh: "这就种族歧视了？💀" },
        { floor: 25, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Anyway. Back to the girl. Has anyone gotten her name yet? Or are we just calling her “Patek girl” forever.", zh: "总之。说回那个女生。有人搞到她名字了吗？还是我们就永远叫她‘百达翡丽女’？" },
        { floor: 26, username: "TitusMontimacy", isAnonymous: false, timestamp: "4d ago", en: "She’s cute. 🔥", zh: "她挺好看。🔥" },
        { floor: 27, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>26 OH HE’S HERE. Titus dropping in 🚗💨", zh: ">>26 哦他来了。泰特斯驾到🚗💨" },
        { floor: 28, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Titus commenting on a new girl’s post. Set your watches, folks. Bet he slides into her DMs within 48 hours.", zh: "泰特斯在新女生的帖子里评论了。各位，对表。赌他四十八小时内滑进她私信。" },
        { floor: 29, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "48 hours? Generous. I’m saying 24.", zh: "四十八小时？太宽裕了吧。我说二十四。" },
        { floor: 30, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Y'all talk like he hasn't already made his move 💀 The second someone finds her Instagram, he's gonna be the first to know — watch, he probably already follows her and we just don't know it yet. 👀", zh: "你们说得好像他还没去似的💀 一旦有人找到了她的Instagram账号，他肯定会第一个知道——说不定他早就关注了她的Instagram，只是我们还不知道罢了。👀" },
        { floor: 31, username: "TitusMontimacy", isAnonymous: false, timestamp: "4d ago", en: ">>30 Nah. Just saying what everyone’s thinking.", zh: ">>30 没有。就是说了句大家都想说的而已。" },
        { floor: 32, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Titus commenting is basically his version of a formal introduction. He’s already planning the first date in his head.", zh: "泰特斯评论基本就是他版本的正式介绍了。他脑子里已经在计划第一次约会了。" },
        { floor: 33, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "First date? You mean first hookup. Let’s be real.", zh: "第一次约会？你是指第一次约炮。现实点吧。" },
        { floor: 34, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Not all of us are trying to get into her pants, damn. Some of us are just curious.", zh: "不是所有人都想上她，妈的。有些人就是好奇而已。" },
        { floor: 35, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "By the way, I've literally seen Casper having dinner with her 🍽️ Did none of y'all see it?? There were plenty of people there. How come no one's brought this up? 🤨", zh: "顺便提一句，我真的见过卡斯珀和她一起吃晚饭🍽️ 你们难道都没看见吗？？当时在场的人可不少。为什么没人提过这件事呢？🤨" },
        { floor: 36, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Casper? Dude's just trying to climb. Or throw someone else under the bus. 🙄 What's there to say? Besides, talk too much and this post gets deleted. 🤫💀", zh: "卡斯珀？这家伙就是想往上爬。或者把别人推出去背锅。🙄 有什么好说的？再说了，说太多帖子会被删的。🤫💀" },
        { floor: 37, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>36 You've already said too much, sweetheart 😘 Get ready to get jumped by his fan club, lol. 💀", zh: ">>36 你已经说多了，亲爱的😘 准备好被他的粉丝团‘暗杀’吧哈哈💀" },
        { floor: 38, username: "Anonymous", isOP: true, isAnonymous: true, timestamp: "4d ago", en: "Stop, how did we get so off topic?? 🙄 I'm asking about that girl. Don't bring Casper into this. In a second Hunter's gonna roll up for his little pet 🐶 If he sets his eyes on this girl, y'all might as well pack it up and go home 💀", zh: "停，怎么又歪楼了？？🙄 我问的是那个女孩。别提卡斯珀。一会儿亨特就要为了他的小宠物过来了🐶 要是他看上了这个女孩，大家就准备散伙回家吧💀" },
        { floor: 39, username: "LaurentWynthorpe", isAnonymous: false, timestamp: "4d ago", en: "I checked her in at the reception desk. She’s both beautiful and kind, and I’m sure she’ll settle in here quickly. 😊", zh: "我在迎新点帮她办的手续。她既漂亮又善良，我相信她很快就能适应这里的生活。😊" },
        { floor: 40, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>39 Of course Laurent has already met her. Of course he’s being nice. 🥹", zh: ">>39 洛朗当然已经见过她了。洛朗当然很友善。🥹" },
        { floor: 41, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "If I hadn't been there myself, I'd totally believe it 💀", zh: "如果当时我不在场，我肯定会相信的。💀" },
        { floor: 42, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Anyway. Name? Anyone?", zh: "所以。名字？有人知道吗？" },
        { floor: 43, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "I heard one of the international students call her “Sia.” Not sure if that’s her name or a nickname though.", zh: "我听见一个国际生叫她‘希娅’。不知道是名字还是昵称。" },
        { floor: 44, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "Sia? Like the singer? 💀", zh: "希娅？像那个歌手？💀" },
        { floor: 45, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>44 Pls don’t let that become a thing. 💀", zh: ">>44 拜托别让这个梗传开。💀" },
        { floor: 46, username: "Anonymous", isOP: true, isAnonymous: true, timestamp: "4d ago", en: "Sia. Chinese. Apollyn. Patek. Got it.", zh: "希娅。中国人。阿珀伦。百达翡丽。记下了。" },
        { floor: 47, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: "She’s giving main character energy and she hasn’t even done anything yet. I’m scared but also intrigued.", zh: "她还没做任何事呢，就已经有主角气场了。我有点害怕但也很感兴趣。" },
        { floor: 48, username: "Anonymous", isAnonymous: true, timestamp: "4d ago", en: ">>47 “Scared but also intrigued” is literally the Aetheron experience.", zh: ">>47 ‘害怕但也很感兴趣’基本就是艾瑟隆的体验概括了。" },
        { floor: 49, username: "BrittanyEssen", isAnonymous: false, timestamp: "3d ago", en: "Y’all are hyping her up way too much. She’s been here for two days. Let’s see if she survives the semester first. 🤷‍♀️", zh: "你们把她捧得太高了。她才来了两天。先看看她能不能撑过这个学期再说吧。🤷‍♀️" },
        { floor: 50, username: "Anonymous", isAnonymous: true, timestamp: "3d ago", en: "Brittany has entered the chat and the temperature just dropped ten degrees ❄️", zh: "布列塔妮已进入聊天室，温度骤降十度❄️" },
        { floor: 51, username: "Anonymous", isAnonymous: true, timestamp: "3d ago", en: ">>49 She's not wrong. In this school, a pretty face and a nice body just aren't enough 💅🤷", zh: ">>49 她没说错。在这所学校，光有漂亮的脸蛋和好身材是不够的。💅🤷" },
        { floor: 52, username: "Anonymous", isAnonymous: true, timestamp: "3d ago", en: "Okay but imagine being so pressed about a new girl that you comment on a forum post about her. Couldn’t be me.", zh: "行吧但是想象一下，对一个新女生在意到来论坛帖子底下评论。反正不会是我。" },
        { floor: 53, username: "Anonymous", isAnonymous: true, timestamp: "3d ago", en: ">>52 You’re literally commenting on the same post right now. 💀", zh: ">>52 你现在不就在这个帖子底下评论吗。💀" },
        { floor: 54, username: "Anonymous", isAnonymous: true, timestamp: "3d ago", en: "Anyways. I’m keeping an eye on this one. Something about her feels... different.", zh: "总之。我会盯着这个的。她身上有种……不一样的感觉。" },
        { floor: 55, username: "Anonymous", isAnonymous: true, timestamp: "3d ago", en: "Different how? Like “future Homecoming Queen” different or “gets expelled by October” different.", zh: "不一样是指哪种？像‘未来的返校节女王’那种不一样，还是‘十月份之前被开除’那种不一样？" },
        { floor: 56, username: "Anonymous", isAnonymous: true, timestamp: "3d ago", en: "Both can be true in this school tbh. 🤷", zh: "在这所学校，这两种可能同时成立。🤷" },
        { floor: 57, username: "Anonymous", isAnonymous: true, timestamp: "3d ago", en: "Not me already invested in a girl I’ve never spoken to. The forum really does this to you every time.", zh: "我居然对一个从没说过话的女生已经上心了。这论坛真是每次都这样。" },
        { floor: 58, username: "Anonymous", isAnonymous: true, timestamp: "3d ago", en: ">>57 Welcome to Aetheron Forum. Where your social life is vicarious and your tea is always hot. ☕️", zh: ">>57 欢迎来到艾瑟隆论坛。在这里你的社交生活是替代性的，八卦永远是热的。☕️" },
        { floor: 59, username: "Anonymous", isAnonymous: true, timestamp: "3d ago", en: "Someone get more info on her. Classes? Clubs? Who she’s been seen with? I need the full dossier.", zh: "谁能搞到更多她的信息。课程？社团？跟谁一起出现过？我需要完整档案。" },
        { floor: 60, username: "Anonymous", isAnonymous: true, timestamp: "3d ago", en: ">>59 This isn’t the CIA, bestie. 💀", zh: ">>59 这不是中情局，宝。💀" },
        { floor: 61, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "I saw her walking with a guy today. Blonde. He looks pretty handsome, and seems like a freshman too. Anyone else see that? Who is that?", zh: "我今天看见她跟一个男的走在一起。金发。看起来很酷，也像是新生，有人也看见了吗？那是谁？" },
        { floor: 62, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: ">>61 Wait what. Blonde guy? Which one. There are like fifty blonde guys at this school.", zh: ">>61 等等什么。金发男？哪个。这学校有大概五十个金发男。" },
        { floor: 63, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: ">>62 Tall. Great figure. He looks a bit like a Hollywood star", zh: ">>62 高。身材很好。看着有点像好莱坞的一个明星" },
        { floor: 64, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "That describes half the art kids in Apollyn. 💀", zh: "那形容了阿珀伦一半的艺术生。💀" },
        { floor: 65, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "Nah, but I think I know who they're talking about 👀 It's that new kid who looks like ****, right? That's his son. Yeah, he's a freshman — was even in the school paper yesterday. Brittany was literally throwing herself at him 😬", zh: "不是，但我觉得我知道他们在说谁👀 就是那个长得像****的新来的家伙，对吧？那是他儿子。确实是新生，昨天还上了校报。布列塔尼甚至还在对他示好😬" },
        { floor: 66, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: ">>65 That’s literally every theater kid. Be specific.", zh: ">>65 那基本是每个戏剧社学生的样子。具体点。" },
        { floor: 67, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "Y’all are useless. I’ll just go ask her myself tomorrow.", zh: "你们都没用。我明天自己去问她。" },
        { floor: 68, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: ">>67 And report back immediately. We’re counting on you soldier 🫡", zh: ">>67 然后立刻回来汇报。我们就靠你了战士🫡" },
        { floor: 69, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "This thread is already at 69 replies and we still don’t know anything about her. Peak forum behavior.", zh: "这个帖子已经六十九条回复了，我们还是对她一无所知。典型论坛行为。" },
        { floor: 70, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "That’s the beauty of it. We suffer together. 🤝", zh: "这就是它的美妙之处。我们一起受苦。🤝" },
        { floor: 71, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "Okay but serious question—why does no one seem to actually KNOW her? Like she just appeared out of thin air.", zh: "行吧但是认真问一句——为什么好像没人真的认识她？感觉她就是凭空出现的。" },
        { floor: 72, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: ">>71 That’s what happens when you have money and don’t try to be friends with everyone. Some of us should take notes.", zh: ">>71 当你有钱又不试图跟所有人做朋友时，就会这样。有些人应该学学。" },
        { floor: 73, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "💀💀💀", zh: "💀💀💀" },
        { floor: 74, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "I’m just saying. Give it two weeks. Either she’s running this place or she’s gone. No in-between at Aetheron.", zh: "我就是说说而已。两个星期。要么她统治这地方，要么她走人。艾瑟隆没有中间地带。" },
        { floor: 75, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: ">>74 Realest thing anyone’s said in this whole thread.", zh: ">>74 这整个帖子里最真实的一句话。" },
        { floor: 76, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "Okay I actually need to do my homework now. Someone tag me if more info drops. 🏃‍♂️💨", zh: "行了我真的要去做作业了。有新消息谁@我一下。🏃‍♂️💨" },
        { floor: 77, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "Same. But also... I’ll be checking back. 👀", zh: "同上。但是……我会回来看的。👀" },
        { floor: 78, username: "IsaiahHo", isAnonymous: false, timestamp: "2d ago", en: "She’s fine.", zh: "她还可以。" },
        { floor: 79, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: ">>78 Isaiah???? Ho???? Commenting???? On a forum post???? About a girl????", zh: ">>78 何隐之？？？？在论坛帖子底下评论？？？？关于一个女生？？？？" },
        { floor: 80, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "Titus commented. Laurent commented. Isaiah commented. That’s three of them. Who’s next? The ghost of Aetheron past?", zh: "泰特斯评论了。洛朗评论了。何隐之评论了。三个了。下一个是谁？艾瑟隆过去之鬼魂吗？" },
        { floor: 81, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: ">>80 Don’t jinx it or Kjell’s gonna show up and say one word and break the internet.", zh: ">>80 别乌鸦嘴，不然谢尔要出现了，说一个词，然后整个网络炸了。" },
        { floor: 82, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "Kjell doesn’t even know this forum exists. Man’s probably out reading or something. ❄️", zh: "谢尔压根不知道有这个论坛存在。这人大概在外面阅读还是干嘛。❄️" },
        { floor: 83, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "Okay but Isaiah saying “she’s fine” is basically a love confession from him. You know how he is.", zh: "行吧但是何隐之说‘她还可以’，基本就等于他的告白了。你知道他什么德性。" },
        { floor: 84, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: ">>83 The bar is in hell. 💀", zh: ">>83 这个门槛低到地狱里去了。💀" },
        { floor: 85, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "This thread is making me lose brain cells but I can’t look away. Someone save me.", zh: "这个帖子在消耗我的脑细胞，但我就是移不开眼。谁来救救我。" },
        { floor: 86, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: ">>85 That’s the Aetheron Forum experience babe. Buckle up. 🎢", zh: ">>85 这就是艾瑟隆论坛的体验宝贝。坐稳了。🎢" },
        { floor: 87, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: "Alright I’m going to sleep. Someone wake me up when we have actual information and not just speculation.", zh: "行了我去睡了。等我们有真实信息而不是猜测的时候再叫醒我。" },
        { floor: 88, username: "Anonymous", isAnonymous: true, timestamp: "2d ago", en: ">>87 So you’re never waking up. Got it.", zh: ">>87 那你永远不用醒了。明白。" },
        { floor: 89, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: ">>67 Okay I asked her. Name’s Sia. 11th grade. Apollyn. And get this—she’s in one of the honors suites. The top floor one. 💀", zh: ">>67 行了，我问到了。名字叫希娅。十一年级。阿珀伦楼。而且听好了——她住的是荣誉套房。顶层那间。💀" },
        { floor: 90, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: ">>89 HONORS SUITE??? The one that requires a seven-figure donation AND social standing??? That’s not just “loaded” that’s “your dad owns a small country” loaded.", zh: ">>89 荣誉套房？？？那间要七位数捐款加上社会地位才能拿到的？？？那不叫‘有钱’，那叫‘你爸拥有一个小国家’那种有钱。" },
        { floor: 91, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: "Brittany panicking? 😂 Girl, \"you're threatened\" doesn't even begin to cover it 💀", zh: "布列塔妮慌张吗？😂 姐妹，‘你受威胁’这种说法都不足以形容了💀" },
        { floor: 92, username: "BrittanyEssen", isAnonymous: false, timestamp: "1d ago", en: "Unfortunately, no. Honor Suite doesn't prove anything anyway 🙄 Money can't buy class. Also... don't let me find out who you are. 🫣💀", zh: "很遗憾，没有。荣誉套房说明不了什么 🙄 钱买不来教养。另外……别让我知道你是谁。🫣💀" },
        { floor: 93, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: ">>92 Says the girl whose dad donated exactly the minimum for a privilege suite. 💀", zh: ">>92 这话出自那个她爸刚好捐了特权套房最低限额的女生。💀" },
        { floor: 94, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: "💀💀💀", zh: "💀💀💀" },
        { floor: 95, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: "Okay but can we talk about the fact that she’s been here less than a week and she’s already in Apollyn’s honors suite? That’s not “art kid with daddy’s money.” That’s “art kid whose daddy owns the building.”", zh: "行吧但是我们能聊聊她来了不到一周就已经住进了阿珀伦的荣誉套房这件事吗？那不叫‘用老爸钱的艺术生’，那叫‘艺术生的老爸拥有这栋楼’。" },
        { floor: 96, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: "So is no one going to mention that Hunter and Chance have been lurking on this thread since page one? 👀", zh: "所以没人提亨特和钱斯从第一页就在这个帖子里潜水吗？👀" },
        { floor: 97, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: ">>96 Wait what. How do you know.", zh: ">>96 等等什么。你怎么知道的。" },
        { floor: 98, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: ">>97 Because I have eyes and I saw them reading it during lunch. 💀 They’ve been “discussing” something all week. You know what that means.", zh: ">>97 因为我有眼睛，我午饭时看见他们在看这个帖子。💀 他们整周都在‘讨论’什么事。你知道那意味着什么。" },
        { floor: 99, username: "HunterFoster", isAnonymous: false, timestamp: "1d ago", en: "She’s not responding to DMs. Any of you actually talked to her or is everyone just guessing.", zh: "她没回私信。你们有人真的跟她聊过吗，还是所有人都只是在猜？" },
        { floor: 100, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: ">>99 He just spoke up 👀 He definitely has her Insta.", zh: ">>99 他说话了 👀 他肯定有她的ins。" },
        { floor: 101, username: "ChanceBancroft", isAnonymous: false, timestamp: "1d ago", en: ">>99 Told you. She’s not interested in the usual approach.", zh: ">>99 跟你说了。她对常规套路不感兴趣。" },
        { floor: 102, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: "Wait “the usual approach”??? Chance what does that mean???", zh: "等等‘常规套路’？？？钱斯那是什么意思？？？" },
        { floor: 103, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: ">>102 You really don’t want to know. 💀", zh: ">>102 你真的不会想知道的。💀" },
        { floor: 104, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: "Okay so Hunter and Chance were planning something and now they’re backing off? What changed.", zh: "行吧所以亨特和钱斯本来在计划什么，现在他们收手了？什么变了。" },
        { floor: 105, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: ">>104 Check her family name. Then check the donor list for the past twenty years. 💀", zh: ">>104 查查她的姓氏。再查查过去二十年的捐赠名单。💀" },
        { floor: 106, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: "What family name? No one even knows her last name.", zh: "什么姓氏？根本没人知道她姓什么。" },
        { floor: 107, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: ">>106 Exactly. That’s the point. If you know, you know. And if you don’t, you’re not supposed to.", zh: ">>106 没错。这就对了。知道的就知道。不知道的就不该知道。" },
        { floor: 108, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: "This is so creepy. Y’all are digging into a girl’s family like it’s a background check.", zh: "这也太creepy了。你们在挖一个女生的家庭背景，像在做背景调查似的。" },
        { floor: 109, username: "Anonymous", isAnonymous: true, timestamp: "1d ago", en: ">>108 Welcome to Aetheron. First time? ☕️", zh: ">>108 欢迎来到艾瑟隆。第一次来？☕️" },
        { floor: 110, username: "HunterFoster", isAnonymous: false, timestamp: "12h ago", en: "Alright fine. Since everyone's so curious 🙄 I was gonna make a move, but honestly… after reading this thread? Not worth the risk. So y'all can follow her yourselves. @sia_sijiao", zh: "行吧。既然大家都这么好奇 🙄 我本来是打算下手的，但说实话，看了这个帖子后我觉得不值得冒这个险。所以，你们自己关注她吧。@sia_sijiao" },
        { floor: 111, username: "Anonymous", isAnonymous: true, timestamp: "12h ago", en: ">>110 Hunter just… gave up? Publicly?", zh: ">>110 亨特就这么……放弃了？还公开说的？" },
        { floor: 112, username: "Anonymous", isAnonymous: true, timestamp: "12h ago", en: "Not him dropping her Instagram like a peace offering. 💀 That’s a first.", zh: "他居然把她的Instagram当和好礼物丢出来了。💀 这还是头一回。" },
        { floor: 113, username: "Anonymous", isAnonymous: true, timestamp: "12h ago", en: "Wait her Instagram is public? And she has zero posts?? 💀", zh: "等等她的Instagram是公开的？零帖子？？💀" },
        { floor: 114, username: "Anonymous", isAnonymous: true, timestamp: "12h ago", en: ">>113 Zero posts. Zero. That’s not a flex that’s a statement.", zh: ">>113 零帖子。零。那不是炫耀，那是一种态度。" },
        { floor: 115, username: "Anonymous", isAnonymous: true, timestamp: "12h ago", en: "Alright, but check her following list 🤔 It's empty too. Like… going for that whole mysterious aesthetic? Aren't art kids supposed to follow a bunch of galleries and artists? 🎨💀", zh: "行吧，但是看她的关注列表🤔 也是空的。像……走那种神秘美学路线？艺术生不应该都关注一堆画廊和艺术家吗？🎨💀" },
        { floor: 116, username: "Anonymous", isAnonymous: true, timestamp: "12h ago", en: "Oh, I see Titus already followed her 😂 Ha, Laurent and IsaiahHo too. How long has it even been?? 👀💀", zh: "哦，我看见泰特斯关注了，哈，洛朗和IsaiahHo也关注了，这才过去多久？？👀💀" },
        { floor: 117, username: "Anonymous", isAnonymous: true, timestamp: "12h ago", en: "Titus doesn't waste a single second 💀", zh: "泰特斯一秒都不会浪费 💀" },
        { floor: 118, username: "Anonymous", isAnonymous: true, timestamp: "10h ago", en: "We've gone from \"who is she\" to \"she's off limits\" 💀 Atherton efficiency. 👏", zh: "我们从‘她是谁’发展到‘她碰不得’💀 艾瑟隆效率。👏" },
        { floor: 131, username: "Anonymous", isAnonymous: true, timestamp: "4h ago", en: "OKAY SO. Just saw Titus and Sia walking together on campus. Together. As in. Walking. And talking. And she was SMILING.", zh: "行吧所以。刚看见泰特斯和希娅一起在校园里走。一起。就是说。走路。说话。她还在笑。" },
        { floor: 132, username: "Anonymous", isAnonymous: true, timestamp: "4h ago", en: ">>131 WHAT???", zh: ">>131 什么？？？" },
        { floor: 133, username: "Anonymous", isAnonymous: true, timestamp: "4h ago", en: ">>131 PHOTO??? ANYONE GET A PHOTO???", zh: ">>131 照片？？？有人拍到照片了吗？？？" },
        { floor: 134, username: "Anonymous", isAnonymous: true, timestamp: "4h ago", en: ">>131 It’s been FOUR DAYS since the thread started. That’s not “sliding into DMs” that’s a full-court press. 💀", zh: ">>131 帖子才发了四天。那不是‘滑进私信’，那是全场紧逼。💀" },
        { floor: 135, username: "Anonymous", isAnonymous: true, timestamp: "3h ago", en: "Called it. I called it on page one. 48 hours? Try 96 but still. I was right.", zh: "我说什么来着。我第一页就说了。四十八小时？九十六小时吧但还是。我说对了。" },
        { floor: 136, username: "Anonymous", isAnonymous: true, timestamp: "3h ago", en: ">>135 You said 48 and it took 96. That’s not “called it” that’s “off by double.” 💀", zh: ">>135 你说了四十八小时，结果花了九十六小时。那不叫‘说对了’，那叫‘翻倍了’。💀" },
        { floor: 137, username: "Anonymous", isAnonymous: true, timestamp: "2h ago", en: "Either way. Titus wins again. Man has never lost a race he actually wanted to win.", zh: "不管怎样。泰特斯又赢了。这人从来没输过一场他真正想赢的比赛。" }
    ];

    const posts = postsRaw.map(p => ({ ...p, score: Math.floor(Math.random() * 56) + 10, userVote: 0 }));

    const threadList = [
        { title: "Who's the new girl in the dining hall??? 👀🍝", replies: 137, lastActive: "2h ago", id: "main", author: "Anonymous" },
        { title: "Titus just scored the winning touchdown in practice 🔥 anyone else see that catch?", replies: 45, lastActive: "1h ago", id: "titus1", author: "football_fan" },
        { title: "Laurent Wynthorpe helped me carry my bags... is he always that nice? 😳", replies: 32, lastActive: "3h ago", id: "laurent1", author: "grateful_freshman" },
        { title: "Isaiah Ho's car collection spotted: McLaren 765LT in faculty lot 💸", replies: 28, lastActive: "5h ago", id: "isaiah1", author: "carspotter" },
        { title: "The watercolors in Vastrand Library are haunting. Who is the artist? 🎨", replies: 19, lastActive: "1d ago", id: "kjell1", author: "art_lover" },
        { title: "Hunter & Chance at it again — saw them corner someone near the gym 👀", replies: 67, lastActive: "2h ago", id: "hunter1", author: "Anonymous" },
        { title: "Casper Vickers: scholarship kid or something else? He's always alone 🤔", replies: 23, lastActive: "6h ago", id: "casper1", author: "curious" },
        { title: "Homecoming court predictions? Titus and Brittany? Or maybe the new girl? 👑", replies: 94, lastActive: "1h ago", id: "hc1", author: "drama_king" },
        { title: "Apollyn Hall honors suite — who is the mysterious girl on the top floor?", replies: 58, lastActive: "3h ago", id: "sia2", author: "Anonymous" },
        { title: "Student Council tea: Laurent vs. Titus tension? 👔🏈", replies: 76, lastActive: "4h ago", id: "rivalry", author: "insider" },
        { title: "Anyone else hear whispers about a secret 'Echo' spot? 👂", replies: 41, lastActive: "12h ago", id: "echo", author: "Anonymous" },
        { title: "Isaiah Ho's poker night — heard it's invite only 💰", replies: 33, lastActive: "1d ago", id: "isaiah2", author: "gambler" },
        { title: "Kjell Vastrand: does he ever speak? I've never heard his voice ❄️", replies: 29, lastActive: "2d ago", id: "kjell2", author: "curious_cat" },
        { title: "Luna Lake at midnight: romantic or creepy? 🌙", replies: 52, lastActive: "5h ago", id: "luna", author: "hopeless_romantic" },
        { title: "Freshman initiation stories — share your worst 😬", replies: 88, lastActive: "3h ago", id: "init", author: "survivor" },
        { title: "Titus Montimacy's party this weekend: who's going? 🔥", replies: 112, lastActive: "1h ago", id: "party", author: "party_animal" },
        { title: "Laurent's violin performance at the art center was breathtaking 🎻", replies: 47, lastActive: "6h ago", id: "laurent2", author: "music_lover" },
        { title: "Hunter's new 'pet'? I saw him with a blonde freshman again...", replies: 61, lastActive: "2h ago", id: "hunter2", author: "Anonymous" }
    ];

    function renderThreadList() {
        const container = document.getElementById("threadListContainer");
        container.innerHTML = "";
        threadList.forEach(thread => {
            const div = document.createElement("div");
            div.className = "thread-item";
            div.innerHTML = `
                <div class="thread-votes"><i class="fas fa-arrow-up"></i> ${Math.floor(Math.random() * 90) + 12}<br><span style="font-size:0.65rem;">👍</span></div>
                <div class="thread-main">
                    <div class="thread-title-link">${thread.title}</div>
                    <div class="thread-meta">
                        <span><i class="far fa-comment"></i> ${thread.replies} replies</span>
                        <span><i class="far fa-clock"></i> ${thread.lastActive}</span>
                        <span><i class="fas fa-user-secret"></i> ${thread.author}</span>
                    </div>
                </div>
            `;
            div.addEventListener("click", () => {
                if (thread.id === "main") showThreadDetail();
                else alert("🔒 This thread is not fully loaded. Only the main thread has all 137 replies + bilingual translation & interactive voting.");
            });
            container.appendChild(div);
        });
    }

    function attachVoteEvents(container) {
        container.querySelectorAll(".vote-col").forEach(voteCol => {
            const upBtn = voteCol.querySelector(".upvote-btn");
            const downBtn = voteCol.querySelector(".downvote-btn");
            const scoreSpan = voteCol.querySelector(".vote-score");
            const postId = voteCol.getAttribute("data-floor");
            if (!postId) return;
            const post = posts.find(p => p.floor == postId);
            if (!post) return;
            const updateUI = () => {
                scoreSpan.innerText = post.score;
                if (post.userVote === 1) {
                    upBtn.classList.add("upvote-active");
                    downBtn.classList.remove("downvote-active");
                } else if (post.userVote === -1) {
                    downBtn.classList.add("downvote-active");
                    upBtn.classList.remove("upvote-active");
                } else {
                    upBtn.classList.remove("upvote-active");
                    downBtn.classList.remove("downvote-active");
                }
            };
            const handleUpvote = () => {
                if (post.userVote === 1) {
                    post.score -= 1;
                    post.userVote = 0;
                } else {
                    if (post.userVote === -1) post.score += 1;
                    post.score += 1;
                    post.userVote = 1;
                }
                updateUI();
            };
            const handleDownvote = () => {
                if (post.userVote === -1) {
                    post.score += 1;
                    post.userVote = 0;
                } else {
                    if (post.userVote === 1) post.score -= 1;
                    post.score -= 1;
                    post.userVote = -1;
                }
                updateUI();
            };
            upBtn.removeEventListener("click", handleUpvote);
            downBtn.removeEventListener("click", handleDownvote);
            upBtn.addEventListener("click", handleUpvote);
            downBtn.addEventListener("click", handleDownvote);
            updateUI();
        });
    }

    function showThreadDetail() {
        const listPage = document.getElementById("threadListPage");
        const detailPage = document.getElementById("threadDetailPage");
        // 渲染详情内容（如果还没渲染过，或者每次重新渲染确保最新）
        const container = document.getElementById("postsContainer");
        if (container.children.length === 0) {
            posts.forEach(post => {
                const isOp = post.isOP || false;
                const opBadge = isOp ? '<span class="badge op">OP</span>' : '';
                const anonClass = post.isAnonymous ? "anonymous" : "";
                let enHtml = post.en.replace(/&/g, '&amp;').replace(/</g, '&lt;').replace(/>/g, '&gt;');
                enHtml = enHtml.replace(/&gt;&gt;(\d+)/g, '<span class="quote"><i class="fas fa-reply"></i> <a href="#post-$1" style="text-decoration:none; color:#2c6e9e;">>>$1</a></span>');
                enHtml = enHtml.replace(/\n/g, '<br>');
                let zhHtml = post.zh.replace(/&/g, '&amp;').replace(/</g, '&lt;').replace(/>/g, '&gt;');
                zhHtml = zhHtml.replace(/&gt;&gt;(\d+)/g, '<span class="quote"><i class="fas fa-reply"></i> >>$1</span>');
                zhHtml = zhHtml.replace(/\n/g, '<br>');
                const postDiv = document.createElement("div");
                postDiv.className = "post";
                postDiv.id = `post-${post.floor}`;
                postDiv.innerHTML = `
                    <div class="vote-col" data-floor="${post.floor}">
                        <i class="fas fa-arrow-up upvote-btn"></i>
                        <span class="vote-score">${post.score}</span>
                        <i class="fas fa-arrow-down downvote-btn"></i>
                    </div>
                    <div class="content-col">
                        <div class="post-header">
                            <span class="floor">${post.floor}L</span>
                            <span class="username ${anonClass}">${post.username}</span>
                            ${opBadge}
                            <span class="timestamp"><i class="far fa-clock"></i> ${post.timestamp}</span>
                        </div>
                        <div class="post-content">
                            <div class="en">${enHtml}</div>
                            <div class="zh"><i class="fas fa-language"></i> 中文: ${zhHtml}</div>
                        </div>
                        <div class="post-footer">
                            <span><i class="far fa-comment"></i> Reply</span>
                            <span><i class="fas fa-share-alt"></i> Share</span>
                            <span><i class="fas fa-flag"></i> Report</span>
                        </div>
                    </div>
                `;
                container.appendChild(postDiv);
            });
            attachVoteEvents(container);
            document.getElementById("detailMeta").innerHTML = `<i class="far fa-comment-dots"></i> 137 comments · full bilingual · interactive voting · updated 2h ago`;
        }
        // 动画切换
        listPage.classList.add("exit");
        listPage.classList.remove("enter");
        detailPage.classList.remove("exit");
        detailPage.classList.add("enter");
        // 等待动画结束后调整位置，确保详情页绝对定位不遮挡
        setTimeout(() => {
            listPage.style.display = "none";
            detailPage.style.display = "block";
        }, 250);
    }

    function backToHome() {
        const listPage = document.getElementById("threadListPage");
        const detailPage = document.getElementById("threadDetailPage");
        detailPage.classList.remove("enter");
        detailPage.classList.add("exit");
        listPage.classList.remove("exit");
        listPage.classList.add("enter");
        listPage.style.display = "block";
        setTimeout(() => {
            detailPage.style.display = "none";
        }, 250);
    }

    document.getElementById("backToHomeLink").addEventListener("click", (e) => {
        e.preventDefault();
        backToHome();
    });
    // 初始化列表显示，详情隐藏
    document.getElementById("threadDetailPage").style.display = "none";
    renderThreadList();
</script>
</body>
</html>
