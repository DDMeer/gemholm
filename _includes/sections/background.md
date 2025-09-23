<!-- background.md -->

<div class="card pad tight">
  <h3>相关背景图</h3>
  <p class="text-2">这里写一句简短说明，可删。</p>

  <!-- ========= 走马灯容器（纯 CSS，无缝循环） ========= -->
  <style>
    /* 外层容器：裁剪溢出，保留圆角 */
    .marquee-wrap { overflow: hidden; border-radius: 12px; }

    /* 滚动轨道：横向拼接两份内容，无缝衔接 */
    .marquee-track {
      display: flex;
      gap: 24px;                 /* 卡片之间的间距 */
      width: max-content;        /* 由内容撑开 */
      animation: marquee-scroll 28s linear infinite;
    }

    /* 悬停暂停滚动（可删） */
    .marquee-wrap:hover .marquee-track { animation-play-state: paused; }

    /* 单个图卡 */
    .marquee-item {
      flex: 0 0 auto;
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 4px 12px rgba(0,0,0,.08);
      background: #fff;
    }
    .marquee-item img {
      display: block;
      height: 220px;             /* 统一高度，按比例缩放 */
      width: auto;
    }
    .marquee-caption {
      text-align: center;
      font-size: .95rem;
      padding: 10px 8px;
      background: #fff;
      color: #4b5563;
    }

    /* 关键帧：因为内容重复了一遍(-50%)即可无缝 */
    @keyframes marquee-scroll {
      from { transform: translateX(0); }
      to   { transform: translateX(-50%); }
    }

    /* 如果想从左→右滚动，取消下一行注释即可 */
    /* .marquee-track { animation-direction: reverse; } */

    /* 移动端适配：降低高度 */
    @media (max-width: 640px) {
      .marquee-item img { height: 160px; }
    }
  </style>

  <div class="marquee-wrap">
    <div class="marquee-track">

      <!-- ===== 第一组（你的原始图片） ===== -->
      <figure class="marquee-item">
        <img src="{{ '/assets/images/background/bg-01.jpg' | relative_url }}" alt="背景图 1">
        <figcaption class="marquee-caption">说明文字 1</figcaption>
      </figure>
      <figure class="marquee-item">
        <img src="{{ '/assets/images/background/bg-02.jpg' | relative_url }}" alt="背景图 2">
        <figcaption class="marquee-caption">说明文字 2</figcaption>
      </figure>
      <figure class="marquee-item">
        <img src="{{ '/assets/images/background/bg-03.jpg' | relative_url }}" alt="背景图 3">
        <figcaption class="marquee-caption">说明文字 3</figcaption>
      </figure>

      <!-- ===== 第二组（重复一遍以实现无缝） ===== -->
      <figure class="marquee-item">
        <img src="{{ '/assets/images/background/bg-01.jpg' | relative_url }}" alt="背景图 1">
        <figcaption class="marquee-caption">说明文字 1</figcaption>
      </figure>
      <figure class="marquee-item">
        <img src="{{ '/assets/images/background/bg-02.jpg' | relative_url }}" alt="背景图 2">
        <figcaption class="marquee-caption">说明文字 2</figcaption>
      </figure>
      <figure class="marquee-item">
        <img src="{{ '/assets/images/background/bg-03.jpg' | relative_url }}" alt="背景图 3">
        <figcaption class="marquee-caption">说明文字 3</figcaption>
      </figure>

    </div>
  </div>
  <!-- ========= /走马灯 ========= -->
</div>
