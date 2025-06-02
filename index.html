<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blood Donor App</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f2f5;
        }
        .app-container {
            max-width: 420px;
            min-height: 100vh;
            margin: 0 auto;
            background-color: white;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
            display: flex;
            flex-direction: column;
            position: relative;
        }
        .page {
            display: none;
            flex-grow: 1;
            padding: 1.5rem;
            overflow-y: auto;
        }
        .page.active {
            display: flex;
            flex-direction: column;
        }
        .name-cell-truncate {
            max-width: 70px; 
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        .contact-cell-style {
            max-width: 90px; 
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            cursor: pointer; 
            color: #2563eb; 
            text-decoration: underline;
        }
        .contact-cell-style:hover {
            color: #1d4ed8;
        }
        .location-cell-style {
            max-width: 80px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        #toastMessage {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #10B981; 
            color: white;
            padding: 10px 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            z-index: 1050; 
            opacity: 0;
            transition: opacity 0.3s ease-in-out, bottom 0.3s ease-in-out;
            pointer-events: none;
        }
        #toastMessage.show {
            opacity: 1;
            bottom: 30px;
        }
        #toastMessage.warning {
            background-color: #f59e0b; 
        }
        #loadingSpinnerPage2, #loadingSpinnerResults {
            display: none;
            border: 4px solid #f3f3f3;
            border-top: 4px solid #dc2626;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            animation: spin 1s linear infinite;
            margin: 20px auto;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        .blood-group-card {
            background-color: #f9fafb;
            border: 1px solid #e5e7eb;
            border-radius: 0.75rem;
            padding: 1rem;
            text-align: center;
            cursor: pointer;
            transition: all 0.2s ease-in-out;
        }
        .blood-group-card:hover {
            border-color: #ef4444;
            box-shadow: 0 4px 12px rgba(239, 68, 68, 0.1);
        }
        .blood-group-card .blood-type {
            font-size: 1.875rem;
            font-weight: bold;
            color: #ef4444;
        }
        .blood-group-card .donor-count {
            font-size: 0.875rem;
            color: #4b5563;
        }
        #imageSlideshow {
            width: 100%;
            height: 180px; 
            position: relative;
            overflow: hidden;
            border-radius: 0.5rem;
            margin-bottom: 1rem; 
            background-color: #e5e7eb; /* Fallback background for slideshow area */
        }
        .slide-item {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0;
            transition: opacity 1s ease-in-out;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .slide-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .slide-item.active {
            opacity: 1;
        }
        /* Updated styling for generic fallback */
        .slide-text-fallback {
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column; /* Stack icon and text */
            align-items: center;
            justify-content: center;
            background-color: #e5e7eb; /* Neutral gray */
            color: #6b7280; /* Gray text */
            text-align: center;
            padding: 1rem;
        }
        .slide-text-fallback svg {
            width: 48px; /* Larger icon */
            height: 48px;
            margin-bottom: 0.5rem;
            fill: #9ca3af; /* Lighter gray for icon */
        }
        .slide-text-fallback p {
            font-size: 0.875rem; /* Smaller text */
            font-weight: 500;
        }

        .header-icon {
            width: 28px;
            height: 28px;
            color: #4B5563;
        }
        .header-icon.text-red-600 {
             color: #dc2626;
        }
        .status-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            display: inline-block;
            vertical-align: middle;
        }
        #statusLegend p {
            display: flex;
            align-items: center;
            margin-bottom: 0.25rem;
            color: #4B5563;
        }
        #statusLegend .status-dot {
            margin-right: 8px;
        }
        @keyframes button-click-animation {
            0% { transform: scale(1); }
            50% { transform: scale(0.95); }
            100% { transform: scale(1); }
        }
        .animate-click {
            animation: button-click-animation 0.2s ease-in-out;
        }
        .faq-item {
            margin-bottom: 1rem;
            border-bottom: 1px solid #e5e7eb;
        }
        .faq-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
        }
        .faq-question-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0.75rem 0;
            cursor: pointer;
            font-weight: 600;
            color: #1f2937;
        }
        .faq-question-header:hover {
            color: #0ea5e9;
        }
        .faq-question-text {
             flex-grow: 1;
             margin-right: 0.5rem;
        }
        .faq-answer {
            color: #4b5563;
            line-height: 1.6;
            padding: 0 0 1rem 0;
            display: none;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out, padding 0.3s ease-out;
        }
        .faq-answer.active {
            display: block;
            max-height: 500px;
        }
        .faq-toggle-icon {
            width: 20px;
            height: 20px;
            transition: transform 0.3s ease-out;
        }
        .faq-toggle-icon.active {
            transform: rotate(180deg);
        }
        #floatingFaqButton {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 56px;
            height: 56px;
            background-color: #0ea5e9;
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
            cursor: pointer;
            z-index: 900;
            transition: background-color 0.2s ease-in-out;
        }
        #floatingFaqButton:hover {
            background-color: #0284c7;
        }
        #floatingFaqButton svg {
            width: 28px;
            height: 28px;
        }
        .offline-data-message {
            text-align: center;
            padding: 0.5rem;
            background-color: #fffbeb;
            color: #b45309;
            border: 1px solid #fef3c7;
            border-radius: 0.375rem;
            font-size: 0.875rem;
            margin-bottom: 1rem;
        }
        #locationFilterSelect {
            min-width: 120px; 
            padding: 0.3rem 0.5rem; 
            border-radius: 0.375rem;
            border: 1px solid #d1d5db; 
            background-color: white;
            font-size: 0.875rem;
            margin-left: 0.5rem; 
        }
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0, 0, 0, 0.6); 
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1000; 
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }
        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }
        .modal-content {
            background-color: white;
            padding: 1.5rem;
            border-radius: 0.5rem;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            width: 90%;
            max-width: 320px; 
            text-align: center; 
        }
        .modal-content h3 {
            font-size: 1.125rem; 
            font-weight: 600;
            color: #1f2937;
            margin-bottom: 0.5rem;
        }
        .modal-content p#contactActionNumber { 
            font-size: 1.25rem; 
            color: #1d4ed8; 
            font-weight: 500;
            margin-bottom: 1.5rem;
            word-break: break-all; 
        }
        .modal-actions {
            display: flex;
            flex-direction: column; 
            gap: 0.75rem; 
        }
        .modal-button {
            padding: 0.75rem 1rem; 
            border-radius: 0.375rem;
            font-weight: 500;
            transition: background-color 0.2s;
            width: 100%; 
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem; 
        }
        .modal-button-primary { 
            background-color: #16a34a; 
            color: white;
        }
        .modal-button-primary:hover {
            background-color: #15803d;
        }
        .modal-button-secondary { 
            background-color: #0ea5e9; 
            color: white;
        }
        .modal-button-secondary:hover {
            background-color: #0284c7;
        }
         .modal-button-tertiary { 
            background-color: #e5e7eb; 
            color: #374151;
            margin-top: 0.5rem; 
        }
        .modal-button-tertiary:hover {
            background-color: #d1d5db;
        }
    </style>
