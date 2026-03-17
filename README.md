<!-- Modern Dashboard -->
<!DOCTYPE html>

<html class="dark" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>HVAC PRO - Industrial Order System</title>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;600;700&amp;family=IBM+Plex+Mono:wght@400;500;600&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "primary": "#f5a623", // Amber accent
                        "secondary": "#2ec4e0", // Cyan accent
                        "industrial-black": "#070d16",
                        "industrial-dark": "#0f172a",
                        "industrial-border": "#1e293b",
                    },
                    fontFamily: {
                        "sans": ["Barlow Condensed", "sans-serif"],
                        "mono": ["IBM Plex Mono", "monospace"]
                    },
                },
            },
        }
    </script>
<style>
        body {
            font-family: 'Barlow Condensed', sans-serif;
            background-color: #070d16;
            -webkit-tap-highlight-color: transparent;
        }
        .mono-text { font-family: 'IBM Plex Mono', monospace; }
        .industrial-grid {
            background-image: radial-gradient(#1e293b 0.5px, transparent 0.5px);
            background-size: 24px 24px;
        }
        .clip-slant {
            clip-path: polygon(0 0, 100% 0, 95% 100%, 0% 100%);
        }
        .material-symbols-outlined {
            font-variation-settings: 'FILL' 0, 'wght' 300, 'GRAD' 0, 'opsz' 24;
        }
        .nav-active .material-symbols-outlined {
            font-variation-settings: 'FILL' 1, 'wght' 400;
        }
    </style>
</head>
<body class="text-slate-300 min-h-screen flex flex-col industrial-grid">
<!-- Header -->
<header class="sticky top-0 z-30 bg-industrial-black/95 backdrop-blur-md border-b border-industrial-border/60 px-4 py-3 flex items-center justify-between">
<div class="flex items-center gap-3">
<div class="relative">
<div class="size-10 rounded-sm bg-primary/20 flex items-center justify-center border border-primary/40 overflow-hidden">
<img alt="User Profile" class="w-full h-full object-cover grayscale opacity-80" src="https://lh3.googleusercontent.com/aida-public/AB6AXuAGg2bGhTCEMlBZXlsCGJF86XR9ClwOzRQOFADx5mRDZXJn-cXqKUvRv12uXFr7Z22fTij5W1iBiZT-j6TKVmxJTw6vLxzokvv8a0GjcfvKhxOnk-MG7rO4b5mGfyS28goklewvxq1UL5z7M3JMfBicHZRSAfJ2oJjRClSgqZ65Z-zxviLmmye799VsULxFCTvT_vTAPBeHHY9uZ_Uo405orvhV1mKUodsi9sgm84GGrU8MWKkNmhnXtc3bWoyGLCAJsNrrb1ofLII"/>
</div>
<div class="absolute -bottom-1 -right-1 size-3 bg-emerald-500 border-2 border-industrial-black rounded-full"></div>
</div>
<div>
<h1 class="text-lg font-bold tracking-wider text-white leading-none uppercase">Haley <span class="text-primary">Systems</span></h1>
<p class="mono-text text-[10px] text-secondary font-medium tracking-tighter uppercase">Technician ID: AX-942</p>
</div>
</div>
<div class="flex gap-2">
<button class="size-10 flex items-center justify-center border border-industrial-border bg-slate-900 text-slate-400 active:bg-primary active:text-black transition-all">
<span class="material-symbols-outlined text-[20px]">notifications</span>
</button>
<button class="size-10 flex items-center justify-center border border-industrial-border bg-slate-900 text-slate-400 active:bg-primary active:text-black transition-all">
<span class="material-symbols-outlined text-[20px]">search</span>
</button>
</div>
</header>
<main class="flex-1 overflow-y-auto pb-32">
<!-- Field Status Hero -->
<section class="p-4">
<div class="relative bg-industrial-dark border-l-4 border-primary border border-industrial-border p-5 shadow-2xl">
<div class="flex justify-between items-start mb-6">
<div>
<h2 class="text-3xl font-bold tracking-tight text-white uppercase italic">Active Session</h2>
<p class="mono-text text-xs text-slate-500 mt-1">OPERATOR: ALEX_VANCE</p>
</div>
<div class="bg-primary/10 px-2 py-1 border border-primary/20">
<span class="mono-text text-[10px] text-primary font-bold">SYS_READY_01</span>
</div>
</div>
<button class="group relative w-full bg-primary hover:bg-white text-black py-4 px-6 font-bold flex items-center justify-between transition-all overflow-hidden">
<div class="flex items-center gap-3">
<span class="material-symbols-outlined font-bold">precision_manufacturing</span>
<span class="uppercase tracking-widest text-lg">Initialize New Order</span>
</div>
<span class="material-symbols-outlined group-hover:translate-x-1 transition-transform">arrow_forward</span>
<div class="absolute right-0 bottom-0 size-4 bg-industrial-black/20 translate-x-2 translate-y-2 rotate-45"></div>
</button>
</div>
</section>
<!-- Catalog Selection -->
<section class="px-4 py-2">
<div class="flex items-center gap-2 mb-3">
<div class="h-[1px] flex-1 bg-industrial-border"></div>
<h3 class="mono-text text-[11px] font-bold text-slate-500 uppercase tracking-widest">Catalog Index</h3>
<div class="h-[1px] flex-1 bg-industrial-border"></div>
</div>
<div class="grid grid-cols-3 gap-3">
<button class="group flex flex-col items-center gap-2 p-4 bg-industrial-black border border-industrial-border hover:border-secondary transition-all active:scale-95">
<div class="size-12 bg-slate-900 flex items-center justify-center text-secondary border border-industrial-border group-hover:bg-secondary/10">
<span class="material-symbols-outlined text-3xl">view_in_ar</span>
</div>
<span class="mono-text text-[10px] font-bold uppercase text-slate-400 group-hover:text-secondary">Rectangular</span>
</button>
<button class="group flex flex-col items-center gap-2 p-4 bg-industrial-black border border-industrial-border hover:border-secondary transition-all active:scale-95">
<div class="size-12 bg-slate-900 flex items-center justify-center text-secondary border border-industrial-border group-hover:bg-secondary/10">
<span class="material-symbols-outlined text-3xl">radio_button_unchecked</span>
</div>
<span class="mono-text text-[10px] font-bold uppercase text-slate-400 group-hover:text-secondary">Round Duct</span>
</button>
<button class="group flex flex-col items-center gap-2 p-4 bg-industrial-black border border-industrial-border hover:border-secondary transition-all active:scale-95">
<div class="size-12 bg-slate-900 flex items-center justify-center text-secondary border border-industrial-border group-hover:bg-secondary/10">
<span class="material-symbols-outlined text-3xl">construction</span>
</div>
<span class="mono-text text-[10px] font-bold uppercase text-slate-400 group-hover:text-secondary">Hardware</span>
</button>
</div>
</section>
<!-- Activity Log -->
<section class="px-4 py-6">
<div class="flex items-center justify-between mb-4 px-1">
<h3 class="text-sm font-bold text-white uppercase tracking-widest flex items-center gap-2">
<span class="size-2 bg-secondary animate-pulse rounded-full"></span>
                Transmission Log
            </h3>
<button class="mono-text text-[10px] text-secondary font-bold hover:text-white transition-colors border-b border-secondary/30">VIEW_ALL</button>
</div>
<div class="space-y-2">
<!-- Order 1 -->
<div class="bg-industrial-dark p-3 border border-industrial-border flex items-center justify-between group active:bg-slate-800">
<div class="flex gap-3 items-center">
<div class="size-10 bg-slate-900 flex items-center justify-center text-slate-500 border border-industrial-border">
<span class="material-symbols-outlined text-[20px]">analytics</span>
</div>
<div>
<p class="font-bold text-sm text-slate-200 uppercase tracking-wide">Skyline Office Complex</p>
<p class="mono-text text-[10px] text-slate-500">REF: #9821 // DATE: 24.10.24</p>
</div>
</div>
<div class="flex flex-col items-end gap-1">
<span class="mono-text text-[10px] font-bold px-2 py-0.5 border border-primary/50 text-primary bg-primary/5">PENDING</span>
</div>
</div>
<!-- Order 2 -->
<div class="bg-industrial-dark p-3 border border-industrial-border flex items-center justify-between group active:bg-slate-800">
<div class="flex gap-3 items-center">
<div class="size-10 bg-slate-900 flex items-center justify-center text-slate-500 border border-industrial-border">
<span class="material-symbols-outlined text-[20px]">local_shipping</span>
</div>
<div>
<p class="font-bold text-sm text-slate-200 uppercase tracking-wide">Riverfront Warehouse</p>
<p class="mono-text text-[10px] text-slate-500">REF: #9745 // DATE: 22.10.24</p>
</div>
</div>
<div class="flex flex-col items-end gap-1">
<span class="mono-text text-[10px] font-bold px-2 py-0.5 border border-secondary/50 text-secondary bg-secondary/5">SHIPPED</span>
</div>
</div>
<!-- Order 3 -->
<div class="bg-industrial-dark p-3 border border-industrial-border flex items-center justify-between group active:bg-slate-800">
<div class="flex gap-3 items-center">
<div class="size-10 bg-slate-900 flex items-center justify-center text-slate-500 border border-industrial-border">
<span class="material-symbols-outlined text-[20px]">check_circle</span>
</div>
<div>
<p class="font-bold text-sm text-slate-200 uppercase tracking-wide">Oakview School HVAC</p>
<p class="mono-text text-[10px] text-slate-500">REF: #9612 // DATE: 18.10.24</p>
</div>
</div>
<div class="flex flex-col items-end gap-1">
<span class="mono-text text-[10px] font-bold px-2 py-0.5 border border-slate-600 text-slate-400 bg-slate-800">DELIVERED</span>
</div>
</div>
</div>
</section>
</main>
<!-- Bottom Nav -->
<nav class="fixed bottom-0 left-0 right-0 bg-industrial-black border-t border-industrial-border pb-6 pt-3 px-8 z-40">
<div class="flex justify-between items-center max-w-md mx-auto">
<a class="flex flex-col items-center gap-1 text-primary nav-active group" href="#">
<span class="material-symbols-outlined text-[26px]">dashboard</span>
<span class="mono-text text-[9px] font-bold uppercase tracking-tighter">Terminal</span>
</a>
<a class="flex flex-col items-center gap-1 text-slate-500 hover:text-secondary transition-colors" href="#">
<span class="material-symbols-outlined text-[26px]">receipt_long</span>
<span class="mono-text text-[9px] font-bold uppercase tracking-tighter">Orders</span>
</a>
<a class="flex flex-col items-center gap-1 text-slate-500 hover:text-secondary transition-colors" href="#">
<span class="material-symbols-outlined text-[26px]">hub</span>
<span class="mono-text text-[9px] font-bold uppercase tracking-tighter">Assets</span>
</a>
<a class="flex flex-col items-center gap-1 text-slate-500 hover:text-secondary transition-colors" href="#">
<span class="material-symbols-outlined text-[26px]">settings_input_component</span>
<span class="mono-text text-[9px] font-bold uppercase tracking-tighter">Config</span>
</a>
</div>
</nav>
</body></html>

<!-- Project Identification (Updated) -->
<!DOCTYPE html>

<html class="dark" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Haley Order System - New Order</title>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&amp;family=Inter:wght@400;500;600;700&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "primary": "#0ea5e9",
                        "background-dark": "#070d16",
                        "panel-dark": "#0f172a",
                        "accent": "#f59e0b"
                    },
                    fontFamily: {
                        "mono": ["JetBrains Mono", "monospace"],
                        "sans": ["Inter", "sans-serif"]
                    },
                    borderRadius: {
                        "DEFAULT": "0px",
                        "lg": "0px",
                        "xl": "0px",
                        "full": "0px"
                    },
                },
            },
        }
    </script>
<style>
        body {
            min-height: max(884px, 100dvh);
            font-family: 'Inter', sans-serif;
        }
        .font-mono { font-family: 'JetBrains Mono', monospace; }
        
        /* Industrial Form Styling */
        .form-input-industrial {
            @apply bg-slate-900/50 border-slate-700 text-slate-100 placeholder:text-slate-600 focus:border-primary focus:ring-1 focus:ring-primary/30 transition-all duration-200 uppercase text-sm tracking-wider font-mono;
        }
        
        /* Custom scrollbar for industrial look */
        ::-webkit-scrollbar { width: 4px; }
        ::-webkit-scrollbar-track { background: #070d16; }
        ::-webkit-scrollbar-thumb { background: #1e293b; }
    </style>
</head>
<body class="bg-background-dark text-slate-100 min-h-screen">
<div class="relative flex h-auto min-h-screen w-full flex-col bg-background-dark overflow-x-hidden border-x border-slate-800/50 max-w-lg mx-auto">
<header class="flex items-center bg-background-dark/80 backdrop-blur-md p-4 border-b border-slate-800 sticky top-0 z-10">
<div class="text-slate-400 flex size-10 shrink-0 items-center justify-start hover:text-white cursor-pointer transition-colors">
<span class="material-symbols-outlined text-2xl" data-icon="close">close</span>
</div>
<h2 class="text-slate-100 text-sm font-mono font-bold leading-tight tracking-[0.2em] flex-1 text-center uppercase">System // New_Order</h2>
<div class="size-10"></div>
</header>
<!-- Progress Indicator -->
<div class="flex w-full flex-row items-center justify-center gap-1.5 py-4 bg-slate-900/30 border-b border-slate-800/50">
<div class="h-1 w-8 bg-primary shadow-[0_0_8px_rgba(14,165,233,0.5)]"></div>
<div class="h-1 w-8 bg-slate-800"></div>
<div class="h-1 w-8 bg-slate-800"></div>
<div class="h-1 w-8 bg-slate-800"></div>
<div class="h-1 w-8 bg-slate-800"></div>
</div>
<main class="flex-1 px-6 pb-40">
<div class="py-8">
<div class="flex items-center gap-2 mb-2">
<span class="bg-primary/10 text-primary px-2 py-0.5 text-[10px] font-mono font-bold tracking-tighter border border-primary/20 uppercase">Stage 01</span>
<span class="text-slate-500 font-mono text-[10px] tracking-widest uppercase">ID: JOB_IDENTIFICATION</span>
</div>
<h3 class="text-slate-100 text-2xl font-bold leading-tight uppercase tracking-tight font-mono">Project Identification</h3>
<div class="h-1 w-12 bg-primary mt-4"></div>
<p class="text-slate-500 text-xs font-mono leading-relaxed mt-4 max-w-xs uppercase tracking-tight">System configuration for upcoming Haley installation sequence.</p>
</div>
<div class="space-y-8">
<!-- Job Name -->
<label class="flex flex-col w-full group">
<div class="flex justify-between items-end pb-2">
<p class="text-slate-500 text-[10px] font-mono font-bold uppercase tracking-[0.15em] group-focus-within:text-primary transition-colors">01. Job_Name</p>
<span class="text-[10px] text-slate-700 font-mono italic">REQUIRED</span>
</div>
<input class="form-input-industrial flex w-full h-12 p-4" placeholder="SKYLINE_PHASE_II" type="text"/>
</label>
<!-- Date (Read Only) -->
<label class="flex flex-col w-full opacity-70">
<p class="text-slate-500 text-[10px] font-mono font-bold uppercase tracking-[0.15em] pb-2">02. System_Date</p>
<div class="flex items-center w-full h-12 bg-slate-900/30 border border-slate-800/50 p-4 font-mono text-sm text-slate-400">
                        OCT_24_2023
                    </div>
</label>
<!-- Required Delivery Date -->
<label class="flex flex-col w-full group">
<p class="text-slate-500 text-[10px] font-mono font-bold uppercase tracking-[0.15em] pb-2 group-focus-within:text-primary transition-colors">03. Delivery_Target</p>
<div class="relative">
<input class="form-input-industrial flex w-full h-12 p-4 appearance-none" type="date"/>
<span class="material-symbols-outlined absolute right-4 top-1/2 -translate-y-1/2 text-slate-500 pointer-events-none text-xl">calendar_today</span>
</div>
</label>
<div class="pt-8 border-t border-slate-800/50">
<div class="flex items-center gap-3 mb-6">
<div class="size-2 bg-accent"></div>
<h4 class="text-slate-100 font-mono font-bold text-sm uppercase tracking-widest">Personnel // On-Site Contact</h4>
</div>
<div class="space-y-8">
<!-- Foreman Name -->
<label class="flex flex-col w-full group">
<p class="text-slate-500 text-[10px] font-mono font-bold uppercase tracking-[0.15em] pb-2 group-focus-within:text-primary transition-colors">04. Lead_Foreman</p>
<input class="form-input-industrial flex w-full h-12 p-4" placeholder="OPERATOR_NAME" type="text"/>
</label>
<!-- Phone Number -->
<label class="flex flex-col w-full group">
<p class="text-slate-500 text-[10px] font-mono font-bold uppercase tracking-[0.15em] pb-2 group-focus-within:text-primary transition-colors">05. Comms_Channel</p>
<input class="form-input-industrial flex w-full h-12 p-4" placeholder="+1-555-000-0000" type="tel"/>
</label>
</div>
</div>
</div>
</main>
<footer class="fixed bottom-0 left-0 right-0 max-w-lg mx-auto p-4 bg-background-dark/95 backdrop-blur-lg border-t border-slate-800 flex flex-col gap-3 z-20">
<div class="flex gap-2">
<button class="flex-1 flex items-center justify-center gap-3 bg-primary hover:bg-sky-400 text-white font-mono font-bold text-sm py-4 px-6 border-b-4 border-sky-700 active:border-b-0 active:translate-y-[2px] transition-all uppercase tracking-widest">
<span>Next: Duct_Specs</span>
<span class="material-symbols-outlined text-lg">chevron_right</span>
</button>
</div>
<div class="flex justify-between items-center px-2">
<button class="text-slate-500 hover:text-slate-300 font-mono text-[10px] uppercase tracking-widest flex items-center gap-1 transition-colors">
<span class="material-symbols-outlined text-sm">save</span>
                    Cache_Draft
                </button>
<span class="text-[9px] text-slate-700 font-mono">HVAC_PRO_OS_v2.4.0</span>
</div>
</footer>
</div>
</body></html>

<!-- Rectangular Duct Order -->
<!DOCTYPE html>

<html class="dark" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Public+Sans:wght@300;400;500;600;700;800&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "primary": "#00E5FF", // Neon Cyan
                        "primary-dark": "#00B8CC",
                        "background-dark": "#0B0F13",
                        "surface-dark": "#161B22",
                        "border-dark": "#30363D",
                        "accent-yellow": "#FFD600"
                    },
                    fontFamily: {
                        "display": ["Public Sans", "sans-serif"],
                        "mono": ["JetBrains Mono", "monospace"]
                    },
                    borderRadius: {
                        "DEFAULT": "2px",
                        "lg": "4px",
                        "xl": "8px",
                        "full": "9999px"
                    },
                },
            },
        }
    </script>
