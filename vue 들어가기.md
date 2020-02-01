전역 선언시에는 Vue.component로 부터 시작함
일부는 new Vue({el:#container})로 선언함
Hello.vue
<template>
    <p>{{greeting}} World!</p>
</template>
<script>
module.exports = {
    data: function(){
        return {
            greeting: 'Hello'
        }
    }
}
</script>

<style scoped>
p{
    font-size: 2em;
    text-align: center;
}
</style>

=>
1. 완전한 구문 강조
2. CommonJS 모듈
3. 컴포넌트에만 제한된 css

관심사의 분리를 무엇입니다.

진행 한 내용 - https://kr.vuejs.org/v2/guide/unit-testing.html