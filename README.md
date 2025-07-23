<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comp Sci High: 11th Grade College Visit Guide</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Emerald & Mint (Light Green, Dark Green, White) -->
    <!-- Application Structure Plan: A single-page application with a top navigation bar to switch between four main sections: Overview, Fall CUNY Visit, Spring Choice Visit, and a consolidated Deadlines & Resources section. The Fall and Spring procedures are visualized as step-by-step timelines to make the multi-stage process clear and manageable. A YouTube video is now integrated into the Overview section to provide a dynamic and inspiring visual context of past student college visit experiences, making it immediately part of the user's initial engagement. This architecture prioritizes task-oriented navigation and clarity over mirroring the original document's linear format, while adding compelling visual elements directly to relevant content. -->
    <!-- Visualization & Content Choices: The primary "visualization" is a procedural timeline/checklist for the Fall and Spring visit processes. Report Info: Step-by-step procedures for college visits. Goal: Organize and clarify a complex process. Viz/Presentation Method: An interactive, icon-based timeline created with HTML/CSS (Tailwind). Interaction: Users click tabs to navigate between sections. Justification: A visual timeline is more engaging and easier to follow than a dense block of text, helping students track their progress. Library/Method: Vanilla JavaScript for tab functionality and Tailwind CSS for styling. For video: Report Info: User-provided YouTube video of a past college trip. Goal: Enhance engagement and provide dynamic visual context directly within the main content. Viz/Presentation Method: Responsive YouTube embed (iframe) within the Overview section, with a brief introduction. Interaction: Passive viewing/playback. Justification: A video offers a rich, immersive way to convey the experience of college visits, making the policy more relatable and inspiring. CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .tab-active {
            border-bottom-color: #166534; /* dark green */
            color: #166534;
            font-weight: 600;
        }
        .tab-inactive {
            border-bottom-color: transparent;
            color: #4b5563; /* gray-600 */
        }
        .timeline-item .timeline-icon {
            background-color: #16a34a; /* green-600 */
            color: white;
        }
        .timeline-item .timeline-content {
            border-left: 2px solid #d1fae5; /* green-100 */
        }
        .section-content {
            display: none;
        }
        .section-content.active {
            display: block;
        }
        .video-container {
            position: relative;
            width: 100%;
            padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
            height: 0;
            overflow: hidden;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            margin-top: 1.5rem;
            margin-bottom: 1.5rem;
        }
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800">

    <div class="container mx-auto p-4 md:p-8 max-w-6xl">
        
        <header class="text-center mb-8">
            <h1 class="text-4xl md:text-5xl font-bold text-green-800">Comp Sci High</h1>
            <p class="text-xl text-gray-600 mt-2">11th Grade College Visit Launchpad</p>
        </header>

        <nav class="mb-8 border-b border-gray-200">
            <ul class="flex flex-wrap -mb-px justify-center text-sm font-medium text-center">
                <li class="mr-2">
                    <button class="tab-button inline-block p-4 border-b-2 rounded-t-lg tab-active" data-target="overview">Overview</button>
                </li>
                <li class="mr-2">
                    <button class="tab-button inline-block p-4 border-b-2 rounded-t-lg tab-inactive" data-target="fall-visit">Fall CUNY Visit</button>
                </li>
                <li class="mr-2">
                    <button class="tab-button inline-block p-4 border-b-2 rounded-t-lg tab-inactive" data-target="spring-visit">Spring Choice Visit</button>
                </li>
                <li>
                    <button class="tab-button inline-block p-4 border-b-2 rounded-t-lg tab-inactive" data-target="resources">Deadlines & Resources</button>
                </li>
            </ul>
        </nav>

        <main id="main-content">
            <!-- Overview Section -->
            <section id="overview" class="section-content active">
                <div class="bg-white p-6 md:p-8 rounded-lg shadow-md">
                    <h2 class="text-2xl font-bold text-green-800 mb-4">Charting Your Post-Secondary Path</h2>
                    <p class="mb-4 text-gray-700">Welcome, Juniors! This guide outlines the official Comp Sci High policy for your required college visits. This program is designed to give you a firsthand look at different campus environments, helping you make informed decisions about your future. It's also about empowering you to take more control of your college process journey and significantly increase your knowledge of the college landscape. You are required to complete two visits this year, and following this procedure will ensure your absences are excused.</p>
                    <div class="grid md:grid-cols-2 gap-6 mt-6">
                        <div class="bg-green-50 p-4 rounded-lg border border-green-200 flex flex-col items-center justify-center text-center">
                            <h4 class="font-bold text-green-700">Required Visits</h4>
                            <p class="text-gray-600">Complete **two** official college visits during the year.</p>
                        </div>
                        <div class="bg-green-50 p-4 rounded-lg border border-green-200 flex flex-col items-center justify-center text-center">
                            <h4 class="font-bold text-green-700">Excused Absences</h4>
                            <p class="text-gray-600">Up to **two** school days are excused if all procedures are followed.</p>
                        </div>
                        <div class="bg-green-50 p-4 rounded-lg border border-green-200 flex flex-col items-center justify-center text-center">
                            <h4 class="font-bold text-green-700">Group Structure</h4>
                            <p class="text-gray-600">Visits are done in **groups of four**, assigned by Ms. Del Toro.</p>
                        </div>
                        <div class="bg-green-50 p-4 rounded-lg border border-green-200 flex flex-col items-center justify-center text-center">
                            <h4 class="font-bold text-green-700">Visit Structure</h4>
                            <p class="text-gray-600">One CUNY visit in the Fall, and one school of your choice in the Spring.</p>
                        </div>
                    </div>

                    <div class="mt-8">
                        <h3 class="text-xl font-bold text-green-800 mb-4">Remember Our Trip Last Year?</h3>
                        <p class="mb-4 text-gray-700">Relive some moments from your sophomore college trip. Get ready for new experiences this year!</p>
                        <div class="video-container">
                            <iframe src="https://www.youtube.com/embed/ZAZACPo3u0g" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Fall CUNY Visit Section -->
            <section id="fall-visit" class="section-content">
                <div class="bg-white p-6 md:p-8 rounded-lg shadow-md">
                    <h2 class="text-2xl font-bold text-green-800 mb-4">Procedure: Fall CUNY Visit</h2>
                    <p class="mb-6 text-gray-700">Your first required visit is to a CUNY (City University of New York) institution. This is a great opportunity to explore the excellent and affordable higher education options right here in our city. Follow these steps carefully to ensure a successful and excused visit.</p>
                    <div class="timeline">
                        <!-- Step 1 -->
                        <div class="timeline-item mb-8 flex">
                            <div class="flex flex-col items-center mr-4">
                                <div><div class="flex items-center justify-center w-10 h-10 rounded-full timeline-icon">1</div></div>
                                <div class="w-px h-full bg-green-200"></div>
                            </div>
                            <div class="timeline-content pb-8 pl-4">
                                <h3 class="text-lg font-semibold text-green-700">Group Up & Meet Counselor</h3>
                                <p class="text-sm text-gray-500 mb-2">By September 30th</p>
                                <p class="text-gray-600">Ms. Del Toro will assign you to a group of four by Sept. 15th. Your group must schedule a meeting with your counselor by the end of the month to discuss which CUNY schools you're interested in.</p>
                            </div>
                        </div>
                        <!-- Step 2 -->
                        <div class="timeline-item mb-8 flex">
                            <div class="flex flex-col items-center mr-4">
                                <div><div class="flex items-center justify-center w-10 h-10 rounded-full timeline-icon">2</div></div>
                                <div class="w-px h-full bg-green-200"></div>
                            </div>
                            <div class="timeline-content pb-8 pl-4">
                                <h3 class="text-lg font-semibold text-green-700">Sign Up for an Official Tour</h3>
                                <p class="text-gray-600">Visit the official admissions website of your chosen CUNY school and register for a formal, admissions-led campus tour. Self-guided walks do not count. Forward the confirmation email to Ms. Del Toro.</p>
                            </div>
                        </div>
                        <!-- Step 3 -->
                        <div class="timeline-item mb-8 flex">
                            <div class="flex flex-col items-center mr-4">
                                <div><div class="flex items-center justify-center w-10 h-10 rounded-full timeline-icon">3</div></div>
                                <div class="w-px h-full bg-green-200"></div>
                            </div>
                            <div class="timeline-content pb-8 pl-4">
                                <h3 class="text-lg font-semibold text-green-700">Submit Your Travel Plan</h3>
                                <p class="text-sm text-gray-500 mb-2">At least 2 weeks before your visit</p>
                                <p class="text-gray-600">Submit a detailed plan to your counselor including transportation routes, timings, and emergency contacts for all group members.</p>
                            </div>
                        </div>
                        <!-- Step 4 -->
                        <div class="timeline-item mb-8 flex">
                            <div class="flex flex-col items-center mr-4">
                                <div><div class="flex items-center justify-center w-10 h-10 rounded-full timeline-icon">4</div></div>
                                <div class="w-px h-full bg-green-200"></div>
                            </div>
                            <div class="timeline-content pb-8 pl-4">
                                <h3 class="text-lg font-semibold text-green-700">Complete Pre-Visit Worksheets</h3>
                                <p class="text-sm text-gray-500 mb-2">At least 1 week before your visit</p>
                                <p class="text-gray-600">Each student must individually complete and submit the "CUNY School Pre-Worksheet" and the "College Visit Best Practices Worksheet." Your counselor will provide these.</p>
                            </div>
                        </div>
                        <!-- Step 5 -->
                        <div class="timeline-item flex">
                            <div class="flex flex-col items-center mr-4">
                                <div><div class="flex items-center justify-center w-10 h-10 rounded-full timeline-icon">5</div></div>
                            </div>
                            <div class="timeline-content pb-8 pl-4">
                                <h3 class="text-lg font-semibold text-green-700">Submit Post-Visit Reflection</h3>
                                <p class="text-sm text-gray-500 mb-2">Within 1 week after your visit</p>
                                <p class="text-gray-600">After your trip, complete the "Reflection Document" detailing your experience and what you learned. This is the final step to ensure your absence is excused.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Spring Choice Visit Section -->
            <section id="spring-visit" class="section-content">
                <div class="bg-white p-6 md:p-8 rounded-lg shadow-md">
                    <h2 class="text-2xl font-bold text-green-800 mb-4">Procedure: Spring Choice Visit</h2>
                    <p class="mb-6 text-gray-700">Your second visit allows you to explore any accredited college or university that interests you. This process begins in late January and requires a formal proposal to ensure the visit is a good fit for your academic goals. The steps are similar to the Fall visit, but with a crucial planning phase first.</p>
                     <div class="timeline">
                        <!-- Step 1 -->
                        <div class="timeline-item mb-8 flex">
                            <div class="flex flex-col items-center mr-4">
                                <div><div class="flex items-center justify-center w-10 h-10 rounded-full timeline-icon">1</div></div>
                                <div class="w-px h-full bg-green-200"></div>
                            </div>
                            <div class="timeline-content pb-8 pl-4">
                                <h3 class="text-lg font-semibold text-green-700">Submit Your Proposal</h3>
                                <p class="text-sm text-gray-500 mb-2">Starting in late January</p>
                                <p class="text-gray-600">Submit a detailed "Second Visit Proposal" to Ms. Del Toro. You must justify your choice and provide evidence (GPA, coursework) that you are on an academic path for that school. <strong>Honors College Prep students or those visiting private schools must submit their proposal to Mr. Meyers.</strong></p>
                            </div>
                        </div>
                        <!-- Step 2 -->
                        <div class="timeline-item mb-8 flex">
                            <div class="flex flex-col items-center mr-4">
                                <div><div class="flex items-center justify-center w-10 h-10 rounded-full timeline-icon">2</div></div>
                                <div class="w-px h-full bg-green-200"></div>
                            </div>
                            <div class="timeline-content pb-8 pl-4">
                                <h3 class="text-lg font-semibold text-green-700">Sign Up for an Official Tour</h3>
                                <p class="text-gray-600">Once your proposal is approved, register for an official, admissions-led tour on the college's website. Submit proof of registration to your counselor.</p>
                            </div>
                        </div>
                        <!-- Step 3 -->
                        <div class="timeline-item mb-8 flex">
                            <div class="flex flex-col items-center mr-4">
                                <div><div class="flex items-center justify-center w-10 h-10 rounded-full timeline-icon">3</div></div>
                                <div class="w-px h-full bg-green-200"></div>
                            </div>
                            <div class="timeline-content pb-8 pl-4">
                                <h3 class="text-lg font-semibold text-green-700">Submit Your Travel Plan</h3>
                                <p class="text-sm text-gray-500 mb-2">At least 2 weeks before your visit</p>
                                <p class="text-gray-600">Submit a detailed travel plan to your counselor, just like you did for the CUNY visit.</p>
                            </div>
                        </div>
                        <!-- Step 4 -->
                        <div class="timeline-item mb-8 flex">
                            <div class="flex flex-col items-center mr-4">
                                <div><div class="flex items-center justify-center w-10 h-10 rounded-full timeline-icon">4</div></div>
                                <div class="w-px h-full bg-green-200"></div>
                            </div>
                            <div class="timeline-content pb-8 pl-4">
                                <h3 class="text-lg font-semibold text-green-700">Complete Pre-Visit Worksheets</h3>
                                <p class="text-sm text-gray-500 mb-2">At least 1 week before your visit</p>
                                <p class="text-gray-600">Complete the school-specific and best practices worksheets for your chosen institution.</p>
                            </div>
                        </div>
                        <!-- Step 5 -->
                        <div class="timeline-item flex">
                            <div class="flex flex-col items-center mr-4">
                                <div><div class="flex items-center justify-center w-10 h-10 rounded-full timeline-icon">5</div></div>
                            </div>
                            <div class="timeline-content pb-8 pl-4">
                                <h3 class="text-lg font-semibold text-green-700">Submit Post-Visit Reflection</h3>
                                <p class="text-sm text-gray-500 mb-2">Within 1 week after your visit</p>
                                <p class="text-gray-600">Complete and submit your final "Reflection Document" to your counselor to finalize the process and ensure your absence is excused.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Deadlines & Resources Section -->
            <section id="resources" class="section-content">
                <div class="bg-white p-6 md:p-8 rounded-lg shadow-md">
                    <h2 class="text-2xl font-bold text-green-800 mb-4">Deadlines & Resources</h2>
                    <p class="mb-6 text-gray-700">Stay on top of your junior year journey! This section is your cheat sheet for important deadlines and helpful links. Remember to check these resources regularly.</p>
                    
                    <div class="grid md:grid-cols-2 gap-8">
                        <div>
                            <h3 class="text-xl font-semibold text-green-700 mb-3">Key Deadlines</h3>
                            <ul class="space-y-3 text-gray-600">
                                <li class="flex items-start">
                                    <span class="text-green-600 font-bold mr-2">&#10148;</span>
                                    <div><strong class="text-gray-800">Sept. 15:</strong> Group assignments from Ms. Del Toro.</div>
                                </li>
                                <li class="flex items-start">
                                    <span class="text-green-600 font-bold mr-2">&#10148;</span>
                                    <div><strong class="text-gray-800">Sept. 30:</strong> Deadline for initial group meeting with Ms. Del Toro.</div>
                                </li>
                                <li class="flex items-start">
                                    <span class="text-green-600 font-bold mr-2">&#10148;</span>
                                    <div><strong class="text-gray-800">Dec. 10:</strong> Trip One complete, all docs submitted.</div>
                                </li>
                                <li class="flex items-start">
                                    <span class="text-green-600 font-bold mr-2">&#10148;</span>
                                    <div><strong class="text-gray-800">Late Jan:</strong> Begin working on Spring Visit proposals.</div>
                                </li>
                                <li class="flex items-start">
                                    <span class="text-green-600 font-bold mr-2">&#10148;</span>
                                    <div><strong class="text-gray-800">Ongoing:</strong></div>
                                </li>
                            </ul>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold text-green-700 mb-3">Essential Links</h3>
                            <ul class="space-y-3">
                                <li><a href="https://www.cuny.edu/about/colleges/" target="_blank" class="text-blue-600 hover:text-blue-800 hover:underline">CUNY Colleges Official Website</a></li>
                            </ul>
                            <h3 class="text-xl font-semibold text-green-700 mt-6 mb-3">Required Worksheets</h3>
                            <ul class="space-y-3 text-gray-600">
                                <li class="flex items-start">
                                    <span class="text-green-600 font-bold mr-2">&#10148;</span>
                                    <div><strong class="text-gray-800">CUNY School Pre-Worksheet:</strong> (Link Pending)</div>
                                </li>
                                <li class="flex items-start">
                                    <span class="text-green-600 font-bold mr-2">&#10148;</span>
                                    <div><strong class="text-gray-800">College Visit Best Practices Worksheet:</strong> (Link Pending)</div>
                                </li>
                                <li class="flex items-start">
                                    <span class="text-green-600 font-bold mr-2">&#10148;</span>
                                    <div><strong class="text-gray-800">Reflection Document:</strong> (Link Pending)</div>
                                </li>
                            </ul>
                        </div>
                    </div>

                    <div class="mt-8 border-t pt-6">
                         <h3 class="text-xl font-semibold text-green-700 mb-3">Compliance Reminder</h3>
                         <p class="text-gray-700">Following all procedures and meeting deadlines is mandatory. Failure to do so may result in unexcused absences and could impact school support for your post-secondary plans. If you have any questions, please reach out to Ms. Del Toro or Mr. Meyers immediately!</p>
                    </div>
                </div>
            </section>
        </main>

    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            const tabs = document.querySelectorAll('.tab-button');
            const sections = document.querySelectorAll('.section-content');

            tabs.forEach(tab => {
                tab.addEventListener('click', () => {
                    // Deactivate all tabs and sections
                    tabs.forEach(t => {
                        t.classList.remove('tab-active');
                        t.classList.add('tab-inactive');
                    });
                    sections.forEach(s => {
                        s.classList.remove('active');
                    });

                    // Activate the clicked tab
                    tab.classList.remove('tab-inactive');
                    tab.classList.add('tab-active');

                    // Activate the corresponding section
                    const targetId = tab.getAttribute('data-target');
                    const targetSection = document.getElementById(targetId);
                    if (targetSection) {
                        targetSection.classList.add('active');
                    }
                });
            });
        });
    </script>

</body>
</html>