<title>HVAC PRO - Rectangular Duct</title>
<style>
        body {
            min-height: max(884px, 100dvh);
            background-color: #0B0F13;
        }
        .industrial-grid {
            background-image: radial-gradient(rgba(0, 229, 255, 0.05) 1px, transparent 0);
            background-size: 24px 24px;
        }
        .tech-border {
            border: 1px solid #30363D;
            position: relative;
        }
        .tech-border::after {
            content: '';
            position: absolute;
            top: 0; right: 0;
            width: 8px; height: 8px;
            border-top: 2px solid #00E5FF;
            border-right: 2px solid #00E5FF;
        }
    </style>
</head>
<body class="font-display bg-background-dark text-slate-100 min-h-screen industrial-grid">
<div class="relative flex h-auto min-h-screen w-full flex-col overflow-x-hidden max-w-md mx-auto shadow-2xl bg-background-dark border-x border-border-dark">
<!-- TopAppBar -->
<div class="flex items-center bg-surface-dark/80 backdrop-blur-md p-4 pb-3 justify-between sticky top-0 z-20 border-b border-border-dark">
<div class="text-slate-100 flex size-10 shrink-0 items-center justify-start">
<span class="material-symbols-outlined cursor-pointer hover:text-primary transition-colors">close</span>
</div>
<div class="flex flex-col items-center">
<h2 class="text-slate-100 text-xs font-black uppercase tracking-[0.2em] leading-tight">Order System</h2>
<span class="text-[10px] text-primary font-mono">ID: HV-992-RD</span>
</div>
<div class="flex w-10 items-center justify-end">
<button class="flex items-center justify-center rounded bg-transparent text-primary">
<span class="material-symbols-outlined text-[20px]">settings</span>
</button>
</div>
</div>
<!-- Progress Indicator -->
<div class="flex w-full flex-row items-center justify-center gap-1.5 py-4 bg-surface-dark/40 border-b border-border-dark">
<div class="h-1 w-6 rounded-full bg-primary shadow-[0_0_8px_rgba(0,229,255,0.6)]"></div>
<div class="h-1 w-12 rounded-full bg-primary shadow-[0_0_8px_rgba(0,229,255,0.6)]"></div>
<div class="h-1 w-6 rounded-full bg-slate-700"></div>
<div class="h-1 w-6 rounded-full bg-slate-700"></div>
<div class="h-1 w-6 rounded-full bg-slate-700"></div>
</div>
<!-- Hero Content -->
<div class="px-5 pt-8 pb-6">
<div class="flex items-center gap-2 mb-1">
<div class="h-4 w-1 bg-primary"></div>
<h3 class="text-white tracking-tight text-2xl font-black uppercase italic">Rectangular Duct</h3>
</div>
<p class="text-slate-400 text-[11px] font-mono leading-normal uppercase tracking-wider">Industrial Specification Module // Part 01</p>
</div>
<!-- Repeatable Item Section -->
<div class="px-4 space-y-6 pb-32">
<!-- Item Card -->
<div class="p-5 tech-border bg-surface-dark shadow-lg">
<div class="flex justify-between items-center mb-6 border-b border-border-dark pb-3">
<div class="flex items-center gap-2">
<span class="text-[10px] font-mono text-primary bg-primary/10 px-2 py-0.5 border border-primary/20">MODULE</span>
<h3 class="text-white text-sm font-black italic">ITEM 001</h3>
</div>
<button class="text-slate-500 hover:text-red-400 transition-colors">
<span class="material-symbols-outlined text-lg">delete_sweep</span>
</button>
</div>
<div class="grid grid-cols-2 gap-5">
<!-- Qty -->
<div class="flex flex-col gap-1.5">
<label class="text-[10px] font-bold text-slate-400 uppercase tracking-widest">Qty / Cant</label>
<div class="relative">
<input class="w-full bg-background-dark border-border-dark text-primary font-mono text-sm focus:ring-1 focus:ring-primary focus:border-primary py-2.5" placeholder="1" type="number"/>
</div>
</div>
<!-- Gauge -->
<div class="flex flex-col gap-1.5">
<label class="text-[10px] font-bold text-slate-400 uppercase tracking-widest">Gauge / Calibre</label>
<select class="w-full bg-background-dark border-border-dark text-slate-200 font-mono text-sm focus:ring-1 focus:ring-primary focus:border-primary py-2.5">
<option>24 Ga</option>
<option>22 Ga</option>
<option>20 Ga</option>
<option>18 Ga</option>
</select>
</div>
</div>
<!-- Technical Dimensions -->
<div class="mt-6">
<label class="text-[10px] font-bold text-slate-400 uppercase tracking-widest block mb-3">Dimensions (Inch)</label>
<div class="grid grid-cols-3 gap-3">
<div class="flex flex-col gap-1">
<div class="text-[9px] font-mono text-slate-500 flex justify-between">
<span>WIDTH</span>
<span class="text-primary">[W]</span>
</div>
<input class="w-full bg-background-dark border-border-dark text-slate-200 font-mono text-xs focus:ring-1 focus:ring-primary focus:border-primary py-2 px-3" placeholder='24.0"' type="text"/>
</div>
<div class="flex flex-col gap-1">
<div class="text-[9px] font-mono text-slate-500 flex justify-between">
<span>HEIGHT</span>
<span class="text-primary">[H]</span>
</div>
<input class="w-full bg-background-dark border-border-dark text-slate-200 font-mono text-xs focus:ring-1 focus:ring-primary focus:border-primary py-2 px-3" placeholder='12.0"' type="text"/>
</div>
<div class="flex flex-col gap-1">
<div class="text-[9px] font-mono text-slate-500 flex justify-between">
<span>LENGTH</span>
<span class="text-primary">[L]</span>
</div>
<input class="w-full bg-background-dark border-border-dark text-slate-200 font-mono text-xs focus:ring-1 focus:ring-primary focus:border-primary py-2 px-3" placeholder='60.0"' type="text"/>
</div>
</div>
</div>
<!-- Description -->
<div class="mt-6 flex flex-col gap-1.5">
<label class="text-[10px] font-bold text-slate-400 uppercase tracking-widest">Description / Fitting</label>
<input class="w-full bg-background-dark border-border-dark text-slate-200 text-xs focus:ring-1 focus:ring-primary focus:border-primary py-2.5 px-3" placeholder="Straight Duct, Transition, Elbow..." type="text"/>
</div>
<!-- Connection Type -->
<div class="mt-8">
<div class="flex items-center justify-between mb-3">
<label class="text-[10px] font-bold text-slate-400 uppercase tracking-widest">Connection Type</label>
<span class="text-[9px] font-mono text-primary/60">SYS_SEL_READY</span>
</div>
<div class="flex p-1 bg-background-dark border border-border-dark rounded">
<button class="flex-1 py-2.5 text-[10px] font-black tracking-tighter uppercase transition-all bg-primary text-background-dark shadow-[0_0_12px_rgba(0,229,255,0.4)]">TDC</button>
<button class="flex-1 py-2.5 text-[10px] font-black tracking-tighter uppercase text-slate-500 hover:text-slate-300">S&amp;D</button>
<button class="flex-1 py-2.5 text-[10px] font-black tracking-tighter uppercase text-slate-500 hover:text-slate-300 border-l border-border-dark/50">S/S</button>
</div>
</div>
</div>
<!-- Add Another Item Button -->
<button class="w-full py-5 border-2 border-dashed border-border-dark hover:border-primary/40 group transition-all duration-300 flex items-center justify-center gap-3">
<span class="material-symbols-outlined text-slate-500 group-hover:text-primary transition-colors">add_circle</span>
<span class="text-[11px] font-black text-slate-500 group-hover:text-primary uppercase tracking-[0.2em]">Add Module Item</span>
</button>
</div>
<!-- Bottom Navigation -->
<div class="fixed bottom-0 left-0 right-0 max-w-md mx-auto bg-surface-dark/95 backdrop-blur-md border-t border-border-dark p-5 space-y-4 shadow-[0_-10px_30px_rgba(0,0,0,0.5)] z-20">
<div class="flex gap-4">
<button class="flex-[1] py-3.5 border border-border-dark font-black text-[10px] uppercase tracking-widest text-slate-400 hover:bg-slate-800 transition-colors">
                    Back
                </button>
<button class="flex-[2] bg-primary py-3.5 font-black text-[11px] text-background-dark uppercase tracking-widest flex items-center justify-center gap-2 hover:bg-white transition-all shadow-[0_0_20px_rgba(0,229,255,0.2)]">
                    Next: Round Duct
                    <span class="material-symbols-outlined text-sm font-bold">arrow_forward</span>
</button>
</div>
<button class="w-full text-center text-[9px] font-bold text-slate-500 py-1 uppercase tracking-[0.3em] hover:text-primary transition-colors">
                Save System Draft
            </button>
</div>
</div>
</body></html>

<!-- Round Duct & Flex System (Updated) -->
<!DOCTYPE html>

<html class="dark" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<link href="https://fonts.googleapis.com/css2?family=Public+Sans:wght@400;500;600;700&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "primary": "#00E5FF", // Cyan accent
                        "secondary": "#FF8C00", // Orange accent
                        "background-dark": "#0A0F14",
                        "surface-dark": "#141B23",
                        "border-dark": "#232D38",
                    },
                    fontFamily: {
                        "display": ["Public Sans"],
                        "mono": ["JetBrains Mono"]
                    },
                    borderRadius: {"DEFAULT": "0px", "lg": "2px", "xl": "4px", "full": "9999px"},
                },
            },
        }
    </script>
