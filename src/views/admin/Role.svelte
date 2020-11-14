<script>
    import RoleCreate from "../../components/Form/Admin/RoleCreate.svelte";
    import RoleUpdate from "../../components/Form/Admin/RoleUpdate.svelte";
    import RoleTable from "../../components/Table/Admin/RoleTable.svelte";

    let openTab = 1;

    function toggleTabs(tabNumber) {
        openTab = tabNumber;
    }
</script>

<div class="flex flex-wrap mt-4">
    <div class="w-full mb-12 px-4">
        <div
            class="relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded">
            <ul class="flex mb-0 list-none flex-wrap pt-3 pb-4 flex-row">
                <li class="-mb-px mr-2 last:mr-0 flex-auto text-center">
                    <a
                        href="#"
                        class="text-xs font-bold uppercase px-5 py-3 shadow-lg rounded block leading-normal {openTab === 1 ? 'text-white bg-teal-600' : 'text-teal-600 bg-white'}"
                        on:click={() => toggleTabs(1)}>
                        List
                    </a>
                </li>
                <li class="-mb-px mr-2 last:mr-0 flex-auto text-center">
                    <a
                        href="#"
                        class="text-xs font-bold uppercase px-5 py-3 shadow-lg rounded block leading-normal {openTab === 2 ? 'text-white bg-teal-600' : 'text-teal-600 bg-white'}"
                        on:click={() => toggleTabs(2)}>
                        Create
                    </a>
                </li>
                <li class="-mb-px mr-2 last:mr-0 flex-auto text-center">
                    <a
                        href="#"
                        class="text-xs font-bold uppercase px-5 py-3 shadow-lg rounded block leading-normal {openTab === 3 ? 'text-white bg-teal-600' : 'text-teal-600 bg-white'}"
                        on:click={() => toggleTabs(3)}>
                        Update
                    </a>
                </li>
            </ul>
            <div
                class="relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded">
                <div class="px-4 py-5 flex-auto">
                    <div class="tab-content tab-space">
                        <div class={openTab === 1 ? 'block' : 'hidden'}>
                            <RoleTable />
                        </div>
                        <div class={openTab === 2 ? 'block' : 'hidden'}>
                            <RoleCreate />
                        </div>
                        <div class={openTab === 3 ? 'block' : 'hidden'}>
                            <RoleUpdate />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
