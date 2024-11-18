<svelte:head>
  <title>Signup | PocketBalance</title>
</svelte:head>

<form class="my-20">
    <div class="container mx-auto p-4 max-w-sm  border-2 rounded-xl border-slate-900">
        <h2 class="text-4xl my-4 text-center">Signup</h2>

        <div class="my-5">
            <label for="fullname">Full name</label>
            <input type="text" id="fullname" placeholder="John Doe" class="form-input rounded-xl px-4 py-2 border-slate-700 w-full">
        </div>

        <div class="my-5">
            <label for="email">Email</label>
            <input type="email" id="email" placeholder="johndoe@example.com" class="form-input rounded-xl px-4 py-2 border-slate-700 w-full">
        </div>

        <div class="my-5">
            <label for="password">Password</label>
            <input type="password" id="password" placeholder="suPers#cretPa$$W0rd" class="rounded-xl px-4 py-2 border-slate-700 w-full">
        </div>

        <button class="my-2 w-full rounded-xl bg-slate-800 py-3 text-white hover:bg-slate-900 focus:ring focus:ring-slate-500">Signup</button>
    </div>

    <p class="container mx-auto max-w-sm p-0 my-5">
        Already have an account? <a href="/login" class="text-cyan-500">Login</a>
    </p>
</form>