<title>HVAC PRO - Round Duct &amp; Flex</title>
<style>
    body {
      min-height: max(884px, 100dvh);
      background-color: #0A0F14;
    }
    .technical-grid {
        background-image: radial-gradient(#232D38 0.5px, transparent 0.5px);
        background-size: 20px 20px;
    }
  </style>
</head>
<body class="dark:bg-background-dark font-display text-slate-300 antialiased technical-grid">
<div class="relative flex min-h-screen w-full flex-col overflow-x-hidden">
<!-- Header -->
<header class="sticky top-0 z-10 flex items-center bg-surface-dark/95 backdrop-blur-md border-b border-border-dark p-4 justify-between">
<div class="flex items-center gap-4">
<button class="text-primary hover:bg-primary/10 p-2 transition-colors border border-border-dark">
<span class="material-symbols-outlined block">arrow_back</span>
</button>
<div>
<h1 class="text-sm font-bold uppercase tracking-widest text-white flex items-center gap-2">
<span class="size-2 bg-secondary animate-pulse rounded-full"></span>
    Round Duct &amp; Flex System
</h1>
<p class="text-[10px] text-slate-500 font-mono uppercase">Haley Order System • Step 3/5 • Session: #HV-8842</p>
</div>
</div>
<button class="border border-secondary/50 text-secondary px-4 py-1.5 text-[11px] font-bold uppercase tracking-wider hover:bg-secondary hover:text-black transition-all">
    Save Draft
</button>
</header>
<!-- Progress Bar -->
<div class="p-4 bg-surface-dark/50 border-b border-border-dark flex items-center gap-4">
<div class="flex-1">
<div class="flex justify-between items-center mb-1.5">
<p class="text-[10px] font-bold text-slate-500 uppercase tracking-tighter">Installation Readiness</p>
<p class="text-[10px] font-mono text-primary">60.0%</p>
</div>
<div class="h-1 w-full bg-border-dark overflow-hidden">
<div class="h-full bg-primary shadow-[0_0_8px_rgba(0,229,255,0.5)]" style="width: 60%;"></div>
</div>
</div>
</div>
<!-- Main Content Area -->
<main class="flex-1 p-4 space-y-6 max-w-4xl mx-auto w-full pb-32">
<!-- Category Header -->
<div class="flex items-center justify-between border-l-2 border-secondary pl-4">
<div>
<h2 class="text-sm font-bold uppercase tracking-widest text-white">Duct Components</h2>
<p class="text-[11px] text-slate-500 font-mono">SPECIFICATION-READY SELECTIONS</p>
</div>
<span class="text-[10px] text-slate-600 font-mono">ID: SEC-D03</span>
</div>
<!-- Item Card: Adjustable Elbow -->
<div class="bg-surface-dark border border-border-dark hover:border-primary/30 transition-colors">
<div class="flex flex-col sm:flex-row gap-4 p-4">
<div class="h-32 w-full sm:w-32 bg-background-dark border border-border-dark p-2 flex items-center justify-center grayscale hover:grayscale-0 transition-all">
<img alt="Adjustable Elbow" class="h-full object-contain" src="https://lh3.googleusercontent.com/aida-public/AB6AXuAJNWWMv9Q1n2zFUeCm3nqvfT56M1OqnpH9XA0ZywKBKuf1yCdl2wOwdTYQX52v-VF-ijc5J_b7OYJeiZ20vw3HLJCqO_ZKlbsehi5JCC3rJYGoCXtuW-mYSeEmbUkCImtZ3BY3CP_Kmj5-iXgwV1XGepqnxXGTBMvMIYfuHv8NTW4GeZSqPYFIfe5y0pw75EFY7M6fkJNw_Qx0Q-lVvVOViVi48WjxyIMW1RcwpKvWjHC5tldQZISuOp3cY2OLTdLl8AVjR_2TbTQ"/>
</div>
<div class="flex-1 space-y-4">
<div class="flex justify-between items-start">
<h3 class="font-bold text-xs uppercase tracking-wider text-white">Adjustable Elbow</h3>
<span class="px-2 py-0.5 bg-primary/10 text-primary text-[9px] font-mono border border-primary/20">GALV-30GA</span>
</div>
<div class="grid grid-cols-2 gap-2">
<label class="relative flex items-center justify-center p-3 border border-border-dark cursor-pointer group hover:bg-white/5 transition-colors">
<input checked="" class="absolute opacity-0" name="elbow_deg" type="radio"/>
<span class="text-[10px] font-bold uppercase tracking-tight text-slate-500 peer-checked:text-primary group-has-[:checked]:text-primary group-has-[:checked]:border-primary transition-colors">90° Degree</span>
<div class="absolute inset-0 border border-transparent group-has-[:checked]:border-primary pointer-events-none"></div>
</label>
<label class="relative flex items-center justify-center p-3 border border-border-dark cursor-pointer group hover:bg-white/5 transition-colors">
<input class="absolute opacity-0" name="elbow_deg" type="radio"/>
<span class="text-[10px] font-bold uppercase tracking-tight text-slate-500 group-has-[:checked]:text-primary transition-colors">45° Degree</span>
<div class="absolute inset-0 border border-transparent group-has-[:checked]:border-primary pointer-events-none"></div>
</label>
</div>
<div class="flex items-center justify-between gap-4 pt-2 border-t border-border-dark/50">
<div class="flex items-center bg-background-dark border border-border-dark">
<button class="px-3 py-2 text-slate-400 hover:text-white transition-colors">-</button>
<input class="w-12 text-center bg-transparent border-none focus:ring-0 text-sm font-mono text-primary font-bold" type="number" value="0"/>
<button class="px-3 py-2 text-slate-400 hover:text-white transition-colors">+</button>
</div>
<button class="flex-1 bg-primary text-black text-[11px] font-black uppercase tracking-widest py-3 hover:brightness-110 transition-all">Add to System</button>
</div>
</div>
</div>
</div>
<!-- Item Card: Flex Duct -->
<div class="bg-surface-dark border border-border-dark">
<div class="flex flex-col sm:flex-row gap-4 p-4">
<div class="h-32 w-full sm:w-32 bg-background-dark border border-border-dark p-2 flex items-center justify-center grayscale hover:grayscale-0 transition-all">
<img alt="Flex Duct" class="h-full object-contain" src="https://lh3.googleusercontent.com/aida-public/AB6AXuAK_ui2sNoL_pWjDvyeSkI5benp1RT1rAlrDVDnTOEFPRjGttBWw7hwpQ55H2-zJdfjn9iHuC1JoH8ycwufFEMDFZ9sjut9WQmTk4T4gsOrhQ6t5sBUf3GajZXJ9ESj9VopmiSo4nc_R2E6PSi1eeR9bMzyt3iK89ls6RjxBap4lyaWqVpH6xx-o2hXL76HDEgoHYQricV7KfdMLTQn4c0Cn-8EK-Cjhl8tC6RUHix7AzEm9QMLlsLgfF9crvPLeYxAJmEIQzcQl-g"/>
</div>
<div class="flex-1 space-y-4">
<h3 class="font-bold text-xs uppercase tracking-wider text-white">Flex Duct (25ft)</h3>
<div class="space-y-1">
<label class="text-[9px] font-mono text-slate-500 uppercase">Thermal Insulation (R-Value)</label>
<select class="w-full bg-background-dark border-border-dark text-slate-300 text-[11px] font-bold uppercase tracking-tight focus:ring-primary focus:border-primary px-3 py-3">
<option>Silver Jacket R-6.0</option>
<option>Silver Jacket R-8.0</option>
</select>
</div>
<div class="flex items-center justify-between gap-4 pt-2 border-t border-border-dark/50">
<div class="flex items-center bg-background-dark border border-border-dark">
<button class="px-3 py-2 text-slate-400 hover:text-white">-</button>
<input class="w-12 text-center bg-transparent border-none focus:ring-0 text-sm font-mono text-primary font-bold" type="number" value="0"/>
<button class="px-3 py-2 text-slate-400 hover:text-white">+</button>
</div>
<button class="flex-1 bg-primary text-black text-[11px] font-black uppercase tracking-widest py-3 hover:brightness-110">Add to System</button>
</div>
</div>
</div>
</div>
<!-- Grid Items: Technical Selectors -->
<div class="grid grid-cols-1 md:grid-cols-2 gap-4">
<!-- Take-offs -->
<div class="bg-surface-dark border border-border-dark p-4 space-y-4">
<div class="flex justify-between items-center">
<h3 class="font-bold text-[11px] uppercase tracking-widest text-white">Take-offs</h3>
<span class="material-symbols-outlined text-secondary text-sm">settings_input_component</span>
</div>
<div class="space-y-3">
<div class="space-y-1">
<label class="text-[9px] font-mono text-slate-500 uppercase">Collar Diameter</label>
<select class="w-full bg-background-dark border-border-dark text-slate-300 text-[11px] uppercase py-2 focus:ring-primary">
<option>6" Nominal</option>
<option>8" Nominal</option>
<option>10" Nominal</option>
</select>
</div>
<div class="space-y-1">
<label class="text-[9px] font-mono text-slate-500 uppercase">Mounting Interface</label>
<select class="w-full bg-background-dark border-border-dark text-slate-300 text-[11px] uppercase py-2 focus:ring-primary">
<option>Sticky (Self-Adhesive)</option>
<option>Dovetail Mechanized</option>
</select>
</div>
</div>
<div class="flex items-center justify-between pt-2">
<div class="flex items-center bg-background-dark border border-border-dark">
<button class="px-2 py-1.5 text-slate-400 text-xs">-</button>
<input class="w-10 text-center bg-transparent border-none focus:ring-0 text-xs font-mono text-primary font-bold" type="number" value="0"/>
<button class="px-2 py-1.5 text-slate-400 text-xs">+</button>
</div>
<button class="border border-primary/50 text-primary text-[10px] font-bold uppercase tracking-widest px-4 py-2 hover:bg-primary/10">Add to Cart</button>
</div>
</div>
<!-- Nylon Ties -->
<div class="bg-surface-dark border border-border-dark p-4 space-y-4">
<div class="flex justify-between items-center">
<h3 class="font-bold text-[11px] uppercase tracking-widest text-white">Nylon Ties</h3>
<span class="material-symbols-outlined text-secondary text-sm">link</span>
</div>
<div class="grid grid-cols-2 gap-2">
<button class="py-2.5 text-[10px] font-black border border-primary text-primary bg-primary/5 uppercase">36 INCH</button>
<button class="py-2.5 text-[10px] font-black border border-border-dark text-slate-500 uppercase hover:text-slate-300">48 INCH</button>
</div>
<div class="flex items-center justify-between pt-2 mt-auto">
<div class="flex items-center bg-background-dark border border-border-dark">
<button class="px-2 py-1.5 text-slate-400 text-xs">-</button>
<input class="w-10 text-center bg-transparent border-none focus:ring-0 text-xs font-mono text-primary font-bold" type="number" value="0"/>
<button class="px-2 py-1.5 text-slate-400 text-xs">+</button>
</div>
<button class="border border-primary/50 text-primary text-[10px] font-bold uppercase tracking-widest px-4 py-2 hover:bg-primary/10">Add to Cart</button>
</div>
</div>
</div>
<!-- Item Card: Spiral Duct -->
<div class="bg-surface-dark border border-border-dark">
<div class="flex flex-col sm:flex-row gap-4 p-4">
<div class="h-32 w-full sm:w-32 bg-background-dark border border-border-dark p-2 flex items-center justify-center grayscale hover:grayscale-0 transition-all">
<img alt="Spiral Duct" class="h-full object-contain" src="https://lh3.googleusercontent.com/aida-public/AB6AXuAiBrL9rxqPoH4muoo8FJsW16n_e_PsZkxFjLRKz24VJmHZ6rqiI4XPkAe_Bc4YRf7wzCtM9wgAfTJILxFZFr_oIwmINy6RIvu7UkhjZUzMsQNCDoClzJb1TdDnYebFKFJfQn5mbCQR3J9WE-aT1rfl7pAU8WmqkR5ZlYThX0ffSlhlo6ju0ipLQaYiyQAUAfX4SGNkoMNNF8yIvzC1IRdfGro9ccLmxzuyRkuMwPlBmsvUJVoFy01CXZHi53bqTa_4oQRHOZUWE9U"/>
</div>
<div class="flex-1 space-y-4">
<div>
<h3 class="font-bold text-xs uppercase tracking-wider text-white">Spiral Duct (10ft)</h3>
<p class="text-[10px] font-mono text-slate-500 mt-1 uppercase">Heavy-duty galvanized industrial seam</p>
</div>
<div class="flex items-center justify-between gap-4 pt-2 border-t border-border-dark/50">
<div class="flex items-center bg-background-dark border border-border-dark">
<button class="px-3 py-2 text-slate-400 hover:text-white">-</button>
<input class="w-12 text-center bg-transparent border-none focus:ring-0 text-sm font-mono text-primary font-bold" type="number" value="0"/>
<button class="px-3 py-2 text-slate-400 hover:text-white">+</button>
</div>
<button class="flex-1 bg-primary text-black text-[11px] font-black uppercase tracking-widest py-3 hover:brightness-110">Add to System</button>
</div>
</div>
</div>
</div>
</main>
<!-- Bottom Navigation -->
<nav class="fixed bottom-0 left-0 right-0 bg-surface-dark border-t border-border-dark p-4 z-20">
<div class="flex gap-3 max-w-4xl mx-auto">
<button class="flex-1 border border-border-dark bg-background-dark text-slate-400 font-bold py-4 text-[11px] uppercase tracking-widest flex items-center justify-center gap-2 hover:text-white transition-colors">
<span class="material-symbols-outlined text-sm">chevron_left</span>
            Return
        </button>
<button class="flex-[2_2_0%] bg-secondary text-black font-black py-4 text-[11px] uppercase tracking-[0.2em] flex items-center justify-center gap-2 shadow-[0_4px_20px_rgba(255,140,0,0.3)] hover:brightness-110">
            Next Configuration
            <span class="material-symbols-outlined text-sm">chevron_right</span>
</button>
</div>
</nav>
<!-- Sidebar Nav (Desktop) -->
<div class="hidden lg:flex fixed left-0 top-0 bottom-0 w-20 flex-col items-center bg-surface-dark border-r border-border-dark py-8 gap-10">
<div class="text-primary pb-8 border-b border-border-dark mb-4">
<span class="material-symbols-outlined text-4xl">precision_manufacturing</span>
</div>
<a class="flex flex-col items-center gap-2 text-primary" href="#">
<span class="material-symbols-outlined text-xl">description</span>
<span class="text-[9px] font-black uppercase tracking-tighter">Orders</span>
</a>
<a class="flex flex-col items-center gap-2 text-slate-600 hover:text-slate-400" href="#">
<span class="material-symbols-outlined text-xl">inventory_2</span>
<span class="text-[9px] font-black uppercase tracking-tighter">Products</span>
</a>
<a class="flex flex-col items-center gap-2 text-slate-600 hover:text-slate-400" href="#">
<span class="material-symbols-outlined text-xl">settings</span>
<span class="text-[9px] font-black uppercase tracking-tighter">System</span>
</a>
</div>
</div>
</body></html>

<!-- Mechanical Fasteners Updated -->
<!DOCTYPE html>

<html class="dark" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Haley Order System - Step 4</title>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Public+Sans:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "primary": "#3b82f6",
                        "accent": "#60a5fa",
                        "background-dark": "#0f172a",
                        "surface-dark": "#1e293b",
                        "border-dark": "#334155",
                    },
                    fontFamily: {
                        "display": ["Public Sans"]
                    },
                    borderRadius: {"DEFAULT": "0.25rem", "lg": "0.5rem", "xl": "0.75rem", "full": "9999px"},
                },
            },
        }
    </script>
