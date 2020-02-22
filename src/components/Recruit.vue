<template>
  <div class="sub">
    <SubTitle v-bind:titledata = "title"></SubTitle>
    <!--  -->
    <div class="recruit">
      <div class="contents">
        <h2>월급만 필요하다면 지원하지 마세요<br>
        우리는 의미 있는 일을 하려고 합니다<br>
        대신 함께 할 수 있다면 업계 최고대우를 보장합니다.</h2>
        <p class="par">교육에 대한 열정이 남다르고 아이디어가 넘쳐나는 사람들은<br>
        절대로 현재에 머무르려고 하지 않는다고 믿습니다.<br><br>
        그래서 저희 회사에는 없는 것이 다음과 같습니다.</p>
        <div class="icon">
          <div id="upmargin">
            <div class="subicon up">
              <div class="char1">
                <h2><img src="../assets/icon_recruit01.png"></h2>
                <h3><span class="num">01</span>직급이 없습니다.</h3><div class="numback"></div>
                <p class="far">동등한 관계에서만 좋은 아이디어가 나온다고 믿기 때문입니다.<br>
                그래서 모두 'oo씨'라고 부릅니다.</p>
              </div>
              
              <div class="char1">
                <h2><img src="../assets/icon_recruit02.png"></h2>
                <h3><span class="num">02</span>야근이 없습니다.</h3><div class="numback"></div>
                <p class="far">모든 직원이 재택근무를 하기 때문에 야근이 없습니다.<br>
                대신 주어진 일을 책임 있게 해내지 못하면 불이익이 있습니다.<br>
                월 2회 전체회의 4시간은 필참입니다.</p>
              </div>
            </div>
          </div>
          <div class="subicon down">
            <div class="char2">
              <h2><img src="../assets/icon_recruit03.png"></h2>
              <h3><span class="num">03</span>회식이 없습니다.</h3><div class="numback"></div>
              <p class="far">의무적인 회식문화 자체가 없습니다.<br>
              대표가 회식을 싫어합니다.<br>
              회식비 모았다가 해외 워크샵 갑니다.</p>
            </div>

            <div class="char2">
              <h2><img src="../assets/icon_recruit04.png"></h2>
              <h3><span class="num">04</span>경력직이 없습니다.</h3><div class="numback1"></div>
              <p class="far">모든 직원은 3년 안에 독립(창업)하는 것을 목표로 합니다.<br>
              3년 이후에는 회사를 설립하여 파트너쉽을 맺어 일을 함께 합니다.<br>
              3년 이상 일하고 싶을 때는 합당한 사유서를 제출해야 합니다.</p>
            </div>
          </div>    
        </div>
        <section class="business">
          <ul class="businesstype">
            <li class="type">
              <h2>교육사업부</h2>
              <p>교육사업부는 오프라인 스쿨과정과 전국 학교에<br>
              출강하는 교육컨텐츠의 기획 및 운영과<br>
              기업체 홍보 및 마케팅 업부를 담당합니다.</p>
              <div class="bar"></div>
              <p>-프로그램 개발 및 교육<br>
              -프로그램 홍보 및 마케팅</p>
            </li>
            <li class="type">
              <h2>IT사업부</h2>
              <p>IT사업부는 온라인 스쿨과정과 개발과 운영<br>
              필요한 서비스를 제공하는 업무를 담당하며,<br>
              추후 IT 스타트업으로의 독립을 목표로 합니다.</p>
              <div class="bar"></div>
              <p>-온라인 서비스 기획 및 개발<br>
              -Android / iOS 개발<br>
              -온라인 홍보 및 마케팅</p>
            </li>
            <li class="type">
              <h2>경영지원부</h2>
              <p>경영지원팀은 Mentoring-lab의<br>
              전반적인 업무가 원활하게 진행될 수 있도록<br>
              돕는 핵심적인 부서입니다.</p>
              <div class="bar"></div>
              <p>-재무, 회계관리<br>
              -행정, 사업일정관리<br></p>
            </li>
          </ul>
          <div class="download"><a href="#">지원서 다운로드</a></div>
        </section>
    </div>
    </div>
  </div>
</template>

<script>
import SubTitle from './Sub/SubTitle'
export default {
  name: 'Recruit',
  components : {
    SubTitle
  },
  data : function() {
return {
    title : "RECRUIT"
  };
}
}
</script>
  
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
