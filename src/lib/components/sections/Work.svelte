<script>
  import Drop from "../icons/Drop.svelte";
  import Factory from "../icons/Factory.svelte";
  import Gamepad from "../icons/Gamepad.svelte";
  import Leaf from "../icons/Leaf.svelte";

  const getMonthsFromDate = (dateFrom) => {
    let now = new Date();
    let months =
      now.getMonth() -
      dateFrom.getMonth() +
      12 * (now.getFullYear() - dateFrom.getFullYear());

    return months > 12
      ? (months / 12).toFixed(1) + " years"
      : months + " Months";
  };
</script>

<div
  id="work"
  aria-label="Work history"
  class="flex justify-center text-left flex-col container"
>
  <div class="text-center">
    <h1 class="mb-8 text-4xl">WORK HISTORY</h1>
  </div>

  <div class="grid grid-flow-row grid-cols-1 sm:grid-cols-2 gap-6">
    <div class="px-8 py-10 bg-neutral-900 text-neutral-50 rounded-lg">
      <div class="flex mt-4">
        <span class="mr-2"><Leaf /></span>
        <div>
          <h2>Fullstack developer at Sogeti</h2>
          <p class="text-neutral-400">
            {getMonthsFromDate(new Date("02/01/2022"))}
          </p>
        </div>
      </div>

      <div class="mt-8">
        <div class="flex">
          <span class="mr-2">•</span>
          <p>
            Maintenance and development of new features on websites built with
            asp.net and optimizely, both frontend and backend.
          </p>
        </div>
        <div class="flex">
          <span class="mr-2">•</span>
          <p>Manage releases and set up pipelines in azure.</p>
        </div>
        <div class="flex">
          <span class="mr-2">•</span>
          <p>Updating websites to follow wcag guidlines.</p>
        </div>
        <p class="mt-8 text-neutral-400">
          # Javascript, C#, HTML, CSS, .Net MVC, React, SQL Server, Azure
          DevOps, Optimizely
        </p>
      </div>
    </div>

    <div class="px-8 py-10 bg-neutral-900 text-neutral-50 rounded-lg">
      <div class="flex mt-4">
        <span class="mr-2"><Drop /></span>
        <div>
          <h2>Fullstack developer at Bonigi</h2>
          <p class="text-neutral-400">1.5 years</p>
        </div>
      </div>
      <div class="mt-8">
        <div class="flex">
          <span class="mr-2">•</span>
          <p>
            Maintenance and development of Bonigis main website in asp.net
            webforms. Included both frontend and backend development.
          </p>
        </div>
        <div class="flex">
          <span class="mr-2">•</span>
          <p>
            Implementing jquery querybuilder for customers to make easy queries
            to the database.
          </p>
        </div>
        <div class="flex">
          <span class="mr-2">•</span>
          <p>Writing procedures and processing data in the database.</p>
        </div>
        <div class="flex">
          <span class="mr-2">•</span>
          <p>
            Backend and database implementation of a customer project in vue.js
            and strapi.
          </p>
        </div>
        <p class="mt-8 text-neutral-400">
          # SQL, C#, Javascript, JQuery, HTML, CSS, .Net Webforms, Vue.Js, SQL
          Server, Azure DevOps, Azure functions, Strapi
        </p>
      </div>
    </div>

    <div class="px-8 py-10 bg-neutral-900 text-neutral-50 rounded-lg">
      <div class="flex mt-4">
        <span class="mr-2"> <Gamepad /></span>
        <div>
          <h2>Web developer at ATH Games</h2>
          <p class="text-neutral-400">1 month</p>
        </div>
      </div>
      <div class="mt-8">
        <div class="flex">
          <span class="mr-2">•</span>
          <p>
            Built their website with Vue.Js and deployed it to google cloud.
          </p>
        </div>
        <p class="mt-8 text-neutral-400">
          # Javascript, Figma, Vue.Js, Google cloud
        </p>
      </div>
    </div>

    <div class="px-8 py-10 bg-neutral-900 text-neutral-50 rounded-lg">
      <div class="flex mt-4">
        <span class="mr-2"><Factory /></span>
        <div>
          <h2>Software developer at Husqvarna</h2>
          <p class="text-neutral-400">6 months</p>
        </div>
      </div>

      <div class="mt-8">
        <div class="flex">
          <span class="mr-2">•</span>
          <p>
            Maintenance and development of Husqvarnas software for robotic
            lawnmowers.
          </p>
        </div>
        <p class="mt-8 text-neutral-400">
          # Javascript, C#, JQuery, HTML, CSS, WPF, Azure DevOps
        </p>
      </div>
    </div>
  </div>
</div>