<style>
        body {
            min-height: 100dvh;
        }
        .pro-shadow {
            box-shadow: 0 4px 20px -2px rgba(0, 0, 0, 0.5);
        }
        .technical-grid {
            background-image: radial-gradient(#334155 0.5px, transparent 0.5px);
            background-size: 20px 20px;
        }
    </style>
</head>
<body class="bg-background-dark font-display text-slate-100 min-h-screen flex flex-col technical-grid">
<header class="sticky top-0 z-30 bg-surface-dark/95 backdrop-blur-md border-b border-border-dark">
<div class="flex items-center p-4 gap-4">
<button class="text-slate-400 hover:text-white transition-colors">
<span class="material-symbols-outlined">arrow_back</span>
</button>
<h1 class="text-lg font-bold tracking-tight uppercase text-slate-200">Mechanical Fasteners</h1>
</div>
<div class="px-4 pb-4">
<div class="flex justify-between items-center mb-2">
<span class="text-[10px] font-bold uppercase tracking-[0.2em] text-slate-500">Haley Order System</span>
<span class="text-xs font-black text-primary">STEP 04 <span class="text-slate-600">/ 05</span></span>
</div>
<div class="w-full bg-slate-800 h-1.5 rounded-full overflow-hidden">
<div class="bg-primary h-full w-[80%] shadow-[0_0_10px_rgba(59,130,246,0.5)]"></div>
</div>
</div>
</header>
<main class="flex-1 overflow-y-auto pb-48">
<!-- Zip Screws Section -->
<section class="p-5 border-b border-border-dark bg-surface-dark/40 backdrop-blur-sm">
<div class="flex items-center gap-3 mb-5">
<div class="w-10 h-10 rounded-lg bg-primary/20 flex items-center justify-center border border-primary/30">
<span class="material-symbols-outlined text-primary">build</span>
</div>
<div>
<h3 class="text-lg font-bold text-white uppercase tracking-tight leading-tight">Zip Screws</h3>
<p class="text-[11px] text-slate-500 font-bold uppercase tracking-widest leading-none">Tornillos</p>
</div>
</div>
<div class="flex items-center justify-between p-4 bg-primary/5 border border-primary/20 rounded-xl mb-6 relative overflow-hidden">
<div class="absolute top-0 left-0 w-1 h-full bg-primary"></div>
<div class="flex items-center gap-3">
<span class="material-symbols-outlined text-primary fill-1">check_circle</span>
<div>
<p class="text-xs text-slate-400 font-medium uppercase tracking-wider">Current Diameter</p>
<p class="font-bold text-lg text-white">5/16"</p>
</div>
</div>
<span class="text-[10px] font-black text-primary bg-primary/10 px-2 py-1 rounded border border-primary/20">SELECTED</span>
</div>
<div class="mb-6">
<p class="text-xs font-bold text-slate-500 uppercase tracking-widest mb-3">Length (Largo)</p>
<div class="grid grid-cols-3 gap-3">
<button class="py-3 px-4 bg-primary text-white rounded-xl font-bold border border-primary shadow-lg shadow-primary/20">1"</button>
<button class="py-3 px-4 bg-slate-800/50 border border-slate-700 hover:border-primary/50 text-slate-400 rounded-xl font-bold transition-all">2"</button>
<button class="py-3 px-4 bg-slate-800/50 border border-slate-700 hover:border-primary/50 text-slate-400 rounded-xl font-bold transition-all">3"</button>
</div>
</div>
<div class="flex items-center justify-between bg-slate-900/50 p-3 rounded-xl border border-border-dark">
<p class="text-xs font-bold text-slate-400 uppercase tracking-widest">Qty (Boxes)</p>
<div class="flex items-center bg-slate-800 rounded-lg border border-slate-700 overflow-hidden">
<button class="w-10 h-10 flex items-center justify-center text-slate-400 hover:bg-slate-700 active:bg-slate-600 transition-colors border-r border-slate-700">
<span class="material-symbols-outlined text-xl">remove</span>
</button>
<input class="w-14 text-center border-none bg-transparent focus:ring-0 text-base font-black text-white" readonly="" type="number" value="1"/>
<button class="w-10 h-10 flex items-center justify-center text-slate-400 hover:bg-slate-700 active:bg-slate-600 transition-colors border-l border-slate-700">
<span class="material-symbols-outlined text-xl">add</span>
</button>
</div>
</div>
</section>
<!-- Bolts Section -->
<section class="p-5 border-b border-border-dark">
<h3 class="text-md font-bold text-slate-300 uppercase tracking-tight mb-4 flex items-center gap-2">
<span class="w-1.5 h-1.5 rounded-full bg-slate-500"></span>
            Bolts (Pernos)
        </h3>
<div class="mb-5">
<p class="text-[10px] font-bold text-slate-500 uppercase tracking-[0.15em] mb-3">Size Selection</p>
<button class="w-1/3 py-3 px-4 bg-primary text-white rounded-xl font-bold border border-primary shadow-lg shadow-primary/20">9/16"</button>
</div>
<div class="flex items-center justify-between bg-slate-900/30 p-3 rounded-xl border border-border-dark/50">
<p class="text-xs font-bold text-slate-500 uppercase tracking-widest">Qty (Boxes)</p>
<div class="flex items-center bg-slate-800/50 rounded-lg border border-slate-700/50 overflow-hidden">
<button class="w-9 h-9 flex items-center justify-center text-slate-500 hover:text-white transition-colors border-r border-slate-700/50">
<span class="material-symbols-outlined text-lg">remove</span>
</button>
<input class="w-12 text-center border-none bg-transparent focus:ring-0 text-sm font-bold text-slate-400" readonly="" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center text-slate-500 hover:text-white transition-colors border-l border-slate-700/50">
<span class="material-symbols-outlined text-lg">add</span>
</button>
</div>
</div>
</section>
<!-- Nuts Section -->
<section class="p-5 border-b border-border-dark">
<h3 class="text-md font-bold text-slate-300 uppercase tracking-tight mb-4 flex items-center gap-2">
<span class="w-1.5 h-1.5 rounded-full bg-slate-500"></span>
            Nuts (Tuercas)
        </h3>
<div class="mb-5">
<p class="text-[10px] font-bold text-slate-500 uppercase tracking-[0.15em] mb-3">Size Selection</p>
<div class="grid grid-cols-3 gap-3">
<button class="py-3 px-4 bg-slate-800/30 border border-slate-700 text-slate-400 rounded-xl font-bold">3/8"</button>
<button class="py-3 px-4 bg-slate-800/30 border border-slate-700 text-slate-400 rounded-xl font-bold">1/2"</button>
</div>
</div>
<div class="flex items-center justify-between bg-slate-900/30 p-3 rounded-xl border border-border-dark/50">
<p class="text-xs font-bold text-slate-500 uppercase tracking-widest">Qty (Boxes)</p>
<div class="flex items-center bg-slate-800/50 rounded-lg border border-slate-700/50 overflow-hidden">
<button class="w-9 h-9 flex items-center justify-center text-slate-500 border-r border-slate-700/50">
<span class="material-symbols-outlined text-lg">remove</span>
</button>
<input class="w-12 text-center border-none bg-transparent focus:ring-0 text-sm font-bold text-slate-400" readonly="" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center text-slate-500 border-l border-slate-700/50">
<span class="material-symbols-outlined text-lg">add</span>
</button>
</div>
</div>
</section>
<!-- Washers Section -->
<section class="p-5">
<h3 class="text-md font-bold text-slate-300 uppercase tracking-tight mb-4 flex items-center gap-2">
<span class="w-1.5 h-1.5 rounded-full bg-slate-500"></span>
            Flat Washers (Arandelas)
        </h3>
<div class="mb-5">
<p class="text-[10px] font-bold text-slate-500 uppercase tracking-[0.15em] mb-3">Size Selection</p>
<div class="grid grid-cols-3 gap-3">
<button class="py-3 px-4 bg-slate-800/30 border border-slate-700 text-slate-400 rounded-xl font-bold">3/8"</button>
<button class="py-3 px-4 bg-slate-800/30 border border-slate-700 text-slate-400 rounded-xl font-bold">1/2"</button>
</div>
</div>
<div class="flex items-center justify-between bg-slate-900/30 p-3 rounded-xl border border-border-dark/50">
<p class="text-xs font-bold text-slate-500 uppercase tracking-widest">Qty (Boxes)</p>
<div class="flex items-center bg-slate-800/50 rounded-lg border border-slate-700/50 overflow-hidden">
<button class="w-9 h-9 flex items-center justify-center text-slate-500 border-r border-slate-700/50">
<span class="material-symbols-outlined text-lg">remove</span>
</button>
<input class="w-12 text-center border-none bg-transparent focus:ring-0 text-sm font-bold text-slate-400" readonly="" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center text-slate-500 border-l border-slate-700/50">
<span class="material-symbols-outlined text-lg">add</span>
</button>
</div>
</div>
</section>
</main>
<div class="fixed bottom-0 left-0 right-0 z-40">
<!-- Action Buttons -->
<div class="bg-surface-dark/95 backdrop-blur-xl border-t border-border-dark p-4 pt-6 pro-shadow">
<div class="flex gap-3 mb-6">
<button class="flex-1 py-4 px-4 rounded-xl border border-slate-700 font-bold text-slate-400 hover:bg-slate-800 transition-colors uppercase tracking-widest text-xs">
                Back
            </button>
<button class="flex-[2] py-4 px-4 rounded-xl bg-primary text-white font-black shadow-xl shadow-primary/30 hover:bg-blue-500 transition-all uppercase tracking-[0.1em] flex items-center justify-center gap-2">
                Next Step
                <span class="material-symbols-outlined text-lg">arrow_forward</span>
</button>
</div>
<!-- Bottom Tab Nav -->
<nav class="flex justify-between items-center px-2 pb-2">
<a class="flex flex-col items-center gap-1.5 text-slate-600 transition-colors" href="#">
<span class="material-symbols-outlined text-[26px]">home</span>
<span class="text-[9px] font-black uppercase tracking-tighter">Home</span>
</a>
<a class="flex flex-col items-center gap-1.5 text-primary transition-colors" href="#">
<span class="material-symbols-outlined text-[26px]" style="font-variation-settings: 'FILL' 1">content_copy</span>
<span class="text-[9px] font-black uppercase tracking-tighter">Orders</span>
</a>
<a class="flex flex-col items-center gap-1.5 text-slate-600 transition-colors" href="#">
<span class="material-symbols-outlined text-[26px]">inventory_2</span>
<span class="text-[9px] font-black uppercase tracking-tighter">Inventory</span>
</a>
<a class="flex flex-col items-center gap-1.5 text-slate-600 transition-colors" href="#">
<span class="material-symbols-outlined text-[26px]">group</span>
<span class="text-[9px] font-black uppercase tracking-tighter">Clients</span>
</a>
<a class="flex flex-col items-center gap-1.5 text-slate-600 transition-colors" href="#">
<span class="material-symbols-outlined text-[26px]">more_horiz</span>
<span class="text-[9px] font-black uppercase tracking-tighter">Menu</span>
</a>
</nav>
<!-- Home Indicator Spacer -->
<div class="h-5 w-full"></div>
</div>
</div>
</body></html>

<!-- Support & Specialty Anchors Updated -->
<!DOCTYPE html>

<html class="dark" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Haley Order System - Support &amp; Specialty Anchors</title>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Public+Sans:wght@400;500;600;700;800&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "primary": "#0091FF",
                        "industry-dark": "#0B1117",
                        "industry-card": "#161B22",
                        "industry-border": "#30363D",
                        "industry-text": "#C9D1D9",
                        "industry-muted": "#8B949E",
                        "industry-accent": "#58A6FF",
                    },
                    fontFamily: {
                        "display": ["Public Sans", "sans-serif"]
                    },
                    borderRadius: {
                        "DEFAULT": "4px",
                        "lg": "8px",
                        "xl": "12px",
                        "full": "9999px"
                    },
                },
            },
        }
    </script>
