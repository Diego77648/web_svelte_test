<script>
  import ProjectCard from '@components/ProjectCard.svelte'
  import CircuitBackground from '@components/CircuitBackground.svelte'
</script>

<section id="projects">
  <CircuitBackground />
  <div class="container">
    <article class="message">
      <h2 class="subtitle white">Proyectos de la comunidad</h2>
      <p class="text white">
TEXTO5
      </p>
    </article>
    <article class="grid-projects">
      <ProjectCard
        icon="web"
        title=""
        label=""
        link="eb"
        desc="WEB OFICIAL" />
      <ProjectCard
        icon="api"
        title=""
        label=""
        link=""
        desc="API" />
      <ProjectCard
        icon="bot"
        title=""
        label=""
        link=""
        desc="BOT" />
      <ProjectCard
        icon="database"
        title=""
        label=""
        link=""
        desc="DB." />
    </article>
  </div>
</section>

<style lang="scss">
  @import 'src/styles/utils';

  section {
    padding-top: $size-7xl;
    padding-bottom: $size-7xl;
    background: $color-secondary-light;

    .container {
      display: grid;
      position: relative;
      gap: $size-4xl;
      grid-template-rows: repeat(2, fit-content(100%));
      z-index: $z-10;

      .message {
        display: grid;
        gap: $size-base;
        max-width: 696px;
        justify-self: center;
      }

      .grid-projects {
        display: grid;
        gap: $size-3xl;
        justify-content: center;
        grid-template-rows: repeat(4, fit-content(100%));
      }
    }
  }

  @include media(lg) {
    section {
      padding-top: 9.75rem;
      padding-bottom: 9.75rem;

      .container {
        .message {
          h2,
          p {
            text-align: center;
          }
        }

        .grid-projects {
          grid-template-rows: repeat(2, fit-content(100%));
          grid-template-columns: repeat(2, fit-content(100%));
        }
      }
    }
  }
</style>
