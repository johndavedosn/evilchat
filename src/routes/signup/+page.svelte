<script>
    import favicon from "$lib/assets/favicon.png"
    let email = ""
    let password = ""
    let emailError = ""
    let passwordError = ""
    $: emailError = email && !email.includes("@") ? "Invalid email address" : ""
    function ensurePasswordStrength(){
        const lengthCheck = password.length >= 8 
        const oneNumberRegex = /\d+/
        const oneCapitalRegex = /[A-Z]+/
        const specialCharsRegex = /[^a-zA-Z0-9]/;
        const numberCheck = oneNumberRegex.test(password)
        const capitalCheck = oneCapitalRegex.test(password)
        const specialCharsCheck = specialCharsRegex.test(password)
        return lengthCheck && numberCheck && capitalCheck && specialCharsCheck
    }
    $: passwordError = password && !ensurePasswordStrength() ? "Password is too weak" : ""
</script>
<header class="bg-black w-full h-15 border-b border-b-gray-400 text-white flex items-center">
    <div class="flex items-center pl-10">
        <img src={favicon} class="h-10 w-10" alt="">
        <a class="font-mono text-3xl pl-8" href="/">Evil Chat</a>
    </div>
</header>

<article class=" text-white flex flex-col justify-center items-center min-h-screen">
    <div class="bg-black h-100 p-8 m-8 w-100 border flex flex-col border-gray-700 shadow-[-17px_-5px_100px_50px_rgba(149,157,165,0.2)]">
        <h1 class="text-3xl text-center pb-8">Sign up</h1>
        <label for="email">Email *</label>
        <input type="text" class="bg-gray-900" placeholder="Email Address..." bind:value={email}>
        <h6 class="mb-6 text-red-800">{emailError}</h6>
        <label for="password">Password *</label>
        <input type="password" class="bg-gray-900" placeholder="Password..." bind:value={password}>
        <h6 class="mb-10 text-red-800">{passwordError}</h6>
        <button class="cursor-pointer border border-gray-700 h-10 transition duration-300 ease-in-out hover:bg-gray-800 hover:scale-110">Sign up</button>
    </div>
    <p class="text-center">Already have an account? <a href="/signin" class="transition duration-300 ease-in-out hover:text-gray-400">Sign in!</a></p>
</article>^