<style>
        body {
            min-height: 100dvh;
            background-color: #0B1117;
        }
        .step-active {
            background: linear-gradient(90deg, #0091FF 0%, #58A6FF 100%);
        }
        .technical-border {
            border: 1px solid #30363D;
        }
        input[type="number"]::-webkit-inner-spin-button,
        input[type="number"]::-webkit-outer-spin-button {
            -webkit-appearance: none;
            margin: 0;
        }
    </style>
</head>
<body class="font-display text-industry-text selection:bg-primary/30">
<div class="relative flex min-h-screen w-full flex-col overflow-x-hidden pb-40">
<!-- Header -->
<header class="flex items-center bg-industry-dark/80 backdrop-blur-md p-4 border-b border-industry-border sticky top-0 z-30">
<button class="text-industry-text flex items-center justify-center p-2 hover:bg-industry-card rounded-full transition-colors active:scale-95">
<span class="material-symbols-outlined">arrow_back</span>
</button>
<div class="flex-1 ml-3">
<h2 class="text-lg font-extrabold leading-tight tracking-tight text-white">Support &amp; Specialty Anchors</h2>
<div class="flex items-center gap-2">
<span class="text-[10px] text-primary font-black uppercase tracking-[0.15em]">System Component 05</span>
<span class="h-1 w-1 rounded-full bg-industry-border"></span>
<span class="text-[10px] text-industry-muted font-bold uppercase tracking-wider italic">Step 5 of 5</span>
</div>
</div>
<button class="relative text-industry-text p-2 hover:bg-industry-card rounded-lg transition-colors">
<span class="material-symbols-outlined">shopping_cart</span>
<span class="absolute top-1 right-1 h-2 w-2 bg-primary rounded-full border border-industry-dark"></span>
</button>
</header>
<!-- Progress Indicator (Technical Style) -->
<div class="flex w-full items-center justify-center gap-1.5 py-4 bg-industry-dark border-b border-industry-border">
<div class="h-1 w-6 rounded-full bg-industry-border"></div>
<div class="h-1 w-6 rounded-full bg-industry-border"></div>
<div class="h-1 w-6 rounded-full bg-industry-border"></div>
<div class="h-1 w-6 rounded-full bg-industry-border"></div>
<div class="h-1 w-12 rounded-full step-active shadow-[0_0_8px_rgba(0,145,255,0.4)]"></div>
</div>
<main class="flex-1 space-y-4 pt-4 px-3">
<!-- Threaded Rod Section -->
<section class="rounded-xl bg-industry-card border border-industry-border overflow-hidden">
<h3 class="bg-industry-border/30 px-4 py-2.5 text-[11px] font-black text-industry-muted uppercase tracking-[0.2em] border-b border-industry-border flex items-center gap-2">
<span class="material-symbols-outlined text-[16px]">link</span>
                    Threaded Rod (Varilla)
                </h3>
<!-- Items list -->
<div class="divide-y divide-industry-border">
<!-- 3/8" Item -->
<div class="p-4 space-y-4">
<div class="flex justify-between items-start">
<div>
<p class="font-bold text-white text-base">3/8" Threaded Rod</p>
<p class="text-[11px] text-industry-muted font-medium italic">Standard Grade ASTM-A36</p>
</div>
<button class="bg-primary/10 hover:bg-primary/20 text-primary text-[11px] font-black px-3 py-1.5 rounded flex items-center gap-1.5 transition-all active:scale-95 border border-primary/20">
<span class="material-symbols-outlined text-[16px]">add_box</span> ADD ITEM
                            </button>
</div>
<div class="grid grid-cols-2 gap-4">
<div class="space-y-1.5">
<label class="text-[10px] font-black text-industry-muted uppercase tracking-wider ml-1">Qty (Pcs)</label>
<div class="flex items-center justify-between bg-industry-dark rounded-lg border border-industry-border p-1 group focus-within:border-primary/50 transition-colors">
<button class="w-9 h-9 flex items-center justify-center bg-industry-card hover:bg-industry-border text-primary rounded transition-colors">-</button>
<input class="w-full bg-transparent border-none text-center font-bold text-sm text-white focus:ring-0" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center bg-industry-card hover:bg-industry-border text-primary rounded transition-colors">+</button>
</div>
</div>
<div class="space-y-1.5">
<label class="text-[10px] font-black text-industry-muted uppercase tracking-wider ml-1">Qty (Boxes)</label>
<div class="flex items-center justify-between bg-industry-dark rounded-lg border border-industry-border p-1 group focus-within:border-primary/50 transition-colors">
<button class="w-9 h-9 flex items-center justify-center bg-industry-card hover:bg-industry-border text-primary rounded transition-colors">-</button>
<input class="w-full bg-transparent border-none text-center font-bold text-sm text-white focus:ring-0" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center bg-industry-card hover:bg-industry-border text-primary rounded transition-colors">+</button>
</div>
</div>
</div>
</div>
<!-- 1/2" Item -->
<div class="p-4 space-y-4">
<div class="flex justify-between items-start">
<div>
<p class="font-bold text-white text-base">1/2" Threaded Rod</p>
<p class="text-[11px] text-industry-muted font-medium italic">Heavy-Duty Structural Support</p>
</div>
<button class="bg-primary/10 hover:bg-primary/20 text-primary text-[11px] font-black px-3 py-1.5 rounded flex items-center gap-1.5 transition-all border border-primary/20">
<span class="material-symbols-outlined text-[16px]">add_box</span> ADD ITEM
                            </button>
</div>
<div class="grid grid-cols-2 gap-4">
<div class="space-y-1.5">
<label class="text-[10px] font-black text-industry-muted uppercase tracking-wider ml-1">Qty (Pcs)</label>
<div class="flex items-center justify-between bg-industry-dark rounded-lg border border-industry-border p-1">
<button class="w-9 h-9 flex items-center justify-center bg-industry-card hover:bg-industry-border text-primary rounded">-</button>
<input class="w-full bg-transparent border-none text-center font-bold text-sm text-white focus:ring-0" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center bg-industry-card hover:bg-industry-border text-primary rounded">+</button>
</div>
</div>
<div class="space-y-1.5">
<label class="text-[10px] font-black text-industry-muted uppercase tracking-wider ml-1">Qty (Boxes)</label>
<div class="flex items-center justify-between bg-industry-dark rounded-lg border border-industry-border p-1">
<button class="w-9 h-9 flex items-center justify-center bg-industry-card hover:bg-industry-border text-primary rounded">-</button>
<input class="w-full bg-transparent border-none text-center font-bold text-sm text-white focus:ring-0" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center bg-industry-card hover:bg-industry-border text-primary rounded">+</button>
</div>
</div>
</div>
</div>
</div>
</section>
<!-- Unistrut Section -->
<section class="rounded-xl bg-industry-card border border-industry-border overflow-hidden">
<h3 class="bg-industry-border/30 px-4 py-2.5 text-[11px] font-black text-industry-muted uppercase tracking-[0.2em] border-b border-industry-border flex items-center gap-2">
<span class="material-symbols-outlined text-[16px]">view_column</span>
                    Unistrut (Canal)
                </h3>
<div class="p-4 space-y-4">
<div class="flex gap-2 p-1 bg-industry-dark rounded-xl border border-industry-border">
<button class="flex-1 py-2.5 rounded-lg bg-primary text-white text-[11px] font-black uppercase tracking-wider shadow-lg shadow-primary/20">U Channel</button>
<button class="flex-1 py-2.5 rounded-lg text-industry-muted text-[11px] font-black uppercase tracking-wider hover:text-white transition-colors">Slotted</button>
</div>
<div class="grid grid-cols-2 gap-4">
<div class="space-y-1.5">
<label class="text-[10px] font-black text-industry-muted uppercase ml-1">Qty (Pcs)</label>
<div class="flex items-center bg-industry-dark rounded-lg border border-industry-border p-1">
<button class="w-9 h-9 flex items-center justify-center bg-industry-card text-primary rounded">-</button>
<input class="w-full bg-transparent border-none text-center font-bold text-sm text-white focus:ring-0" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center bg-industry-card text-primary rounded">+</button>
</div>
</div>
<div class="space-y-1.5">
<label class="text-[10px] font-black text-industry-muted uppercase ml-1">Qty (Boxes)</label>
<div class="flex items-center bg-industry-dark rounded-lg border border-industry-border p-1">
<button class="w-9 h-9 flex items-center justify-center bg-industry-card text-primary rounded">-</button>
<input class="w-full bg-transparent border-none text-center font-bold text-sm text-white focus:ring-0" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center bg-industry-card text-primary rounded">+</button>
</div>
</div>
</div>
<button class="w-full py-3 bg-industry-dark border border-primary/30 text-primary hover:bg-primary/5 rounded-lg font-black text-xs uppercase tracking-widest transition-all">
                        Commit Unistrut Configuration
                    </button>
</div>
</section>
<!-- Hanger Strips Section -->
<section class="rounded-xl bg-industry-card border border-industry-border overflow-hidden">
<h3 class="bg-industry-border/30 px-4 py-2.5 text-[11px] font-black text-industry-muted uppercase tracking-[0.2em] border-b border-industry-border flex items-center gap-2">
<span class="material-symbols-outlined text-[16px]">straighten</span>
                    Hanger Strips (Fleje)
                </h3>
<div class="p-4">
<div class="flex flex-col gap-3">
<div class="flex justify-between items-center px-1">
<p class="text-[10px] font-black text-industry-muted uppercase tracking-wider">Include Hanger Strips?</p>
<span class="material-symbols-outlined text-[18px] text-industry-border">help</span>
</div>
<div class="flex gap-2 p-1 bg-industry-dark rounded-xl border border-industry-border">
<button class="flex-1 py-2.5 rounded-lg text-industry-muted text-[11px] font-black uppercase tracking-wider hover:bg-industry-border transition-all">No</button>
<button class="flex-1 py-2.5 rounded-lg bg-primary text-white text-[11px] font-black uppercase tracking-wider shadow-lg shadow-primary/20">Yes</button>
</div>
</div>
</div>
</section>
<!-- Sammy's Rod Anchors -->
<section class="rounded-xl bg-industry-card border border-industry-border overflow-hidden">
<h3 class="bg-industry-border/30 px-4 py-2.5 text-[11px] font-black text-industry-muted uppercase tracking-[0.2em] border-b border-industry-border flex items-center gap-2">
<span class="material-symbols-outlined text-[16px]">bolt</span>
                    Sammy's Rod Anchors
                </h3>
<div class="divide-y divide-industry-border">
<!-- Concrete Anchors -->
<div class="p-4 space-y-4">
<p class="font-bold text-white text-sm flex items-center gap-2">
<span class="h-2 w-2 rounded-full bg-primary/40"></span>
                            Concrete Anchors
                        </p>
<div class="flex gap-2">
<button class="flex-1 py-2 rounded-lg bg-primary text-white text-[11px] font-black">3/8"</button>
<button class="flex-1 py-2 rounded-lg bg-industry-dark border border-industry-border text-industry-muted text-[11px] font-black">1/2"</button>
</div>
<div class="space-y-1.5">
<label class="text-[10px] font-black text-industry-muted uppercase tracking-wider ml-1">Qty (Boxes)</label>
<div class="flex items-center justify-between bg-industry-dark rounded-lg border border-industry-border p-1">
<button class="w-9 h-9 flex items-center justify-center bg-industry-card text-primary rounded">-</button>
<input class="w-full bg-transparent border-none text-center font-bold text-sm text-white focus:ring-0" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center bg-industry-card text-primary rounded">+</button>
</div>
</div>
<button class="w-full py-2.5 bg-industry-border/50 text-industry-text rounded-lg font-black text-[10px] uppercase tracking-[0.15em] border border-industry-border/50 hover:bg-industry-border transition-colors">
                            Add Concrete Sammy's
                        </button>
</div>
<!-- Wood Anchors -->
<div class="p-4 space-y-4">
<p class="font-bold text-white text-sm flex items-center gap-2">
<span class="h-2 w-2 rounded-full bg-amber-500/40"></span>
                            Wood Anchors
                        </p>
<div class="grid grid-cols-2 gap-2">
<button class="py-2 rounded-lg bg-primary text-white text-[11px] font-black">3/8"</button>
<button class="py-2 rounded-lg bg-industry-dark border border-industry-border text-industry-muted text-[11px] font-black">1/2"</button>
</div>
<div class="space-y-1.5">
<label class="text-[10px] font-black text-industry-muted uppercase tracking-wider ml-1">Qty (Boxes)</label>
<div class="flex items-center justify-between bg-industry-dark rounded-lg border border-industry-border p-1">
<button class="w-9 h-9 flex items-center justify-center bg-industry-card text-primary rounded">-</button>
<input class="w-full bg-transparent border-none text-center font-bold text-sm text-white focus:ring-0" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center bg-industry-card text-primary rounded">+</button>
</div>
</div>
<button class="w-full py-2.5 bg-industry-border/50 text-industry-text rounded-lg font-black text-[10px] uppercase tracking-[0.15em] border border-industry-border/50 hover:bg-industry-border transition-colors">
                            Add Wood Sammy's
                        </button>
</div>
</div>
</section>
<!-- Drop-in / Strong-Tie Section -->
<section class="rounded-xl bg-industry-card border border-industry-border overflow-hidden">
<h3 class="bg-industry-border/30 px-4 py-2.5 text-[11px] font-black text-industry-muted uppercase tracking-[0.2em] border-b border-industry-border flex items-center gap-2">
<span class="material-symbols-outlined text-[16px]">pin_drop</span>
                    Drop-in / Strong-Tie
                </h3>
<div class="p-4 space-y-4">
<div class="flex items-center justify-between px-1">
<p class="text-[10px] font-black text-industry-muted uppercase tracking-widest">Select Size</p>
<span class="px-2 py-0.5 bg-emerald-500/10 text-emerald-500 text-[9px] font-black rounded border border-emerald-500/20 uppercase">Available</span>
</div>
<div class="flex gap-2">
<button class="flex-1 py-2.5 rounded-lg bg-primary text-white text-[11px] font-black uppercase">3/8"</button>
<button class="flex-1 py-2.5 rounded-lg bg-industry-dark border border-industry-border text-industry-muted text-[11px] font-black uppercase">1/2"</button>
</div>
<div class="space-y-1.5">
<label class="text-[10px] font-black text-industry-muted uppercase tracking-wider ml-1">Qty (Boxes)</label>
<div class="flex items-center justify-between bg-industry-dark rounded-lg border border-industry-border p-1">
<button class="w-9 h-9 flex items-center justify-center bg-industry-card text-primary rounded">-</button>
<input class="w-full bg-transparent border-none text-center font-bold text-sm text-white focus:ring-0" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center bg-industry-card text-primary rounded">+</button>
</div>
</div>
<button class="w-full py-3 border-2 border-primary/40 text-primary rounded-lg font-black text-xs uppercase tracking-widest hover:bg-primary/5 transition-all">
                        Stage Drop-in Order
                    </button>
</div>
</section>
<!-- Beam Clamps Section -->
<section class="rounded-xl bg-industry-card border border-industry-border overflow-hidden">
<h3 class="bg-industry-border/30 px-4 py-2.5 text-[11px] font-black text-industry-muted uppercase tracking-[0.2em] border-b border-industry-border flex items-center gap-2">
<span class="material-symbols-outlined text-[16px]">hardware</span>
                    Beam Clamps (Grapas de Viga)
                </h3>
<div class="p-4 space-y-4">
<div class="space-y-1.5">
<p class="text-[10px] font-black text-industry-muted uppercase tracking-widest ml-1">Clamp Specification</p>
<div class="flex gap-2">
<button class="flex-1 py-2.5 rounded-lg bg-primary text-white text-[11px] font-black uppercase">3/8"</button>
<button class="flex-1 py-2.5 rounded-lg bg-industry-dark border border-industry-border text-industry-muted text-[11px] font-black uppercase">1/2"</button>
</div>
</div>
<div class="space-y-1.5">
<label class="text-[10px] font-black text-industry-muted uppercase tracking-wider ml-1">Qty (Boxes)</label>
<div class="flex items-center justify-between bg-industry-dark rounded-lg border border-industry-border p-1">
<button class="w-9 h-9 flex items-center justify-center bg-industry-card text-primary rounded">-</button>
<input class="w-full bg-transparent border-none text-center font-bold text-sm text-white focus:ring-0" type="number" value="0"/>
<button class="w-9 h-9 flex items-center justify-center bg-industry-card text-primary rounded">+</button>
</div>
</div>
<button class="w-full py-3 bg-primary/10 text-primary border border-primary/20 rounded-lg font-black text-xs uppercase tracking-[0.2em] hover:bg-primary/20 transition-all">
                        Add Beam Clamps
                    </button>
</div>
</section>
<!-- Hex Concrete Screws Section -->
<section class="rounded-xl bg-industry-card border border-industry-border overflow-hidden">
<h3 class="bg-industry-border/30 px-4 py-2.5 text-[11px] font-black text-industry-muted uppercase tracking-[0.2em] border-b border-industry-border flex items-center gap-2">
<span class="material-symbols-outlined text-[16px]">architecture</span>
                    Hex Concrete Screws
                </h3>
<div class="p-4 space-y-5">
<div class="space-y-2">
<p class="text-[10px] font-black text-industry-muted uppercase tracking-widest ml-1">Size Selection</p>
<div class="w-1/2">
<button class="w-full py-2.5 rounded-lg bg-primary text-white text-[11px] font-black uppercase shadow-lg shadow-primary/10">1/4"</button>
</div>
</div>
<div class="space-y-2">
<div class="flex items-center justify-between px-1">
<label class="text-[10px] font-black text-industry-muted uppercase tracking-wider">Technical Specifications</label>
<span class="text-[9px] text-industry-muted italic font-bold">(Opcional)</span>
</div>
<textarea class="w-full bg-industry-dark border-industry-border rounded-lg text-sm text-white p-3 focus:ring-primary/50 focus:border-primary/50 placeholder:text-industry-border/80 resize-none h-20" placeholder="Specify custom length or grade requirements..."></textarea>
</div>
<button class="w-full py-3 border-2 border-primary/40 text-primary rounded-lg font-black text-xs uppercase tracking-widest hover:bg-primary/5 transition-all">
                        Submit Hex Screw Spec
                    </button>
</div>
</section>
</main>
<!-- Fixed Bottom Navigation (Modern Dark Style) -->
<footer class="fixed bottom-0 left-0 right-0 bg-industry-dark/95 backdrop-blur-xl border-t border-industry-border px-4 pt-4 pb-2 z-40">
<div class="flex gap-4 mb-4">
<button class="flex-1 flex items-center justify-center gap-2 py-4 px-4 border border-industry-border rounded-xl font-black text-[11px] uppercase tracking-[0.15em] text-industry-text hover:bg-industry-card active:scale-95 transition-all">
<span class="material-symbols-outlined text-[20px]">chevron_left</span>
                    Back
                </button>
<button class="flex-[2] flex items-center justify-center gap-3 py-4 px-4 bg-primary text-white rounded-xl font-black text-[11px] uppercase tracking-[0.2em] shadow-[0_8px_20px_-4px_rgba(0,145,255,0.4)] active:scale-95 transition-all group">
                    Verify &amp; Finish
                    <span class="material-symbols-outlined text-[20px] group-hover:translate-x-1 transition-transform">check_circle</span>
</button>
</div>
<!-- Bottom Tab Bar -->
<nav class="flex justify-around items-center px-2">
<a class="flex flex-col items-center gap-1 text-industry-muted py-1" href="#">
<span class="material-symbols-outlined">home</span>
<span class="text-[9px] font-black uppercase tracking-wider">Home</span>
</a>
<a class="flex flex-col items-center gap-1 text-primary py-1 relative" href="#">
<span class="material-symbols-outlined" style="font-variation-settings: 'FILL' 1">inventory_2</span>
<span class="text-[9px] font-black uppercase tracking-wider">Ordering</span>
<span class="absolute -top-1 right-2 h-1 w-1 bg-primary rounded-full"></span>
</a>
<a class="flex flex-col items-center gap-1 text-industry-muted py-1" href="#">
<span class="material-symbols-outlined">analytics</span>
<span class="text-[9px] font-black uppercase tracking-wider">Stats</span>
</a>
<a class="flex flex-col items-center gap-1 text-industry-muted py-1" href="#">
<span class="material-symbols-outlined">support_agent</span>
<span class="text-[9px] font-black uppercase tracking-wider">Support</span>
</a>
<a class="flex flex-col items-center gap-1 text-industry-muted py-1" href="#">
<span class="material-symbols-outlined">person</span>
<span class="text-[9px] font-black uppercase tracking-wider">Account</span>
</a>
</nav>
</footer>
</div>
</body></html>

<!-- Logistics & Approval -->
<!DOCTYPE html>

<html class="dark" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Haley Order System - Logistics &amp; Approval</title>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@600;700&amp;family=JetBrains+Mono:wght@400;500&amp;family=Inter:wght@400;500;600&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "primary": "#fbbf24", // Industrial Yellow
                        "background-dark": "#0f1115",
                        "panel-dark": "#1a1d23",
                        "accent-blue": "#0ea5e9"
                    },
                    fontFamily: {
                        "display": ["Barlow Condensed", "sans-serif"],
                        "mono": ["JetBrains Mono", "monospace"],
                        "sans": ["Inter", "sans-serif"]
                    },
                    borderRadius: {
                        "DEFAULT": "0px",
                        "lg": "2px",
                        "xl": "4px",
                        "full": "9999px"
                    },
                },
            },
        }
    </script>
