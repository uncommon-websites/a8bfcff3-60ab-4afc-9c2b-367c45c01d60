<script>
    import Icon from './Icon.svelte';
    
    // Icons
    const Sparkles = `<path d="m12 3-1.912 5.813a2 2 0 0 1-1.275 1.275L3 12l5.813 1.912a2 2 0 0 1 1.275 1.275L12 21l1.912-5.813a2 2 0 0 1 1.275-1.275L21 12l-5.813-1.912a2 2 0 0 1-1.275-1.275L12 3Z"/>`;
    const Bell = `<path d="M6 8a6 6 0 0 1 12 0c0 7 3 9 3 9H3s3-2 3-9"/><path d="M10.3 21a1.94 1.94 0 0 0 3.4 0"/>`;
    const Home = `<path d="m3 9 9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/>`;
    const MapPin = `<path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"/><circle cx="12" cy="10" r="3"/>`;
</script>

<section class="relative min-h-[90vh] flex flex-col items-center pt-32 pb-20 px-4 overflow-hidden">
    <!-- Background Gradient Mesh -->
    <div class="mesh-gradient">
        <!-- Teal/Cyan top left -->
        <div class="mesh-blob w-[600px] h-[600px] -top-[200px] -left-[100px] opacity-30 blur-[100px]" style="background: oklch(0.696 0.17 162.48);"></div>
        <!-- Blue top center -->
        <div class="mesh-blob w-[500px] h-[500px] top-[0px] left-[30%] opacity-20 blur-[120px]" style="background: oklch(0.596 0.145 163.225);"></div>
        <!-- Teal top right -->
        <div class="mesh-blob w-[600px] h-[600px] -top-[100px] -right-[100px] opacity-25 blur-[100px]" style="background: oklch(0.765 0.177 163.223);"></div>
        <!-- Bottom right sweep -->
        <div class="mesh-blob w-[800px] h-[800px] top-[40%] -right-[200px] opacity-15 blur-[150px]" style="background: oklch(0.508 0.118 165.612);"></div>
    </div>

    <!-- Content -->
    <div class="relative z-10 text-center max-w-3xl mx-auto mb-16">
        <h1 class="text-5xl md:text-7xl font-bold tracking-tight mb-6 leading-[1.1]">
            <span class="text-white">Never miss a</span><br/>
            <span class="text-white/40">rent-stabilized apartment</span>
        </h1>
        <p class="text-lg md:text-xl text-gray-400 mb-10 max-w-2xl mx-auto leading-relaxed">
            RentReboot delivers <span class="text-white font-medium">instant alerts</span> for rent-stabilized NYC apartments. Beat StreetEasy by minutes, not hours.
        </p>

        <!-- Email Form -->
        <div class="flex flex-col items-center gap-3">
            <div class="flex w-full max-w-md bg-[#111] border border-white/10 rounded-xl p-1.5 pl-4 shadow-2xl">
                <input 
                    type="email" 
                    placeholder="Enter your email" 
                    class="bg-transparent border-none outline-none text-white flex-1 placeholder-gray-500 text-sm"
                />
                <button class="bg-[var(--color-primary)] hover:bg-[var(--color-primary-hover)] text-white px-5 py-2.5 rounded-lg text-sm font-medium transition-colors cursor-pointer">
                    Get early access
                </button>
            </div>
            <p class="text-xs text-gray-600">Join 500+ NYC renters finding their perfect apartment.</p>
        </div>
    </div>

    <!-- Mockup Card -->
    <div class="relative z-10 w-full max-w-md mx-auto perspective-1000">
        <!-- Handwritten Arrow -->
        <div class="absolute -right-[160px] top-[40px] hidden md:block w-40">
            <p class="font-hand text-xl text-white transform -rotate-6 mb-2">Get alerts before anyone else</p>
            <svg width="80" height="60" viewBox="0 0 100 80" fill="none" class="text-white ml-2 transform rotate-12">
                <path d="M80 5 C 60 25, 40 15, 10 55" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round"/>
                <path d="M10 55 L 20 50 M 10 55 L 18 63" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round"/>
            </svg>
        </div>

        <div class="glass-card rounded-2xl p-6 shadow-2xl border border-white/10 bg-[#111]/80 backdrop-blur-xl">
            <!-- Header -->
            <div class="flex items-center gap-3 mb-6">
                <div class="text-[var(--color-primary)] animate-pulse">
                    <Icon size={24} color="currentColor">{@html Bell}</Icon>
                </div>
                <div>
                    <h3 class="text-lg font-semibold text-white">New listings found</h3>
                    <p class="text-xs text-gray-500">12 rent-stabilized apartments today</p>
                </div>
            </div>

            <!-- List -->
            <div class="space-y-3">
                <!-- Item 1 -->
                <div class="bg-white/5 rounded-xl p-3 flex items-center justify-between border border-white/5 hover:bg-white/10 transition-colors">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-[var(--color-primary)]/20 flex items-center justify-center border border-[var(--color-primary)]/30">
                            <div class="w-5 h-5 text-[var(--color-primary)]">
                                <Icon size={20} color="currentColor">{@html Home}</Icon>
                            </div>
                        </div>
                        <div>
                            <h4 class="text-sm font-medium text-white">2BR in Astoria</h4>
                            <p class="text-xs text-gray-500">$1,850/mo • Just posted</p>
                        </div>
                    </div>
                    <div class="bg-[var(--color-primary)]/20 text-[var(--color-primary)] text-[10px] font-bold px-2 py-1 rounded-full">
                        NEW
                    </div>
                </div>

                <!-- Item 2 -->
                <div class="bg-white/5 rounded-xl p-3 flex items-center justify-between border border-white/5 hover:bg-white/10 transition-colors">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-[var(--color-primary)]/20 flex items-center justify-center border border-[var(--color-primary)]/30">
                            <div class="w-5 h-5 text-[var(--color-primary)]">
                                <Icon size={20} color="currentColor">{@html Home}</Icon>
                            </div>
                        </div>
                        <div>
                            <h4 class="text-sm font-medium text-white">1BR in Williamsburg</h4>
                            <p class="text-xs text-gray-500">$2,100/mo • 3 mins ago</p>
                        </div>
                    </div>
                    <div class="bg-[var(--color-primary)]/20 text-[var(--color-primary)] text-[10px] font-bold px-2 py-1 rounded-full">
                        NEW
                    </div>
                </div>

                <!-- Item 3 -->
                <div class="bg-white/5 rounded-xl p-3 flex items-center justify-between border border-white/5 hover:bg-white/10 transition-colors">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-[var(--color-primary)]/20 flex items-center justify-center border border-[var(--color-primary)]/30">
                            <div class="w-5 h-5 text-[var(--color-primary)]">
                                <Icon size={20} color="currentColor">{@html Home}</Icon>
                            </div>
                        </div>
                        <div>
                            <h4 class="text-sm font-medium text-white">Studio in East Village</h4>
                            <p class="text-xs text-gray-500">$1,650/mo • 8 mins ago</p>
                        </div>
                    </div>
                    <div class="bg-[var(--color-primary)]/20 text-[var(--color-primary)] text-[10px] font-bold px-2 py-1 rounded-full">
                        NEW
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
