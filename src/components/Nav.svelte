<script lang="ts">
  export let segment: string;
</script>

<style>
  ._bottom-line {
    position: relative;
  }
  ._bottom-line:before {
    content: '';
    display: block;
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 0;
    background: #0078f2;
    transition: height 0.1s ease-in-out;
  }
  ._bottom-line:hover:before {
    height: 5px;
  }
</style>

<nav class="bg-green-600 px-4 text-white">
  <ul class="flex">
    <li class="_bottom-line">
      <div class="p-4 ">
        <a
          class="hoge"
          aria-current="{segment === undefined ? 'page' : undefined}"
          href=".">home</a>
      </div>
    </li>

    <li class="_bottom-line">
      <div class="p-4">
        <a
          aria-current="{segment === 'about' ? 'page' : undefined}"
          href="about">about</a>
      </div>
    </li>

    <!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
    <li class="_bottom-line">
      <div class="p-4">
        <a
          rel="prefetch"
          aria-current="{segment === 'blog' ? 'page' : undefined}"
          href="blog">blog</a>
      </div>
    </li>
  </ul>
</nav>