<style>
        body {
            min-height: max(884px, 100dvh);
            text-rendering: optimizeLegibility;
        }
        .scanline {
            background: linear-gradient(to bottom, transparent 50%, rgba(251, 191, 36, 0.02) 50%);
            background-size: 100% 4px;
        }
    </style>
</head>
<body class="bg-background-dark font-sans text-slate-300 min-h-screen flex flex-col scanline">
<!-- Header Section -->
<header class="sticky top-0 z-10 bg-panel-dark/90 backdrop-blur-md border-b-2 border-primary/20 px-4 py-4">
<div class="flex items-center justify-between">
<div class="flex items-center gap-3">
<button class="text-primary hover:bg-primary/10 p-2 border border-primary/30">
<span class="material-symbols-outlined block">arrow_back</span>
</button>
<div>
<h1 class="text-2xl font-display font-bold tracking-tight text-white leading-none uppercase">Logistics &amp; Approval</h1>
<p class="text-[10px] font-mono font-medium text-primary/80 uppercase tracking-[0.2em] mt-1">System Module: ORD-LOG-06</p>
</div>
</div>
<div class="text-right">
<span class="text-[10px] font-mono font-semibold text-slate-500 uppercase">Phase 06/06</span>
<div class="flex gap-1 mt-1 justify-end">
<div class="h-1 w-3 bg-primary/20"></div>
<div class="h-1 w-3 bg-primary/20"></div>
<div class="h-1 w-3 bg-primary/20"></div>
<div class="h-1 w-3 bg-primary/20"></div>
<div class="h-1 w-3 bg-primary/20"></div>
<div class="h-1 w-3 bg-primary shadow-[0_0_8px_rgba(251,191,36,0.5)]"></div>
</div>
</div>
</div>
</header>
<main class="flex-1 overflow-y-auto pb-32">
<!-- Section 1: Priority -->
<section class="p-4 border-b border-white/5 bg-panel-dark/30">
<h3 class="text-xs font-mono font-bold uppercase tracking-widest text-slate-500 mb-4 flex items-center gap-2">
<span class="w-1.5 h-1.5 bg-primary rounded-full"></span>
            Priority Level
        </h3>
<div class="flex bg-black/40 p-1 border border-white/10">
<label class="flex-1 flex items-center justify-center py-2.5 cursor-pointer transition-all has-[:checked]:bg-primary has-[:checked]:text-black text-slate-500 font-display font-bold text-lg uppercase tracking-wider">
<input class="hidden" name="priority" type="radio" value="urgent"/>
<span>Urgent</span>
</label>
<label class="flex-1 flex items-center justify-center py-2.5 cursor-pointer transition-all has-[:checked]:bg-primary has-[:checked]:text-black text-slate-500 font-display font-bold text-lg uppercase tracking-wider">
<input checked="" class="hidden" name="priority" type="radio" value="standard"/>
<span>Standard</span>
</label>
</div>
</section>
<!-- Section 2: Delivery Method -->
<section class="p-4 border-b border-white/5">
<h3 class="text-xs font-mono font-bold uppercase tracking-widest text-slate-500 mb-4 flex items-center gap-2">
<span class="w-1.5 h-1.5 bg-primary rounded-full"></span>
            Dispatch Method
        </h3>
<div class="grid grid-cols-2 gap-3">
<label class="relative flex flex-col items-center gap-2 p-4 border border-white/10 bg-panel-dark/50 cursor-pointer has-[:checked]:border-primary has-[:checked]:bg-primary/5 group transition-colors">
<input checked="" class="hidden" name="delivery" type="radio" value="delivery"/>
<span class="material-symbols-outlined text-3xl text-slate-600 group-has-[:checked]:text-primary group-has-[:checked]:drop-shadow-[0_0_5px_rgba(251,191,36,0.3)]">local_shipping</span>
<span class="font-display font-bold text-sm uppercase tracking-wide">Delivery</span>
<div class="absolute top-0 right-0 w-2 h-2 border-t border-r border-white/20 group-has-[:checked]:border-primary"></div>
</label>
<label class="relative flex flex-col items-center gap-2 p-4 border border-white/10 bg-panel-dark/50 cursor-pointer has-[:checked]:border-primary has-[:checked]:bg-primary/5 group transition-colors">
<input class="hidden" name="delivery" type="radio" value="pickup"/>
<span class="material-symbols-outlined text-3xl text-slate-600 group-has-[:checked]:text-primary group-has-[:checked]:drop-shadow-[0_0_5px_rgba(251,191,36,0.3)]">storefront</span>
<span class="font-display font-bold text-sm uppercase tracking-wide">Shop Pickup</span>
<div class="absolute top-0 right-0 w-2 h-2 border-t border-r border-white/20 group-has-[:checked]:border-primary"></div>
</label>
</div>
</section>
<!-- Section 3: Personnel -->
<section class="p-4 border-b border-white/5 space-y-4 bg-panel-dark/30">
<h3 class="text-xs font-mono font-bold uppercase tracking-widest text-slate-500 mb-2 flex items-center gap-2">
<span class="w-1.5 h-1.5 bg-primary rounded-full"></span>
            Authorization
        </h3>
<div class="space-y-4">
<div class="flex flex-col gap-1.5">
<label class="text-[10px] font-mono font-semibold text-slate-500 uppercase px-1">Field Tech / Ordered by</label>
<div class="relative">
<span class="material-symbols-outlined absolute left-3 top-1/2 -translate-y-1/2 text-primary/40 text-sm">person</span>
<input class="w-full bg-black/40 border border-white/10 rounded-none py-3 pl-10 pr-4 text-sm font-mono focus:border-primary/50 focus:ring-0 outline-none text-white placeholder:text-slate-700" placeholder="ID_NUMBER or NAME" type="text"/>
</div>
</div>
<div class="flex flex-col gap-1.5">
<label class="text-[10px] font-mono font-semibold text-slate-500 uppercase px-1">Supervisor / Approved by</label>
<div class="relative">
<span class="material-symbols-outlined absolute left-3 top-1/2 -translate-y-1/2 text-primary/40 text-sm">verified_user</span>
<input class="w-full bg-black/40 border border-white/10 rounded-none py-3 pl-10 pr-4 text-sm font-mono focus:border-primary/50 focus:ring-0 outline-none text-white placeholder:text-slate-700" placeholder="AUTH_KEY or NAME" type="text"/>
</div>
</div>
</div>
</section>
<!-- Section 4: Final Confirmation / Signature -->
<section class="p-4">
<h3 class="text-xs font-mono font-bold uppercase tracking-widest text-slate-500 mb-4 flex items-center gap-2">
<span class="w-1.5 h-1.5 bg-primary rounded-full"></span>
            Final Verification
        </h3>
<div class="w-full aspect-[16/9] bg-black/60 border border-white/10 relative overflow-hidden group">
<div class="absolute inset-0 opacity-10 pointer-events-none" style="background-image: radial-gradient(circle at 2px 2px, #fff 1px, transparent 0); background-size: 20px 20px;"></div>
<div class="flex flex-col items-center justify-center h-full text-slate-500 gap-2 relative z-10">
<span class="material-symbols-outlined text-4xl text-primary/20">edit_square</span>
<p class="text-[10px] font-mono uppercase tracking-tighter">Awaiting Digital Signature...</p>
<p class="text-[10px] opacity-40 text-center px-8 uppercase font-mono leading-tight">I attest that all line items match specified HVAC maintenance protocols</p>
</div>
<!-- Decorative corner brackets -->
<div class="absolute top-2 left-2 w-4 h-4 border-t border-l border-primary/40"></div>
<div class="absolute top-2 right-2 w-4 h-4 border-t border-r border-primary/40"></div>
<div class="absolute bottom-2 left-2 w-4 h-4 border-b border-l border-primary/40"></div>
<div class="absolute bottom-2 right-2 w-4 h-4 border-b border-r border-primary/40"></div>
</div>
</section>
<!-- Action Button -->
<div class="px-4 py-6">
<button class="w-full bg-primary text-black font-display font-bold py-4 shadow-[0_0_20px_rgba(251,191,36,0.15)] hover:bg-white active:scale-[0.99] transition-all flex items-center justify-center gap-3 border-b-4 border-black/20">
<span class="text-xl tracking-tighter uppercase">Transmit Order Data</span>
<span class="material-symbols-outlined scale-110">sensors</span>
</button>
<p class="text-[9px] font-mono text-center mt-3 text-slate-600 uppercase tracking-widest">Encrypted Transmission Ready</p>
</div>
</main>
<!-- Bottom Navigation Bar -->
<nav class="fixed bottom-0 left-0 right-0 bg-panel-dark border-t border-white/10 px-2 pb-6 pt-2">
<div class="flex items-center justify-around max-w-lg mx-auto">
<a class="flex flex-col items-center gap-1 p-2 text-slate-600" href="#">
<span class="material-symbols-outlined text-xl">home</span>
<span class="text-[9px] font-mono font-bold uppercase tracking-tighter">Home</span>
</a>
<a class="flex flex-col items-center gap-1 p-2 text-slate-600" href="#">
<span class="material-symbols-outlined text-xl">assignment</span>
<span class="text-[9px] font-mono font-bold uppercase tracking-tighter">Orders</span>
</a>
<a class="flex flex-col items-center gap-1 p-2 text-slate-600" href="#">
<span class="material-symbols-outlined text-xl">inventory_2</span>
<span class="text-[9px] font-mono font-bold uppercase tracking-tighter">Inventory</span>
</a>
<a class="flex flex-col items-center gap-1 p-2 text-primary" href="#">
<span class="material-symbols-outlined text-xl" style="font-variation-settings: 'FILL' 1">local_shipping</span>
<span class="text-[9px] font-mono font-bold uppercase tracking-tighter">Logistics</span>
</a>
<a class="flex flex-col items-center gap-1 p-2 text-slate-600" href="#">
<span class="material-symbols-outlined text-xl">settings</span>
<span class="text-[9px] font-mono font-bold uppercase tracking-tighter">Setup</span>
</a>
</div>
</nav>
</body></html>

<!-- Order Confirmation with Print Option Adjusted -->
<!DOCTYPE html>

<html lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Public+Sans:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "primary": "#00E5FF",
                        "industrial-gray": "#1A1C1E",
                        "industrial-dark": "#0D0E10",
                        "hvac-accent": "#FFB74D",
                        "background-dark": "#0D0E10",
                    },
                    fontFamily: {
                        "display": ["Public Sans"],
                        "mono": ["JetBrains Mono"]
                    },
                    borderRadius: {"DEFAULT": "0px", "lg": "2px", "xl": "4px", "full": "9999px"},
                },
            },
        }
    </script>
<title>Order Confirmation - Haley HVAC PRO</title>
<style>
        body {
            min-height: max(884px, 100dvh);
            background-color: #0D0E10;
        }
        .scanline {
            width: 100%;
            height: 100px;
            z-index: 5;
            background: linear-gradient(0deg, rgba(0, 229, 255, 0) 0%, rgba(0, 229, 255, 0.05) 50%, rgba(0, 229, 255, 0) 100%);
            opacity: 0.1;
            position: absolute;
            bottom: 100%;
            animation: scanline 6s linear infinite;
        }
        @keyframes scanline {
            0% { bottom: 100%; }
            100% { bottom: -100px; }
        }
    </style>
</head>
<body class="dark bg-industrial-dark font-display text-slate-100 min-h-screen selection:bg-primary selection:text-black overflow-x-hidden">
<div class="relative flex h-auto min-h-screen w-full flex-col bg-industrial-dark group/design-root overflow-x-hidden">
<!-- Technical Overlay -->
<div class="fixed inset-0 pointer-events-none opacity-20 bg-[url('https://www.transparenttextures.com/patterns/carbon-fibre.png')]"></div>
<div class="scanline"></div>
<!-- Top Navigation -->
<div class="flex items-center bg-industrial-gray/80 backdrop-blur-md p-4 pb-4 justify-between border-b border-primary/20 relative z-10">
<div class="text-primary flex size-10 shrink-0 items-center justify-center cursor-pointer border border-primary/20 hover:bg-primary/10 transition-colors" data-icon="ArrowLeft">
<span class="material-symbols-outlined text-xl">arrow_back</span>
</div>
<div class="flex flex-col items-center flex-1">
<h2 class="text-slate-100 text-sm font-bold leading-tight tracking-[0.2em] uppercase">Haley HVAC PRO</h2>
<span class="text-[10px] text-primary/60 font-mono">SYSTEM_STATUS: SECURE_LINK</span>
</div>
<div class="size-10"></div>
</div>
<!-- Main Content Area -->
<div class="flex flex-col px-6 py-10 flex-grow items-center justify-center relative z-10">
<div class="flex flex-col items-center gap-10 w-full max-w-md">
<!-- Success Visual: Industrial Gauge Style -->
<div class="relative flex items-center justify-center">
<div class="absolute w-40 h-40 border-2 border-primary/10 rounded-full"></div>
<div class="absolute w-36 h-36 border border-primary/30 rounded-full animate-[spin_10s_linear_infinite] border-t-transparent"></div>
<div class="relative flex items-center justify-center w-28 h-28 bg-industrial-gray border-2 border-primary text-primary rounded-full shadow-[0_0_30px_rgba(0,229,255,0.2)]">
<span class="material-symbols-outlined text-5xl">task_alt</span>
</div>
<!-- Status Corner Indicators -->
<div class="absolute -top-2 -right-2 bg-primary text-black text-[10px] font-bold px-2 py-0.5 uppercase tracking-tighter">Verified</div>
</div>
<!-- Headline & Technical Message -->
<div class="flex flex-col items-center gap-4 text-center">
<div class="flex items-center gap-2">
<div class="h-[1px] w-8 bg-primary/30"></div>
<h1 class="text-primary text-4xl font-black leading-tight tracking-tighter uppercase font-mono italic">SUCCESS</h1>
<div class="h-[1px] w-8 bg-primary/30"></div>
</div>
<p class="text-slate-100 text-lg font-bold leading-tight tracking-wide uppercase">Transmission Received</p>
<p class="text-slate-400 text-sm font-normal leading-relaxed max-w-[280px] font-mono">
                    PROCUREMENT_DATA_SPOOLING...<br/>
                    Order logged to centralized database. Technical review in progress.
                </p>
</div>
<!-- Order ID Badge: Industrial Plate Style -->
<div class="bg-primary/5 border-l-4 border-primary px-6 py-6 w-full relative overflow-hidden">
<div class="absolute top-0 right-0 p-1 opacity-20">
<span class="material-symbols-outlined text-4xl">qr_code_2</span>
</div>
<span class="text-primary/60 text-[10px] font-bold uppercase tracking-[0.3em] block mb-2 font-mono">Reference Identification</span>
<div class="flex items-baseline gap-2">
<h3 class="text-white tracking-tighter text-4xl font-black leading-none font-mono">#9822</h3>
<span class="text-primary text-xs font-mono animate-pulse">| ONLINE</span>
</div>
</div>
<!-- Details Panel -->
<div class="w-full bg-industrial-gray border border-white/10 p-5 relative">
<div class="absolute top-0 left-0 w-2 h-2 border-t border-l border-primary"></div>
<div class="absolute top-0 right-0 w-2 h-2 border-t border-r border-primary"></div>
<div class="absolute bottom-0 left-0 w-2 h-2 border-b border-l border-primary"></div>
<div class="absolute bottom-0 right-0 w-2 h-2 border-b border-r border-primary"></div>
<div class="flex justify-between items-center text-xs mb-4 font-mono">
<span class="text-slate-500 uppercase tracking-widest">Process State</span>
<span class="text-primary font-bold flex items-center gap-2 bg-primary/10 px-2 py-1">
<span class="relative flex h-2 w-2">
<span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-primary opacity-75"></span>
<span class="relative inline-flex rounded-full h-2 w-2 bg-primary"></span>
</span>
                        ACTIVE_QUEUE
                    </span>
