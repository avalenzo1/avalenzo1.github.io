<template>
  <header class="gutter">
    <h1>Projects</h1>
  </header>

  <div class="gutter">
    <div v-for="era in milestones" class="py-4">
      <h2 class="mb-2">{{ era.name }}</h2>

      <ul class="grid gap-4 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
        <li v-for="project in era.projects">
          <article class="card">
            <header class="card-header">
              <img :src="`images/thumbnails/${project.imgSrc}`"
                class="object-cover aspect-square rounded-lg" />
            </header>
            <main class="card-body">
              <h3>{{ project.name }}</h3>
              <p>{{ project.desc }}</p>
            </main>
            <footer class="card-footer">
              <NuxtLink :to="project.to.site" class="btn btn-primary btn-prominent btn-md flex-1" target="_blank">View Site
                <Icon name="mdi:open-in-new" />
              </NuxtLink>
              <NuxtLink :to="project.to.repo" class="btn btn-md" target="_blank">Repo
                <Icon name="mdi:github" />
              </NuxtLink>
            </footer>
          </article>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      milestones: [
        {
          name: "Fellowship 2022-23",
          projects: [
            {
              name: "Playlist Project",
              desc: "A project that does menial things.",
              imgSrc: "flw-playlist.png",
              to: {
                repo: "https://avalenzo1.github.io/FLW-Playlist",
                site: "https://flw-playlist.avalenzo1.repl.co/",
              },
            },
            {
              name: "What CN Character Are You?",
              desc: "Cartoon Network",
              imgSrc: "flw-buzzfeed.png",
              to: {
                repo: "https://github.com/avalenzo1/flw-buzzfeed-character-quiz",
                site: "https://flw-01p-buzzfeed-character-quiz-starter-code-light.avalenzo1.repl.co/",
              },
            }
          ]
        },
        {
          name: "School Projects 2020-23",
          projects: [
            {
              name: "Commission: Javascript Helper",
              desc: "Website that helps students use canvas",
              imgSrc: "javascript-helper.png",
              to: {
                repo: "https://www.github.com/avalenzo1/Javascript-Adapter-Fancification/",
                site: "https://avalenzo1.github.io/Javascript-Adapter-Fancification/help.html",
                about: "/projects/javascript-helper",
              },
            },
            {
              name: "Handmaid's Tale Project",
              desc: "AP Literature Multi-Media Project",
              imgSrc: "handmaids-tale.png",
              to: {
                repo: "https://www.github.com/avalenzo1/Handmaids-Tale-AP-Literature/",
                site: "https://avalenzo1.github.io/Handmaids-Tale-AP-Literature",
              },
            },
          ]
        },
        {
          name: "Personal Projects 2017-23",
          projects: [
            {
              name: "Take Turns",
              desc: "A project that does menial things.",
              imgSrc: "take-turns.png",
              to: {
                repo: "https://github.com/avalenzo1/take-turns",
                site: "https://take-turns.glitch.me/",
              },
            },
            {
              name: "Blobius.IO",
              desc: "A project that does menial things.",
              imgSrc: "blobius-io.png",
              to: {
                repo: "https://github.com/avalenzo1/blobius-io",
                site: "https://blobius-io.glitch.me/",
              },
            },
          ]
        },
        {
          name: "Code Nation 2021-22",
          projects: [
            {
              name: "Codename Twitify",
              desc: "A project that does menial things.",
              imgSrc: "codename-twitify.png",
              to: {
                repo: "https://www.github.com/avalenzo1/Codename-Twitify/",
                site: "https://avalenzo1.github.io/Codename-Twitify/",
              },
            },
            {
              name: "ARM-aggedon",
              desc: "A project that does menial things.",
              imgSrc: "ARMageddon.png",
              to: {
                repo: "https://www.github.com/avalenzo1/ARMageddon/",
                site: "https://avalenzo1.github.io/ARMageddon/",
              },
            },
          ]
        },

      ]
    }
  }
}
</script>