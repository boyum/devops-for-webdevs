<script lang="ts">
  import { getLevels } from "../../utils/level.utils";
  import { Link } from "svelte-navigator";

  
  const levels = getLevels();
</script>

<h1>Levels</h1>
<ul class="levels">
  {#each levels as level, index}
  <li class="level">
    <Link to="/levels/{level.id}">
      {index+1}
    </Link>
  </li>
  {/each}
</ul>

<style>
  .levels {
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .level {
    height: 0;
    padding-top: 100%;
    position: relative;
  }

  .level a {
    inset: 0;
    position: absolute;
  }
</style>