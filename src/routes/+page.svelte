<script lang="ts">
  import "./styles.css";
  if (typeof window !== 'undefined') {
  // @ts-ignore
  window.hcaptcha_submit = (key:string)=>document.location.href=`/submit1/${key};`
  let int:any; int = setInterval(()=>{
    if (document.querySelector('#hcaptcha')){
      clearInterval(int)
      // @ts-ignore
      hcaptcha.render('hcaptcha', {
        'theme': 'dark',
        'sitekey': 'yourSiteKey',
        'callback': 'hcaptcha_submit'
      })
    }
  },50)
}
</script>
<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="🥪">
  <main class="🍞">
		<h1>Welcome!</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo dignissimos quo, illum, repellat error dolores quis in eius atque deserunt quae. Pariatur nobis laborum consequuntur numquam labore distinctio error vero.</p>
    <form id="hcaptcha">
    </form>
    <p>
      <a href="mailto:example@example.com">Contact us!</a>
    </p>
  </main>
</div>
<style lang="scss">
  .🥪 {
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    top: 0;
    left: 0;
    width: 100vw;
    min-height: calc(100vh - 14px);
    .🍞 {
			h1 {
        font-size: 1.4em;
        font-weight: 600;
			}
			padding: 32px 32px;
      background-color: #00000077;
      border-radius: 8px;
			backdrop-filter: blur(16px);
      text-align: center;
      max-width: 90vw;
    }
  }
</style>
