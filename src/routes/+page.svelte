<script>
    import favicon from "$lib/assets/favicon.png"
    import sveltekit from "$lib/assets/sveltekit.png"
    import tailwindcss from "$lib/assets/tailwindcss.png";
    import Vite from "$lib/assets/Vite.png";
</script>
<header class="bg-black w-full h-15 border-b border-b-gray-400 text-white flex items-center">
    <div class="flex items-center pl-10">
        <img src={favicon} class="h-10 w-10" alt="">
        <a class="font-mono text-3xl pl-8" href="/">Evil Chat</a>
    </div>
</header>

<div class="flex flex-col justify-center items-center text-white bg-linear-to-r from-blue-700 to-purple-800 h-100">
    <h1 class="text-3xl">Welcome to the Evil Chat.</h1>
    <p class="pt-5">
        A full-stack real time chat application project I'm working on to 
        improve my web development skills.
    </p>
    <button type="button" class="text-white bg-green-600 mt-6 h-10 w-30 border border-gray-500 cursor-pointer hover:bg-green-700 hover:scale-110 transition duration-300 ease-in-out">Get Started!</button>
</div>

<div class="text-white mt-10 mb flex flex-col items-center">
    <h1 class="text-3xl text-center">Tech stack</h1>
    <div class="grid grid-cols-3 gap-10 pt-6">
        <div class="border border-grey h-70 w-65 flex flex-col items-center">
            <img src={sveltekit} alt="" class="w-50 h-10 mt-10">
            <p class="pt-15 text-center pl-1 pr-1">
                SveltKit provides a very intuitive and simple way to handle things such as state and frontend-backend connection.
            </p>
        </div>
        <div class="border border-grey h-70 w-65 flex flex-col items-center">
            <img src={tailwindcss} alt="" class="w-40 h-20 mt-10">
            <p class="pt-5 text-center pl-1 pr-1">Mate, I am <b>NOT</b> going to deal with CSS, okay? Tailwind saves me the hassle.</p>
        </div>
        <div class="border border-grey h-70 w-65 flex flex-col items-center">
            <img src={Vite} alt="" class="w-30 h-25 mt-6">
            <p class="pt-5 text-center pl-1 pr-1">One of my favourite humanity inventions. Saves the hassle of having to deal wiith manual project setup.</p>
        </div>
    </div>
</div>

<div class="text-white w-full h-15 border-t mt-10 flex items-center justify-center">
    <p>© <a href="https://ali-moumen.tech">Ali moumen</a> 2026. All rights reserved.</p>
</div>