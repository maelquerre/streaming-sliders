<template>
  <div class="py-4 md:py-8">
    <header class="flex items-center justify-between px-4 md:px-16">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="h-8 w-8 text-sky-400 md:hidden"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M7 4v16M17 4v16M3 8h4m10 0h4M3 12h18M3 16h4m10 0h4M4 20h16a1 1 0 001-1V5a1 1 0 00-1-1H4a1 1 0 00-1 1v14a1 1 0 001 1z"
        />
      </svg>
      <h1 class="hidden text-5xl font-bold tracking-tight md:block">Sliders</h1>

      <a
        href="https://tailwindcss.com/"
        class="flex items-center ml-4 py-1 px-3 text-xs font-medium text-sky-400 bg-sky-400/10 rounded-full hover:bg-sky-400/20"
      >
        <span>Made with <strong class="font-semibold">Tailwind CSS</strong></span>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          class="ml-.5 h-4 w-4 transform rotate-45">
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M7 11l5-5m0 0l5 5m-5-5v12"
          />
        </svg>
      </a>
    </header>

    <section class="mt-12">
      <Prose class="mb-4">
        <h2>Apple TV+</h2>
        <h3><code>data-grid="A"</code></h3>
      </Prose>
      <AppleShelfGrid
        :movies="popularMovies"
        grid="A"
      />

      <Prose class="mt-6 mb-4">
        <h3><code>data-grid="B"</code></h3>
      </Prose>
      <AppleShelfGrid
        :movies="topRatedMovies"
        grid="B"
      />

      <Prose class="mt-6 mb-4">
        <h3><code>data-grid="C"</code></h3>
      </Prose>
      <AppleShelfGrid
        :movies="upcomingMovies"
        grid="C"
      />

      <Prose class="mt-6 mb-4">
        <h3><code>data-grid="EpicInline"</code></h3>
      </Prose>
      <AppleShelfGrid
        :movies="popularMovies"
        grid="EpicInline"
      />

      <Prose class="mt-6 mb-4">
        <h3><code>data-grid="FullWidth"</code></h3>
      </Prose>
      <AppleShelfGrid
        :movies="popularMovies"
        grid="FullWidth"
      />

      <Prose
        class="mt-6"
        split
      >
        <h3>Sliding</h3>
        <p>
          Apple TV+ uses CSS
          <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Scroll_Snap/Basic_concepts">Scroll Snap</a>
          to control how the children should stick while scrolling.
        </p>

        <h3>Positioning</h3>
        <p>
          The container uses the <code>grid-auto-columns</code> CSS property to determine the number of columns
          to display in a row according to the breakpoints.
        </p>

        <h3>Columns</h3>
        <p>
          There are multiple types of rows, with multiple columns layouts for each breakpoint.
        </p>

        <div class="overflow-auto break-before-column">
          <table class="overflow-scroll">
            <thead>
              <tr>
                <th><code>data-grid</code></th>
                <th>Default</th>
                <th>740px</th>
                <th>1000px</th>
                <th>1320px</th>
                <th>1680px</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>A</td>
                <td class="text-center">298px</td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
              </tr>
              <tr>
                <td>B</td>
                <td class="text-center">270px</td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
              </tr>
              <tr>
                <td>C</td>
                <td class="text-center">200px</td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
              </tr>
              <tr>
                <td>EpicInline</td>
                <td class="text-center">126px</td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
              </tr>
              <tr>
                <td>FullWidth</td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
                <td>
                  <div class="flex items-center space-x-1 h-3">
                    <div class="flex-grow h-full bg-current rounded-sm" />
                  </div>
                </td>
              </tr>
            </tbody>
          </table>
        </div>

        <h3>Naming</h3>
        <table>
          <tbody>
            <tr>
              <td>Container</td>
              <td><code>.shelf-grid</code></td>
            </tr>
            <tr>
              <td>List</td>
              <td><code>.shelf-grid__list</code></td>
            </tr>
            <tr>
              <td>Children</td>
              <td><code>.shelf-grid__list-item</code></td>
            </tr>
          </tbody>
        </table>
      </Prose>
    </section>

    <section class="mt-12">
      <Prose class="mb-4">
        <h2>Disney+</h2>
      </Prose>

      <DisneySlickSlider
        name="Trending"
        :movies="popularMovies"
      />

      <Prose split>
        <h3>Sliding</h3>
        <p>
          The container takes the width of all the children combined. It is computed via JavaScript
          and expands beyond the viewport. The sliding behavior is controlled with JavaScript and is
          only triggerable with the arrow buttons.
        </p>

        <h3>Positioning</h3>
        <p>
          The children are positioned with the <code>float</code> CSS property.
          The gap is controlled with the children padding. This padding also allows for the thumbnails
          to scale when hovering them.
        </p>

        <h3>Columns</h3>
        <p>
          There is only one type of row throughout the whole application.
          The number of columns is computed via JavaScript.
        </p>
        <table>
          <thead>
            <tr>
              <th>Breakpoint prefix</th>
              <th>Minimum width</th>
              <th>Columns count</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>None</td>
              <td>—</td>
              <td>2</td>
            </tr>
            <tr>
              <td><code>lg</code></td>
              <td>1024px</td>
              <td>3</td>
            </tr>
            <tr>
              <td><code>xl</code></td>
              <td>1280px</td>
              <td>4</td>
            </tr>
            <tr>
              <td><code>2xl</code></td>
              <td>1536px</td>
              <td>5</td>
            </tr>
          </tbody>
        </table>

        <h3>Naming</h3>
        <table>
          <thead>
            <tr>
              <th>Element</th>
              <th>Name</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Container</td>
              <td><code>slick-slider</code></td>
            </tr>
            <tr>
              <td>List</td>
              <td><code>slick-list</code></td>
            </tr>
            <tr>
              <td>Children</td>
              <td><code>slick-slide</code></td>
            </tr>
          </tbody>
        </table>
      </Prose>
    </section>

    <section class="mt-12">
      <Prose class="mb-4">
        <h2>Netflix</h2>
      </Prose>

      <Prose split>
        <h3>Columns</h3>
        <p>
          There is only one type of row throughout the whole application.
          The number of columns is computed via JavaScript.
        </p>
        <table>
          <thead>
            <tr>
              <th>Breakpoint prefix</th>
              <th>Minimum width</th>
              <th>Columns count</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>None</td>
              <td>—</td>
              <td>2</td>
            </tr>
            <tr>
              <td><code>sm</code></td>
              <td>500px</td>
              <td>3</td>
            </tr>
            <tr>
              <td><code>lg</code></td>
              <td>800px</td>
              <td>4</td>
            </tr>
            <tr>
              <td><code>xl</code></td>
              <td>1100px</td>
              <td>5</td>
            </tr>
            <tr>
              <td><code>xl-2xl</code></td>
              <td>1400px</td>
              <td>6</td>
            </tr>
          </tbody>
        </table>
      </Prose>
    </section>

    <section class="mt-12">
      <Prose class="mb-4">
        <h2>Arte</h2>
      </Prose>

      <div class="px-4 md:px-16">
        <ArteSlider
          :movies="popularMovies"
        />
      </div>

      <Prose split>
        <h3>Sliding</h3>
        <p>
          Arte benefits from the CSS behavior of combined overflows values. It uses <code>overflow-y: hidden</code> and
          <code>overflow-x: visible</code>, which actually makes the <code>overflow-x</code> compute to
          <code>auto</code>
          <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/overflow-x#values" target="_blank">as described in the MDN docs</a>:
        </p>
        <blockquote>
          <p>
            If <code>overflow-y</code> is <code>hidden</code>, <code>scroll</code> or <code>auto</code> and this
            property is <code>visible</code>, it will implicitly compute to <code>auto</code>.
          </p>
        </blockquote>

        <h3>Naming</h3>
        <table>
          <thead>
            <tr>
              <th>Element</th>
              <th>Name</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Container</td>
              <td><code>Slider</code></td>
            </tr>
            <tr>
              <td>List</td>
              <td><code>slick-list</code></td>
            </tr>
            <tr>
              <td>Children</td>
              <td><code>Teaser</code></td>
            </tr>
          </tbody>
        </table>
      </Prose>
    </section>
  </div>
</template>

<script>
import AppleShelfGrid from '../components/apple/ShelfGrid'
import ArteSlider from '../components/arte/Slider'
import DisneySlickSlider from '../components/disney/SlickSlider'
import Prose from '../components/core/Prose'

export default {
  components: {
    AppleShelfGrid,
    ArteSlider,
    DisneySlickSlider,
    Prose,
  },

  async asyncData({ $api, store }) {
    const configuration = await $api.$get('configuration')
    store.commit('tmdb/setConfiguration', configuration)

    const popularMoviesResponse = await $api.$get('movie/popular')
    const popularMovies = popularMoviesResponse.results

    const topRatedMoviesResponse = await $api.$get('movie/top_rated')
    const topRatedMovies = topRatedMoviesResponse.results

    const upcomingMoviesResponse = await $api.$get('movie/upcoming')
    const upcomingMovies = upcomingMoviesResponse.results

    return {
      popularMovies,
      topRatedMovies,
      upcomingMovies
    }
  }
}
</script>
