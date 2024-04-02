<!-- <script>
    import { writable } from 'svelte/store';
    import simpleGit from 'simple-git';
    const git = simpleGit();

    let showDialog = writable(false); // Controls the visibility of the dialog

    async function gitAdd() {
        try {
            await git.add('./*');
            alert('Files added successfully.');
        } catch (error) {
            console.error('Failed to add files:', error);
            alert('Failed to add files. Check the console for more details.');
        }
    }

    async function gitCommit() {
        try {
            await git.commit("Your commit message");
            alert('Commit successful.');
        } catch (error) {
            console.error('Failed to commit:', error);
            alert('Failed to commit. Check the console for more details.');
        }
    }

    async function gitPush() {
        try {
            await git.push();
            alert('Push successful.');
        } catch (error) {
            console.error('Failed to push:', error);
            alert('Failed to push. Check the console for more details.');
        }
    }

    async function gitPull() {
        try {
            await git.pull();
            alert('Pull successful.');
        } catch (error) {
            console.error('Failed to pull:', error);
            alert('Failed to pull. Check the console for more details.');
        }
    }
    function toggleDialog() {
        showDialog.update(v => !v);
    }
     // Function to close the dialog if the overlay is clicked
     function closeDialogOnClickOutside(event) {
        if (event.target.classList.contains('dialog-overlay')) {
            showDialog.set(false);
        }
    }
</script>

<button class="bg-gray-300 text-black py-2 px-4 rounded hover:bg-gray-400 transition-colors" on:click={toggleDialog}> Git</button>

{#if $showDialog}
    <div class="fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center dialog-overlay" on:click={closeDialogOnClickOutside}>
        <div class="bg-white p-4 rounded-lg shadow-lg w-64 h-64 flex flex-col justify-center items-center" on:click|stopPropagation>
            <h2 class="text-xl font-bold mb-4">Git Operations</h2>
            <div class="flex flex-col space-y-2">
                <button class="bg-blue-500 text-white font-semibold py-1 px-3 rounded-full hover:bg-blue-700 transition-colors">Git Add</button>
                <button class="bg-green-500 text-white font-semibold py-1 px-3 rounded-full hover:bg-green-700 transition-colors">Git Commit</button>
                <button class="bg-yellow-500 text-white font-semibold py-1 px-3 rounded-full hover:bg-yellow-700 transition-colors">Git Push</button>
                <button class="bg-red-500 text-white font-semibold py-1 px-3 rounded-full hover:bg-red-700 transition-colors">Git Pull</button>
            </div>
            <button class="mt-4 bg-gray-300 text-black py-2 px-4 rounded hover:bg-gray-400 transition-colors" on:click={toggleDialog}>Close</button>
        </div>
    </div>
{/if}

{#if $showDialog}
    <div class="fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center dialog-overlay" on:click={closeDialogOnClickOutside}>
        <div class="bg-white p-4 rounded-lg shadow-lg w-64 h-64 flex flex-col justify-center items-center" on:click|stopPropagation>
            <h2 class="text-xl font-bold mb-4">Git Operations</h2>
            <div class="flex flex-col space-y-2">
               
                <button class="bg-blue-500 text-white font-semibold py-1 px-3 rounded-full hover:bg-blue-700 transition-colors">Git Add</button>
                <button class="bg-green-500 text-white font-semibold py-1 px-3 rounded-full hover:bg-green-700 transition-colors">Git Commit</button>
                <button class="bg-yellow-500 text-white font-semibold py-1 px-3 rounded-full hover:bg-yellow-700 transition-colors">Git Push</button>
                <button class="bg-red-500 text-white font-semibold py-1 px-3 rounded-full hover:bg-red-700 transition-colors">Git Pull</button>
            
            </div>
            <button class="mt-4 bg-gray-300 text-black py-2 px-4 rounded hover:bg-gray-400 transition-colors" on:click={toggleDialog}>Close</button>
        </div>
    </div>
{/if}
 -->



 <script>
    import simpleGit from 'simple-git';
    const git = simpleGit();

    async function gitAdd() {
        try {
            await git.add('./*');
            alert('Files added successfully.');
        } catch (error) {
            console.error('Failed to add files:', error);
            alert('Failed to add files. Check the console for more details.');
        }
    }

    async function gitCommit() {
        try {
            await git.commit("Your commit message");
            alert('Commit successful.');
        } catch (error) {
            console.error('Failed to commit:', error);
            alert('Failed to commit. Check the console for more details.');
        }
    }

    async function gitPush() {
        try {
            await git.push();
            alert('Push successful.');
        } catch (error) {
            console.error('Failed to push:', error);
            alert('Failed to push. Check the console for more details.');
        }
    }

    async function gitPull() {
        try {
            await git.pull();
            alert('Pull successful.');
        } catch (error) {
            console.error('Failed to pull:', error);
            alert('Failed to pull. Check the console for more details.');
        }
    }
</script>

<main class="flex flex-col space-y-2 mt-4">
    <button on:click={gitAdd} class="bg-blue-500 text-white font-semibold py-1 px-3 rounded-full hover:bg-blue-700 transition-colors">Git Add</button>
    <button on:click={gitCommit} class="bg-green-500 text-white font-semibold py-1 px-3 rounded-full hover:bg-green-700 transition-colors">Git Commit</button>
    <button on:click={gitPush} class="bg-yellow-500 text-white font-semibold py-1 px-3 rounded-full hover:bg-yellow-700 transition-colors">Git Push</button>
    <button on:click={gitPull} class="bg-red-500 text-white font-semibold py-1 px-3 rounded-full hover:bg-red-700 transition-colors">Git Pull</button>
</main>
