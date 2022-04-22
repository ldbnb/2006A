<template>
    <div>
        <!-- 头 -->
        <div class="header">
            <div class="el-icon-back" style="font-size: 21px;"></div>
            <div style="text-align: center;">新建居民档案</div>
            <div></div>
        </div>

        <!-- 表单 -->
        <van-form>
            <van-field v-model="username" name="真实姓名" label="真实姓名" placeholder="请填写居民的真实姓名"
                :rules="[{ required: true, message: '请填写姓名' }]" />
            <van-field v-model="password" name="身份证号" label="身份证号" placeholder="请填写居民的身份证号"
                :rules="[{ required: true, message: '请填写身份证号' }]" />
            <!-- 点击出弹窗 -->
            <van-field v-model="password" name="性别" label="性别" placeholder="请选择居民的性别" is-link @click="showPopup" />


            <!-- 底部弹窗 -->
            <van-popup v-model="show" position="bottom" :style="{ height: '30%' }" class="btm">
                <div class="top1">
                    请选择患者性别
                </div>
                <div class="top2">
                    男
                </div>
                <div class="top2">
                    女
                </div>
                <div class="top4">
                    取消
                </div>
            </van-popup>

            <!-- 日期 -->
            <van-field v-model="password" name="性别" label="出生日期" placeholder="请选择居民的出生日期" is-link @click="showPopup" />
            <van-popup v-model="show" position="bottom" :style="{ height: '30%' }" class="btm"></van-popup>

            <!-- 手机号码 -->
            <van-field v-model="password" name="手机号码" label="手机号码" placeholder="居民登陆账号，请正确填写"
                :rules="[{ required: true, message: '请填写手机号码' }]" />
           
            <!-- 登录密码 -->
            <van-field v-model="password" name="登录密码" label="登录密码" placeholder="8位以上的数字和字母组合"
                :rules="[{ required: true, message: '请填写登录密码' }]" />
                
            <!-- 现居地 -->
            <van-field v-model="password" name="现居地" label="现居地" placeholder="请填写现居地" />
            
            <!-- 居民标签 -->
            <van-field v-model="password" name="居民标签" label="居民标签" placeholder="点击选择居民标签">
                123
            </van-field>
            <div style="margin: 16px;">
                <van-button round block type="info" native-type="submit">提交</van-button>
            </div>


        </van-form>



    </div>
</template>
<script>
export default {
    data() {
        return {
            username: '',
            password: '',
            show: false,
        }
    },
    methods: {
        showPopup() {
            this.show = true;
        },
        qwe(e) {
            console.log(e);
        }
    },
}
</script>
<style lang="scss">
.header {
    width: 100%;
    line-height: 50px;
    background-color: #fff;

    div {
        flex: 1;
        line-height: 50px;
    }
}

.btm {
    border-radius: 16px 16px 0px 0px;
    width: 100%;
    text-align: center;
    background-color: #f2f2f2;

    .top1 {
        font-size: 17px;
        font-weight: 100;
        color: #999999;
        line-height: 55px;
        border-bottom: 1px solid;
    }

    .top2 {
        color: #1877f2;
        font-size: 20px;
        border-bottom: 1px solid #999999;
        line-height: 65px;
    }

    .top4 {
        line-height: 70px;
        font-size: 22px;
        color: #999999;
        position: relative;
        top: 5px;
    }
}
</style>