<script>
  import CardTable from "./CardTable.svelte";

  // core components
  let openTab = 1;

  function toggleTabs(tabNumber) {
    openTab = tabNumber;
  }
</script>

<div class="relative flex flex-col min-w-0 rounded mb-6 xl:mb-0 shadow-lg">
  <div class="flex-auto p-4">
    <!-- test -->
    <div class="w-full">
      <ul class="flex mb-0 list-none flex-wrap pt-3 pb-4 flex-row">
        <li class="-mb-px mr-2 last:mr-0 flex-auto text-center">
          <a
            class="text-xs font-bold uppercase px-5 py-3 shadow-lg rounded block leading-normal {openTab === 1 ? 'text-white bg-teal-600' : 'text-teal-600 bg-white'}"
            on:click={() => toggleTabs(1)}>
            Account Data
          </a>
        </li>
        <li class="-mb-px mr-2 last:mr-0 flex-auto text-center">
          <a
            class="text-xs font-bold uppercase px-5 py-3 shadow-lg rounded block leading-normal {openTab === 2 ? 'text-white bg-teal-600' : 'text-teal-600 bg-white'}"
            on:click={() => toggleTabs(2)}>
            Create Account
          </a>
        </li>
        <li class="-mb-px mr-2 last:mr-0 flex-auto text-center">
          <a
            class="text-xs font-bold uppercase px-5 py-3 shadow-lg rounded block leading-normal {openTab === 3 ? 'text-white bg-teal-600' : 'text-teal-600 bg-white'}"
            on:click={() => toggleTabs(3)}>
            Update Account
          </a>
        </li>
      </ul>
      <div
        class="relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded">
        <div class="px-4 py-5 flex-auto">
          <div class="tab-content tab-space">
            <div class={openTab === 1 ? 'block' : 'hidden'}>
              <CardTable />
            </div>
            <div class={openTab === 2 ? 'block' : 'hidden'}>
              <p>
                Completely synergize resource taxing relationships via premier
                niche markets. Professionally cultivate one-to-one customer
                service with robust ideas.
                <br />
                <br />
                Dynamically innovate resource-leveling customer service for
                state of the art customer service.
              </p>
            </div>
            <div class={openTab === 3 ? 'block' : 'hidden'}>
              <p>
                Efficiently unleash cross-media information without cross-media
                value. Quickly maximize timely deliverables for real-time
                schemas.
                <br />
                <br />
                Dramatically maintain clicks-and-mortar solutions without
                functional solutions.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
