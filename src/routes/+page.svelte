<script>
    import "../app.css";
    import Navbar from "../components/Navbar.svelte";
    import {Button, Tooltip} from 'flowbite-svelte';

    let tooltip = "stephen#1234";
    function tooltipClick() {
        tooltip = "discord copied";
        navigator.clipboard.writeText("stephen#1234")
    }
</script>

<div class="bg-[#19191c] h-full min-h-[100vh] max-h-[100vh]">
    <Navbar/>
    <div class="bg-[#19191c] flex-col flex h-[93vh] justify-between max-sm:pt-5 md:pt-20 pb-8 max-sm:gap-7">
        <div class="flex-col self-center lg:w-[40vw] md:w-[50vw] sm:w-[80vw] mx-5 gap-4 flex">
            <img src="/img/stephen.png" class="h-40 w-40 rounded-full bg-[#16161A] mb-2">
            <p class="font-bold text-white text-[36px]">Hey, I'm Stephen</p>
            <p class="text-[#A9A9BF] text-[20px] pb-2">Leading my company to make cool things.</p>
            <div class="flex gap-2">
                <img src="/img/cloud.png" class="h-5 self-center">
                <p class="text-[#A9A9BF] text-[20px]">Soon working at <b>Microsoft</b> as a <b>Cloud Architect</b>.</p>
            </div>
            <div class="flex gap-2">
                <img src="/img/hat.png" class="self-center h-5">
                <p class="text-[#A9A9BF] text-[20px]">Graduating with degree in <b>International Business Management</b>.</p>
            </div>
        </div>
        <div class="flex-col self-center lg:w-[40vw] md:w-[50vw] sm:w-[80vw] mx-5 gap-4 flex">
            <p class="font-bold text-white text-[36px]">Connect with me</p>
            <p class="text-[#A9A9BF] text-[20px]">For business enquiries, reach me at <a class="hover:brightness-125 underline decoration-dotted transition duration-110 ease-in-out" href="mailto:hello@stephen.gg">hello@stephen.gg</a>.</p>
            <div class="flex gap-7">
                <Tooltip class="bg-[#161619]" arrow={true} placement="bottom" triggeredBy="#hover">{tooltip}</Tooltip>
                <Button on:mouseleave={tooltip="stephen#1234"} on:click={tooltipClick} id="hover" class="cursor-pointer hover:brightness-125 transition duration-110 ease-in-out"><img id="click" src="/img/discord.png" class="h-14 hover:brightness-125"></Button>
                <a href="https://github.com/sttephen/" target="_blank" class="hover:brightness-125 transition duration-110 ease-in-out">
                    <img src="/img/github.png" class="h-14">
                </a>
            </div>
        </div>
        <div class="text-[13px] text-[#A9A9BF] self-center max-sm:pb-5">© Virtual Ventures Ltd. All Rights Reserved.</div>
    </div>
</div>

