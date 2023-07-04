---
# the default layout is 'page'
icon: fas fa-info-circle
order: 4
---

您好，我是 [yexca](https://a.yexca.xyz/)，<s>这个网站是我和我的同学 [Hiyoung](https://blog.yexca.xyz/index.php/author/hiyoung/) 一起运营的</s>

此网站为我<s>们</s>的日常学习分享

## 建站目的

由于本人记忆力不是特别好，故建立此网站记录自己进行探索时遇到困难的解决过程

文章仅作解决问题的记录

## 联系我

Email: <yexca@duck.com>

<div class="wp-block-group is-layout-flow"><div class="wp-block-group__inner-container">## 网站历史

</div></div>- 2021.11.04 建立
- 2021.11.11 通过ICP域名备案
- 2021.11.12 开始建设，通过多次修改，最终使用Astra主题（崩溃重装过）
- 2021.11.16 通过公安联网备案
- 2021.11.22 更换主题[Sakurairo](https://iro.tw/)
- 2022.01.30 更换主题[Argon](https://github.com/solstice23/argon-theme)
- 2023.04.04 转换为全 Docker 部署
- 2023.05.05 纪念服务器第一次崩了
- 2023.07.03 转移博客至 Jekyll


<!-- 博客运行时间 - 开始 -->
<script>
    function secondToDate(second) {
        if (!second) {
            return 0;
        }
        var time = new Array(0, 0, 0, 0, 0);
        if (second >= 365 * 24 * 3600) {
            time[0] = parseInt(second / (365 * 24 * 3600));
            second %= 365 * 24 * 3600;
        }
        if (second >= 24 * 3600) {
            time[1] = parseInt(second / (24 * 3600));
            second %= 24 * 3600;
        }
        if (second >= 3600) {
            time[2] = parseInt(second / 3600);
            second %= 3600;
        }
        if (second >= 60) {
            time[3] = parseInt(second / 60);
            second %= 60;
        }
        if (second > 0) {
            time[4] = second;
        }
        return time;
    }</script>
<script type="text/javascript" language="javascript">
    function setTime() {
        var create_time = Math.round(new Date(Date.UTC(2021, 10, 06, 14, 15, 19)).getTime() / 1000);
        var timestamp = Math.round((new Date().getTime() + 8 * 60 * 60 * 1000) / 1000);
        currentTime = secondToDate((timestamp - create_time));
        currentTimeHtml = 'This Blog has running: <br/>' + currentTime[0] + ' y ' + currentTime[1] + ' d '
                + currentTime[2] + ' h ' + currentTime[3] + ' m ' + currentTime[4]
                + ' s';
        document.getElementById("htmer_time").innerHTML = currentTimeHtml;
    }    setInterval(setTime, 1000);
</script>
<!-- 博客运行时间 - 结束 -->

<p><span id="htmer_time" style="color: var(--themecolor);"></span></p>