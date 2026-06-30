<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box Craft | Premium Packaging Solutions</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brandNavy: {
                            light: '#1B2E4B',
                            DEFAULT: '#0A1C36',
                            dark: '#050E1C',
                        },
                        brandGold: {
                            light: '#F3D285',
                            DEFAULT: '#D4AF37',
                            dark: '#A6821E',
                        },
                        brandKraft: '#FAF6F0'
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', '-apple-system', 'BlinkMacSystemFont', 'Segoe UI', 'Roboto', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        .custom-scrollbar::-webkit-scrollbar {
            width: 6px;
        }
        .custom-scrollbar::-webkit-scrollbar-track {
            background: #111827;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb {
            background: #D4AF37;
            border-radius: 3px;
        }
        .pulse-gold {
            animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }
        @keyframes pulse {
            0%, 100% { opacity: 1; transform: scale(1); }
            50% { opacity: .8; transform: scale(1.05); }
        }
    </style>
</head>
<body class="bg-[#FCFAF7] text-gray-800 font-sans">

    <!-- Announcement Bar with Slogans -->
    <div class="bg-brandNavy-dark text-white text-xs sm:text-sm py-2 px-4 overflow-hidden border-b border-brandGold/30">
        <div id="slogan-ticker" class="flex justify-center items-center space-x-8 animate-pulse text-center">
            <span class="flex items-center"><i data-lucide="sparkles" class="w-4 h-4 text-brandGold mr-2"></i> "Think Inside the Box, Think BOX CRAFT"</span>
            <span class="hidden md:inline text-brandGold">|</span>
            <span class="hidden md:flex items-center"><i data-lucide="package" class="w-4 h-4 text-brandGold mr-2"></i> Strong Boxes, Strong Brands</span>
            <span class="hidden lg:inline text-brandGold">|</span>
            <span class="hidden lg:flex items-center"><i data-lucide="truck" class="w-4 h-4 text-brandGold mr-2"></i> Packaging Excellence, Delivered Perfectly</span>
        </div>
    </div>

    <!-- Header / Navbar -->
    <header class="sticky top-0 z-40 bg-brandNavy/95 backdrop-blur-md border-b border-brandGold/20 shadow-lg text-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <!-- Logo -->
                <div class="flex-shrink-0 flex items-center space-x-3">
                    <div class="relative bg-brandGold p-2.5 rounded-lg shadow-md border border-brandGold-light/30">
                        <svg class="w-7 h-7 text-brandNavy" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"></path>
                            <polyline points="3.27 6.96 12 12.01 20.73 6.96"></polyline>
                            <line x1="12" y1="22.08" x2="12" y2="12"></line>
                        </svg>
                    </div>
                    <div>
                        <span class="text-2xl font-black tracking-wider text-white">BOX <span class="text-brandGold">CRAFT</span></span>
                        <p class="text-[9px] tracking-[0.25em] text-gray-300 font-semibold uppercase">Packaging Solutions</p>
                    </div>
                </div>

                <!-- Desktop Navigation -->
                <nav class="hidden md:flex space-x-8 text-sm font-medium">
                    <a href="#about" class="hover:text-brandGold transition-colors">Who We Are</a>
                    <a href="#products" class="hover:text-brandGold transition-colors">Our Products</a>
                    <a href="#industries" class="hover:text-brandGold transition-colors">Industries Served</a>
                    <a href="#strengths" class="hover:text-brandGold transition-colors">Our Strengths</a>
                    <a href="#calculator" class="text-brandGold hover:text-brandGold-light font-semibold transition-colors flex items-center gap-1">
                        <i data-lucide="calculator" class="w-4 h-4"></i> Box Configurator
                    </a>
                    <a href="#contact" class="hover:text-brandGold transition-colors">Contact</a>
                </nav>

                <!-- Quick Action Buttons -->
                <div class="hidden lg:flex items-center space-x-4">
                    <a href="tel:8929131333" class="flex items-center text-xs font-semibold bg-brandNavy-light border border-brandGold/30 px-3.5 py-2 rounded-full hover:bg-brandNavy transition">
                        <i data-lucide="phone" class="w-3.5 h-3.5 text-brandGold mr-2"></i> +91 8929131333
                    </a>
                    <button onclick="toggleInquiryModal()" class="relative bg-brandGold text-brandNavy font-bold text-xs px-5 py-2.5 rounded-lg shadow-lg hover:bg-brandGold-light transition duration-300 flex items-center">
                        <i data-lucide="shopping-cart" class="w-4 h-4 mr-1.5"></i> Custom Inquiry
                        <span id="cart-badge" class="absolute -top-2 -right-2 bg-red-600 text-white text-[10px] px-1.5 py-0.5 rounded-full hidden">0</span>
                    </button>
                </div>

                <!-- Mobile Menu Button -->
                <div class="md:hidden flex items-center space-x-3">
                    <button onclick="toggleInquiryModal()" class="relative p-2 text-brandGold hover:text-white">
                        <i data-lucide="shopping-cart" class="w-6 h-6"></i>
                        <span id="cart-badge-mobile" class="absolute -top-1 -right-1 bg-red-600 text-white text-[9px] px-1.5 py-0.2 rounded-full hidden">0</span>
                    </button>
                    <button id="mobile-menu-btn" onclick="toggleMobileMenu()" class="p-2 text-gray-300 hover:text-white focus:outline-none">
                        <i data-lucide="menu" id="menu-icon" class="w-6 h-6"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu panel -->
        <div id="mobile-menu" class="hidden md:hidden bg-brandNavy border-t border-brandGold/20 px-4 pt-2 pb-6 space-y-3 shadow-inner">
            <a href="#about" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-md hover:bg-brandNavy-light text-base font-medium">Who We Are</a>
            <a href="#products" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-md hover:bg-brandNavy-light text-base font-medium">Our Products</a>
            <a href="#industries" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-md hover:bg-brandNavy-light text-base font-medium">Industries Served</a>
            <a href="#strengths" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-md hover:bg-brandNavy-light text-base font-medium">Our Strengths</a>
            <a href="#calculator" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-md bg-brandGold/10 text-brandGold font-semibold text-base">Box Configurator</a>
            <a href="#contact" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-md hover:bg-brandNavy-light text-base font-medium">Contact Us</a>
            <div class="pt-4 border-t border-brandGold/10 space-y-2">
                <a href="tel:8929131333" class="flex items-center justify-center bg-brandNavy-light py-2 rounded-lg text-sm border border-brandGold/30">
                    <i data-lucide="phone" class="w-4 h-4 text-brandGold mr-2"></i> Call Support
                </a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="relative bg-brandNavy text-white overflow-hidden py-16 md:py-24">
        <!-- Visual Accent Background elements -->
        <div class="absolute inset-0 opacity-10 pointer-events-none">
            <div class="absolute top-10 left-10 w-96 h-96 bg-brandGold rounded-full blur-3xl"></div>
            <div class="absolute bottom-10 right-10 w-96 h-96 bg-brandGold rounded-full blur-3xl"></div>
        </div>
        
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                
                <!-- Left Content Column -->
                <div class="lg:col-span-7 space-y-6">
                    <div class="inline-flex items-center bg-brandGold/10 border border-brandGold/30 px-3.5 py-1.5 rounded-full text-brandGold text-xs font-semibold uppercase tracking-wider">
                        <i data-lucide="award" class="w-3.5 h-3.5 mr-1.5"></i> India's Premier Packaging Partner
                    </div>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-black leading-tight">
                        Designed to Protect,<br>
                        <span class="text-transparent bg-clip-text bg-gradient-to-r from-brandGold via-brandGold-light to-brandGold-dark italic font-serif">Crafted to Impress</span>
                    </h1>
                    <p class="text-gray-300 text-base sm:text-lg max-w-xl leading-relaxed">
                        BOX CRAFT is a leading packaging solutions company providing high-quality, innovative and sustainable packaging products that protect your products and promote your brand.
                    </p>

                    <!-- CTAs -->
                    <div class="flex flex-col sm:flex-row gap-4 pt-2">
                        <a href="#calculator" class="bg-brandGold text-brandNavy font-extrabold px-8 py-4 rounded-xl shadow-lg hover:bg-brandGold-light hover:shadow-brandGold/20 hover:shadow-2xl transition duration-300 text-center flex items-center justify-center gap-2">
                            <i data-lucide="box" class="w-5 h-5"></i> Build Custom Box
                        </a>
                        <a href="#products" class="bg-brandNavy-light border border-gray-500/30 hover:border-brandGold/70 text-white font-semibold px-8 py-4 rounded-xl hover:bg-brandNavy transition duration-300 text-center flex items-center justify-center">
                            Explore Products
                        </a>
                    </div>

                    <!-- Trust Badges Grid -->
                    <div class="pt-8 border-t border-brandGold/20 grid grid-cols-2 sm:grid-cols-4 gap-4">
                        <div class="flex items-center space-x-2">
                            <div class="p-1.5 bg-brandGold/10 rounded-lg text-brandGold">
                                <i data-lucide="shield-check" class="w-5 h-5"></i>
                            </div>
                            <span class="text-xs font-medium text-gray-300">Qualify Packaging</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <div class="p-1.5 bg-brandGold/10 rounded-lg text-brandGold">
                                <i data-lucide="leaf" class="w-5 h-5"></i>
                            </div>
                            <span class="text-xs font-medium text-gray-300">Sustainable Solutions</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <div class="p-1.5 bg-brandGold/10 rounded-lg text-brandGold">
                                <i data-lucide="award" class="w-5 h-5"></i>
                            </div>
                            <span class="text-xs font-medium text-gray-300">Stronger Brands</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <div class="p-1.5 bg-brandGold/10 rounded-lg text-brandGold">
                                <i data-lucide="trending-up" class="w-5 h-5"></i>
                            </div>
                            <span class="text-xs font-medium text-gray-300">Better Future</span>
                        </div>
                    </div>
                </div>

                <!-- Right Graphic Column (Flyer Showdown/Packaging stack) -->
                <div class="lg:col-span-5 relative">
                    <div class="relative mx-auto max-w-md lg:max-w-none">
                        <!-- Premium Box stack graphic -->
                        <div class="bg-gradient-to-tr from-brandGold-dark/40 to-transparent absolute -inset-2 rounded-2xl blur-lg pointer-events-none"></div>
                        <div class="relative bg-brandNavy-light border border-brandGold/20 p-6 sm:p-8 rounded-2xl shadow-2xl">
                            <div class="absolute -top-4 -right-4 bg-brandGold text-brandNavy text-xs font-black px-4 py-1.5 rounded-full shadow-md uppercase tracking-wider transform rotate-12">
                                Best Price
                            </div>
                            
                            <h3 class="text-xl font-bold text-brandGold mb-4 flex items-center">
                                <i data-lucide="package-open" class="w-5 h-5 mr-2"></i> Standard Box Types
                            </h3>

                            <div class="space-y-3">
                                <div class="flex items-center justify-between p-3 bg-brandNavy/55 rounded-lg border border-brandGold/10">
                                    <div class="flex items-center space-x-3">
                                        <div class="w-8 h-8 rounded bg-amber-800/40 flex items-center justify-center text-brandGold text-sm">
                                            📦
                                        </div>
                                        <span class="font-semibold text-sm">Corrugated (3, 5, 7 Ply)</span>
                                    </div>
                                    <span class="text-xs text-brandGold font-bold">Standard Duty</span>
                                </div>
                                <div class="flex items-center justify-between p-3 bg-brandNavy/55 rounded-lg border border-brandGold/10">
                                    <div class="flex items-center space-x-3">
                                        <div class="w-8 h-8 rounded bg-yellow-600/30 flex items-center justify-center text-brandGold text-sm">
                                            🎁
                                        </div>
                                        <span class="font-semibold text-sm">Premium Gift Boxes</span>
                                    </div>
                                    <span class="text-xs text-brandGold font-bold">Luxury Matte</span>
                                </div>
                                <div class="flex items-center justify-between p-3 bg-brandNavy/55 rounded-lg border border-brandGold/10">
                                    <div class="flex items-center space-x-3">
                                        <div class="w-8 h-8 rounded bg-emerald-800/30 flex items-center justify-center text-emerald-400 text-sm">
                                            🌿
                                        </div>
                                        <span class="font-semibold text-sm">Eco-friendly Kraft</span>
                                    </div>
                                    <span class="text-xs text-emerald-400 font-bold">100% Recycled</span>
                                </div>
                            </div>

                            <!-- Fast Contact Badge inside Graphic -->
                            <div class="mt-6 p-4 bg-brandNavy rounded-lg border border-brandGold/20 flex items-center justify-between">
                                <div>
                                    <p class="text-xs text-gray-400">Quick Response Hotline</p>
                                    <p class="text-base font-extrabold text-white">+91 8929131333</p>
                                </div>
                                <a href="https://wa.me/918929131333" target="_blank" class="bg-green-600 hover:bg-green-700 text-white p-2.5 rounded-full shadow transition">
                                    <svg class="w-5 h-5 fill-current" viewBox="0 0 24 24"><path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946C.06 5.348 5.397.01 12.008.01c3.202.001 6.212 1.246 8.477 3.514 2.266 2.268 3.507 5.28 3.505 8.484-.004 6.657-5.34 11.997-11.953 11.997-2.005-.001-3.973-.502-5.724-1.455L0 24zm6.59-4.846c1.665.988 3.3 1.478 5.353 1.479 5.428 0 9.845-4.414 9.848-9.847.002-2.63-1.023-5.101-2.882-6.961-1.859-1.861-4.331-2.885-6.961-2.887-5.43 0-9.848 4.415-9.851 9.849-.001 2.13.563 4.21 1.634 6.013l-.973 3.548 3.632-.953z"/></svg>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Why Choose Box Craft Section -->
    <section id="about" class="py-16 bg-white border-b border-gray-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                
                <!-- Left side: Value proposition / Slogan -->
                <div class="lg:col-span-5 space-y-6">
                    <div class="text-sm font-bold text-brandGold uppercase tracking-wider">About Our Company</div>
                    <h2 class="text-3xl sm:text-4xl font-black text-brandNavy">
                        Why Choose <span class="text-brandGold">BOX CRAFT</span>?
                    </h2>
                    <p class="text-gray-600 leading-relaxed">
                        We don't just manufacture boxes; we craft a security vault for your high-value shipments and a stylish billboard for your retail presence. From robust industrial solutions to delicate luxury gift wraps, we cater to every spectrum of modern commerce.
                    </p>
                    
                    <div class="p-6 bg-brandKraft rounded-xl border-l-4 border-brandGold space-y-3">
                        <p class="text-xs text-brandGold font-bold uppercase tracking-wider">Our Commitment</p>
                        <p class="text-sm italic font-medium text-brandNavy">
                            "Safe Packaging. Stronger Brand. Better Tomorrow. All types of packaging solutions under one comprehensive roof."
                        </p>
                    </div>
                </div>

                <!-- Right side: Why Choose US Checks & Visual Card Grid -->
                <div class="lg:col-span-7 bg-brandNavy text-white p-8 rounded-2xl shadow-xl space-y-6">
                    <h3 class="text-2xl font-extrabold text-brandGold">Our Guaranteed Promise</h3>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div class="flex items-start space-x-3">
                            <i data-lucide="check-circle-2" class="w-6 h-6 text-brandGold flex-shrink-0 mt-0.5"></i>
                            <div>
                                <h4 class="font-bold text-sm">Premium Quality Materials</h4>
                                <p class="text-xs text-gray-400 mt-0.5">We use high-grade tested virgin and recycled boards.</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-3">
                            <i data-lucide="check-circle-2" class="w-6 h-6 text-brandGold flex-shrink-0 mt-0.5"></i>
                            <div>
                                <h4 class="font-bold text-sm">Customized Solutions</h4>
                                <p class="text-xs text-gray-400 mt-0.5">Precise bespoke sizing and structural configurations.</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-3">
                            <i data-lucide="check-circle-2" class="w-6 h-6 text-brandGold flex-shrink-0 mt-0.5"></i>
                            <div>
                                <h4 class="font-bold text-sm">Competitive Pricing</h4>
                                <p class="text-xs text-gray-400 mt-0.5">Unmatched manufacturing-direct rates with tier discounts.</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-3">
                            <i data-lucide="check-circle-2" class="w-6 h-6 text-brandGold flex-shrink-0 mt-0.5"></i>
                            <div>
                                <h4 class="font-bold text-sm">Timely Delivery</h4>
                                <p class="text-xs text-gray-400 mt-0.5">Guaranteed supply schedules with quick turnaround times.</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-3">
                            <i data-lucide="check-circle-2" class="w-6 h-6 text-brandGold flex-shrink-0 mt-0.5"></i>
                            <div>
                                <h4 class="font-bold text-sm">Modern Manufacturing</h4>
                                <p class="text-xs text-gray-400 mt-0.5">Equipped with state-of-the-art automatic corrugation.</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-3">
                            <i data-lucide="check-circle-2" class="w-6 h-6 text-brandGold flex-shrink-0 mt-0.5"></i>
                            <div>
                                <h4 class="font-bold text-sm">100% Customer Satisfaction</h4>
                                <p class="text-xs text-gray-400 mt-0.5">Dedicated client account executives for real-time support.</p>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Product Section -->
    <section id="products" class="py-20 bg-brandKraft">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16 space-y-4">
                <span class="inline-block text-brandGold font-bold text-sm uppercase tracking-widest bg-brandGold/10 px-4 py-1.5 rounded-full">Our Catalog</span>
                <h2 class="text-3xl sm:text-5xl font-black text-brandNavy">
                    Premium Packaging Offerings
                </h2>
                <p class="text-gray-600">
                    Engineered to withstand physical stresses, beautifully finished to display your brand value. Choose standard or custom configurations.
                </p>
            </div>

            <!-- Product Category Grid (9 Products) -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                
                <!-- Product 1 -->
                <div class="bg-white rounded-2xl overflow-hidden shadow-md border border-gray-100 hover:shadow-xl hover:-translate-y-1 transition duration-300 flex flex-col justify-between">
                    <div>
                        <div class="relative bg-amber-100 h-48 flex items-center justify-center p-4">
                            <!-- Custom elegant placeholder design -->
                            <div class="absolute inset-0 bg-gradient-to-br from-amber-500/10 to-amber-900/10"></div>
                            <svg class="w-24 h-24 text-amber-800" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                                <path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"></path>
                                <polyline points="3.27 6.96 12 12.01 20.73 6.96"></polyline>
                                <line x1="12" y1="22.08" x2="12" y2="12"></line>
                            </svg>
                            <span class="absolute top-3 left-3 bg-brandNavy text-brandGold font-bold text-[10px] px-2 py-1 rounded">HEAVY DUTY</span>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-brandNavy mb-2">Corrugated Boxes</h3>
                            <p class="text-xs text-brandGold font-extrabold uppercase tracking-wider mb-3">3 Ply, 5 Ply & 7 Ply</p>
                            <p class="text-sm text-gray-600">Designed for ultimate durability and shock absorption. Perfect for bulk shipping, shipping electronics, and relocation.</p>
                        </div>
                    </div>
                    <div class="p-6 border-t border-gray-50 flex items-center justify-between">
                        <button onclick="quickInquiry('Corrugated Boxes')" class="text-xs font-extrabold text-brandNavy hover:text-brandGold transition flex items-center gap-1">
                            <i data-lucide="plus-circle" class="w-4 h-4"></i> Add to Inquiry
                        </button>
                        <a href="#calculator" onclick="prefillConfigurator('Corrugated Boxes', '5')" class="text-xs font-bold text-brandGold border border-brandGold hover:bg-brandGold hover:text-brandNavy px-3 py-1.5 rounded transition">Customize</a>
                    </div>
                </div>

                <!-- Product 2 -->
                <div class="bg-white rounded-2xl overflow-hidden shadow-md border border-gray-100 hover:shadow-xl hover:-translate-y-1 transition duration-300 flex flex-col justify-between">
                    <div>
                        <div class="relative bg-orange-100 h-48 flex items-center justify-center p-4">
                            <div class="absolute inset-0 bg-gradient-to-br from-orange-500/10 to-orange-900/10"></div>
                            <svg class="w-24 h-24 text-orange-800" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                                <rect x="3" y="3" width="18" height="18" rx="2" ry="2"></rect>
                                <line x1="3" y1="9" x2="21" y2="9"></line>
                                <line x1="9" y1="21" x2="9" y2="9"></line>
                            </svg>
                            <span class="absolute top-3 left-3 bg-brandNavy text-brandGold font-bold text-[10px] px-2 py-1 rounded">RETAIL READY</span>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-brandNavy mb-2">Carton Boxes</h3>
                            <p class="text-xs text-brandGold font-extrabold uppercase tracking-wider mb-3">Bespoke Branding ready</p>
                            <p class="text-sm text-gray-600">Lightweight yet strong duplex board boxes. Ideal for primary product shelves, medicine packaging, and retail store displays.</p>
                        </div>
                    </div>
                    <div class="p-6 border-t border-gray-50 flex items-center justify-between">
                        <button onclick="quickInquiry('Carton Boxes')" class="text-xs font-extrabold text-brandNavy hover:text-brandGold transition flex items-center gap-1">
                            <i data-lucide="plus-circle" class="w-4 h-4"></i> Add to Inquiry
                        </button>
                        <a href="#calculator" onclick="prefillConfigurator('Carton Boxes', '3')" class="text-xs font-bold text-brandGold border border-brandGold hover:bg-brandGold hover:text-brandNavy px-3 py-1.5 rounded transition">Customize</a>
                    </div>
                </div>

                <!-- Product 3 -->
                <div class="bg-white rounded-2xl overflow-hidden shadow-md border border-gray-100 hover:shadow-xl hover:-translate-y-1 transition duration-300 flex flex-col justify-between">
                    <div>
                        <div class="relative bg-yellow-100 h-48 flex items-center justify-center p-4">
                            <div class="absolute inset-0 bg-gradient-to-br from-yellow-500/10 to-yellow-900/10"></div>
                            <svg class="w-24 h-24 text-yellow-800" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                                <path d="M12 2L2 7l10 5 10-5-10-5z"></path>
                                <path d="M2 17l10 5 10-5"></path>
                                <path d="M2 12l10 5 10-5"></path>
                            </svg>
                            <span class="absolute top-3 left-3 bg-brandNavy text-brandGold font-bold text-[10px] px-2 py-1 rounded">LUXURY MATTE</span>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-brandNavy mb-2">Premium Gift Boxes</h3>
                            <p class="text-xs text-brandGold font-extrabold uppercase tracking-wider mb-3">Rigid & Elegant finishes</p>
                            <p class="text-sm text-gray-600">Specially crafted boxes featuring gold foiling, magnetic flaps, and textured boards. Excellent for high-end gifting, jewelry, and luxury items.</p>
                        </div>
                    </div>
                    <div class="p-6 border-t border-gray-50 flex items-center justify-between">
                        <button onclick="quickInquiry('Premium Gift Boxes')" class="text-xs font-extrabold text-brandNavy hover:text-brandGold transition flex items-center gap-1">
                            <i data-lucide="plus-circle" class="w-4 h-4"></i> Add to Inquiry
                        </button>
                        <a href="#calculator" onclick="prefillConfigurator('Premium Gift Boxes', '3')" class="text-xs font-bold text-brandGold border border-brandGold hover:bg-brandGold hover:text-brandNavy px-3 py-1.5 rounded transition">Customize</a>
                    </div>
                </div>

                <!-- Product 4 -->
                <div class="bg-white rounded-2xl overflow-hidden shadow-md border border-gray-100 hover:shadow-xl hover:-translate-y-1 transition duration-300 flex flex-col justify-between">
                    <div>
                        <div class="relative bg-emerald-100 h-48 flex items-center justify-center p-4">
                            <div class="absolute inset-0 bg-gradient-to-br from-emerald-500/10 to-emerald-900/10"></div>
                            <svg class="w-24 h-24 text-emerald-800" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                                <path d="M6 2L3 6v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V6l-3-4z"></path>
                                <line x1="3" y1="6" x2="21" y2="6"></line>
                                <path d="M16 10a4 4 0 0 1-8 0"></path>
                            </svg>
                            <span class="absolute top-3 left-3 bg-brandNavy text-brandGold font-bold text-[10px] px-2 py-1 rounded">HIGH VISIBILITY</span>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-brandNavy mb-2">Retail Packaging Boxes</h3>
                            <p class="text-xs text-brandGold font-extrabold uppercase tracking-wider mb-3">Custom printing visual</p>
                            <p class="text-sm text-gray-600">Exquisite display shelf box structures, designed to secure product posture while creating impactful brand impressions for cosmetic or lifestyle goods.</p>
                        </div>
                    </div>
                    <div class="p-6 border-t border-gray-50 flex items-center justify-between">
                        <button onclick="quickInquiry('Retail Packaging Boxes')" class="text-xs font-extrabold text-brandNavy hover:text-brandGold transition flex items-center gap-1">
                            <i data-lucide="plus-circle" class="w-4 h-4"></i> Add to Inquiry
                        </button>
                        <a href="#calculator" onclick="prefillConfigurator('Retail Packaging Boxes', '3')" class="text-xs font-bold text-brandGold border border-brandGold hover:bg-brandGold hover:text-brandNavy px-3 py-1.5 rounded transition">Customize</a>
                    </div>
                </div>

                <!-- Product 5 -->
                <div class="bg-white rounded-2xl overflow-hidden shadow-md border border-gray-100 hover:shadow-xl hover:-translate-y-1 transition duration-300 flex flex-col justify-between">
                    <div>
                        <div class="relative bg-sky-100 h-48 flex items-center justify-center p-4">
                            <div class="absolute inset-0 bg-gradient-to-br from-sky-500/10 to-sky-900/10"></div>
                            <svg class="w-24 h-24 text-sky-800" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                                <rect x="3" y="3" width="18" height="18" rx="2"></rect>
                                <path d="M21 12H3"></path>
                                <path d="M12 3v18"></path>
                            </svg>
                            <span class="absolute top-3 left-3 bg-brandNavy text-brandGold font-bold text-[10px] px-2 py-1 rounded">ULTRA STRONGEST</span>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-brandNavy mb-2">Industrial Packaging</h3>
                            <p class="text-xs text-brandGold font-extrabold uppercase tracking-wider mb-3">Heavy Machinery & Logistics</p>
                            <p class="text-sm text-gray-600">Extra heavy-duty crates and reinforced packaging frameworks to protect high-tonnage engineering parts and goods during logistics operations.</p>
                        </div>
                    </div>
                    <div class="p-6 border-t border-gray-50 flex items-center justify-between">
                        <button onclick="quickInquiry('Industrial Packaging')" class="text-xs font-extrabold text-brandNavy hover:text-brandGold transition flex items-center gap-1">
                            <i data-lucide="plus-circle" class="w-4 h-4"></i> Add to Inquiry
                        </button>
                        <a href="#calculator" onclick="prefillConfigurator('Industrial Packaging', '7')" class="text-xs font-bold text-brandGold border border-brandGold hover:bg-brandGold hover:text-brandNavy px-3 py-1.5 rounded transition">Customize</a>
                    </div>
                </div>

                <!-- Product 6 -->
                <div class="bg-white rounded-2xl overflow-hidden shadow-md border border-gray-100 hover:shadow-xl hover:-translate-y-1 transition duration-300 flex flex-col justify-between">
                    <div>
                        <div class="relative bg-purple-100 h-48 flex items-center justify-center p-4">
                            <div class="absolute inset-0 bg-gradient-to-br from-purple-500/10 to-purple-900/10"></div>
                            <svg class="w-24 h-24 text-purple-800" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                                <polyline points="22 12 16 12 14 15 10 15 8 12 2 12"></polyline>
                                <path d="M5.45 5.11L2 12v6a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2v-6l-3.45-6.89A2 2 0 0 0 16.76 4H7.24a2 2 0 0 0-1.79 1.11z"></path>
                            </svg>
                            <span class="absolute top-3 left-3 bg-brandNavy text-brandGold font-bold text-[10px] px-2 py-1 rounded">FAST LOGISTICS</span>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-brandNavy mb-2">E-Commerce Packaging</h3>
                            <p class="text-xs text-brandGold font-extrabold uppercase tracking-wider mb-3">Self-Sealing Options</p>
                            <p class="text-sm text-gray-600">Smart mailer designs with integrated self-adhesive tapes and tear strips. Quick assembly box formats tailored for digital brands.</p>
                        </div>
                    </div>
                    <div class="p-6 border-t border-gray-50 flex items-center justify-between">
                        <button onclick="quickInquiry('E-Commerce Packaging')" class="text-xs font-extrabold text-brandNavy hover:text-brandGold transition flex items-center gap-1">
                            <i data-lucide="plus-circle" class="w-4 h-4"></i> Add to Inquiry
                        </button>
                        <a href="#calculator" onclick="prefillConfigurator('E-Commerce Packaging', '3')" class="text-xs font-bold text-brandGold border border-brandGold hover:bg-brandGold hover:text-brandNavy px-3 py-1.5 rounded transition">Customize</a>
                    </div>
                </div>

                <!-- Product 7 -->
                <div class="bg-white rounded-2xl overflow-hidden shadow-md border border-gray-100 hover:shadow-xl hover:-translate-y-1 transition duration-300 flex flex-col justify-between">
                    <div>
                        <div class="relative bg-teal-100 h-48 flex items-center justify-center p-4">
                            <div class="absolute inset-0 bg-gradient-to-br from-teal-500/10 to-teal-900/10"></div>
                            <svg class="w-24 h-24 text-teal-800" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                                <path d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2V12H12V22Z"></path>
                                <path d="M12 22C6.47715 22 2 17.5228 2 12C2 6.47715 6.47715 2 12 2V12H12V22Z"></path>
                            </svg>
                            <span class="absolute top-3 left-3 bg-brandNavy text-brandGold font-bold text-[10px] px-2 py-1 rounded">100% ORGANIC</span>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-brandNavy mb-2">Eco-Friendly Kraft Boxes</h3>
                            <p class="text-xs text-brandGold font-extrabold uppercase tracking-wider mb-3">Biodegradable Material</p>
                            <p class="text-sm text-gray-600">Produced completely with unbleached organic pulp. Naturally chemical-free and extremely elegant, presenting high-value environmental accountability.</p>
                        </div>
                    </div>
                    <div class="p-6 border-t border-gray-50 flex items-center justify-between">
                        <button onclick="quickInquiry('Eco-Friendly Kraft Boxes')" class="text-xs font-extrabold text-brandNavy hover:text-brandGold transition flex items-center gap-1">
                            <i data-lucide="plus-circle" class="w-4 h-4"></i> Add to Inquiry
                        </button>
                        <a href="#calculator" onclick="prefillConfigurator('Eco-Friendly Kraft Boxes', '3')" class="text-xs font-bold text-brandGold border border-brandGold hover:bg-brandGold hover:text-brandNavy px-3 py-1.5 rounded transition">Customize</a>
                    </div>
                </div>

                <!-- Product 8 -->
                <div class="bg-white rounded-2xl overflow-hidden shadow-md border border-gray-100 hover:shadow-xl hover:-translate-y-1 transition duration-300 flex flex-col justify-between">
                    <div>
                        <div class="relative bg-rose-100 h-48 flex items-center justify-center p-4">
                            <div class="absolute inset-0 bg-gradient-to-br from-rose-500/10 to-rose-900/10"></div>
                            <svg class="w-24 h-24 text-rose-800" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                                <path d="M12 22c5.523 0 10-4.477 10-10S17.523 2 12 2 2 6.477 2 12s4.477 10 10 10z"></path>
                                <path d="M12 8v8"></path>
                                <path d="M8 12h8"></path>
                            </svg>
                            <span class="absolute top-3 left-3 bg-brandNavy text-brandGold font-bold text-[10px] px-2 py-1 rounded">BRANDED</span>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-brandNavy mb-2">Custom Printed Packaging</h3>
                            <p class="text-xs text-brandGold font-extrabold uppercase tracking-wider mb-3">Flexo & Offset capabilities</p>
                            <p class="text-sm text-gray-600">Full color printed cartons using eco-friendly water inks. Crisp custom graphics with unmatched clarity to guarantee top tier brand unboxing presence.</p>
                        </div>
                    </div>
                    <div class="p-6 border-t border-gray-50 flex items-center justify-between">
                        <button onclick="quickInquiry('Custom Printed Packaging')" class="text-xs font-extrabold text-brandNavy hover:text-brandGold transition flex items-center gap-1">
                            <i data-lucide="plus-circle" class="w-4 h-4"></i> Add to Inquiry
                        </button>
                        <a href="#calculator" onclick="prefillConfigurator('Custom Printed Packaging', '3')" class="text-xs font-bold text-brandGold border border-brandGold hover:bg-brandGold hover:text-brandNavy px-3 py-1.5 rounded transition">Customize</a>
                    </div>
                </div>

                <!-- Product 9 -->
                <div class="bg-white rounded-2xl overflow-hidden shadow-md border border-gray-100 hover:shadow-xl hover:-translate-y-1 transition duration-300 flex flex-col justify-between">
                    <div>
                        <div class="relative bg-indigo-100 h-48 flex items-center justify-center p-4">
                            <div class="absolute inset-0 bg-gradient-to-br from-indigo-500/10 to-indigo-900/10"></div>
                            <svg class="w-24 h-24 text-indigo-800" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                                <path d="M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9"></path>
                                <path d="M13.73 21a2 2 0 0 1-3.46 0"></path>
                            </svg>
                            <span class="absolute top-3 left-3 bg-brandNavy text-brandGold font-bold text-[10px] px-2 py-1 rounded">SHOCK ABSORTION</span>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-brandNavy mb-2">Electronics Packaging</h3>
                            <p class="text-xs text-brandGold font-extrabold uppercase tracking-wider mb-3">Anti-Static foam linings</p>
                            <p class="text-sm text-gray-600">High precise structural designs combined with custom inserts to hold fragile microprocessors, phones, cameras and expensive component accessories.</p>
                        </div>
                    </div>
                    <div class="p-6 border-t border-gray-50 flex items-center justify-between">
                        <button onclick="quickInquiry('Electronics Packaging')" class="text-xs font-extrabold text-brandNavy hover:text-brandGold transition flex items-center gap-1">
                            <i data-lucide="plus-circle" class="w-4 h-4"></i> Add to Inquiry
                        </button>
                        <a href="#calculator" onclick="prefillConfigurator('Electronics Packaging', '5')" class="text-xs font-bold text-brandGold border border-brandGold hover:bg-brandGold hover:text-brandNavy px-3 py-1.5 rounded transition">Customize</a>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Dynamic Box Configurator & Quote Calculator Section -->
    <section id="calculator" class="py-20 bg-brandNavy text-white relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-start">
                
                <!-- Left Details Content Column -->
                <div class="lg:col-span-5 space-y-6 lg:sticky lg:top-28">
                    <span class="inline-block text-brandGold font-bold text-sm uppercase tracking-widest bg-brandGold/10 px-4 py-1.5 rounded-full">Interactive Tools</span>
                    <h2 class="text-3xl sm:text-4xl font-black">
                        Custom Box <span class="text-brandGold">Dimension Engine</span>
                    </h2>
                    <p class="text-gray-300">
                        Input your product dimensions below. Our real-time quoting engine will estimate parameters, recommended board thickness (plys), and simulated tier pricing.
                    </p>
                    <div class="bg-brandNavy-light p-6 rounded-xl border border-brandGold/20 space-y-3 text-xs">
                        <h4 class="font-bold text-brandGold uppercase tracking-wider flex items-center">
                            <i data-lucide="info" class="w-4 h-4 mr-2"></i> Real-time Estimator logic
                        </h4>
                        <ul class="space-y-1.5 text-gray-300">
                            <li>• Price is calculated dynamically based on overall surface area.</li>
                            <li>• High ply specifications increase sturdiness and durability parameters.</li>
                            <li>• Custom branding toggles standard design plate setup costs.</li>
                            <li>• Volume tier discount applied automatically: <strong>&gt;1000 units (10%), &gt;5000 units (25% off)</strong>.</li>
                        </ul>
                    </div>
                </div>

                <!-- Right Configurator Form -->
                <div class="lg:col-span-7 bg-white text-gray-800 p-8 rounded-2xl shadow-2xl border border-gray-100">
                    <form id="quoteForm" onsubmit="handleCalculatorSubmit(event)" class="space-y-6">
                        
                        <!-- Box Material Selection -->
                        <div>
                            <label class="block text-sm font-extrabold text-brandNavy mb-2">1. Select Packaging Category</label>
                            <select id="calc-category" class="w-full border-2 border-gray-200 focus:border-brandGold focus:ring-0 rounded-xl p-3 text-sm font-medium" onchange="calculateRealTimeQuote()">
                                <option value="Corrugated Boxes">Corrugated Shipping Box (Heavy duty)</option>
                                <option value="Carton Boxes">Standard Duplex Carton (Retail)</option>
                                <option value="Premium Gift Boxes">Premium Rigid Gift Box (Luxury)</option>
                                <option value="E-Commerce Packaging">Self-Sealing Mailer Box (Quick Assemble)</option>
                                <option value="Eco-Friendly Kraft Boxes">Organic Bio-Kraft Box</option>
                                <option value="Electronics Packaging">Anti-Static Engineered Packaging</option>
                            </select>
                        </div>

                        <!-- Ply Strength -->
                        <div>
                            <label class="block text-sm font-extrabold text-brandNavy mb-2">2. Structure Thickness (Ply Strength)</label>
                            <div class="grid grid-cols-3 gap-3">
                                <label class="border-2 border-gray-100 rounded-xl p-3 flex flex-col items-center justify-center cursor-pointer hover:border-brandGold transition text-center select-none" id="label-ply-3">
                                    <input type="radio" name="calc-ply" value="3" class="sr-only" checked onchange="updatePlyUI('3')">
                                    <span class="font-black text-lg text-brandNavy">3-Ply</span>
                                    <span class="text-[10px] text-gray-500 font-medium">Standard Retail</span>
                                </label>
                                <label class="border-2 border-gray-100 rounded-xl p-3 flex flex-col items-center justify-center cursor-pointer hover:border-brandGold transition text-center select-none" id="label-ply-5">
                                    <input type="radio" name="calc-ply" value="5" class="sr-only" onchange="updatePlyUI('5')">
                                    <span class="font-black text-lg text-brandNavy">5-Ply</span>
                                    <span class="text-[10px] text-gray-500 font-medium">Heavy Shipping</span>
                                </label>
                                <label class="border-2 border-gray-100 rounded-xl p-3 flex flex-col items-center justify-center cursor-pointer hover:border-brandGold transition text-center select-none" id="label-ply-7">
                                    <input type="radio" name="calc-ply" value="7" class="sr-only" onchange="updatePlyUI('7')">
                                    <span class="font-black text-lg text-brandNavy">7-Ply</span>
                                    <span class="text-[10px] text-gray-500 font-medium">Ultra Industrial</span>
                                </label>
                            </div>
                        </div>

                        <!-- Sizing sliders / Dimension inputs -->
                        <div>
                            <label class="block text-sm font-extrabold text-brandNavy mb-4">3. Dimensions (Centimeters)</label>
                            <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                                <div class="space-y-1">
                                    <div class="flex justify-between text-xs font-bold text-gray-500">
                                        <span>Length (L)</span>
                                        <span id="length-val" class="text-brandGold">20 cm</span>
                                    </div>
                                    <input type="range" id="calc-length" min="5" max="100" value="20" class="w-full accent-brandGold" oninput="calculateRealTimeQuote()">
                                </div>
                                <div class="space-y-1">
                                    <div class="flex justify-between text-xs font-bold text-gray-500">
                                        <span>Width (W)</span>
                                        <span id="width-val" class="text-brandGold">20 cm</span>
                                    </div>
                                    <input type="range" id="calc-width" min="5" max="100" value="20" class="w-full accent-brandGold" oninput="calculateRealTimeQuote()">
                                </div>
                                <div class="space-y-1">
                                    <div class="flex justify-between text-xs font-bold text-gray-500">
                                        <span>Height (H)</span>
                                        <span id="height-val" class="text-brandGold">15 cm</span>
                                    </div>
                                    <input type="range" id="calc-height" min="5" max="80" value="15" class="w-full accent-brandGold" oninput="calculateRealTimeQuote()">
                                </div>
                            </div>
                        </div>

                        <!-- Printing and quantity configurations -->
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-sm font-extrabold text-brandNavy mb-2">4. Branding & Custom Printing</label>
                                <select id="calc-print" class="w-full border-2 border-gray-200 focus:border-brandGold focus:ring-0 rounded-xl p-3 text-sm font-medium" onchange="calculateRealTimeQuote()">
                                    <option value="none">No Printing (Plain Kraft/Brown)</option>
                                    <option value="single">Single Color Branding</option>
                                    <option value="multi">Multi-Color Printed Graphic</option>
                                </select>
                            </div>
                            <div>
                                <label class="block text-sm font-extrabold text-brandNavy mb-2">5. Quantity Required</label>
                                <input type="number" id="calc-qty" min="100" value="1000" class="w-full border-2 border-gray-200 focus:border-brandGold focus:ring-0 rounded-xl p-2.5 text-sm font-semibold text-brandNavy" oninput="calculateRealTimeQuote()">
                                <p class="text-[10px] text-gray-400 mt-1">Minimum order starts from 100 pcs</p>
                            </div>
                        </div>

                        <!-- Interactive Calculation Display Area -->
                        <div class="bg-brandKraft p-6 rounded-2xl border-2 border-brandGold/30">
                            <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center border-b border-gray-200 pb-4 mb-4">
                                <div>
                                    <p class="text-xs font-bold text-gray-400 uppercase tracking-widest">Estimated Price (per pc)</p>
                                    <span id="unit-price" class="text-3xl font-black text-brandNavy">₹ 14.20</span>
                                </div>
                                <div class="mt-2 sm:mt-0 bg-emerald-100 text-emerald-800 text-[10px] font-black px-3 py-1 rounded-full uppercase tracking-wider" id="discount-badge">
                                    Volume Discount Active (10% Off)
                                </div>
                            </div>
                            <div class="flex justify-between items-end">
                                <div>
                                    <p class="text-xs text-gray-500 font-bold">Total Quote Estimate (Excl. Tax)</p>
                                    <span id="total-price" class="text-xl font-black text-brandGold-dark">₹ 14,200.00</span>
                                </div>
                                <button type="submit" class="bg-brandGold text-brandNavy font-black text-xs px-6 py-3 rounded-xl shadow-lg hover:bg-brandGold-light transition duration-300 uppercase tracking-wider flex items-center">
                                    <i data-lucide="plus" class="w-4 h-4 mr-1"></i> Add To Inquiry Box
                                </button>
                            </div>
                        </div>

                    </form>
                </div>

            </div>
        </div>
    </section>

    <!-- Industries We Serve Section -->
    <section id="industries" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-16 space-y-4">
                <span class="text-brandGold font-bold text-sm uppercase tracking-widest bg-brandGold/10 px-4 py-1.5 rounded-full">Sectors</span>
                <h2 class="text-3xl sm:text-4xl font-black text-brandNavy">Industries We Serve</h2>
                <p class="text-gray-500">Perfectly customized solutions matching critical regulatory standards across domains.</p>
            </div>

            <!-- Grid matching items in Flyer -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6 text-center">
                <div class="p-6 bg-brandKraft rounded-2xl border border-gray-100 hover:border-brandGold hover:shadow-lg transition">
                    <div class="mx-auto w-12 h-12 rounded-full bg-brandGold/15 flex items-center justify-center text-brandGold mb-4">
                        <i data-lucide="laptop" class="w-6 h-6"></i>
                    </div>
                    <h3 class="font-extrabold text-brandNavy text-sm">E-Commerce</h3>
                </div>
                <div class="p-6 bg-brandKraft rounded-2xl border border-gray-100 hover:border-brandGold hover:shadow-lg transition">
                    <div class="mx-auto w-12 h-12 rounded-full bg-brandGold/15 flex items-center justify-center text-brandGold mb-4">
                        <i data-lucide="shopping-bag" class="w-6 h-6"></i>
                    </div>
                    <h3 class="font-extrabold text-brandNavy text-sm">FMCG</h3>
                </div>
                <div class="p-6 bg-brandKraft rounded-2xl border border-gray-100 hover:border-brandGold hover:shadow-lg transition">
                    <div class="mx-auto w-12 h-12 rounded-full bg-brandGold/15 flex items-center justify-center text-brandGold mb-4">
                        <i data-lucide="activity" class="w-6 h-6"></i>
                    </div>
                    <h3 class="font-extrabold text-brandNavy text-sm">Pharmaceuticals</h3>
                </div>
                <div class="p-6 bg-brandKraft rounded-2xl border border-gray-100 hover:border-brandGold hover:shadow-lg transition">
                    <div class="mx-auto w-12 h-12 rounded-full bg-brandGold/15 flex items-center justify-center text-brandGold mb-4">
                        <i data-lucide="utensils" class="w-6 h-6"></i>
                    </div>
                    <h3 class="font-extrabold text-brandNavy text-sm">Food & Beverage</h3>
                </div>
                <div class="p-6 bg-brandKraft rounded-2xl border border-gray-100 hover:border-brandGold hover:shadow-lg transition">
                    <div class="mx-auto w-12 h-12 rounded-full bg-brandGold/15 flex items-center justify-center text-brandGold mb-4">
                        <i data-lucide="heart" class="w-6 h-6"></i>
                    </div>
                    <h3 class="font-extrabold text-brandNavy text-sm">Cosmetics</h3>
                </div>
                <div class="p-6 bg-brandKraft rounded-2xl border border-gray-100 hover:border-brandGold hover:shadow-lg transition">
                    <div class="mx-auto w-12 h-12 rounded-full bg-brandGold/15 flex items-center justify-center text-brandGold mb-4">
                        <i data-lucide="cpu" class="w-6 h-6"></i>
                    </div>
                    <h3 class="font-extrabold text-brandNavy text-sm">Electronics</h3>
                </div>
                <div class="p-6 bg-brandKraft rounded-2xl border border-gray-100 hover:border-brandGold hover:shadow-lg transition">
                    <div class="mx-auto w-12 h-12 rounded-full bg-brandGold/15 flex items-center justify-center text-brandGold mb-4">
                        <i data-lucide="shirt" class="w-6 h-6"></i>
                    </div>
                    <h3 class="font-extrabold text-brandNavy text-sm">Textile & Apparel</h3>
                </div>
                <div class="p-6 bg-brandKraft rounded-2xl border border-gray-100 hover:border-brandGold hover:shadow-lg transition">
                    <div class="mx-auto w-12 h-12 rounded-full bg-brandGold/15 flex items-center justify-center text-brandGold mb-4">
                        <i data-lucide="settings" class="w-6 h-6"></i>
                    </div>
                    <h3 class="font-extrabold text-brandNavy text-sm">Industrial Mfg.</h3>
                </div>
            </div>
        </div>
    </section>

    <!-- Our Strengths Section -->
    <section id="strengths" class="py-20 bg-brandKraft">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-16 space-y-4">
                <span class="text-brandGold font-bold text-sm uppercase tracking-widest bg-brandGold/10 px-4 py-1.5 rounded-full">Core Strengths</span>
                <h2 class="text-3xl sm:text-4xl font-black text-brandNavy">Our Corporate Pillars</h2>
                <p class="text-gray-500">How we deliver on our promises to keep your shipping flow running uninterruptedly.</p>
            </div>

            <!-- Strengths Cards Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Strength 1 -->
                <div class="bg-white p-8 rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition">
                    <div class="w-12 h-12 rounded-xl bg-brandGold/10 flex items-center justify-center text-brandGold mb-6">
                        <i data-lucide="shield-check" class="w-6 h-6"></i>
                    </div>
                    <h3 class="text-lg font-bold text-brandNavy mb-2">Quality Assurance</h3>
                    <p class="text-sm text-gray-500 leading-relaxed">Strict quality verification protocols executed across every single processing step—from raw paper board intake to visual box construction.</p>
                </div>
                <!-- Strength 2 -->
                <div class="bg-white p-8 rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition">
                    <div class="w-12 h-12 rounded-xl bg-brandGold/10 flex items-center justify-center text-brandGold mb-6">
                        <i data-lucide="pen-tool" class="w-6 h-6"></i>
                    </div>
                    <h3 class="text-lg font-bold text-brandNavy mb-2">Innovative Designs</h3>
                    <p class="text-sm text-gray-500 leading-relaxed">Expert packaging engineers designing functional shapes. Custom fit interior inserts that eliminate shipping displacement.</p>
                </div>
                <!-- Strength 3 -->
                <div class="bg-white p-8 rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition">
                    <div class="w-12 h-12 rounded-xl bg-brandGold/10 flex items-center justify-center text-brandGold mb-6">
                        <i data-lucide="palette" class="w-6 h-6"></i>
                    </div>
                    <h3 class="text-lg font-bold text-brandNavy mb-2">Custom Branding</h3>
                    <p class="text-sm text-gray-500 leading-relaxed">Maximize shelf identity. Highly premium custom flexo-graphic and offset prints turning containers into mobile brand ambassadors.</p>
                </div>
                <!-- Strength 4 -->
                <div class="bg-white p-8 rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition">
                    <div class="w-12 h-12 rounded-xl bg-brandGold/10 flex items-center justify-center text-brandGold mb-6">
                        <i data-lucide="zap" class="w-6 h-6"></i>
                    </div>
                    <h3 class="text-lg font-bold text-brandNavy mb-2">Fast Delivery</h3>
                    <p class="text-xs bg-emerald-100 text-emerald-800 font-extrabold px-2 py-0.5 rounded inline-block mb-3">Strong Logistics Partner</p>
                    <p class="text-sm text-gray-500 leading-relaxed">On-time guaranteed supply chains leveraging state level warehousing partnerships to prevent business shipping pauses.</p>
                </div>
                <!-- Strength 5 -->
                <div class="bg-white p-8 rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition">
                    <div class="w-12 h-12 rounded-xl bg-brandGold/10 flex items-center justify-center text-brandGold mb-6">
                        <i data-lucide="coins" class="w-6 h-6"></i>
                    </div>
                    <h3 class="text-lg font-bold text-brandNavy mb-2">Competitive Pricing</h3>
                    <p class="text-sm text-gray-500 leading-relaxed">Direct manufacturing-based pricing frameworks engineered without mediator fees. Maximum cost optimization benefits for bulk items.</p>
                </div>
                <!-- Strength 6 -->
                <div class="bg-white p-8 rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition">
                    <div class="w-12 h-12 rounded-xl bg-brandGold/10 flex items-center justify-center text-brandGold mb-6">
                        <i data-lucide="users" class="w-6 h-6"></i>
                    </div>
                    <h3 class="text-lg font-bold text-brandNavy mb-2">Professional Service</h3>
                    <p class="text-sm text-gray-500 leading-relaxed">A specialized packaging solutions sales crew available around the clock to organize dimensions, box samples, and logistics support.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Vision, Mission and Slogan cards block -->
    <section class="py-16 bg-[#12243C] text-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                <!-- Vision -->
                <div class="p-8 bg-brandNavy-light rounded-2xl border border-brandGold/20 space-y-4">
                    <div class="flex items-center space-x-3 text-brandGold">
                        <i data-lucide="eye" class="w-8 h-8"></i>
                        <h3 class="text-2xl font-black uppercase tracking-wider">Our Vision</h3>
                    </div>
                    <p class="text-gray-300 text-sm leading-relaxed">
                        To become India's most trusted and sustainable packaging solutions brand. We aim to define industry benchmarks by providing completely eco-safe, visually stellar, and high-quality logistics packaging.
                    </p>
                </div>
                <!-- Mission -->
                <div class="p-8 bg-brandNavy-light rounded-2xl border border-brandGold/20 space-y-4">
                    <div class="flex items-center space-x-3 text-brandGold">
                        <i data-lucide="target" class="w-8 h-8"></i>
                        <h3 class="text-2xl font-black uppercase tracking-wider">Our Mission</h3>
                    </div>
                    <p class="text-gray-300 text-sm leading-relaxed">
                        To build highly reliable packaging products that protect shipments, secure goods during rough freight, strengthen client branding parameters, and foster clean recycling habits for a healthier earth.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Interactive Contact Form & Details Section -->
    <section id="contact" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
                
                <!-- Left Details Column -->
                <div class="lg:col-span-5 space-y-8">
                    <div class="space-y-4">
                        <span class="text-brandGold font-bold text-sm uppercase tracking-widest bg-brandGold/10 px-4 py-1.5 rounded-full">Contact Box Craft</span>
                        <h2 class="text-3xl sm:text-4xl font-black text-brandNavy">Ready to Upgrade Your Packaging?</h2>
                        <p class="text-gray-500">Connect with a Box Craft packaging consultant today. Let's design safe, sustainable, and memorable unboxing experiences together.</p>
                    </div>

                    <!-- Direct Contacts Cards -->
                    <div class="space-y-4">
                        <div class="flex items-center space-x-4 p-4 bg-brandKraft rounded-xl border border-gray-100">
                            <div class="w-12 h-12 rounded-lg bg-brandGold/15 flex items-center justify-center text-brandGold-dark">
                                <i data-lucide="phone-call" class="w-6 h-6"></i>
                            </div>
                            <div>
                                <p class="text-xs font-bold text-gray-400 uppercase">Support Hotline</p>
                                <a href="tel:8929131333" class="text-base font-extrabold text-brandNavy hover:underline">+91 8929131333</a>
                            </div>
                        </div>

                        <div class="flex items-center space-x-4 p-4 bg-brandKraft rounded-xl border border-gray-100">
                            <div class="w-12 h-12 rounded-lg bg-brandGold/15 flex items-center justify-center text-brandGold-dark">
                                <i data-lucide="mail" class="w-6 h-6"></i>
                            </div>
                            <div class="flex-1 min-w-0">
                                <p class="text-xs font-bold text-gray-400 uppercase">Email Inbox</p>
                                <div class="flex items-center justify-between">
                                    <a href="mailto:yadavdushyant494@gmail.com" class="text-sm sm:text-base font-extrabold text-brandNavy truncate hover:underline">yadavdushyant494@gmail.com</a>
                                    <button onclick="copyEmailToClipboard()" class="text-xs text-brandGold hover:text-brandGold-dark font-semibold">Copy</button>
                                </div>
                            </div>
                        </div>

                        <div class="flex items-center space-x-4 p-4 bg-brandKraft rounded-xl border border-gray-100">
                            <div class="w-12 h-12 rounded-lg bg-brandGold/15 flex items-center justify-center text-brandGold-dark">
                                <i data-lucide="map-pin" class="w-6 h-6"></i>
                            </div>
                            <div>
                                <p class="text-xs font-bold text-gray-400 uppercase">Registered Location</p>
                                <p class="text-sm font-extrabold text-brandNavy">New Delhi, India</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Right Contact Form / Inquiry Box -->
                <div class="lg:col-span-7 bg-brandKraft p-8 rounded-2xl border border-gray-100">
                    <h3 class="text-xl font-bold text-brandNavy mb-6 flex items-center">
                        <i data-lucide="send" class="w-5 h-5 mr-2 text-brandGold"></i> Direct Inquiry Message
                    </h3>
                    <form id="contact-form" onsubmit="handleContactSubmit(event)" class="space-y-4">
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-xs font-bold uppercase text-gray-500 mb-1">Your Name</label>
                                <input type="text" id="contact-name" required class="w-full border-2 border-gray-200 focus:border-brandGold focus:ring-0 rounded-xl p-3 text-sm font-semibold" placeholder="Full Name">
                            </div>
                            <div>
                                <label class="block text-xs font-bold uppercase text-gray-500 mb-1">Company / Brand Name</label>
                                <input type="text" id="contact-company" class="w-full border-2 border-gray-200 focus:border-brandGold focus:ring-0 rounded-xl p-3 text-sm font-semibold" placeholder="Company Name">
                            </div>
                        </div>

                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-xs font-bold uppercase text-gray-500 mb-1">Mobile Number</label>
                                <input type="tel" id="contact-phone" required class="w-full border-2 border-gray-200 focus:border-brandGold focus:ring-0 rounded-xl p-3 text-sm font-semibold" placeholder="10 Digit Mobile">
                            </div>
                            <div>
                                <label class="block text-xs font-bold uppercase text-gray-500 mb-1">Email Address</label>
                                <input type="email" id="contact-email" required class="w-full border-2 border-gray-200 focus:border-brandGold focus:ring-0 rounded-xl p-3 text-sm font-semibold" placeholder="you@domain.com">
                            </div>
                        </div>

                        <div>
                            <label class="block text-xs font-bold uppercase text-gray-500 mb-1">Write your packaging requirements</label>
                            <textarea id="contact-msg" rows="4" required class="w-full border-2 border-gray-200 focus:border-brandGold focus:ring-0 rounded-xl p-3 text-sm font-semibold" placeholder="Please outline box size, plys, expected quantities or any design queries..."></textarea>
                        </div>

                        <button type="submit" class="w-full bg-brandNavy text-brandGold font-extrabold py-4 rounded-xl shadow-lg hover:bg-brandNavy-dark transition flex items-center justify-center gap-2">
                            <i data-lucide="mail-check" class="w-5 h-5"></i> Send Corporate Inquiry
                        </button>
                    </form>
                </div>

            </div>
        </div>
    </section>

    <!-- Floating AI Packaging Assistant Badge / Chat UI -->
    <div class="fixed bottom-6 right-6 z-50">
        <!-- AI trigger icon button -->
        <button onclick="toggleAIChat()" id="ai-chat-btn" class="bg-brandNavy text-brandGold border border-brandGold/40 p-4 rounded-full shadow-2xl flex items-center justify-center hover:bg-brandNavy-light transition pulse-gold focus:outline-none">
            <i data-lucide="bot" class="w-7 h-7"></i>
            <span class="absolute -top-1 -right-1 bg-red-600 text-white text-[8px] font-bold px-1.5 py-0.5 rounded-full uppercase">Ask AI</span>
        </button>

        <!-- AI Chat window box -->
        <div id="ai-chat-window" class="hidden absolute bottom-16 right-0 w-80 sm:w-96 bg-brandNavy-dark text-white rounded-2xl shadow-2xl border border-brandGold/30 flex flex-col overflow-hidden max-h-[500px]">
            <!-- Header bar -->
            <div class="bg-brandNavy p-4 border-b border-brandGold/30 flex items-center justify-between">
                <div class="flex items-center space-x-2">
                    <div class="p-1.5 bg-brandGold/10 rounded-lg text-brandGold">
                        <i data-lucide="bot" class="w-5 h-5"></i>
                    </div>
                    <div>
                        <h4 class="font-bold text-sm">Box Craft AI Consultant</h4>
                        <span class="text-[10px] text-emerald-400 flex items-center"><span class="w-1.5 h-1.5 rounded-full bg-emerald-400 mr-1 animate-pulse"></span> Intelligent Assistant</span>
                    </div>
                </div>
                <button onclick="toggleAIChat()" class="text-gray-400 hover:text-white">
                    <i data-lucide="x" class="w-5 h-5"></i>
                </button>
            </div>

            <!-- Messages Stream -->
            <div id="ai-messages-stream" class="p-4 overflow-y-auto space-y-4 h-80 custom-scrollbar text-xs">
                <div class="bg-brandNavy/40 p-3 rounded-lg border border-brandGold/15">
                    <p class="font-semibold text-brandGold mb-1">Box Craft AI Bot:</p>
                    <p>Namaste! I am your Box Craft packaging guide. Describe what you want to package (e.g. weight, fragility, item name) and I will suggest the best box, ply specification, and dimensions for you!</p>
                </div>
            </div>

            <!-- Input area -->
            <div class="p-3 border-t border-brandGold/20 bg-brandNavy">
                <form id="ai-chat-form" onsubmit="handleAIConsultantSubmit(event)" class="flex space-x-2">
                    <input type="text" id="ai-user-query" required placeholder="What is the best ply for shipping mugs?" class="flex-1 bg-brandNavy-dark border border-brandGold/30 focus:border-brandGold focus:ring-0 text-white text-xs p-2.5 rounded-xl">
                    <button type="submit" class="bg-brandGold text-brandNavy p-2.5 rounded-xl hover:bg-brandGold-light transition flex items-center justify-center">
                        <i data-lucide="send" class="w-4 h-4"></i>
                    </button>
                </form>
            </div>
        </div>
    </div>

    <!-- Inquiry List Modal / Shopping Cart -->
    <div id="inquiry-modal" class="fixed inset-0 bg-brandNavy/60 backdrop-blur-sm z-50 flex items-center justify-center hidden p-4">
        <div class="bg-white text-gray-800 rounded-2xl shadow-2xl border border-gray-100 max-w-xl w-full max-h-[85vh] flex flex-col overflow-hidden">
            <!-- Header -->
            <div class="bg-brandNavy text-white p-6 flex items-center justify-between border-b border-brandGold/30">
                <div class="flex items-center space-x-2">
                    <i data-lucide="shopping-cart" class="text-brandGold w-5 h-5"></i>
                    <h3 class="text-xl font-bold">Your Custom Inquiry Basket</h3>
                </div>
                <button onclick="toggleInquiryModal()" class="text-gray-400 hover:text-white"><i data-lucide="x" class="w-6 h-6"></i></button>
            </div>

            <!-- List of items -->
            <div id="inquiry-items-container" class="p-6 overflow-y-auto flex-1 space-y-4 custom-scrollbar">
                <!-- Injected via JavaScript dynamically -->
                <p class="text-gray-500 text-center py-8">Your inquiry basket is empty. Click "Add to Inquiry" on any product category to configure!</p>
            </div>

            <!-- Modal Action Buttons -->
            <div class="bg-brandKraft p-6 border-t border-gray-100 flex flex-col space-y-3">
                <button onclick="submitConsolidatedInquiry()" id="modal-submit-btn" class="w-full bg-brandGold text-brandNavy font-extrabold py-3.5 rounded-xl text-sm shadow-md hover:bg-brandGold-light transition disabled:opacity-50 disabled:cursor-not-allowed">
                    Proceed with inquiry message
                </button>
                <p class="text-[10px] text-gray-400 text-center">We will cross verify specifications and respond over call/email inside 2 working hours.</p>
            </div>
        </div>
    </div>

    <!-- Success Feedback Custom Toast Message -->
    <div id="success-toast" class="fixed top-24 left-1/2 transform -translate-x-1/2 bg-emerald-600 text-white font-extrabold px-6 py-3.5 rounded-xl shadow-2xl z-50 hidden items-center space-x-2 text-sm">
        <i data-lucide="check-circle" class="w-5 h-5"></i>
        <span id="toast-message">Success message has been processed!</span>
    </div>

    <!-- Footer Area -->
    <footer class="bg-brandNavy-dark text-white pt-16 pb-8 border-t border-brandGold/30">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 md:grid-cols-4 gap-12">
            
            <!-- Branding details column -->
            <div class="space-y-4">
                <div class="flex items-center space-x-3">
                    <div class="bg-brandGold p-2 rounded">
                        <svg class="w-6 h-6 text-brandNavy" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
                            <path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"></path>
                            <polyline points="3.27 6.96 12 12.01 20.73 6.96"></polyline>
                        </svg>
                    </div>
                    <span class="text-xl font-black text-white">BOX <span class="text-brandGold">CRAFT</span></span>
                </div>
                <p class="text-xs text-gray-400 leading-relaxed">
                    India's premium packaging manufacturer specializing in structural stability, visual branding values, and environment friendly organic pulp sheets.
                </p>
                <div class="flex space-x-3 pt-2">
                    <a href="https://wa.me/918929131333" target="_blank" class="w-8 h-8 rounded-full bg-brandNavy border border-brandGold/20 flex items-center justify-center text-brandGold hover:bg-brandGold hover:text-brandNavy transition"><i data-lucide="phone" class="w-4 h-4"></i></a>
                    <a href="mailto:yadavdushyant494@gmail.com" class="w-8 h-8 rounded-full bg-brandNavy border border-brandGold/20 flex items-center justify-center text-brandGold hover:bg-brandGold hover:text-brandNavy transition"><i data-lucide="mail" class="w-4 h-4"></i></a>
                </div>
            </div>

            <!-- Quick Links -->
            <div class="space-y-4">
                <h4 class="font-bold text-brandGold text-sm uppercase tracking-wider">Quick Links</h4>
                <ul class="space-y-2 text-xs text-gray-400 font-medium">
                    <li><a href="#about" class="hover:text-brandGold transition">Who We Are</a></li>
                    <li><a href="#products" class="hover:text-brandGold transition">Our Products</a></li>
                    <li><a href="#industries" class="hover:text-brandGold transition">Industries We Serve</a></li>
                    <li><a href="#strengths" class="hover:text-brandGold transition">Core Strengths</a></li>
                    <li><a href="#calculator" class="hover:text-brandGold transition">Box Custom Estimator</a></li>
                </ul>
            </div>

            <!-- Slogan options and direct stats -->
            <div class="space-y-4 col-span-1">
                <h4 class="font-bold text-brandGold text-sm uppercase tracking-wider">Our Slogans</h4>
                <ul class="space-y-2.5 text-[11px] text-gray-400 font-medium italic">
                    <li>"Think Inside the Box, Think BOX CRAFT"</li>
                    <li>"Strong Boxes, Strong Brands"</li>
                    <li>"Packaging Excellence, Delivered Perfectly"</li>
                    <li>"Every Box Tells a Story"</li>
                </ul>
            </div>

            <!-- Scanning Mock Simulator QR -->
            <div class="space-y-4 text-center sm:text-left">
                <h4 class="font-bold text-brandGold text-sm uppercase tracking-wider">Interactive Scan Support</h4>
                <div class="inline-block p-2 bg-white rounded-xl shadow-lg border border-brandGold/20">
                    <!-- Custom SVG representing QR Code -->
                    <svg class="w-24 h-24 text-brandNavy" viewBox="0 0 100 100" fill="currentColor">
                        <!-- Top-Left Finder Pattern -->
                        <rect x="10" y="10" width="25" height="25" fill="#0A1C36"/>
                        <rect x="15" y="15" width="15" height="15" fill="white"/>
                        <rect x="18" y="18" width="9" height="9" fill="#D4AF37"/>
                        
                        <!-- Top-Right Finder Pattern -->
                        <rect x="65" y="10" width="25" height="25" fill="#0A1C36"/>
                        <rect x="70" y="15" width="15" height="15" fill="white"/>
                        <rect x="73" y="18" width="9" height="9" fill="#D4AF37"/>
                        
                        <!-- Bottom-Left Finder Pattern -->
                        <rect x="10" y="65" width="25" height="25" fill="#0A1C36"/>
                        <rect x="15" y="70" width="15" height="15" fill="white"/>
                        <rect x="18" y="73" width="9" height="9" fill="#D4AF37"/>
                        
                        <!-- Random Simulated QR blocks -->
                        <rect x="42" y="15" width="6" height="6"/>
                        <rect x="52" y="25" width="6" height="6"/>
                        <rect x="42" y="35" width="6" height="6"/>
                        <rect x="15" y="45" width="6" height="6"/>
                        <rect x="25" y="55" width="6" height="6"/>
                        <rect x="35" y="45" width="6" height="6"/>
                        <rect x="45" y="55" width="6" height="6"/>
                        <rect x="55" y="45" width="6" height="6"/>
                        
                        <rect x="75" y="45" width="6" height="6"/>
                        <rect x="85" y="55" width="6" height="6"/>
                        <rect x="65" y="65" width="6" height="6"/>
                        <rect x="75" y="75" width="6" height="6"/>
                        <rect x="85" y="85" width="6" height="6"/>
                    </svg>
                </div>
                <p class="text-[9px] text-gray-400">Scan for direct packaging contact</p>
            </div>

        </div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mt-12 pt-8 border-t border-brandGold/10 flex flex-col md:flex-row justify-between items-center text-xs text-gray-500">
            <p>© 2026 Box Craft Packaging Solutions. All Rights Reserved.</p>
            <p class="mt-2 md:mt-0 flex items-center gap-1">SAFE PACKAGING <span class="text-brandGold">•</span> STRONGER BRAND <span class="text-brandGold">•</span> BETTER TOMORROW</p>
        </div>
    </footer>

    <!-- JavaScript Interactions Logic -->
    <script>
        // Init Lucide Icons
        lucide.createIcons();

        // Application State
        const state = {
            inquiryCart: [],
            aiChatActive: false,
            apiInProgress: false,
            selectedPly: "3"
        };

        const apiKey = ""; // Provided automatically at runtime

        // Navigation Menu Helpers
        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            const icon = document.getElementById('menu-icon');
            const isHidden = menu.classList.contains('hidden');
            if (isHidden) {
                menu.classList.remove('hidden');
                icon.setAttribute('data-lucide', 'x');
            } else {
                menu.classList.add('hidden');
                icon.setAttribute('data-lucide', 'menu');
            }
            lucide.createIcons();
        }

        // Custom Modal Controllers
        function toggleInquiryModal() {
            const modal = document.getElementById('inquiry-modal');
            const isHidden = modal.classList.contains('hidden');
            if (isHidden) {
                modal.classList.remove('hidden');
                renderInquiryCart();
            } else {
                modal.classList.add('hidden');
            }
        }

        // Ply radio selector UI decorator
        function updatePlyUI(ply) {
            state.selectedPly = ply;
            const labels = ['3', '5', '7'];
            labels.forEach(l => {
                const el = document.getElementById(`label-ply-${l}`);
                if (l === ply) {
                    el.classList.add('border-brandGold', 'bg-brandGold/10');
                    el.classList.remove('border-gray-100');
                } else {
                    el.classList.remove('border-brandGold', 'bg-brandGold/10');
                    el.classList.add('border-gray-100');
                }
            });
            calculateRealTimeQuote();
        }

        // Real-Time Math Quote Logic
        function calculateRealTimeQuote() {
            const category = document.getElementById('calc-category').value;
            const length = parseFloat(document.getElementById('calc-length').value);
            const width = parseFloat(document.getElementById('calc-width').value);
            const height = parseFloat(document.getElementById('calc-height').value);
            const printType = document.getElementById('calc-print').value;
            const quantity = parseInt(document.getElementById('calc-qty').value) || 100;

            // Render slider labels
            document.getElementById('length-val').innerText = `${length} cm`;
            document.getElementById('width-val').innerText = `${width} cm`;
            document.getElementById('height-val').innerText = `${height} cm`;

            // Core Surface Area math: 2 * (LW + WH + LH)
            const surfaceAreaSqCm = 2 * ((length * width) + (width * height) + (length * height));

            // Rates base calculation (rupees per square centimeter)
            let categoryMultiplier = 0.005; // Base rate
            if (category === "Premium Gift Boxes") categoryMultiplier = 0.015;
            if (category === "Industrial Packaging") categoryMultiplier = 0.008;
            if (category === "Electronics Packaging") categoryMultiplier = 0.012;

            let basePrice = surfaceAreaSqCm * categoryMultiplier;

            // Ply adjustment
            const plyFactor = state.selectedPly === "3" ? 1.0 : state.selectedPly === "5" ? 1.5 : 2.2;
            basePrice *= plyFactor;

            // Custom printing fees
            let printingFixed = 0;
            let printingPerUnit = 0;
            if (printType === "single") {
                printingFixed = 150;
                printingPerUnit = 1.25;
            } else if (printType === "multi") {
                printingFixed = 450;
                printingPerUnit = 2.50;
            }

            let unitPrice = basePrice + printingPerUnit + (printingFixed / quantity);

            // Cap a Minimum practical unboxing cost based on ply
            const minAllowed = parseFloat(state.selectedPly) * 2.5;
            if (unitPrice < minAllowed) unitPrice = minAllowed;

            // Apply Volume tier discounts
            let discountPercentage = 0;
            const badge = document.getElementById('discount-badge');
            if (quantity >= 5000) {
                discountPercentage = 25;
                badge.innerText = "Volume Discount Active (25% Off)";
                badge.classList.remove('hidden');
            } else if (quantity >= 1000) {
                discountPercentage = 10;
                badge.innerText = "Volume Discount Active (10% Off)";
                badge.classList.remove('hidden');
            } else {
                badge.classList.add('hidden');
            }

            const discountedUnitPrice = unitPrice * (1 - (discountPercentage / 100));
            const totalCostValue = discountedUnitPrice * quantity;

            // Format UI Currency
            document.getElementById('unit-price').innerText = `₹ ${discountedUnitPrice.toFixed(2)}`;
            document.getElementById('total-price').innerText = `₹ ${totalCostValue.toLocaleString('en-IN', { minimumFractionDigits: 2, maximumFractionDigits: 2 })}`;
        }

        // Custom Quick Add Catalog Action
        function quickInquiry(productName) {
            const newItem = {
                id: Date.now(),
                name: productName,
                category: productName,
                ply: "3",
                length: 25,
                width: 25,
                height: 15,
                print: "none",
                qty: 1000,
                unitPrice: 12.50,
                total: 12500.00
            };
            state.inquiryCart.push(newItem);
            updateCartBadges();
            showSuccessToast(`Added ${productName} to inquiry basket!`);
        }

        // Prefill config button handler
        function prefillConfigurator(category, plyStr) {
            document.getElementById('calc-category').value = category;
            updatePlyUI(plyStr);
            calculateRealTimeQuote();
            // Smooth navigate
            document.getElementById('calculator').scrollIntoView({ behavior: 'smooth' });
        }

        // Calculator configuration submit action
        function handleCalculatorSubmit(event) {
            event.preventDefault();

            const category = document.getElementById('calc-category').value;
            const length = parseFloat(document.getElementById('calc-length').value);
            const width = parseFloat(document.getElementById('calc-width').value);
            const height = parseFloat(document.getElementById('calc-height').value);
            const printType = document.getElementById('calc-print').value;
            const quantity = parseInt(document.getElementById('calc-qty').value) || 100;

            const unitPriceText = document.getElementById('unit-price').innerText.replace('₹', '').trim();
            const totalText = document.getElementById('total-price').innerText.replace('₹', '').replace(/,/g, '').trim();

            const customConfig = {
                id: Date.now(),
                name: `Custom ${category}`,
                category: category,
                ply: state.selectedPly,
                length: length,
                width: width,
                height: height,
                print: printType,
                qty: quantity,
                unitPrice: parseFloat(unitPriceText),
                total: parseFloat(totalText)
            };

            state.inquiryCart.push(customConfig);
            updateCartBadges();
            showSuccessToast("Added configured specifications to basket!");
            toggleInquiryModal();
        }

        // Cart State & Badges UI syncing
        function updateCartBadges() {
            const count = state.inquiryCart.length;
            const dBadge = document.getElementById('cart-badge');
            const mBadge = document.getElementById('cart-badge-mobile');
            
            if (count > 0) {
                dBadge.innerText = count;
                dBadge.classList.remove('hidden');
                mBadge.innerText = count;
                mBadge.classList.remove('hidden');
            } else {
                dBadge.classList.add('hidden');
                mBadge.classList.add('hidden');
            }
        }

        // Dynamic inquiry listing modal
        function renderInquiryCart() {
            const container = document.getElementById('inquiry-items-container');
            const submitBtn = document.getElementById('modal-submit-btn');

            if (state.inquiryCart.length === 0) {
                container.innerHTML = `<p class="text-gray-500 text-center py-8">Your inquiry basket is empty. Add item configs from the dimension tools or product catalog.</p>`;
                submitBtn.disabled = true;
                return;
            }

            submitBtn.disabled = false;
            let html = '<div class="space-y-4">';
            let grandTotal = 0;

            state.inquiryCart.forEach(item => {
                grandTotal += item.total;
                html += `
                    <div class="p-4 bg-brandKraft rounded-xl border border-brandGold/20 flex flex-col sm:flex-row justify-between items-start sm:items-center">
                        <div>
                            <h4 class="font-bold text-brandNavy text-base">${item.name}</h4>
                            <p class="text-xs text-gray-500 mt-0.5">
                                Size: ${item.length}x${item.width}x${item.height} cm | ${item.ply}-Ply | Prints: ${item.print}
                            </p>
                            <p class="text-xs text-gray-500">Quantity: <strong class="text-brandNavy">${item.qty} units</strong></p>
                        </div>
                        <div class="mt-3 sm:mt-0 flex items-center justify-between w-full sm:w-auto sm:space-x-4">
                            <div class="text-left sm:text-right">
                                <p class="text-xs text-gray-400">Est. Total</p>
                                <span class="font-black text-brandNavy text-sm">₹ ${item.total.toLocaleString('en-IN', { minimumFractionDigits: 2 })}</span>
                            </div>
                            <button onclick="removeCartItem(${item.id})" class="text-red-500 hover:text-red-700 p-1.5 rounded-lg hover:bg-red-50 transition" title="Delete">
                                <i data-lucide="trash-2" class="w-4.5 h-4.5"></i>
                            </button>
                        </div>
                    </div>
                `;
            });

            html += `
                <div class="pt-4 border-t border-gray-200 flex justify-between items-center">
                    <span class="text-sm font-bold text-gray-500 uppercase tracking-wider">Estimated Subtotal:</span>
                    <span class="text-xl font-black text-brandNavy">₹ ${grandTotal.toLocaleString('en-IN', { minimumFractionDigits: 2 })}</span>
                </div>
            `;
            html += '</div>';

            container.innerHTML = html;
            lucide.createIcons();
        }

        function removeCartItem(id) {
            state.inquiryCart = state.inquiryCart.filter(item => item.id !== id);
            updateCartBadges();
            renderInquiryCart();
        }

        function submitConsolidatedInquiry() {
            state.inquiryCart = [];
            updateCartBadges();
            toggleInquiryModal();
            showSuccessToast("Your consolidated packaging inquiry has been submitted! Our engineers will contact you shortly.");
        }

        // Contact feedback submission
        function handleContactSubmit(event) {
            event.preventDefault();
            const name = document.getElementById('contact-name').value;
            showSuccessToast(`Thank you ${name}! Your inquiry message has been submitted successfully.`);
            document.getElementById('contact-form').reset();
        }

        // Fallback Clipboard copy implementation
        function copyEmailToClipboard() {
            const email = "yadavdushyant494@gmail.com";
            const tempInput = document.createElement("input");
            tempInput.value = email;
            document.body.appendChild(tempInput);
            tempInput.select();
            document.execCommand("copy");
            document.body.removeChild(tempInput);
            showSuccessToast("Email successfully copied to your clipboard!");
        }

        // Success Toast Notification overlay
        function showSuccessToast(message) {
            const toast = document.getElementById('success-toast');
            document.getElementById('toast-message').innerText = message;
            toast.classList.remove('hidden');
            toast.classList.add('flex');
            setTimeout(() => {
                toast.classList.add('hidden');
                toast.classList.remove('flex');
            }, 4500);
        }

        // AI Chat Widget controller
        function toggleAIChat() {
            const windowEl = document.getElementById('ai-chat-window');
            state.aiChatActive = !state.aiChatActive;
            if (state.aiChatActive) {
                windowEl.classList.remove('hidden');
            } else {
                windowEl.classList.add('hidden');
            }
        }

        // Gemini AI Consultant Integration with Exponential Backoff
        async function callGeminiAPI(query, retries = 5, delay = 1000) {
            const systemPrompt = `You are the expert Box Craft Packaging Solutions AI Consultant. 
            You advise corporate and retail clients in India on packaging structure design.
            Guidance criteria:
            - Heavy products (>5kg) or fragile electronics require at least 5-Ply or 7-Ply corrugated boxes.
            - Delicate premium items like jewelry require Rigid Luxury Gift boxes.
            - Retail display items require custom duplex board carton boxes with high visibility printing.
            - Mailer boxes (Self-sealing) are optimized for lightweight e-commerce parcels (<2kg).
            Keep explanations brief, professional, friendly, and quote metrics in centimeters (cm) and Indian Rupees (INR) where helpful. Always include the brand name "BOX CRAFT" with pride.`;

            const payload = {
                contents: [{ parts: [{ text: query }] }],
                systemInstruction: { parts: [{ text: systemPrompt }] }
            };

            const endpoint = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;

            for (let i = 0; i < retries; i++) {
                try {
                    const response = await fetch(endpoint, {
                        method: 'POST',
                        headers: { 'Content-Type': 'application/json' },
                        body: JSON.stringify(payload)
                    });

                    if (response.status === 429 || (response.status >= 500 && response.status < 600)) {
                        // Rate limit or server error - wait and retry
                        await new Promise(resolve => setTimeout(resolve, delay));
                        delay *= 2; // exponential backoff
                        continue;
                    }

                    if (!response.ok) {
                        throw new Error(`API returned HTTP ${response.status}`);
                    }

                    const result = await response.json();
                    const text = result.candidates?.[0]?.content?.parts?.[0]?.text;
                    if (text) return text;
                    throw new Error("Empty candidate parts response received.");

                } catch (error) {
                    if (i === retries - 1) {
                        return "I apologize, but my consultant systems are heavily busy right now. Please connect directly with our experts on our hotline at +91 8929131333!";
                    }
                    await new Promise(resolve => setTimeout(resolve, delay));
                    delay *= 2;
                }
            }
        }

        // Handle AI question submit
        async function handleAIConsultantSubmit(event) {
            event.preventDefault();
            const inputEl = document.getElementById('ai-user-query');
            const streamEl = document.getElementById('ai-messages-stream');
            const query = inputEl.value.trim();
            if (!query) return;

            // Render User query in chat list
            streamEl.innerHTML += `
                <div class="text-right">
                    <div class="inline-block bg-brandGold text-brandNavy font-semibold p-2.5 rounded-xl text-xs max-w-[85%] text-left">
                        <p class="font-bold text-[10px] text-brandNavy-dark opacity-75 mb-0.5">You:</p>
                        <p>${query}</p>
                    </div>
                </div>
            `;
            inputEl.value = "";
            streamEl.scrollTop = streamEl.scrollHeight;

            // Show Typing indicator
            const typingId = `type-${Date.now()}`;
            streamEl.innerHTML += `
                <div id="${typingId}" class="text-left">
                    <div class="inline-block bg-brandNavy/50 border border-brandGold/15 p-2.5 rounded-xl text-xs max-w-[85%]">
                        <p class="font-bold text-brandGold text-[10px] mb-0.5">Box Craft AI Bot:</p>
                        <p class="animate-pulse flex items-center gap-1">Analyzing spec sheet... <span class="w-1.5 h-1.5 bg-brandGold rounded-full animate-bounce"></span></p>
                    </div>
                </div>
            `;
            streamEl.scrollTop = streamEl.scrollHeight;

            // Query Gemini API
            const botResponse = await callGeminiAPI(query);

            // Remove typing and render actual response
            const typingEl = document.getElementById(typingId);
            if (typingEl) typingEl.remove();

            streamEl.innerHTML += `
                <div class="text-left">
                    <div class="inline-block bg-brandNavy/40 border border-brandGold/20 p-2.5 rounded-xl text-xs max-w-[85%]">
                        <p class="font-bold text-brandGold text-[10px] mb-0.5">Box Craft AI Bot:</p>
                        <p class="leading-relaxed whitespace-pre-line">${botResponse}</p>
                    </div>
                </div>
            `;
            streamEl.scrollTop = streamEl.scrollHeight;
        }

        // Initial setup on load
        window.onload = function() {
            updatePlyUI('3');
            calculateRealTimeQuote();
        };
    </script>
</body>
</html>