</div>
<div class="flex justify-between items-center text-xs font-mono">
<span class="text-slate-500 uppercase tracking-widest">System Time</span>
<span class="text-slate-200 font-medium">2023.10.24 // 14:22:00</span>
</div>
</div>
</div>
</div>
<!-- Footer Action: Control Panel Group -->
<div class="p-6 bg-industrial-dark border-t border-white/10 relative z-20">
<div class="max-w-md mx-auto flex flex-col gap-4">
<!-- Primary Command -->
<button class="flex w-full cursor-pointer items-center justify-center overflow-hidden h-14 bg-primary text-black text-base font-black leading-normal tracking-[0.1em] uppercase shadow-[0_0_20px_rgba(0,229,255,0.15)] hover:bg-white transition-all active:scale-[0.98] group">
<span class="truncate">Return to Command Center</span>
<span class="material-symbols-outlined ml-2 group-hover:translate-x-1 transition-transform">terminal</span>
</button>
<!-- Technical Control Panel Grid -->
<div class="bg-industrial-gray border border-white/5 p-1">
<div class="grid grid-cols-2 gap-1">
<button class="flex items-center justify-start px-4 h-11 bg-industrial-dark/50 border border-white/5 text-slate-400 text-[11px] font-bold uppercase tracking-wider hover:text-primary hover:border-primary/50 transition-all gap-3 font-mono">
<span class="material-symbols-outlined text-lg">database</span>
<span>Details</span>
</button>
<button class="flex items-center justify-start px-4 h-11 bg-industrial-dark/50 border border-white/5 text-slate-400 text-[11px] font-bold uppercase tracking-wider hover:text-primary hover:border-primary/50 transition-all gap-3 font-mono">
<span class="material-symbols-outlined text-lg">description</span>
<span>View PDF</span>
</button>
<button class="flex items-center justify-start px-4 h-11 bg-industrial-dark/50 border border-white/5 text-slate-400 text-[11px] font-bold uppercase tracking-wider hover:text-primary hover:border-primary/50 transition-all gap-3 font-mono">
<span class="material-symbols-outlined text-lg">install_desktop</span>
<span>Export</span>
</button>
<button class="flex items-center justify-start px-4 h-11 bg-industrial-dark/50 border border-white/5 text-slate-400 text-[11px] font-bold uppercase tracking-wider hover:text-primary hover:border-primary/50 transition-all gap-3 font-mono">
<span class="material-symbols-outlined text-lg">alternate_email</span>
<span>Dispatch</span>
</button>
<button class="flex items-center justify-center col-span-2 h-11 bg-industrial-dark/50 border border-white/5 text-slate-400 text-[11px] font-bold uppercase tracking-wider hover:text-primary hover:border-primary/50 transition-all gap-3 font-mono">
<span class="material-symbols-outlined text-lg">print</span>
<span>Hard Copy (Print)</span>
</button>
</div>
</div>
</div>
</div>
<!-- Decorative bottom spacers -->
<div class="h-6 bg-industrial-dark border-t border-white/5"></div>
</div>
</body></html>

<!-- Order History with Item Search -->
<!DOCTYPE html>

<html class="dark" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Public+Sans:wght@400;500;600;700&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "primary": "#1388e7",
                        "hvac-orange": "#f59e0b",
                        "hvac-cyan": "#06b6d4",
                        "hvac-green": "#10b981",
                        "background-dark": "#0b1218",
                        "panel-dark": "#16202a",
                        "border-industrial": "#2d3a4b",
                    },
                    fontFamily: {
                        "display": ["Public Sans"]
                    },
                    borderRadius: {"DEFAULT": "0px", "lg": "2px", "xl": "4px", "full": "9999px"},
                },
            },
        }
    </script>
<title>Haley Order System - Order History</title>
<style>
        body {
            min-height: max(884px, 100dvh);
            background-color: #0b1218;
        }
        .field-log-entry::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            bottom: 0;
            width: 3px;
        }
        .status-pending::before { background-color: #f59e0b; }
        .status-shipped::before { background-color: #06b6d4; }
        .status-delivered::before { background-color: #10b981; }
        
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
    </style>
</head>
<body class="dark bg-background-dark font-display text-slate-100 min-h-screen flex flex-col">
<!-- Header -->
<header class="sticky top-0 z-20 bg-panel-dark/95 backdrop-blur-md border-b border-border-industrial px-4 py-4 flex items-center gap-4">
<button class="flex items-center justify-center p-2 hover:bg-slate-800 rounded transition-colors">
<span class="material-symbols-outlined text-slate-400">arrow_back</span>
</button>
<div>
<h1 class="text-lg font-bold tracking-tight uppercase">Order History</h1>
<p class="text-[10px] text-slate-500 font-bold tracking-[0.2em]">FIELD OPERATIONS LOG</p>
</div>
</header>
<main class="flex-1 overflow-y-auto">
<!-- Industrial Search and Filter Section -->
<div class="p-4 space-y-3 bg-panel-dark border-b border-border-industrial shadow-lg">
<div class="relative group">
<span class="material-symbols-outlined absolute left-3 top-1/2 -translate-y-1/2 text-slate-500 group-focus-within:text-primary transition-colors">search</span>
<input class="w-full pl-10 pr-12 py-3 bg-background-dark border border-border-industrial rounded-lg focus:ring-1 focus:ring-primary focus:border-primary outline-none text-sm transition-all placeholder:text-slate-600" placeholder="Search Project, ID, or Items..." type="text"/>
<button class="absolute right-3 top-1/2 -translate-y-1/2 p-1 text-slate-500 hover:text-primary transition-colors">
<span class="material-symbols-outlined text-xl">tune</span>
</button>
</div>
<div class="flex gap-2 overflow-x-auto pb-1 no-scrollbar">
<button class="flex items-center gap-2 px-3 py-2 bg-background-dark border border-border-industrial rounded text-[11px] font-bold uppercase tracking-wider text-slate-400 hover:text-white transition-all whitespace-nowrap">
<span class="material-symbols-outlined text-sm text-primary">calendar_today</span>
                Date Range
                <span class="material-symbols-outlined text-sm">expand_more</span>
</button>
<button class="flex items-center gap-2 px-3 py-2 bg-background-dark border border-border-industrial rounded text-[11px] font-bold uppercase tracking-wider text-slate-400 hover:text-white transition-all whitespace-nowrap">
<span class="material-symbols-outlined text-sm">filter_list</span>
                Status
                <span class="material-symbols-outlined text-sm">expand_more</span>
</button>
<button class="flex items-center gap-2 px-3 py-2 bg-background-dark border border-border-industrial rounded text-[11px] font-bold uppercase tracking-wider text-slate-400 hover:text-white transition-all whitespace-nowrap">
<span class="material-symbols-outlined text-sm">layers</span>
                Project
                <span class="material-symbols-outlined text-sm">expand_more</span>
</button>
</div>
</div>
<!-- Field Log List -->
<div class="px-3 py-4 space-y-3 pb-24">
<!-- Order Card 1: Pending -->
<div class="field-log-entry status-pending relative bg-panel-dark border border-border-industrial p-4 overflow-hidden">
<div class="flex justify-between items-start">
<div class="space-y-0.5">
<div class="flex items-center gap-2">
<span class="text-[10px] font-black text-slate-500 tracking-tighter">ID: #9822</span>
<div class="h-px w-4 bg-border-industrial"></div>
<span class="text-[10px] font-bold text-hvac-orange uppercase tracking-widest">Pending</span>
</div>
<h3 class="text-sm font-bold text-slate-100 uppercase leading-tight">Skyline Apartments Phase II</h3>
<div class="flex items-center gap-1.5 text-[11px] text-slate-500 font-medium">
<span class="material-symbols-outlined text-xs">schedule</span>
                        Oct 24, 2023 · 14:30
                    </div>
</div>
<div class="flex -space-x-3">
<div class="w-10 h-10 rounded border border-border-industrial bg-background-dark flex items-center justify-center overflow-hidden grayscale contrast-125">
<img class="w-full h-full object-cover opacity-80" data-alt="Close up of industrial metal ductwork" src="https://lh3.googleusercontent.com/aida-public/AB6AXuCNroSpteHLNGkfvub5_W25eLh2b5ZJrbZ9sHeOIxASvjqI6UdJMvZrCaGiOuIbj8aDpGGDS9o5lqc6Kn21CDTHyzahORsC4y2-ZYUS_lyeF8YAjE2j2roREC7nxHjB9FPMmFwAeENy3CTHRUVMy6A5oAWyiSMxHmQ_fquPwnjsbhyrM004rs6zLsKws_Xcs8fbGDm9ww6wf5PISwtnIaKeGa2RjLkllNnnCsx9XcPEVO798wLFDQtGvItmmiOljcw4zNtywtPhpWc"/>
</div>
<div class="w-10 h-10 rounded border border-border-industrial bg-background-dark flex items-center justify-center overflow-hidden grayscale contrast-125">
<img class="w-full h-full object-cover opacity-80" data-alt="Industrial manufacturing equipment and metal parts" src="https://lh3.googleusercontent.com/aida-public/AB6AXuAixnQijAM9ueFaQB8QDqrsPA4x8hVyqsj4fBstOOtGxSwiGdFtK2mCDvrGJhnTQYkV0dLw53Oi_IEsteZAS4gLjV6UG6qfoXlzbpkmKxJ_yBH7OJ2AMYE1ytmvRciLLLhpYpAcwWsYDwV139B5ecsBXF3Wvu8XOwol3QSHcqPfaOLi11uYsNltBRJijblmUbsE-ZFvVrJLg92aS30NhFDEzzYmN_LJcE1ca01JbS8Do2kzmROzc13u4DCN4Y5DjDSBErYVdJwg8Vc"/>
</div>
</div>
</div>
<div class="mt-4 pt-3 border-t border-border-industrial/50">
<p class="text-[11px] text-slate-400 font-medium line-clamp-1 italic tracking-tight">Rectangular Duct, Round Duct, HVAC Fittings, Custom Dampers</p>
</div>
<div class="flex items-center justify-between mt-3">
<div class="text-[10px] text-slate-600 font-bold uppercase tracking-widest">In Queue</div>
<button class="flex items-center gap-1 text-primary text-[11px] font-black uppercase tracking-widest">
                    Log Details
                    <span class="material-symbols-outlined text-sm">open_in_new</span>
</button>
</div>
</div>
<!-- Order Card 2: Shipped -->
<div class="field-log-entry status-shipped relative bg-panel-dark border border-border-industrial p-4 overflow-hidden">
<div class="flex justify-between items-start">
<div class="space-y-0.5">
<div class="flex items-center gap-2">
<span class="text-[10px] font-black text-slate-500 tracking-tighter">ID: #9715</span>
<div class="h-px w-4 bg-border-industrial"></div>
<span class="text-[10px] font-bold text-hvac-cyan uppercase tracking-widest">In Transit</span>
</div>
<h3 class="text-sm font-bold text-slate-100 uppercase leading-tight">Oak Ridge Medical Center</h3>
<div class="flex items-center gap-1.5 text-[11px] text-slate-500 font-medium">
<span class="material-symbols-outlined text-xs">schedule</span>
                        Oct 18, 2023 · 08:15
                    </div>
</div>
<div class="p-2 rounded bg-background-dark border border-border-industrial">
<span class="material-symbols-outlined text-hvac-cyan text-xl">local_shipping</span>
</div>
</div>
<div class="mt-4 pt-3 border-t border-border-industrial/50">
<p class="text-[11px] text-slate-400 font-medium line-clamp-1 italic tracking-tight">VAV Boxes, Flex Duct, Ceiling Diffusers, Registers</p>
<div class="mt-2 flex items-center gap-2 bg-background-dark p-2 border border-border-industrial/30">
<div class="w-1 h-4 bg-hvac-cyan/50"></div>
<span class="text-[10px] text-slate-300 font-bold tracking-wider">ETA: TOMORROW, 09:00 AM</span>
</div>
</div>
<div class="flex items-center justify-between mt-3">
<div class="text-[10px] text-slate-600 font-bold uppercase tracking-widest">Outbound</div>
<button class="flex items-center gap-1 text-primary text-[11px] font-black uppercase tracking-widest">
                    Log Details
                    <span class="material-symbols-outlined text-sm">open_in_new</span>
</button>
</div>
</div>
<!-- Order Card 3: Delivered -->
<div class="field-log-entry status-delivered relative bg-panel-dark border border-border-industrial p-4 overflow-hidden">
<div class="flex justify-between items-start">
<div class="space-y-0.5">
<div class="flex items-center gap-2">
<span class="text-[10px] font-black text-slate-500 tracking-tighter">ID: #9688</span>
<div class="h-px w-4 bg-border-industrial"></div>
<span class="text-[10px] font-bold text-hvac-green uppercase tracking-widest">Delivered</span>
</div>
<h3 class="text-sm font-bold text-slate-100 uppercase leading-tight">Riverview Tech Campus</h3>
<div class="flex items-center gap-1.5 text-[11px] text-slate-500 font-medium">
<span class="material-symbols-outlined text-xs">schedule</span>
                        Oct 12, 2023 · 11:45
                    </div>
</div>
<div class="p-2 rounded bg-background-dark border border-border-industrial">
<span class="material-symbols-outlined text-hvac-green text-xl">check_circle</span>
</div>
</div>
<div class="mt-4 pt-3 border-t border-border-industrial/50">
<p class="text-[11px] text-slate-400 font-medium line-clamp-1 italic tracking-tight">Spiral Ductwork, Custom Dampers, Access Doors</p>
<div class="mt-2 flex items-center gap-2 bg-emerald-900/10 p-2 border border-hvac-green/20">
<span class="text-[10px] text-hvac-green font-bold tracking-wider uppercase">Receipt Confirmed: Oct 15</span>
</div>
</div>
<div class="flex items-center justify-between mt-3">
<div class="text-[10px] text-slate-600 font-bold uppercase tracking-widest">Archived</div>
<button class="flex items-center gap-1 text-primary text-[11px] font-black uppercase tracking-widest">
                    Log Details
                    <span class="material-symbols-outlined text-sm">open_in_new</span>
</button>
</div>
</div>
<!-- Order Card 4: Delivered -->
<div class="field-log-entry status-delivered relative bg-panel-dark border border-border-industrial p-4 overflow-hidden opacity-80">
<div class="flex justify-between items-start">
<div class="space-y-0.5">
<div class="flex items-center gap-2">
<span class="text-[10px] font-black text-slate-500 tracking-tighter">ID: #9540</span>
<div class="h-px w-4 bg-border-industrial"></div>
<span class="text-[10px] font-bold text-hvac-green uppercase tracking-widest">Delivered</span>
</div>
<h3 class="text-sm font-bold text-slate-300 uppercase leading-tight">Downtown Library Reno</h3>
<div class="flex items-center gap-1.5 text-[11px] text-slate-600 font-medium">
<span class="material-symbols-outlined text-xs">schedule</span>
                        Sep 28, 2023 · 16:20
                    </div>
</div>
<div class="p-2 rounded bg-background-dark border border-border-industrial">
<span class="material-symbols-outlined text-slate-500 text-xl">history</span>
</div>
</div>
<div class="mt-4 pt-3 border-t border-border-industrial/50">
<p class="text-[11px] text-slate-500 font-medium line-clamp-1 italic tracking-tight">Standard Insulated Flex, Grilles, Registers</p>
</div>
<div class="flex items-center justify-between mt-3">
<div class="text-[10px] text-slate-700 font-bold uppercase tracking-widest">Archived</div>
<button class="flex items-center gap-1 text-primary/70 text-[11px] font-black uppercase tracking-widest">
                    Log Details
                    <span class="material-symbols-outlined text-sm">open_in_new</span>
</button>
</div>
</div>
</div>
</main>
<!-- Bottom Navigation -->
<nav class="fixed bottom-0 left-0 right-0 bg-panel-dark/95 backdrop-blur-md border-t border-border-industrial px-8 py-3 flex justify-between items-center z-30">
<a class="flex flex-col items-center gap-1 text-slate-500 hover:text-primary transition-colors" href="#">
<span class="material-symbols-outlined">home</span>
<span class="text-[9px] font-black uppercase tracking-[0.1em]">Dashboard</span>
</a>
<a class="flex flex-col items-center gap-1 text-primary transition-colors" href="#">
<span class="material-symbols-outlined" style="font-variation-settings: 'FILL' 1">history_edu</span>
<span class="text-[9px] font-black uppercase tracking-[0.1em]">Field Log</span>
</a>
<a class="flex flex-col items-center gap-1 text-slate-500 hover:text-primary transition-colors" href="#">
<span class="material-symbols-outlined">settings_suggest</span>
<span class="text-[9px] font-black uppercase tracking-[0.1em]">Config</span>
</a>
</nav>
</body></html>

<!-- Order Details -->
<!DOCTYPE html>

<html class="dark" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Order Details - Haley Order System</title>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&amp;family=Public+Sans:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "primary": "#ff9a00", // Industrial Amber
                        "hvac-bg": "#0a0c0e",
                        "hvac-surface": "#14171a",
                        "hvac-border": "#2d3439",
                        "hvac-muted": "#64748b",
                        "hvac-accent": "#00f2ff", // Tech Cyan
                    },
                    fontFamily: {
                        "display": ["Public Sans", "sans-serif"],
                        "mono": ["JetBrains Mono", "monospace"]
                    },
                    borderRadius: {"DEFAULT": "0px", "lg": "0px", "xl": "0px", "full": "9999px"},
                },
            },
        }
    </script>
