<script setup lang="ts">
import { ref } from "vue";

const activeNav = ref("发现");
const navItems = ["发现", "话题", "社区原则"];
const examples = [
  {
    number: "01",
    label: "一句话",
    title: "有些话，过了很久才知道是什么意思。",
    description: "从一句触动你的话开始，聊聊它为什么留在心里。",
    tone: "peach",
  },
  {
    number: "02",
    label: "人生故事",
    title: "后来你才明白的一件小事是什么？",
    description: "不必写成大道理。一个真实的瞬间，就值得被听见。",
    tone: "sage",
  },
  {
    number: "03",
    label: "不同观点",
    title: "我们可以不同意，也可以认真听完。",
    description: "让观点相遇，而不是急着给彼此下结论。",
    tone: "blue",
  },
];
</script>

<template>
  <main class="site-shell">
    <header class="topbar">
      <a class="brand" href="#" aria-label="TA说首页">
        <span class="brand-mark">TA</span>
        <span>TA说</span>
      </a>
      <nav class="topnav" aria-label="主导航">
        <button
          v-for="item in navItems"
          :key="item"
          class="nav-item"
          :class="{ 'nav-item-active': activeNav === item }"
          type="button"
          @click="activeNav = item"
        >
          {{ item }}
        </button>
        <a class="nav-cta" href="#start">开始探索 <span aria-hidden="true">↗</span></a>
      </nav>
    </header>

    <section class="hero">
      <div class="hero-copy">
        <p class="eyebrow"><span class="eyebrow-dot" /> 一个认真交流的地方</p>
        <h1>一句话开始，<br /><span>和真实的人</span>相遇。</h1>
        <p class="hero-description">
          一句喜欢的台词、一段没讲完的故事、一个不同的观点。
          TA说希望每一次表达，都有机会成为一次真正的交流。
        </p>
        <div class="hero-actions" id="start">
          <a class="button button-primary" href="#how-it-works">认识 TA说 <span aria-hidden="true">→</span></a>
          <a class="text-link" href="#community">看看我们相信什么</a>
        </div>
        <div class="hero-note">
          <span class="note-avatar">T</span>
          <span>不必完美表达，真诚就可以开始。</span>
        </div>
      </div>

      <div class="hero-art" aria-label="TA说社区理念插画">
        <div class="art-orbit orbit-one"></div>
        <div class="art-orbit orbit-two"></div>
        <div class="quote-card quote-card-back">
          <span class="quote-mark">“</span>
          <p>原来不止我<br />一个人这样想。</p>
          <span class="quote-caption">一段对话之后</span>
        </div>
        <div class="quote-card quote-card-front">
          <span class="quote-tag">TA 的一句话</span>
          <p>我们不必<br /><em>完全相同</em>，<br />也能彼此理解。</p>
          <div class="card-bottom">
            <span class="tiny-avatars"><i>A</i><i>林</i><i>你</i></span>
            <span>正在发生的交流</span>
          </div>
        </div>
        <span class="floating-dot dot-a"></span>
        <span class="floating-dot dot-b"></span>
        <span class="floating-star">✳</span>
      </div>
    </section>

    <section class="intro-strip" id="how-it-works">
      <p>不是为了刷过更多内容。</p>
      <p>而是让内容，带我们走近彼此一点。</p>
    </section>

    <section class="section community-section" id="community">
      <div class="section-heading">
        <div>
          <p class="eyebrow">从这里开始</p>
          <h2>每一种表达，<br class="mobile-break" />都可以成为话题。</h2>
        </div>
        <p class="section-summary">内容是起点，交流才是目的。<br />你可以分享，也可以只是先听听。</p>
      </div>
      <div class="idea-grid">
        <article v-for="item in examples" :key="item.number" class="idea-card" :class="item.tone">
          <div class="idea-card-top">
            <span>{{ item.number }}</span>
            <span class="idea-label">{{ item.label }}</span>
          </div>
          <h3>{{ item.title }}</h3>
          <p>{{ item.description }}</p>
          <span class="idea-arrow" aria-hidden="true">↗</span>
        </article>
      </div>
    </section>

    <section class="principles" id="principles">
      <div class="principles-copy">
        <p class="eyebrow">社区的底色</p>
        <h2>认真表达，<br />也认真对待<br /><span>每一个表达的人。</span></h2>
      </div>
      <div class="principle-list">
        <div class="principle-item">
          <span>01</span>
          <div><h3>保持真实</h3><p>日常交流使用稳定的社区身份，不需要公开真实姓名。</p></div>
        </div>
        <div class="principle-item">
          <span>02</span>
          <div><h3>给敏感表达留出空间</h3><p>仅在明确开放匿名的指定主题中，提供受保护的表达方式。</p></div>
        </div>
        <div class="principle-item">
          <span>03</span>
          <div><h3>分歧不等于伤害</h3><p>欢迎不同意见；骚扰、威胁和隐私侵犯则需要被认真处理。</p></div>
        </div>
      </div>
    </section>

    <footer class="footer">
      <a class="brand" href="#"><span class="brand-mark">TA</span><span>TA说</span></a>
      <p>让表达成为相遇的开始。</p>
      <span class="footer-meta">一个仍在生长的社区 · 早期开发版本</span>
    </footer>
  </main>
</template>
