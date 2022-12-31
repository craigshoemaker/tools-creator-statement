<script>

  const statement = {
    building: '',
    for: '',
    help: '',
    by: '',
    world: '',
    build: function() {
      const s = statement;
      const value = [];

      if(s.building.length > 0) {
        value.push(`I am building ${s.building}`);
      }

      if(s.for.length > 0) {
        value.push(` for ${s.for}`);
      }

      if(s.help.length > 0) {
        value.push(` to help them ${s.help}`);
      }

      if(s.by.length > 0) {
        value.push(` by ${s.by}`);
      }

      if(s.world.length > 0) {
        value.push(` in a world where ${s.world}.`);
      }

      return value.join('');
    }
  }

</script>

<div class="component">
  <h1 class="has-text-centered">Creator Statement</h1>
  <p class="has-text-centered">As featured in the <a href="https://completecreator.co">Complete Creator</a> from <a href="https://twitter.com/jonbrosio/status/1569687423948410886" target="_blank">Jon Brosio</a>.</p>
  <div class="statement">
    <div class="building">
      <label for="">I'm building</label>
      <input type="input" class="input"
        placeholder="a Twitter account"
        bind:value={statement.building} />
    </div>
    <div class="for">
      <label for="">for</label>
      <input type="input" class="input"
        placeholder="writers"
        bind:value={statement.for} />
    </div>
    <div class="help_">
      <label for="">to help them</label>
      <input type="input" class="input"
        placeholder="become full-time creators"
        bind:value={statement.help} />
    </div>
    <div class="by">
      <label for="">by</label>
      <input type="input" class="input"
        placeholder="writing about their passions"
        bind:value={statement.by} />
    </div>
    <div class="world">
      <label for="">in a world where</label>
      <input type="input" class="input"
        placeholder="solopreneurship is the future"
        bind:value={statement.world} />
    </div>
  </div>
  
  <div class="text">
    <textarea class="textarea"
      value={statement.build()}></textarea>
  </div>

</div>


<style>
  h1 {
    margin: 2em 0 1em 0;
  }

  input {
    display: inline-block;
    margin: .5em 0 .5em 0;
  }

  label {
    display: inline-block;
    padding-top: .85em;
  }

  .statement {
    border-top: 1px solid #ccc;
    border-bottom: 1px solid #ccc;
    width: 60%;
    margin: 0 auto 3em auto;
    padding: 3em 0 3em 0;
  }

  textarea {
    font-size: 1.5em;
  }

  /* .building label { width: 22% }
  .building input { width: 76% }

  .for label { width: 6% }
  .for input { width: 92% }

  .help_ label { width: 25% }
  .help_ input { width: 73% }

  .by label { width: 6% }
  .by input { width: 92% }

  .world label { width: 30% }
  .world input { width: 68% } */

  .component {
    display: block;
    width: 80%;
    margin-left: auto;
    margin-right: auto;
  }

  .building label { width: 27% }
  .building input { width: 70% }

  .for label { width: 6% }
  .for input { width: 92% }

  .help_ label { width: 29% }
  .help_ input { width: 69% }

  .by label { width: 5% }
  .by input { width: 93% }

  .world label { width: 38% }
  .world input { width: 60% }

  @media only screen and (min-width: 1000px) {
    .building label { width: 20% }
    .building input { width: 77% }

    .for label { width: 6% }
    .for input { width: 92% }

    .help_ label { width: 10% }
    .help_ input { width: 88% }

    .help_ label { width: 21% }
    .help_ input { width: 77% }

    .by label { width: 5% }
    .by input { width: 93% }

    .world label { width: 27% }
    .world input { width: 71% }
  }

  @media only screen and (min-width: 1400px) {
    label { background-color: #eee; }
    .building label { width: 27% }
    .building input { width: 70% }

    .for label { width: 6% }
    .for input { width: 92% }

    .help_ label { width: 30% }
    .help_ input { width: 68% }

    .help_ label { width: 25% }
    .help_ input { width: 73% }

    .world label { width: 38% }
    .world input { width: 59% }
  }

  @media only screen and (min-width: 1600px) {
    .building label { width: 27% }
    .building input { width: 70% }

    .for label { width: 6% }
    .for input { width: 92% }

    .help_ label { width: 30% }
    .help_ input { width: 68% }

    .help_ label { width: 25% }
    .help_ input { width: 73% }

    .world label { width: 38% }
    .world input { width: 59% }
  }

  @media only screen and (max-width: 600px) {
   .statement {
      padding: 5px;
      width: 90%;
    }

    .component {
      width: 100%;
    }
    .text {
      padding: 0 2em 0 2em;
    }
  }
</style>