</head>
<body>
    <div class="app-container">
        <header class="flex items-center justify-between p-4 border-b border-gray-200 sticky top-0 bg-white z-50 h-16">
            <div class="w-10 flex items-center justify-start">
                <button id="hamburgerButton" aria-label="Menu" class="hidden">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="header-icon text-gray-700">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
                    </svg>
                </button>
                <button id="headerBackButton" aria-label="Back" class="hidden">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2.5" stroke="currentColor" class="header-icon text-red-600">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5 8.25 12l7.5-7.5" />
                    </svg>
                </button>
            </div>
            <h1 id="headerTitle" class="text-xl font-semibold text-gray-800 text-center flex-grow">Blood Donor</h1>
            <div class="w-10 flex items-center justify-end">
                <button id="profileButton" aria-label="Profile">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="header-icon text-red-600">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 6a3.75 3.75 0 1 1-7.5 0 3.75 3.75 0 0 1 7.5 0ZM4.501 20.118a7.5 7.5 0 0 1 14.998 0A17.933 17.933 0 0 1 12 21.75c-2.676 0-5.216-.584-7.499-1.632Z" />
                    </svg>
                </button>
            </div>
        </header>

        <div id="homePage" class="page active">
            <div id="imageSlideshow"></div>
            <div class="flex-grow flex flex-col justify-start">
                <h2 class="text-4xl font-bold text-gray-800 mb-2 text-left">Save Lives Today</h2>
                <p class="text-gray-600 mb-4 text-left">Connect with blood donors or become one</p>
                <button id="findDonorButton" class="w-full bg-red-600 hover:bg-red-700 text-white font-semibold py-3 px-4 rounded-lg shadow-md mb-3 flex items-center justify-center text-lg">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6 mr-3"><path stroke-linecap="round" stroke-linejoin="round" d="m21 21-5.197-5.197m0 0A7.5 7.5 0 1 0 5.196 5.196a7.5 7.5 0 0 0 10.607 10.607Z" /></svg>
                    Find Donor
                </button>
                <button id="becomeDonorAppButton" class="w-full border-2 border-red-600 text-red-600 hover:bg-red-50 font-semibold py-3 px-4 rounded-lg flex items-center justify-center text-lg">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6 mr-3"><path stroke-linecap="round" stroke-linejoin="round" d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12Z" /></svg>
                    Become a Donor
                </button>
                </div>
        </div>

        <div id="selectBloodGroupPage" class="page">
            <h2 class="text-2xl font-bold text-gray-800 mb-6">Select Blood Groups</h2>
            <div id="bloodGroupCardsContainer" class="grid grid-cols-2 gap-4"></div>
            <div id="loadingSpinnerPage2" class="mt-6"></div>
            <p id="errorMessagePage2" class="mt-4 text-center text-red-600 hidden"></p>
        </div>

        <div id="resultsPage" class="page">
            <div class="flex items-center justify-between mb-4">
                <h2 id="resultsTitle" class="text-xl font-semibold text-gray-700">Donors</h2>
                <div id="locationFilterContainer" class="flex items-center">
                    <select id="locationFilterSelect" name="locationFilter" class="p-1 border border-gray-300 rounded-md text-sm focus:ring-red-500 focus:border-red-500" aria-label="Filter by Location">
                        </select>
                </div>
            </div>
            
            <div id="statusLegend" class="mb-4 text-sm text-gray-700">
                <p><span class="status-dot" style="background-color: #10B981;"></span>রক্তদানের জন্য প্রস্তুত</p>
                <p><span class="status-dot" style="background-color: #EF4444;"></span>সম্প্রতি রক্ত দিয়েছেন</p>
            </div>
            <div id="loadingSpinnerResults"></div>
            <div id="resultsTableContainer" class="overflow-x-auto bg-white rounded-lg shadow">
                <table class="min-w-full divide-y divide-gray-200">
                    <thead class="bg-red-500">
                        <tr>
                            <th scope="col" class="px-2 py-3 text-left text-xs font-medium text-white uppercase tracking-wider">Name</th>
                            <th scope="col" class="px-2 py-3 text-left text-xs font-medium text-white uppercase tracking-wider">Contact</th>
                            <th scope="col" class="px-2 py-3 text-left text-xs font-medium text-white uppercase tracking-wider">Group</th> 
                            <th scope="col" class="px-2 py-3 text-center text-xs font-medium text-white uppercase tracking-wider">Status</th> 
                            <th scope="col" class="px-2 py-3 text-left text-xs font-medium text-white uppercase tracking-wider">Location</th> </tr>
                    </thead>
                    <tbody id="donorsTableBody" class="bg-white divide-y divide-gray-200"></tbody>
                </table>
            </div>
            <p id="noResultsMessage" class="mt-4 text-center text-gray-600 hidden"></p>
            <p id="errorMessageResults" class="mt-4 text-center text-red-600 hidden"></p>
        </div>

        <div id="faqPage" class="page">
            <div id="faqContent">
                 <div class="faq-item">
                    <div class="faq-question-header">
                        <span class="faq-question-text">১. রক্ত কারা দিতে পারবেন?</span>
                        <svg class="faq-toggle-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                    </div>
                    <div class="faq-answer">
                        <p>উত্তর: ১৮ থেকে ৬০ বছর বয়সী যেকোনো সুস্থ মানুষ, যাদের ওজন ৪৫ কেজির উপরে, তারা রক্ত দিতে পারবেন। তবে কিছু বিশেষ শারীরিক অবস্থায় রক্ত দেওয়া থেকে বিরত থাকতে বলা হয়।</p>
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question-header">
                        <span class="faq-question-text">২. কতদিন পর পর রক্ত দেওয়া যায়?</span>
                        <svg class="faq-toggle-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                    </div>
                    <div class="faq-answer">
                        <p>উত্তর: একজন সুস্থ পুরুষ প্রতি ৩ মাস পর পর এবং একজন সুস্থ মহিলা প্রতি ৪ মাস পর পর রক্ত দিতে পারবেন।</p>
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question-header">
                        <span class="faq-question-text">৩. রক্ত দেওয়ার প্রক্রিয়াটি কেমন?</span>
                        <svg class="faq-toggle-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                    </div>
                    <div class="faq-answer">
                        <p>উত্তর: রক্ত দেওয়ার আগে আপনার কিছু সাধারণ স্বাস্থ্য পরীক্ষা করা হবে, যেমন - ওজন, রক্তচাপ, নাড়ির গতি এবং রক্তে হিমোগ্লোবিনের মাত্রা। পুরো প্রক্রিয়াটি সাধারণত ১০-১৫ মিনিট সময় নেয়, তবে রক্তদান পরবর্তী বিশ্রাম সহ মোট ৩০-৪০ মিনিট লাগতে পারে।</p>
                    </div>
                </div>
                 <div class="faq-item">
                    <div class="faq-question-header">
                        <span class="faq-question-text">৪. রক্ত দিলে কি শরীর দুর্বল হয়ে যায়?</span>
                        <svg class="faq-toggle-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                    </div>
                    <div class="faq-answer">
                        <p>উত্তর: রক্ত দেওয়ার পর সাময়িকভাবে সামান্য দুর্বল লাগতে পারে, তবে পর্যাপ্ত বিশ্রাম ও তরল পান করলে শরীর দ্রুত স্বাভাবিক অবস্থায় ফিরে আসে। রক্ত দেওয়ার ফলে শরীরের কোনো স্থায়ী ক্ষতি হয় না, বরং এটি স্বাস্থ্যের জন্য উপকারী।</p>
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question-header">
                        <span class="faq-question-text">৫. রক্ত দেওয়ার আগে কি ধরনের প্রস্তুতি নেওয়া উচিত?</span>
                        <svg class="faq-toggle-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                    </div>
                    <div class="faq-answer">
                        <p>উত্তর: রক্ত দেওয়ার আগে রাতে পর্যাপ্ত ঘুমানো উচিত এবং সকালে স্বাস্থ্যকর নাস্তা করা উচিত। খালি পেটে রক্ত দেওয়া উচিত নয়। প্রচুর পরিমাণে পানি ও তরল পান করুন।</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <button id="floatingFaqButton" aria-label="সাধারণ জিজ্ঞাসা">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" d="M9.879 7.519c1.171-1.025 3.071-1.025 4.242 0 1.172 1.025 1.172 2.687 0 3.712-.203.179-.43.326-.67.442-.745.361-1.45.999-1.45 1.827v.75M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Zm-9 5.25h.008v.008H12v-.008Z" />
        </svg>
    </button>

    <div id="contactActionModal" class="modal-overlay">
        <div class="modal-content">
            <h3>যোগাযোগ করুন</h3>
            <p id="contactActionNumber"></p>
            <div class="modal-actions">
                <button id="contactActionCallButton" class="modal-button modal-button-primary">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5"><path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 0 0 2.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 0 1-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 0 0-1.091-.852H4.5A2.25 2.25 0 0 0 2.25 6.75Z" /></svg>
                    কল করুন
                </button>
                <button id="contactActionCopyButton" class="modal-button modal-button-secondary">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5"><path stroke-linecap="round" stroke-linejoin="round" d="M15.75 17.25v3.375c0 .621-.504 1.125-1.125 1.125h-9.75a1.125 1.125 0 0 1-1.125-1.125V7.875c0-.621.504-1.125 1.125-1.125H6.75a9.06 9.06 0 0 1 1.5.124m7.5 10.376h3.375c.621 0 1.125-.504 1.125-1.125V11.25c0-4.46-3.243-8.161-7.5-8.876a9.06 9.06 0 0 0-1.5-.124H9.375c-.621 0-1.125.504-1.125 1.125v3.5m7.5 10.375H9.375a1.125 1.125 0 0 1-1.125-1.125v-9.25m12 6.625v-1.875a3.375 3.375 0 0 0-3.375-3.375h-1.5a1.125 1.125 0 0 1-1.125-1.125v-1.5a3.375 3.375 0 0 0-3.375-3.375H9.75" /></svg>
                    কপি করুন
                </button>
                <button id="contactActionCloseButton" class="modal-button modal-button-tertiary">বন্ধ করুন</button>
            </div>
        </div>
    </div>


    <div id="toastMessage">Number copied!</div>

    <script>
        // --- CONFIGURATION ---
        const googleSheetCsvUrl = 'https://docs.google.com/spreadsheets/d/e/2PACX-1vRBPra3YNf8aSK4j343nemCQyoU3ZeSOsWWvSFclImWj5Zb4mONvrWcYWacOLh3KDizZ12qouuJDMC0/pub?gid=0&single=true&output=csv';
        const googleFormLink = 'https://docs.google.com/forms/d/e/1FAIpQLScawb_WPHqzRSsk9eHhOd23Xmmed9IxZuwQnImA-8ARIgklqA/viewform?usp=dialog';
        const ANIMATION_DELAY = 150;
        const LOCAL_STORAGE_KEY = 'bloodDonorOfflineData';
        const LAST_FETCH_TIMESTAMP_KEY = 'bloodDonorLastFetchTimestamp';

        // --- GLOBAL STATE VARIABLES ---
        let allDonors = [];
        let bloodGroupCounts = {};
        const bloodGroups = ["A+", "A-", "B+", "B-", "AB+", "AB-", "O+", "O-"];
        let currentPageId = 'home';
        let initialDataFetchFailed = false;
        let currentSelectedBloodGroup = null;
        let currentContactForModal = null; 
        
        // --- DOM ELEMENT REFERENCES ---
        const pages = { /* ... */ };
        const findDonorButton = document.getElementById('findDonorButton');
        const becomeDonorAppButton = document.getElementById('becomeDonorAppButton');
        const floatingFaqButton = document.getElementById('floatingFaqButton');
        const hamburgerButton = document.getElementById('hamburgerButton'); 
        const headerBackButton = document.getElementById('headerBackButton');
        const profileButton = document.getElementById('profileButton');
        const headerTitle = document.getElementById('headerTitle');
        const bloodGroupCardsContainer = document.getElementById('bloodGroupCardsContainer');
        const donorsTableBody = document.getElementById('donorsTableBody');
        const resultsTitle = document.getElementById('resultsTitle'); 
        const slideshowContainer = document.getElementById('imageSlideshow');
        const slideshowImageSources = [ /* ... */ ];
        let currentSlideIndex = 0;
        let slideshowInterval;
        const toastMessage = document.getElementById('toastMessage');
        let toastTimeout;
        const loadingSpinnerPage2 = document.getElementById('loadingSpinnerPage2');
        const loadingSpinnerResults = document.getElementById('loadingSpinnerResults');
        const noResultsMessage = document.getElementById('noResultsMessage');
        const errorMessagePage2 = document.getElementById('errorMessagePage2');
        const errorMessageResults = document.getElementById('errorMessageResults');
        const locationFilterSelect = document.getElementById('locationFilterSelect');
        const contactActionModal = document.getElementById('contactActionModal');
        const contactActionNumber = document.getElementById('contactActionNumber');
        const contactActionCallButton = document.getElementById('contactActionCallButton');
        const contactActionCopyButton = document.getElementById('contactActionCopyButton');
        const contactActionCloseButton = document.getElementById('contactActionCloseButton');

        pages.home = document.getElementById('homePage');
        pages.selectBloodGroup = document.getElementById('selectBloodGroupPage');
        pages.results = document.getElementById('resultsPage');
        pages.faq = document.getElementById('faqPage');
        slideshowImageSources[0] = { url: 'https://raw.githubusercontent.com/sohag525/Blood1/main/image3.jpg', text: 'You Could Save a Life', color: '#ef4444' };
        slideshowImageSources[1] = { url: 'https://raw.githubusercontent.com/sohag525/Blood1/main/image2.jpg', text: 'Donate Blood Today', color: '#3b82f6' };
        slideshowImageSources[2] = { url: 'https://raw.githubusercontent.com/sohag525/Blood1/main/image1.jpg', text: 'Be Someone\'s Hero', color: '#10b981' };

        function animateAndAct(element, callback) {
            if (element) {
                element.classList.add('animate-click');
                setTimeout(() => {
                    callback();
                    element.classList.remove('animate-click'); 
                }, ANIMATION_DELAY);
            } else {
                callback(); 
            }
        }
        function updateHeaderIcons() {
            if (currentPageId === 'home') {
                hamburgerButton.classList.remove('hidden');
                headerBackButton.classList.add('hidden');
                headerTitle.textContent = 'Blood Donor';
            } else {
                hamburgerButton.classList.add('hidden');
                headerBackButton.classList.remove('hidden');
                if (currentPageId === 'faq') {
                    headerTitle.textContent = 'সাধারণ জিজ্ঞাসা';
                } else if (currentPageId === 'selectBloodGroup') {
                     headerTitle.textContent = 'Blood Group';
                } else if (currentPageId === 'results') {
                } else {
                    headerTitle.textContent = 'Blood Donor';
                }
            }
        }
        function showPage(pageId) {
            currentPageId = pageId;
            Object.values(pages).forEach(page => page.classList.remove('active'));
            if (pages[pageId]) pages[pageId].classList.add('active');
            updateHeaderIcons();
            if (pageId === 'home') startSlideshow();
            else stopSlideshow();
        }
        function createTextFallbackSlide(slideData) {
            const fallbackDiv = document.createElement('div');
            fallbackDiv.className = 'slide-text-fallback';
            
            // SVG Icon for image placeholder
            const svgIcon = `
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor">
                    <path d="M16 2H8C4.691 2 2 4.691 2 8v8c0 3.309 2.691 6 6 6h8c3.309 0 6-2.691 6-6V8c0-3.309-2.691-6-6-6zm4 14c0 2.206-1.794 4-4 4H8c-2.206 0-4-1.794-4-4V8c0-2.206 1.794-4 4-4h8c2.206 0 4 1.794 4 4v8z"></path>
                    <path d="M14.293 7.293L11 10.586l-1.293-1.293L8.293 7.707l-4 4V16c0 .827.379 1.561 1 2h13.414A2.993 2.993 0 0 1 18 16.586V9.707l-3.707-2.414zM10 10c1.103 0 2-.897 2-2s-.897-2-2-2-2 .897-2 2 .897 2 2 2z"></path>
                </svg>
            `;
            const textElement = document.createElement('p');
            textElement.textContent = "ছবি উপলব্ধ নেই"; // Bangla: Image not available

            fallbackDiv.innerHTML = svgIcon;
            fallbackDiv.appendChild(textElement);
            return fallbackDiv;
        }
        function initSlideshow() {
            if (!slideshowContainer) return;
            slideshowContainer.innerHTML = ''; 
            slideshowImageSources.forEach((slideData, index) => {
                const slideItemContainer = document.createElement('div');
                slideItemContainer.className = 'slide-item';
                if (index === 0) slideItemContainer.classList.add('active');
                if (navigator.onLine) {
                    const img = document.createElement('img');
                    const imageUrlWithCacheBust = `${slideData.url}?t=${new Date().getTime()}`;
                    img.src = imageUrlWithCacheBust;
                    img.alt = slideData.text; 
                    img.onerror = function() {
                        console.warn(`Slideshow image failed to load: ${imageUrlWithCacheBust}. Showing text fallback.`);
                        slideItemContainer.innerHTML = ''; 
                        slideItemContainer.appendChild(createTextFallbackSlide(slideData)); // Pass slideData for alt text if needed by fallback
                    };
                    slideItemContainer.appendChild(img);
                } else {
                    slideItemContainer.appendChild(createTextFallbackSlide(slideData)); // Pass slideData
                }
                slideshowContainer.appendChild(slideItemContainer);
            });
        }
        function nextSlide() {
            if (!slideshowContainer) return;
            const slides = slideshowContainer.querySelectorAll('.slide-item'); 
            if (slides.length <= 1) return;
            slides[currentSlideIndex].classList.remove('active');
            currentSlideIndex = (currentSlideIndex + 1) % slides.length;
            slides[currentSlideIndex].classList.add('active');
        }
        function startSlideshow() {
            stopSlideshow();
            if (slideshowImageSources.length > 0) { 
                 initSlideshow(); 
                 if (slideshowImageSources.length > 1) {
                    slideshowInterval = setInterval(nextSlide, 3000);
                 }
            }
        }
        function stopSlideshow() {
            clearInterval(slideshowInterval);
        }
        function showOfflineDataMessage(pageContainerId) {
            const pageElement = document.getElementById(pageContainerId);
            if (!pageElement) return;
            const existingMessage = pageElement.querySelector('.offline-data-message');
            if (existingMessage) existingMessage.remove(); 
            const messageDiv = document.createElement('div');
            messageDiv.className = 'offline-data-message';
            const lastFetchTimestamp = localStorage.getItem(LAST_FETCH_TIMESTAMP_KEY);
            let messageText = "⚠️ আপনি অফলাইন ডেটা দেখছেন। এটি সর্বশেষ তথ্য নাও হতে পারে।"; 
            if (lastFetchTimestamp) {
                try {
                    const date = new Date(lastFetchTimestamp);
                    const formattedDate = date.toLocaleString('bn-BD', { 
                        year: 'numeric', month: 'long', day: 'numeric', 
                        hour: 'numeric', minute: '2-digit', hour12: true 
                    });
                    messageText += ` সর্বশেষ আপডেট: ${formattedDate}`; 
                } catch (e) {
                    console.warn("Could not parse last fetch timestamp:", e);
                }
            }
            messageDiv.textContent = messageText;
            pageElement.insertBefore(messageDiv, pageElement.firstChild);
        }
        function loadDataFromCache(isBackgroundFetch, onlineErrorMsg = null) {
            const cachedData = localStorage.getItem(LOCAL_STORAGE_KEY);
            if (cachedData) {
                console.log("Data loaded from localStorage.");
                allDonors = JSON.parse(cachedData);
                calculateBloodGroupCounts();
                if (!isBackgroundFetch) {
                    renderBloodGroupCards();
                    populateLocationFilter(); 
                    showOfflineDataMessage('selectBloodGroupPage');
                }
                if (onlineErrorMsg && !isBackgroundFetch) {
                    errorMessagePage2.textContent = `সর্বশেষ ডেটা আনতে সমস্যা হয়েছে (${onlineErrorMsg})। সংরক্ষিত ডেটা দেখানো হচ্ছে।`; 
                    errorMessagePage2.classList.remove('hidden');
                }
                return true;
            } else {
                console.log("No cached data found.");
                allDonors = [];
                calculateBloodGroupCounts();
                if (!isBackgroundFetch) {
                    renderBloodGroupCards();
                    populateLocationFilter(); 
                    if (onlineErrorMsg) {
                        errorMessagePage2.textContent = `সর্বশেষ ডেটা আনতে সমস্যা হয়েছে (${onlineErrorMsg}) এবং কোনো সংরক্ষিত ডেটা নেই।`; 
                    } else {
                        errorMessagePage2.textContent = "আপনি অফলাইনে আছেন এবং কোনো সংরক্ষিত ডেটা নেই। অনুগ্রহ করে ইন্টারনেট সংযোগ করুন।"; 
                    }
                    errorMessagePage2.classList.remove('hidden');
                }
                initialDataFetchFailed = true;
                return false;
            }
        }
        async function fetchAndParseData(isBackgroundFetch = false) {
            if (!isBackgroundFetch) {
                loadingSpinnerPage2.style.display = 'block';
                errorMessagePage2.classList.add('hidden');
                noResultsMessage.classList.add('hidden');
                const existingOfflineMsg = pages.selectBloodGroup.querySelector('.offline-data-message');
                if (existingOfflineMsg) existingOfflineMsg.remove();
            }
            initialDataFetchFailed = false;
            if (navigator.onLine) {
                try {
                    console.log("Online: Fetching fresh data...");
                    const response = await fetch(`${googleSheetCsvUrl}&t=${new Date().getTime()}`);
                    if (!response.ok) throw new Error(`HTTP error! status: ${response.status}`);
                    const csvText = await response.text();
                    allDonors = parseCSV(csvText); 
                    try {
                        localStorage.setItem(LOCAL_STORAGE_KEY, JSON.stringify(allDonors));
                        localStorage.setItem(LAST_FETCH_TIMESTAMP_KEY, new Date().toISOString());
                        console.log("Data saved to localStorage.");
                    } catch (e) {
                        console.warn("Could not save data to localStorage:", e);
                        if (!isBackgroundFetch) showToast("Offline data could not be saved.", true);
                    }
                    calculateBloodGroupCounts();
                    if (!isBackgroundFetch) {
                        renderBloodGroupCards();
                        populateLocationFilter(); 
                        if (allDonors.length === 0 && (!csvText || !csvText.includes(','))) {
                             errorMessagePage2.textContent = "No donor data found in the sheet.";
                             errorMessagePage2.classList.remove('hidden');
                        }
                    }
                    return true;
                } catch (error) {
                    console.error('Online Fetch Error:', error);
                    initialDataFetchFailed = true;
                    return loadDataFromCache(isBackgroundFetch, error.message);
                } finally {
                    if (!isBackgroundFetch) {
                        loadingSpinnerPage2.style.display = 'none';
                    }
                }
            } else {
                console.log("Offline: Attempting to load data from cache...");
                if (!isBackgroundFetch) showToast("⚠️ You are offline. Showing cached data.", true);
                return loadDataFromCache(isBackgroundFetch);
            }
        }
        async function initialBackgroundFetch() {
            if (navigator.onLine) {
                console.log("Initial background fetch started...");
                await fetchAndParseData(true);
                console.log("Initial background fetch completed.");
            } else {
                console.log("Offline on initial load, attempting to load from cache for background.");
                loadDataFromCache(true); 
            }
        }
        function parseCSV(data) {
            const donors = [];
            const lines = data.trim().split(/\r?\n/).map(line => line.trim()).filter(line => line);
            if (lines.length <= 1) return donors;
            for (let i = 1; i < lines.length; i++) {
                const line = lines[i];
                const values = line.split(',').map(value => value.trim());
                if (values.length >= 3) { 
                    donors.push({
                        name: values[0] || "N/A",
                        contact: values[1] || "N/A",
                        bloodGroup: (values[2] || "N/A").toUpperCase(),
                        lastDonatedDate: values[3] || null, 
                        location: values[4] || "N/A" 
                    });
                }
            }
            return donors;
        }
        function calculateBloodGroupCounts() {
            bloodGroupCounts = {};
            bloodGroups.forEach(bg => bloodGroupCounts[bg] = 0);
            allDonors.forEach(donor => {
                if (bloodGroupCounts.hasOwnProperty(donor.bloodGroup)) {
                    bloodGroupCounts[donor.bloodGroup]++;
                }
            });
        }
        function renderBloodGroupCards() {
            bloodGroupCardsContainer.innerHTML = '';
            bloodGroups.forEach(bg => {
                const count = bloodGroupCounts[bg] || 0;
                const card = document.createElement('div');
                card.className = 'blood-group-card';
                card.dataset.bloodgroup = bg;
                card.innerHTML = `
                    <div class="blood-type">${bg}</div>
                    <div class="donor-count">${count} Donor${count === 1 ? '' : 's'}</div>
                `;
                card.addEventListener('click', (e) => {
                    animateAndAct(e.currentTarget, () => {
                        handleBloodGroupCardClick(bg);
                    });
                });
                bloodGroupCardsContainer.appendChild(card);
            });
        }
        function populateLocationFilter() {
            if (!locationFilterSelect) return;
            locationFilterSelect.innerHTML = ''; 
            const allLocationsOption = document.createElement('option');
            allLocationsOption.value = 'all';
            allLocationsOption.textContent = 'All Locations';
            locationFilterSelect.appendChild(allLocationsOption);
            if (allDonors && allDonors.length > 0) {
                const uniqueLocations = [...new Set(allDonors.map(donor => donor.location).filter(loc => loc && loc !== "N/A"))].sort();
                uniqueLocations.forEach(location => {
                    const option = document.createElement('option');
                    option.value = location;
                    option.textContent = location;
                    locationFilterSelect.appendChild(option);
                });
            }
        }
        function handleBloodGroupCardClick(bloodGroup) {
            currentSelectedBloodGroup = bloodGroup; 
            headerTitle.textContent = `Donors (${bloodGroup})`;
            resultsTitle.textContent = `Donors (${bloodGroup})`; 
            populateLocationFilter(); 
            locationFilterSelect.value = 'all'; 
            showPage('results');
            displayDonorsForGroup(bloodGroup, 'all'); 
        }
        function isDonorAvailable(lastDonatedDateStr) {
            if (!lastDonatedDateStr) {
                return true; 
            }
            try {
                let parts = lastDonatedDateStr.split('/'); 
                let lastDonatedDate;
                if (parts.length === 3) {
                    lastDonatedDate = new Date(parts[2], parts[0] - 1, parts[1]);
                } else {
                    parts = lastDonatedDateStr.split('-'); 
                    if (parts.length === 3) {
                        lastDonatedDate = new Date(parts[0], parts[1] - 1, parts[2]);
                    } else {
                        lastDonatedDate = new Date(lastDonatedDateStr);
                    }
                }
                if (isNaN(lastDonatedDate.getTime())) { 
                    console.warn("Invalid date format for:", lastDonatedDateStr, "Treating as available.");
                    return true; 
                }
                const currentDate = new Date();
                const threeMonthsAgo = new Date();
                threeMonthsAgo.setMonth(currentDate.getMonth() - 3);
                return lastDonatedDate <= threeMonthsAgo;
            } catch (e) {
                console.error("Error parsing date:", lastDonatedDateStr, e);
                return true; 
            }
        }

        function showContactActionModal(contactNumber) {
            currentContactForModal = contactNumber;
            contactActionNumber.textContent = contactNumber;
            contactActionModal.classList.add('active');
        }

        function hideContactActionModal() {
            contactActionModal.classList.remove('active');
            currentContactForModal = null;
        }


        function displayDonorsForGroup(selectedGroup, selectedLocation = 'all') {
            loadingSpinnerResults.style.display = 'block';
            donorsTableBody.innerHTML = '';
            noResultsMessage.classList.add('hidden'); 
            errorMessageResults.classList.add('hidden'); 
            
            const existingOfflineMsg = pages.results.querySelector('.offline-data-message');
            if (existingOfflineMsg) existingOfflineMsg.remove();

            if (!navigator.onLine && localStorage.getItem(LOCAL_STORAGE_KEY)) {
                showOfflineDataMessage('resultsPage');
            }

            if (initialDataFetchFailed && allDonors.length === 0) {
                errorMessageResults.textContent = "Failed to load donor data. Please check your connection.";
                errorMessageResults.classList.remove('hidden');
                resultsTableContainer.classList.add('hidden'); 
                loadingSpinnerResults.style.display = 'none';
                return;
            }
            resultsTableContainer.classList.remove('hidden'); 

            let filteredByBloodGroup = allDonors.filter(donor => donor.bloodGroup === selectedGroup);
            
            let finalFilteredDonors = filteredByBloodGroup;
            if (selectedLocation !== 'all') {
                finalFilteredDonors = filteredByBloodGroup.filter(donor => donor.location === selectedLocation);
            }
            
            finalFilteredDonors.forEach(donor => {
                donor.isAvailable = isDonorAvailable(donor.lastDonatedDate);
            });

            finalFilteredDonors.sort((a, b) => {
                if (a.isAvailable !== b.isAvailable) {
                    return a.isAvailable ? -1 : 1; 
                }
                return a.name.localeCompare(b.name); 
            });

            if (finalFilteredDonors.length === 0) {
                noResultsMessage.textContent = `No donors found for ${selectedGroup} in ${selectedLocation === 'all' ? 'any location' : selectedLocation}.`;
                noResultsMessage.classList.remove('hidden');
                donorsTableBody.innerHTML = `<tr><td colspan="5" class="px-4 py-4 text-center italic text-gray-500">No donors found.</td></tr>`;
            } else {
                finalFilteredDonors.forEach(donor => {
                    const row = donorsTableBody.insertRow();
                    row.className = 'hover:bg-red-50 transition-colors';

                    const nameCell = row.insertCell();
                    nameCell.textContent = donor.name;
                    nameCell.className = 'px-2 py-3 text-sm name-cell-truncate text-gray-700';

                    const contactCell = row.insertCell();
                    const displayContact = donor.contact && !donor.contact.startsWith('0') && /^\d{10}$/.test(donor.contact) ? '0' + donor.contact : donor.contact;
                    contactCell.textContent = displayContact;
                    contactCell.className = 'px-2 py-3 text-sm contact-cell-style text-gray-500';
                    contactCell.title = `Click for options for ${displayContact}`;
                    contactCell.addEventListener('click', (e) => {
                        e.preventDefault(); 
                        animateAndAct(e.currentTarget, () => {
                            showContactActionModal(displayContact);
                        });
                    });
                    
                    const bloodGroupCell = row.insertCell();
                    bloodGroupCell.innerHTML = `<span class="px-2 inline-flex text-xs leading-5 font-semibold rounded-full bg-red-100 text-red-800">${donor.bloodGroup}</span>`;
                    bloodGroupCell.className = 'px-2 py-3 whitespace-nowrap text-sm';

                    const statusCell = row.insertCell();
                    statusCell.className = 'px-2 py-3 whitespace-nowrap text-sm text-center';
                    const statusDot = document.createElement('span');
                    statusDot.className = 'status-dot';
                    
                    if (donor.isAvailable) {
                        statusDot.style.backgroundColor = '#10B981'; 
                        statusDot.title = 'রক্তদানের জন্য প্রস্তুত'; 
                    } else {
                        statusDot.style.backgroundColor = '#EF4444'; 
                        statusDot.title = 'সম্প্রতি রক্ত দিয়েছেন'; 
                    }
                    statusCell.appendChild(statusDot);

                    const locationCell = row.insertCell();
                    locationCell.textContent = donor.location || 'N/A';
                    locationCell.className = 'px-2 py-3 text-sm location-cell-style text-gray-600';
                });
            }
            loadingSpinnerResults.style.display = 'none';
        }
        
        function showToast(message, isWarning = false) {
            toastMessage.textContent = message;
            if (isWarning) {
                toastMessage.classList.add('warning');
            } else {
                toastMessage.classList.remove('warning');
            }
            toastMessage.classList.add('show');
            clearTimeout(toastTimeout);
            toastTimeout = setTimeout(() => {
                toastMessage.classList.remove('show');
                toastMessage.classList.remove('warning'); 
            }, 3000); 
        }
         function copyToClipboard(text) {
            const textarea = document.createElement('textarea');
            textarea.value = text;
            textarea.style.position = 'fixed'; textarea.style.left = '-9999px'; textarea.style.top = '-9999px'; textarea.style.opacity = 0;
            document.body.appendChild(textarea);
            textarea.focus(); textarea.select();
            try {
                if (document.execCommand('copy')) {
                    showToast(`কপি করা হয়েছে: ${text}`);
                } else {
                    showToast('কপি করতে সমস্যা হয়েছে।', true);
                }
            } catch (err) {
                console.error('Clipboard copy error:', err);
                showToast('কপি করতে সমস্যা হয়েছে।', true);
            }
            document.body.removeChild(textarea);
        }
        function initializeFaqAccordion() {
            const faqItems = document.querySelectorAll('#faqContent .faq-question-header');
            faqItems.forEach(header => {
                header.addEventListener('click', () => {
                    const answer = header.nextElementSibling;
                    const icon = header.querySelector('.faq-toggle-icon');
                    
                    faqItems.forEach(otherHeader => {
                        if (otherHeader !== header) {
                            const otherAnswer = otherHeader.nextElementSibling;
                            const otherIcon = otherHeader.querySelector('.faq-toggle-icon');
                            if (otherAnswer.classList.contains('active')) {
                                otherAnswer.classList.remove('active');
                                otherIcon.classList.remove('active');
                            }
                        }
                    });
                    answer.classList.toggle('active');
                    icon.classList.toggle('active');
                });
            });
        }

        findDonorButton.addEventListener('click', (e) => {
            animateAndAct(e.currentTarget, async () => {
                showPage('selectBloodGroup');
                await fetchAndParseData(); 
            });
        });
        becomeDonorAppButton.addEventListener('click', () => window.open(googleFormLink, '_blank'));
        floatingFaqButton.addEventListener('click', (e) => {
            animateAndAct(e.currentTarget, () => {
                showPage('faq');
            });
        });
        headerBackButton.addEventListener('click', (e) => {
            animateAndAct(e.currentTarget, () => {
                if (currentPageId === 'selectBloodGroup' || currentPageId === 'faq') {
                    showPage('home');
                } else if (currentPageId === 'results') {
                    showPage('selectBloodGroup');
                }
            });
        });
        hamburgerButton.addEventListener('click', (e) => {
             animateAndAct(e.currentTarget, () => {
                showPage('home'); 
            });
        });
        profileButton.addEventListener('click', (e) => {
            animateAndAct(e.currentTarget, () => {
                 showToast('Profile feature coming soon!');
            });
        });
        window.addEventListener('online', async () => {
            if(currentPageId === 'home') initSlideshow(); 
            showToast("আপনি এখন অনলাইনে আছেন! ডেটা আপডেট করা হচ্ছে...", false); 
            const dataRefreshed = await fetchAndParseData(true); 
            if (dataRefreshed) {
                populateLocationFilter(); 
                if (currentPageId === 'selectBloodGroup') { 
                    const existingOfflineMsg = pages.selectBloodGroup.querySelector('.offline-data-message');
                    if (existingOfflineMsg) existingOfflineMsg.remove();
                    renderBloodGroupCards(); 
                } else if (currentPageId === 'results' && currentSelectedBloodGroup) { 
                    const existingOfflineMsg = pages.results.querySelector('.offline-data-message');
                    if (existingOfflineMsg) existingOfflineMsg.remove();
                    displayDonorsForGroup(currentSelectedBloodGroup, locationFilterSelect.value); 
                }
            }
        });
        window.addEventListener('offline', () => {
             if(currentPageId === 'home') initSlideshow(); 
             showToast("⚠️ আপনি এখন অফলাইনে আছেন। সংরক্ষিত ডেটা দেখানো হচ্ছে।", true); 
             if (currentPageId === 'selectBloodGroup' && localStorage.getItem(LOCAL_STORAGE_KEY)) { 
                showOfflineDataMessage('selectBloodGroupPage');
             } else if (currentPageId === 'results' && localStorage.getItem(LOCAL_STORAGE_KEY)) { 
                showOfflineDataMessage('resultsPage');
             }
        });
        if (locationFilterSelect) {
            locationFilterSelect.addEventListener('change', (e) => {
                if (currentSelectedBloodGroup) { 
                    displayDonorsForGroup(currentSelectedBloodGroup, e.target.value);
                }
            });
        }

        contactActionCallButton.addEventListener('click', () => {
            if (currentContactForModal) {
                window.location.href = `tel:${currentContactForModal}`;
            }
            hideContactActionModal();
        });

        contactActionCopyButton.addEventListener('click', () => {
            if (currentContactForModal) {
                copyToClipboard(currentContactForModal);
            }
            hideContactActionModal();
        });

        contactActionCloseButton.addEventListener('click', hideContactActionModal);

        contactActionModal.addEventListener('click', (event) => {
            if (event.target === contactActionModal) {
                hideContactActionModal();
            }
        });

        document.addEventListener('DOMContentLoaded', () => {
            initializeFaqAccordion();
            initialBackgroundFetch().then(() => {
                if (currentPageId === 'results' || allDonors.length > 0) {
                     populateLocationFilter();
                }
            }); 
            showPage('home'); 
        });
    </script>
</body>
</html>
