<template>
    <div class="home-main">
        <div class="container">
            <div class="details">
                <div><img src="../assets/components_logo.png" alt="componentslogo" /></div>
                <div class="component"><img src="../assets/components.png" alt="components" /></div>
                <p class="fte">设计、前端高效协同，快速搭建移动端组件库</p>
                <div class="WeChat">
                    <qrcode :value="qrcodeValue" :options="qrcodeOptions"></qrcode>
                </div>
            </div>
            <div class="phone" ref="phone">
                <div class="doc-simulator">
                    <div class="doc-simulator__nav">
                        <div class="doc-simulator__url">{{qrcodeValue}}</div>
                        <div class="doc-simulator__reload"></div>
                    </div>
                    <iframe :src="qrcodeValue" frameborder="0"></iframe>
                </div>
            </div>
        </div>
        <div class="cards">
            <ul>
                <li>
                    <img src="../assets/diamond.png" alt="" />
                    <div class="card">SKETCH 组件下载</div>
                </li>
                <li>
                    <img src="../assets/palette.png" alt="" />
                    <div class="card">移动设计规范文档下载</div>
                </li>
                <li>
                    <img src="../assets/exploit.png" alt="" />
                    <div class="card">前端开发文档下载</div>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
import qrcode from '../components/qrcode.js';
import { hostName } from '../config/env.js';
export default {
    data() {
        return {
            qrcodeValue: hostName + '/demo.html',
            qrcodeOptions: {
                size: 164
            }
        }
    },
    components: {
        qrcode
    }
}
</script>

<style lang="less">

</style>
