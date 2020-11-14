<script>
    // can be one of light or dark
    export let color = "light";
</script>

<div
    class="relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded {color === 'light' ? 'bg-white' : 'bg-red-800 text-white'}">
    <div class="rounded-t mb-0 px-4 py-3 border-0">
        <div class="flex flex-wrap items-center">
            <div class="relative w-full px-4 max-w-full flex-grow flex-1">
                <h3
                    class="font-semibold text-lg {color === 'light' ? 'text-gray-800' : 'text-white'}">
                    Role Management
                </h3>
            </div>
        </div>
    </div>
    <div class="block w-full overflow-x-auto">
        <!-- Projects table -->
        <table class="items-center w-full bg-transparent border-collapse">
            <thead>
                <tr>
                    <th
                        class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-no-wrap font-semibold text-left {color === 'light' ? 'bg-gray-100 text-gray-600 border-gray-200' : 'bg-red-700 text-red-200 border-red-600'}">
                        Project
                    </th>
                    <th
                        class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-no-wrap font-semibold text-left {color === 'light' ? 'bg-gray-100 text-gray-600 border-gray-200' : 'bg-red-700 text-red-200 border-red-600'}">
                        Status
                    </th>
                    <th
                        class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-no-wrap font-semibold text-left {color === 'light' ? 'bg-gray-100 text-gray-600 border-gray-200' : 'bg-red-700 text-red-200 border-red-600'}">
                        Action
                    </th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td
                        class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-no-wrap p-4">
                        1
                    </td>
                    <td
                        class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-no-wrap p-4">
                        <i class="fas fa-circle text-green-500 mr-2" />
                        completed
                    </td>
                    <td
                        class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-no-wrap p-4">
                        <i class="fas fa-trash text-red-500 mr-2" />
                        <i class="fas fa-edit text-yellow-500 mr-2" />
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
</div>
