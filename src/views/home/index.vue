<template>
    <div>
       <div class="top">
        <div class="top_box">
            <div class="top_left">
                <div class="logo">
                    <img src="./imgs/logo.png" alt="">
                </div>
                <div class="title">
                    <h1>智慧党建平台</h1>
                </div>
            </div>
            <div class="top_right">
                <div class="login">
                    <div class="guanliyuan">
                        <span class="iconfont icon-guanliyuan"></span>
                        <a href="">管理员登录</a>
                    </div>
                    <div class="yonghu">
                        <span class="iconfont icon-yonghu"></span>
                        <a href="">用户登录</a>
                    </div>
                </div>
                <div class="search">
                    <div class="input-group mb-3">
                        <input type="text" class="form-control" placeholder="请输入关键词">
                        <button class="btn btn-success" type="submit">搜索</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- 轮播图 + 通知公告 -->
    <div class="mgTop15 bagW1 w1">
        <div class="constainer">
            <div class="row">
                <div class="col-sm-7">
                    <!-- 轮播 -->
                    <div id="demo" class="carousel slide" data-bs-ride="carousel">
                        <!-- 轮播图片 -->
                        <div class="carousel-inner">
                            <div class="carousel-item active">
                                <img src="./imgs/ceshi.png" class="d-block"
                                    style="width:100%">
                            </div>
                        </div>
                        <!-- 左右切换按钮 -->
                        <button class="carousel-control-prev" type="button" data-bs-target="#demo" data-bs-slide="prev">
                            <span class="carousel-control-prev-icon"></span>
                        </button>
                        <button class="carousel-control-next" type="button" data-bs-target="#demo" data-bs-slide="next">
                            <span class="carousel-control-next-icon"></span>
                        </button>
                    </div>
                </div>
                <div class="col-sm-5">
                    <div class="lan_title">
                        <ul>
                            <i class="iconfont"></i>
                            <p>时政新闻</p>
                        </ul>
                        <a href="" target="_blank">更多>></a>
                    </div>
                    <div class="lan_content">
                        <ul>
                            <li>
                                <a href="" target="_blank" title="">2018年ssssssss学雷锋志愿服务“四个100”先进典型名单公示</a>
                                <div class="data">
                                    <em>2022-10-22</em>
                                </div>
                            </li>
                            <li>2</li>
                            <li>3</li>
                            <li>4</li>
                            <li>5</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- 通知公告 + 党建风采 -->
    <div class="mgTop15 bagW1 w2">
        <div class="constainer">
            <div class="row">
                <div class="col-sm-6">
                    <div class="lan_title">
                        <ul>
                            <i class="iconfont"></i>
                            <p>通知公告</p>
                        </ul>
                        <a href="" target="_blank">更多>></a>
                    </div>
                </div>
                <div class="col-sm-6">
                    <div class="lan_title">
                        <ul>
                            <i class="iconfont"></i>
                            <p>党建风采</p>
                        </ul>
                        <a href="" target="_blank">更多>></a>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- 应用管理 -->
    <div class="mgTop15 bagW1 w3">
        <div class="container">
            <div class="row">
                <div class="col-md-2 col-sm-4 col-4">
                    <div class="server">
                        <a href="">
                            <i class="iconfont icon-qiandao"></i>
                            <span>活动签到</span>
                        </a>
                    </div>
                </div>
                <div class="col-md-2 col-sm-4 col-4">
                    <div class="server">
                        <a href="">
                            <i class="iconfont icon-icon_xinyong_xianxing_jijin-207"></i>
                            <span>活动报名</span>
                        </a>
                    </div>
                </div>
                <div class="col-md-2 col-sm-4 col-4">
                    <div class="server">
                        <a href="">
                            <i class="iconfont icon-icon_home_paymentrecord"></i>
                            <span>党费缴纳</span>
                        </a>
                    </div>
                </div>
                <div class="col-md-2 col-sm-4 col-4">
                    <div class="server">
                        <a href="">
                            <i class="iconfont icon-toupiaoguanli"></i>
                            <span>投票管理</span>
                        </a>
                    </div>
                </div>
                <div class="col-md-2 col-sm-4 col-4">
                    <div class="server">
                        <a href="">
                            <i class="iconfont icon-tijiao"></i>
                            <span>提交作业</span>
                        </a>
                    </div>
                </div>
                <div class="col-md-2 col-sm-4 col-4">
                    <div class="server">
                        <a href="">
                            <i class="iconfont icon-tongji"></i>
                            <span>数据分析</span>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div> 
    </div>

