<script setup>

</script>

<template>
<div class="left">
    <div class="photo"></div>
    <div class="mes">
        名称：循矩 <br>
        年龄：22 <br>
        性别：男 <br>
        爱好：看书 旅游 编程 修图 <br>
        地址：Guangdong China <br> 
        邮箱：a1361317804@gmail.com <br>

    </div>
</div>
<div class="right">
    <div class="showcase image-showcase">
        <h2>图片作品</h2>
        <div class="showcase-content">
            <!-- 这里放图片作品内容 -->
             
        </div>
    </div>
    
    <div class="showcase video-showcase">
        <h2>视频作品</h2>
        <div class="showcase-content">
            <!-- 这里放视频作品内容 -->
        </div>
    </div>
    
    <div class="showcase project-showcase">
        <h2>项目展示</h2>
        <div class="showcase-content">
            <!-- 这里放项目作品内容 -->
        </div>
    </div>
</div>
</template>
<style scoped>

.left {
    background-color: rgba(19, 16, 16, 0.3);
    width: 30%;
    height: 100%;
    position: fixed; /* 新增 */
    left: 10px; /* 新增 */
    top: 0; /* 新增 */
}
.photo {
    background-image: url('/src/assets/img/00008-13576920.png');
    position: relative;
    top: 50px;
    margin: 0 auto;
    width: 15vw; /* 改为视口宽度的15% */
    height: 15vw; /* 保持宽高比例一致 */
    min-width: 100px; /* 设置最小宽度 */
    min-height: 100px; /* 设置最小高度 */
    max-width: 200px; /* 设置最大宽度 */
    max-height: 200px; /* 设置最大高度 */
    border-radius: 50%;
    background-position: center; 
    background-size: cover;
}

/* 媒体查询部分可以简化 */
@media screen and (max-width: 768px) {
    .mes {
        font-size: 16px;
        left: 30px;
        max-width: calc(100% - 60px);
    }
    

}
.mes {
    position: relative;
    top: 100px;
    left: 50px;
    color: white;
    font-size: 20px;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
    max-width: calc(100% - 100px);
    word-wrap: break-word;
    overflow-wrap: break-word;
    line-height: 2.0; /* 增加行间距 */
    letter-spacing: 0.5px; /* 增加字间距 */
}

/* 媒体查询部分也需要保持行间距 */
@media screen and (max-width: 768px) {
    .mes {
        font-size: 16px;
        left: 30px;
        max-width: calc(100% - 60px);
        line-height: 1.6; /* 移动端稍微减小行间距 */
    }
}

/* 添加媒体查询，针对移动设备 */
@media screen and (max-width: 768px) {
    .mes {
        font-size: 14px; /* 移动端字体更小 */
        left: 30px; /* 减小左边距 */
        line-height: 1.4; /* 移动端减小行间距 */
        letter-spacing: 0.3px; /* 移动端减小字间距 */
        word-break: break-all; /* 移动端强制换行 */
        white-space: normal; /* 移动端换行符生效 */
        max-width: calc(100% - 60px); /* 调整最大宽度 */
    }
    
    .photo {
        width: 100px; /* 移动端头像更小 */
        height: 100px;
    }
}

/* 更小的屏幕 */
@media screen and (max-width: 480px) {
    .mes {
        font-size: 14px; /* 更小屏幕字体更小 */
    }
}
.right {
    position: fixed;
    left: calc(30% + 20px);
    top: 0;
    width: calc(70% - 30px);
    height: 100%;
    display: flex;
    flex-direction: column;
    padding-top: 20px;
    overflow-y: auto;
}

.showcase {
    background-color: rgba(19, 16, 16, 0.3);
    border-radius: 10px;
    padding: 20px;
    margin-bottom: 20px;
    color: white;
    transition: all 0.3s ease;
}

.showcase:hover {
    background-color: rgba(19, 16, 16, 0.5);
    transform: translateY(-5px);
}

.showcase h2 {
    margin-top: 0;
    border-bottom: 1px solid rgba(255, 255, 255, 0.2);
    padding-bottom: 10px;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}

.showcase-content {
    min-height: 150px;
}

/* 为不同类型的展示区添加特定样式 */
.image-showcase {
    /* 图片展示区特定样式 */
}

.video-showcase {
    /* 视频展示区特定样式 */
}

.project-showcase {
    /* 项目展示区特定样式 */
}

/* 响应式调整 */
@media screen and (max-width: 768px) {
    .left {
        position: relative;
        width: 100%;
        height: auto;
        padding-bottom: 20px;
    }
    .photo {
        position: relative;
        top: 20px;
        margin: 20px auto;
    }
    .mes {
        position: relative;
        top: 20px;
        left: 0;
        margin: 20px;
        text-align: center;
    }
    
    .right {
        position: relative;
        left: 0;
        top: 0;
        width: 100%;
        height: auto;
        padding-top: 10px;
    }
    
    .showcase {
        padding: 15px;
    }
}
</style>