<style>
        body {
            font-family: 'Public Sans', sans-serif;
            background-color: #0a0c0e;
        }
        .mono-text {
            font-family: 'JetBrains Mono', monospace;
        }
        .material-symbols-outlined {
            font-variation-settings: 'FILL' 0, 'wght' 400, 'GRAD' 0, 'opsz' 24;
        }
        .blueprint-grid {
            background-image: radial-gradient(circle, #1a1e22 1px, transparent 1px);
            background-size: 20px 20px;
        }
        .tech-border {
            border: 1px solid #2d3439;
            position: relative;
        }
        .tech-border::before {
            content: '';
            position: absolute;
            top: -1px;
            left: -1px;
            width: 8px;
            height: 8px;
            border-top: 2px solid #ff9a00;
            border-left: 2px solid #ff9a00;
        }
    </style>
</head>
<body class="bg-hvac-bg text-slate-100 font-display">
<div class="relative flex min-h-screen w-full flex-col max-w-lg mx-auto bg-hvac-bg shadow-2xl overflow-x-hidden border-x border-hvac-border">
<!-- Header -->
<header class="flex items-center bg-hvac-surface p-4 border-b-2 border-primary sticky top-0 z-30">
<button class="text-slate-100 flex size-10 items-center justify-center hover:bg-hvac-border transition-colors">
<span class="material-symbols-outlined">arrow_back</span>
</button>
<div class="flex-1 ml-2">
<h1 class="text-lg font-bold leading-tight mono-text uppercase tracking-tighter">SPEC_ORD: #9822</h1>
<div class="flex items-center gap-2">
<span class="size-2 rounded-full bg-primary animate-pulse"></span>
<p class="text-[10px] font-bold text-primary uppercase tracking-[0.2em]">Pending_Approval</p>
</div>
</div>
<button class="text-primary text-xs font-bold px-3 py-1 border border-primary/30 hover:bg-primary/10 mono-text uppercase">
            Logs
        </button>
</header>
<!-- Project Hero Section -->
<div class="p-5 bg-hvac-surface/50 border-b border-hvac-border blueprint-grid">
<div class="flex gap-4 items-start">
<div class="bg-center bg-no-repeat aspect-square bg-cover size-24 border-2 border-hvac-border grayscale contrast-125" data-alt="Project visual" style='background-image: url("https://lh3.googleusercontent.com/aida-public/AB6AXuBJ-2byiKiQ6SSlYZI-23UY5e9CEqDvp6F6phK_Qazx6aSofjy4p0Rv21X8mz0TPPc2xywyKs2fr7sm_imFyyQEP2Sq-uTHQfFqMFzK0FUOTJZpI8IeBjbHP6lX_kJaowZ1rMkJ-Wt6EQhJ-wE3tNCZsNsGOHd571ztRb_twqOvowQIk9zg9jfrPpZ6p6vl3rS_ATWX1MBvZtS3462u-PGIQq5MXMN8meveFNOUfxGIq7NE6sDUDQNQ11kLl2sSm3yvLFkRYaNWgW4");'>
<div class="w-full h-full bg-primary/10"></div>
</div>
<div class="flex flex-col">
<h2 class="text-xl font-bold leading-tight uppercase tracking-tight text-white mono-text">Skyline Apt. P-II</h2>
<div class="mt-1 px-2 py-0.5 bg-hvac-border text-primary inline-block text-[10px] font-bold mono-text w-fit">
                    ID: PRJ-2024-089
                </div>
<div class="mt-3 inline-flex items-center text-[11px] font-medium text-hvac-muted uppercase tracking-wider">
<span class="material-symbols-outlined text-[14px] mr-1 text-primary">location_on</span>
                    Downtown Dist. // SEC-04
                </div>
</div>
</div>
</div>
<!-- Main Content (Items List as Technical Spec) -->
<main class="flex-1 overflow-y-auto pb-64">
<!-- Category: Rectangular Duct -->
<section class="mt-8 px-4">
<div class="flex items-center justify-between mb-2 border-l-4 border-primary pl-3">
<h3 class="text-white text-xs font-bold uppercase tracking-[0.15em] mono-text">01 // Rectangular_System</h3>
<span class="text-[10px] text-hvac-muted mono-text">CAT_RD-001</span>
</div>
<div class="tech-border bg-hvac-surface divide-y divide-hvac-border">
<!-- Item 1 -->
<div class="p-4 grid grid-cols-12 gap-2">
<div class="col-span-8">
<p class="text-sm font-bold mono-text text-white">STRAIGHT_DUCT [24"x12"]</p>
<p class="text-[11px] text-hvac-muted mt-1 uppercase">Galvanized_Steel / 5ft_Length</p>
<div class="flex gap-3 mt-2">
<span class="text-[9px] px-1.5 py-0.5 bg-hvac-border text-slate-300 mono-text">24_GAUGE</span>
<span class="text-[9px] px-1.5 py-0.5 bg-hvac-border text-slate-300 mono-text">TDF_CONN</span>
</div>
</div>
<div class="col-span-4 text-right flex flex-col justify-center">
<span class="text-[10px] text-primary mono-text block">QUANTITY</span>
<span class="text-lg font-bold mono-text text-white">15.00</span>
<span class="text-[10px] text-hvac-muted mono-text">UNIT</span>
</div>
</div>
<!-- Item 2 -->
<div class="p-4 grid grid-cols-12 gap-2">
<div class="col-span-8">
<p class="text-sm font-bold mono-text text-white">90°_ELBOW [SHORT_WAY]</p>
<p class="text-[11px] text-hvac-muted mt-1 uppercase">24"x12" / R=6.00"</p>
<div class="flex gap-3 mt-2">
<span class="text-[9px] px-1.5 py-0.5 bg-hvac-border text-slate-300 mono-text">22_GAUGE</span>
<span class="text-[9px] px-1.5 py-0.5 bg-hvac-border text-slate-300 mono-text">S&amp;D_CONN</span>
</div>
</div>
<div class="col-span-4 text-right flex flex-col justify-center">
<span class="text-[10px] text-primary mono-text block">QUANTITY</span>
<span class="text-lg font-bold mono-text text-white">08.00</span>
<span class="text-[10px] text-hvac-muted mono-text">UNIT</span>
</div>
</div>
</div>
</section>
<!-- Category: Round Duct -->
<section class="mt-8 px-4">
<div class="flex items-center justify-between mb-2 border-l-4 border-hvac-accent pl-3">
<h3 class="text-white text-xs font-bold uppercase tracking-[0.15em] mono-text">02 // Round_&amp;_Flex_System</h3>
<span class="text-[10px] text-hvac-muted mono-text">CAT_RF-002</span>
</div>
<div class="border border-hvac-border bg-hvac-surface divide-y divide-hvac-border">
<div class="p-4 flex justify-between items-center">
<div>
<p class="text-sm font-bold mono-text text-white">SPIRAL_PIPE_10"DIA</p>
<p class="text-[11px] text-hvac-muted uppercase mt-0.5">10ft_Joint / Single_Wall / 26_GA</p>
</div>
<div class="text-right">
<span class="text-base font-bold mono-text text-hvac-accent">20.00</span>
<span class="text-[10px] text-hvac-muted mono-text ml-1">UN</span>
</div>
</div>
<div class="p-4 flex justify-between items-center">
<div>
<p class="text-sm font-bold mono-text text-white">INSUL_FLEX_8"DIA</p>
<p class="text-[11px] text-hvac-muted uppercase mt-0.5">R-6.0 / 25ft_Silver_Jkt</p>
</div>
<div class="text-right">
<span class="text-base font-bold mono-text text-hvac-accent">04.00</span>
<span class="text-[10px] text-hvac-muted mono-text ml-1">BX</span>
</div>
</div>
</div>
</section>
<!-- Category: Fasteners -->
<section class="mt-8 px-4">
<h3 class="text-hvac-muted text-[10px] font-bold uppercase tracking-widest mb-3 mono-text flex items-center gap-2">
<span class="h-px bg-hvac-border flex-1"></span>
                HARDWARE_FASTENERS
                <span class="h-px bg-hvac-border flex-1"></span>
</h3>
<div class="grid grid-cols-2 gap-3">
<div class="bg-hvac-surface border border-hvac-border p-3">
<p class="text-[10px] text-primary font-bold uppercase mono-text mb-1">ZIP_SCREWS</p>
<p class="text-xs font-bold text-white mono-text">#8 x 1/2"</p>
<p class="text-[10px] text-slate-400 mt-2">QTY: 5,000 [BUCKET]</p>
</div>
<div class="bg-hvac-surface border border-hvac-border p-3">
<p class="text-[10px] text-primary font-bold uppercase mono-text mb-1">BOLTS_NUTS</p>
<p class="text-xs font-bold text-white mono-text">3/8"-16 x 1"</p>
<p class="text-[10px] text-slate-400 mt-2">QTY: 200 [SETS]</p>
</div>
</div>
</section>
<!-- Category: Support -->
<section class="mt-8 px-4">
<div class="tech-border bg-hvac-surface p-4">
<h3 class="text-xs font-bold text-white uppercase mono-text mb-4">Support_Spec_v1.2</h3>
<div class="space-y-3">
<div class="flex justify-between items-end border-b border-hvac-border border-dashed pb-1">
<div class="flex flex-col">
<span class="text-[10px] text-hvac-muted mono-text">DESC.</span>
<span class="text-xs text-slate-200 mono-text">1-5/8" UNISTRUT (P-GALV)</span>
</div>
<span class="text-sm font-bold text-white mono-text">120_LF</span>
</div>
<div class="flex justify-between items-end border-b border-hvac-border border-dashed pb-1">
<div class="flex flex-col">
<span class="text-[10px] text-hvac-muted mono-text">DESC.</span>
<span class="text-xs text-slate-200 mono-text">HILTI KH-EZ 3/8" ANCHORS</span>
</div>
<span class="text-sm font-bold text-white mono-text">50_PC</span>
</div>
</div>
</div>
</section>
</main>
<!-- Floating Action -->
<div class="sticky bottom-44 z-30 px-4">
<button class="flex w-full items-center justify-center gap-2 bg-primary text-black font-black py-4 uppercase mono-text tracking-tighter shadow-[0_0_20px_rgba(255,154,0,0.3)] hover:brightness-110 active:translate-y-0.5 transition-all">
<span class="material-symbols-outlined font-black">refresh</span>
<span>Duplicate_Order_Instance</span>
</button>
</div>
<!-- Technical Footer -->
<footer class="fixed bottom-0 max-w-lg w-full bg-hvac-surface border-t-2 border-hvac-border z-40">
<!-- Order Metadata Grid -->
<div class="grid grid-cols-2 bg-hvac-bg/50 border-b border-hvac-border">
<div class="p-3 border-r border-hvac-border">
<span class="text-[9px] text-hvac-muted uppercase mono-text block mb-1">TIMESTAMP_EXEC</span>
<span class="text-xs font-bold text-white mono-text">OCT_24_2024</span>
</div>
<div class="p-3">
<span class="text-[9px] text-hvac-muted uppercase mono-text block mb-1">LOGISTICS_MODE</span>
<span class="text-xs font-bold text-primary mono-text flex items-center gap-1">
<span class="material-symbols-outlined text-sm">local_shipping</span>
                    STD_DELIVERY
                </span>
</div>
<div class="p-3 border-t border-r border-hvac-border">
<span class="text-[9px] text-hvac-muted uppercase mono-text block mb-1">ORIGINATOR</span>
<span class="text-xs font-medium text-slate-300 mono-text">J.MILLER_092</span>
</div>
<div class="p-3 border-t border-hvac-border">
<span class="text-[9px] text-hvac-muted uppercase mono-text block mb-1">AUTH_SIG</span>
<span class="text-xs font-medium text-slate-300 mono-text italic">S_CHEN_APPR</span>
</div>
</div>
<!-- Navigation -->
<div class="flex border-t border-hvac-border bg-hvac-surface pt-2 pb-safe">
<a class="flex flex-1 flex-col items-center py-2 text-primary border-t-2 border-primary" href="#">
<span class="material-symbols-outlined text-xl">terminal</span>
<p class="text-[9px] font-bold mono-text uppercase mt-1">Orders</p>
</a>
<a class="flex flex-1 flex-col items-center py-2 text-hvac-muted" href="#">
<span class="material-symbols-outlined text-xl">domain</span>
<p class="text-[9px] font-bold mono-text uppercase mt-1">Projects</p>
</a>
<a class="flex flex-1 flex-col items-center py-2 text-hvac-muted" href="#">
<span class="material-symbols-outlined text-xl">inventory_2</span>
<p class="text-[9px] font-bold mono-text uppercase mt-1">Stock</p>
</a>
<a class="flex flex-1 flex-col items-center py-2 text-hvac-muted" href="#">
<span class="material-symbols-outlined text-xl">settings_input_component</span>
<p class="text-[9px] font-bold mono-text uppercase mt-1">Config</p>
</a>
</div>
</footer>
</div>
</body></html>