</template>

<script>
export default {
    name:'Home',
    data() {
        return {
            
        }
    },
}
</script>

<style lang="scss" scoped>
  
  * {
    margin: 0;
    top: 0;
    list-style: none;
  }
  body {
    margin: 0px auto;
    padding: 0px;
    border: 0px;
    color: #000;
    text-align: justify;
    text-justify: inter-ideograph;
    position: relative;
    width: 100%;
    background: #f2f2f2;
  }
  div,
  form,
  img,
  ul,
  ol,
  li,
  dl,
  dt,
  dd,
  em,
  i,
  cite,
  h1,
  h2,
  h3,
  h4,
  h5,
  h6,
  p {
    // padding: 0px;
    border: 0px;
    margin: 0px auto;
    list-style: none;
    font-style: normal;
  }
  html,body {
      font-size: 5px;
    }
  .top {
    width: 100%;
    height: 10.9375rem;
    background: red url("./imgs/top.jpg") no-repeat center top;
  }
  .top .top_box {
    width: 75rem;
    height: 10.9375rem;
  }
  .top .top_box .logo {
    margin-top: 3.4375rem;
    width: 5.5rem;
    float: left;
  }
  .top .top_box .logo img {
    width: 4.6875rem;
  }
  .top .top_box h1 {
    font-size: 2.8125rem;
    color: #ffc600;
    height: 10.9375rem;
    line-height: 10.9375rem;
    font-weight: 400;
    float: left;
  }
  .top_right {
    height: 10.9375rem;
    width: 28.25rem;
    float: right;
  }
  .top_right .search {
    width: 18.75rem;
    float: right;
    margin: auto 0;
  }
  .login {
    height: 3.125rem;
    width: 28.25rem;
    margin-top: 1.25rem;
    float: right;
  }
  .login a {
    font-size: 1rem;
  }
  .login .iconfont {
    font-size: 1.625rem;
  }
  .login .guanliyuan {
    float: left;
  }
  .login .yonghu {
    float: left;
  }
  a {
    text-decoration: none;
    color: #333;
  }
  a:hover,
  a:visited,
  a:link,
  a:active {
    color: #333;
  }
  .mgTop15 {
    margin-top: 0.9375rem;
  }
  .bagW1 {
    background-color: #fff;
    padding: 0.9375rem;
    width: 73.125rem;
    overflow: hidden;
  }
  .w2 {
    height: 25rem;
  }
  .lan_title {
    width: 100%;
    height: 2.625rem;
    font: 0.875rem / 2.625rem;
    background: #ededed;
    position: relative;
  }
  .lan_title ul {
    float: left;
    position: absolute;
    height: 2.625rem;
    background: url("./imgs/lan_title.png") no-repeat right bottom;
    padding: 0rem 1.875rem 0rem 0.625rem;
  }
  .lan_title ul p {
    color: #fff;
    font-size: 1rem;
    line-height: 2.625rem;
    height: 2.625rem;
    font-weight: 600;
  }
  .lan_title a {
    float: right;
    line-height: 2.625rem;
    height: 2.625rem;
    font-size: 0.75rem;
    padding-right: 0.625rem;
  }
  .lan_content ul li {
    clear: both;
    float: left;
    height: 2.6875rem;
    width: 100%;
    border-bottom: 1px dashed #f2f2f2;
  }
  .lan_content ul li a {
    float: left;
    font-size: 1rem;
    line-height: 2.6875rem;
    height: 2.6875rem;
    padding-left: 0.9375rem;
    overflow: hidden;
    width: 75%;
    white-space: nowrap;
    text-overflow: ellipsis;
  }
  .lan_content ul li .data {
    float: right;
    width: 25%;
    height: 2.6875rem;
  }
  .lan_content ul li .data em {
    float: right;
    font-size: 0.75rem;
    color: #999;
    line-height: 2.6875rem;
    height: 2.6875rem;
  }
  // .w3 .server {
  //   height: 7.5rem;
  // }
  .w3 .server a {
    background-color: #fff;
    display: block;
    text-align: center;
    border: 0.0625rem #f0f0f0 solid;
  }
  .w3 .server a i {
    display: block;
    color: #e9312e;
    font-weight: 18.75rem;
    font-size: 4.125rem;
  }
  .w3 .server a span {
    display: block;
    width: 100%;
  }
  
</style>