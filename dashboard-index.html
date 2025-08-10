<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Public School – Interactive Student Dashboard</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        html, body { min-height: 100%; }
        .dashboard-bg { background: linear-gradient(135deg, #f8fafc 0%, #ffffff 50%, #fef3c7 100%);}
        .tab-content { display: none; }
        .tab-active { display: block; }
        .transition-smooth { transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);}
        .card-hover:hover { transform: translateY(-4px); box-shadow: 0 10px 25px -5px rgba(0,0,0,0.1);}
        .modal-backdrop { backdrop-filter: blur(5px);}
        .feedback-star { cursor: pointer; }
        .hidden { display: none !important; }
        .show { display: block !important; }
        .dark { background: #18181b; color: #e5e7eb; }
        .dark .bg-white { background: #23232a; color: #e5e7eb; }
        .dark .text-gray-900 { color: #e5e7eb; }
        .dark .text-gray-700 { color: #d1d5db; }
        .dark .text-gray-600 { color: #a1a1aa; }
        .dark .border-gray-200 { border-color: #444; }
        .dark .bg-gradient-to-r { background: linear-gradient(135deg, #23232a 0%, #18181b 100%);}
        .badge { background: #f59e42; color: #fff; font-weight: bold; padding: 2px 8px; border-radius: 8px; font-size: 0.8em; }
        .avatar { object-fit: cover; border-radius: 9999px; width: 48px; height: 48px; }
        .avatar-lg { width: 96px; height: 96px; }
        .comment-box { background: #f3f4f6; border-radius: 8px; padding: 8px 12px; margin-bottom: 8px; }
        .dark .comment-box { background: #23232a; }
        .nav-tab.active { background: #2563eb; color: #fff; }
        .project-month-badge { background: #f59e42; color: #fff; font-weight: bold; padding: 2px 8px; border-radius: 8px; font-size: 0.8em; margin-left: 8px;}
        .top-contributor-badge { background: #3b82f6; color: #fff; font-weight: bold; padding: 2px 8px; border-radius: 8px; font-size: 0.8em; margin-left: 8px;}
        .class-chat-box { max-height: 200px; overflow-y: auto; background: #f3f4f6; border-radius: 8px; padding: 8px; margin-bottom: 8px;}
        .dark .class-chat-box { background: #23232a; }
        input, textarea, select { color: black !important; }
        input::placeholder, textarea::placeholder { color: gray !important; }
        .dark input::placeholder, .dark textarea::placeholder { color: #a1a1aa !important; }
        .project-of-month-card { transform: scale(1.05); border: 2px solid #f59e42; }
        @media (max-width: 640px) {
            .nav-tab { font-size: 0.9em; padding: 0.5em 0.7em; }
        }
        .star-rating { display: flex; flex-direction: row-reverse; justify-content: flex-end; }
        .star-rating input { display: none; }
        .star-rating label { color: #ccc; cursor: pointer; font-size: 1.5em; }
        .star-rating label:before { content: '★'; }
        .star-rating input:checked ~ label { color: #f59e0b; }
        .star-rating label:hover, .star-rating label:hover ~ label { color: #f59e0b; }
    </style>
</head>
<body class="font-sans antialiased text-gray-800 dashboard-bg">
<div id="app" class="min-h-screen">
    <!-- Auth Page -->
    <div id="auth-page" class="min-h-screen flex items-center justify-center p-4 dashboard-bg">
        <div class="w-full max-w-md">
            <div class="text-center mb-8">
                <div class="w-20 h-20 bg-gradient-to-r from-blue-600 to-purple-600 rounded-full inline-flex items-center justify-center mb-4 shadow-lg">
                    <i data-lucide="school" class="w-10 h-10 text-white"></i>
                </div>
                <h1 class="text-3xl font-bold text-gray-900 mb-2">Modern Public School</h1>
                <p class="text-gray-600 mb-2">Delhi, India – Student Dashboard</p>
                <div class="flex items-center justify-center text-blue-600 text-sm gap-1">
                    <i data-lucide="shield" class="w-4 h-4"></i>
                    <span>Secure Authentication (Demo)</span>
                </div>
            </div>
            <div class="bg-white p-8 rounded-xl shadow-xl border border-gray-200">
                <div class="flex justify-center mb-6">
                    <div class="bg-gray-100 p-1 rounded-lg">
                        <button id="login-tab-btn" class="px-4 py-2 rounded-md transition-colors bg-blue-600 text-white">Sign In</button>
                        <button id="signup-tab-btn" class="px-4 py-2 rounded-md transition-colors text-gray-600">Sign Up</button>
                    </div>
                </div>
                <!-- Login Form -->
                <form id="login-form" class="space-y-4">
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Email</label>
                        <input type="email" id="login-email" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 transition-smooth" required>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Password</label>
                        <input type="password" id="login-password" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 transition-smooth" required>
                    </div>
                    <button type="submit" class="w-full bg-gradient-to-r from-blue-600 to-purple-600 text-white py-3 rounded-lg font-medium hover:from-blue-700 hover:to-purple-700 transition-smooth shadow-md flex items-center justify-center gap-2">
                        <i data-lucide="log-in" class="w-5 h-5"></i>
                        Sign In
                    </button>
                </form>
                <!-- Signup Form -->
                <form id="signup-form" class="space-y-4 hidden mt-6">
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Full Name</label>
                        <input type="text" id="signup-name" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 transition-smooth" required>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Role</label>
                        <select id="signup-role" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 transition-smooth">
                            <option value="student">Student</option>
                            <option value="teacher">Teacher</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Email</label>
                        <input type="email" id="signup-email" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 transition-smooth" readonly>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Password</label>
                        <input type="password" id="signup-password" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 transition-smooth" required>
                    </div>
                    <button type="submit" class="w-full bg-gradient-to-r from-blue-600 to-purple-600 text-white py-3 rounded-lg font-medium hover:from-blue-700 hover:to-purple-700 transition-smooth shadow-md flex items-center justify-center gap-2">
                        <i data-lucide="user-plus" class="w-5 h-5"></i>
                        Create Account
                    </button>
                </form>
            </div>
        </div>
    </div>
    <!-- Dashboard -->
    <div id="dashboard" class="min-h-screen hidden">
        <!-- Top Navigation -->
        <nav class="bg-white shadow-md border-b border-gray-200 fixed w-full top-0 z-50">
            <div class="max-w-7xl mx-auto px-4">
                <div class="flex justify-between items-center h-16">
                    <div class="flex items-center gap-2">
                        <div class="w-10 h-10 bg-gradient-to-r from-blue-600 to-purple-600 rounded-full flex items-center justify-center">
                            <i data-lucide="school" class="w-6 h-6 text-white"></i>
                        </div>
                        <div>
                            <div class="font-bold text-gray-900">Modern Public School</div>
                            <div class="text-xs text-gray-500" id="user-role-display">Dashboard</div>
                        </div>
                    </div>
                    <div class="flex gap-1">
                        <button data-tab="home" class="nav-tab flex items-center gap-2 px-4 py-2 rounded-lg text-sm font-medium bg-blue-100 text-blue-700 transition-smooth active">
                            <i data-lucide="home" class="w-4 h-4"></i> Home
                        </button>
                        <button data-tab="classes" class="nav-tab flex items-center gap-2 px-4 py-2 rounded-lg text-sm font-medium text-gray-600 hover:bg-gray-100 transition-smooth">
                            <i data-lucide="book-open" class="w-4 h-4"></i> Classes
                        </button>
                        <button data-tab="projects" class="nav-tab flex items-center gap-2 px-4 py-2 rounded-lg text-sm font-medium text-gray-600 hover:bg-gray-100 transition-smooth">
                            <i data-lucide="folder" class="w-4 h-4"></i> Projects
                        </button>
                        <button data-tab="analytics" class="nav-tab flex items-center gap-2 px-4 py-2 rounded-lg text-sm font-medium text-gray-600 hover:bg-gray-100 transition-smooth">
                            <i data-lucide="bar-chart-3" class="w-4 h-4"></i> Analytics
                        </button>
                        <button data-tab="feedback" class="nav-tab flex items-center gap-2 px-4 py-2 rounded-lg text-sm font-medium text-gray-600 hover:bg-gray-100 transition-smooth">
                            <i data-lucide="message-circle" class="w-4 h-4"></i> Feedback
                        </button>
                        <button data-tab="profile" class="nav-tab flex items-center gap-2 px-4 py-2 rounded-lg text-sm font-medium text-gray-600 hover:bg-gray-100 transition-smooth">
                            <i data-lucide="user" class="w-4 h-4"></i> Profile
                        </button>
                        <button id="theme-toggle" class="ml-2 px-2 py-2 rounded-lg text-gray-600 hover:bg-gray-100 transition-smooth">
                            <i data-lucide="moon" class="w-5 h-5"></i>
                        </button>
                    </div>
                    <div class="flex items-center gap-3">
                        <div class="hidden sm:block text-right">
                            <div class="text-sm font-medium text-gray-900" id="user-name-display">User Name</div>
                            <div class="text-xs text-gray-500" id="user-class-display">Student</div>
                        </div>
                        <img id="user-avatar" class="avatar w-8 h-8 bg-gradient-to-r from-blue-600 to-purple-600 rounded-full flex items-center justify-center text-white font-bold" src="" alt="avatar">
                        <button id="logout-btn" class="p-2 text-gray-600 hover:text-red-600 hover:bg-red-50 rounded-lg transition-smooth">
                            <i data-lucide="log-out" class="w-5 h-5"></i>
                        </button>
                    </div>
                </div>
            </div>
        </nav>
        <!-- Main Content -->
        <main class="pt-16 pb-8">
            <div id="home-tab" class="tab-content tab-active p-4 max-w-7xl mx-auto">
                <h2 class="text-2xl font-bold">Welcome, <span id="welcome-user-name"></span>!</h2>
                <div class="mt-4 grid grid-cols-1 md:grid-cols-3 gap-6">
                    <div class="bg-white p-4 rounded-xl shadow-md border border-gray-200">
                        <div class="flex items-center gap-3">
                            <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center text-blue-600">
                                <i data-lucide="book-open" class="w-6 h-6"></i>
                            </div>
                            <div>
                                <div class="text-gray-500 text-sm">Classes</div>
                                <div class="text-xl font-bold" id="home-classes-count">0</div>
                            </div>
                        </div>
                    </div>
                    <div class="bg-white p-4 rounded-xl shadow-md border border-gray-200">
                        <div class="flex items-center gap-3">
                            <div class="w-12 h-12 bg-green-100 rounded-full flex items-center justify-center text-green-600">
                                <i data-lucide="folder" class="w-6 h-6"></i>
                            </div>
                            <div>
                                <div class="text-gray-500 text-sm">Projects</div>
                                <div class="text-xl font-bold" id="home-projects-count">0</div>
                            </div>
                        </div>
                    </div>
                    <div class="bg-white p-4 rounded-xl shadow-md border border-gray-200">
                        <div class="flex items-center gap-3">
                            <div class="w-12 h-12 bg-amber-100 rounded-full flex items-center justify-center text-amber-600">
                                <i data-lucide="star" class="w-6 h-6"></i>
                            </div>
                            <div>
                                <div class="text-gray-500 text-sm">Project of Month</div>
                                <div class="text-xl font-bold" id="home-potm">0</div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="mt-8 bg-white p-4 rounded-xl shadow-md border border-gray-200">
                    <h3 class="text-lg font-bold mb-4">Recent Classes</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4" id="home-recent-classes"></div>
                </div>

                <div class="mt-8 bg-white p-4 rounded-xl shadow-md border border-gray-200">
                    <h3 class="text-lg font-bold mb-4">Recent Projects</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4" id="home-recent-projects"></div>
                </div>
            </div>
            <div id="classes-tab" class="tab-content p-4 max-w-7xl mx-auto"></div>
            <div id="projects-tab" class="tab-content p-4 max-w-7xl mx-auto"></div>
            <div id="analytics-tab" class="tab-content p-4 max-w-7xl mx-auto"></div>
            <div id="feedback-tab" class="tab-content p-4 max-w-7xl mx-auto"></div>
            <div id="profile-tab" class="tab-content p-4 max-w-7xl mx-auto"></div>
        </main>
    </div>
    <div id="modal-container" class="fixed inset-0 z-50 hidden items-center justify-center p-4 modal-backdrop"></div>
</div>
<script>
// =================== ICONS ===================
lucide.createIcons();

// =================== DATA STORAGE ===================
function getUsers() { return JSON.parse(localStorage.getItem("users") || "[]"); }
function saveUsers(users) { localStorage.setItem("users", JSON.stringify(users)); }
function getCurrentUser() { return JSON.parse(localStorage.getItem("currentUser") || "null"); }
function setCurrentUser(user) { localStorage.setItem("currentUser", JSON.stringify(user)); }
function getClasses() { return JSON.parse(localStorage.getItem("classes") || "[]"); }
function saveClasses(classes) { localStorage.setItem("classes", JSON.stringify(classes)); }
function getProjects() { return JSON.parse(localStorage.getItem("projects") || "[]"); }
function saveProjects(projects) { localStorage.setItem("projects", JSON.stringify(projects)); }
function getFeedbacks() { return JSON.parse(localStorage.getItem("feedbacks") || "[]"); }
function saveFeedbacks(feedbacks) { localStorage.setItem("feedbacks", JSON.stringify(feedbacks)); }
function getProjectOfMonth() { return localStorage.getItem("projectOfMonth") || ""; }
function setProjectOfMonth(id) { localStorage.setItem("projectOfMonth", id); }

// Initialize sample data if empty
function initializeSampleData() {
    // Check if users exist
    if (getUsers().length === 0) {
        const sampleUsers = [
            {
                name: "Mrs. Sharma",
                email: "mrs.sharma@mps.com",
                password: "teacher123",
                role: "teacher",
                avatar: "https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/cc671523-bb26-4fe5-ac9c-3f75343d6acf.png",
                bio: "Mathematics teacher at Modern Public School",
                classes: ["class1"],
                projects: [],
                badges: []
            },
            {
                name: "Rahul Student",
                email: "rahul.student@mps.com",
                password: "student123",
                role: "student",
                avatar: "https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/2fcd49b6-3304-4c0d-9f0b-6247150b9182.png",
                bio: "Class 10 student at Modern Public School",
                classes: ["class1"],
                projects: ["p1"],
                badges: []
            }
        ];
        saveUsers(sampleUsers);
    }

    // Check if classes exist
    if (getClasses().length === 0) {
        const sampleClasses = [{
            id: "class1",
            name: "Mathematics 10A",
            subject: "Mathematics",
            grade: "Grade 10",
            description: "Advanced mathematics course for grade 10 students",
            code: "MATH10A",
            members: ["mrs.sharma@mps.com", "rahul.student@mps.com"],
            chat: [
                { user: "Mrs. Sharma", text: "Welcome to our mathematics class!" },
                { user: "Rahul Student", text: "Thank you, looking forward to learning!" }
            ],
            projects: ["p1"]
        }];
        saveClasses(sampleClasses);
    }

    // Check if projects exist
    if (getProjects().length === 0) {
        const sampleProjects = [{
            id: "p1",
            title: "Geometry in Architecture",
            link: "https://example.com/geometry-architecture",
            video: "https://example.com/videos/geometry",
            description: "Exploring geometric principles in ancient and modern architecture",
            creators: ["rahul.student@mps.com"],
            date: new Date().toLocaleDateString(),
            likes: 3,
            views: 15,
            comments: [
                { user: "Mrs. Sharma", text: "Excellent project demonstrating real-world applications!" }
            ]
        }];
        saveProjects(sampleProjects);
    }
}

initializeSampleData();

// =================== UTILITY FUNCTIONS ===================
function generateEmailFromName(name, role) {
    const cleanName = name.toLowerCase().replace(/\s+/g, '.');
    return `${cleanName}.${role}@mps.com`;
}

function getTopContributor() {
    let projects = getProjects();
    let users = getUsers();
    let counts = {};
    
    projects.forEach(p => {
        p.creators.forEach(email => {
            counts[email] = (counts[email] || 0) + 1;
        });
    });
    
    let top = Object.entries(counts).sort((a,b) => b[1] - a[1])[0];
    if (!top) return null;
    return users.find(u => u.email === top[0]);
}

function getMostLikedProject() {
    let projects = getProjects();
    if (!projects.length) return "None";
    let sorted = projects.slice().sort((a,b) => (b.likes || 0) - (a.likes || 0));
    return sorted[0].title || "None";
}

function updateProjectViews(projectId) {
    let projects = getProjects();
    let project = projects.find(p => p.id === projectId);
    if (project) {
        project.views = (project.views || 0) + 1;
        saveProjects(projects);
    }
}

function renderHomePage(user) {
    // Set welcome message
    document.getElementById("welcome-user-name").textContent = user.name;
    
    // Update stats
    const userClasses = getClasses().filter(c => c.members && c.members.includes(user.email));
    const userProjects = getProjects().filter(p => p.creators.includes(user.email));
    const projectOfMonth = getProjectOfMonth();
    
    document.getElementById("home-classes-count").textContent = userClasses.length;
    document.getElementById("home-projects-count").textContent = userProjects.length;
    document.getElementById("home-potm").textContent = projectOfMonth ? "1" : "0";
    
    // Render recent classes
    const recentClassesContainer = document.getElementById("home-recent-classes");
    recentClassesContainer.innerHTML = userClasses.slice(0, 3).map(c => `
        <div class="bg-white p-4 rounded-lg shadow-sm border border-gray-200 card-hover">
            <div class="font-bold">${c.name}</div>
            <div class="text-sm text-gray-600">${c.subject}</div>
            <div class="text-xs text-gray-500 mt-2">${c.members.length} members</div>
            <button onclick="openClassChat(${getClasses().findIndex(cl => cl.id === c.id)})" class="mt-2 bg-blue-100 text-blue-600 px-2 py-1 rounded text-sm">View Class</button>
        </div>
    `).join("") || "<div class='text-gray-400'>No recent classes</div>";
    
    // Render recent projects
    const recentProjectsContainer = document.getElementById("home-recent-projects");
    recentProjectsContainer.innerHTML = userProjects.slice(0, 3).map(p => `
        <div class="bg-white p-4 rounded-lg shadow-sm border border-gray-200 card-hover">
            <div class="font-bold">${p.title}</div>
            <div class="text-sm text-gray-600">${new Date(p.date).toLocaleDateString()}</div>
            <div class="flex justify-between mt-2">
                <span class="text-sm">${p.likes || 0} likes</span>
                <span class="text-sm">${p.views || 0} views</span>
            </div>
            <button onclick="viewProjectDetail('${p.id}')" class="mt-2 bg-purple-100 text-purple-600 px-2 py-1 rounded text-sm">View Project</button>
        </div>
    `).join("") || "<div class='text-gray-400'>No recent projects</div>";
}

function viewProjectDetail(projectId) {
    updateProjectViews(projectId);
    
    const project = getProjects().find(p => p.id === projectId);
    if (!project) return;
    
    showModal(`
        <div class="p-6">
            <h2 class="text-xl font-bold mb-2">${project.title}</h2>
            <div class="text-gray-500 text-sm mb-4">Created by: ${project.creators.map(c => getUsers().find(u => u.email === c)?.name || c).join(", ")}</div>
            <div class="mb-4">
                <p class="text-gray-700">${project.description}</p>
            </div>
            <div class="flex gap-4 mb-4">
                <div class="bg-blue-100 text-blue-700 px-3 py-1 rounded">${project.views || 0} views</div>
                <div class="bg-green-100 text-green-700 px-3 py-1 rounded">${project.likes || 0} likes</div>
            </div>
            <div>
                <a href="${project.link}" target="_blank" class="text-blue-600 hover:underline">View Project</a>
                ${project.video ? `<a href="${project.video}" target="_blank" class="text-purple-600 hover:underline ml-4">View Video</a>` : ''}
            </div>
            ${getCurrentUser().role === "teacher" ? `
                <div class="mt-4 flex gap-2">
                    <button onclick="setProjectOfMonth('${project.id}'); closeModal(); renderProjectsTab(getCurrentUser());" class="bg-yellow-100 text-yellow-600 px-3 py-1 rounded-md">
                        Set as Project of Month
                    </button>
                    <button onclick="deleteProject('${project.id}')" class="bg-red-100 text-red-600 px-3 py-1 rounded-md">
                        Delete Project
                    </button>
                </div>
            ` : ''}
        </div>
    `);
}

// =================== AUTHENTICATION ===================
document.addEventListener("DOMContentLoaded", function () {
    // Tabs for login/signup
    const loginTabBtn = document.getElementById("login-tab-btn");
    const signupTabBtn = document.getElementById("signup-tab-btn");
    const loginForm = document.getElementById("login-form");
    const signupForm = document.getElementById("signup-form");
    const authPage = document.getElementById("auth-page");
    const dashboard = document.getElementById("dashboard");
    const logoutBtn = document.getElementById("logout-btn");

    // Auto-fill email in signup form based on name and role
    document.getElementById("signup-name").addEventListener('input', function() {
        const name = this.value.trim();
        const role = document.getElementById("signup-role").value;
        if (name && role) {
            document.getElementById("signup-email").value = generateEmailFromName(name, role);
        }
    });
    
    document.getElementById("signup-role").addEventListener('change', function() {
        const name = document.getElementById("signup-name").value.trim();
        if (name) {
            document.getElementById("signup-email").value = generateEmailFromName(name, this.value);
        }
    });

    // Switch tabs
    loginTabBtn.onclick = function () {
        loginTabBtn.classList.add("bg-blue-600", "text-white");
        signupTabBtn.classList.remove("bg-blue-600", "text-white");
        loginForm.classList.remove("hidden");
        signupForm.classList.add("hidden");
    };
    
    signupTabBtn.onclick = function () {
        signupTabBtn.classList.add("bg-blue-600", "text-white");
        loginTabBtn.classList.remove("bg-blue-600", "text-white");
        signupForm.classList.remove("hidden");
        loginForm.classList.add("hidden");
    };

    // Signup
    signupForm.onsubmit = function (e) {
        e.preventDefault();
        const name = document.getElementById("signup-name").value.trim();
        const email = document.getElementById("signup-email").value.trim().toLowerCase();
        const password = document.getElementById("signup-password").value;
        const role = document.getElementById("signup-role").value;
        
        if (!name || !email || !password) {
            alert("Please fill all fields.");
            return;
        }
        
        let users = getUsers();
        if (users.find(u => u.email === email)) {
            alert("Email already registered.");
            return;
        }
        
        const user = { 
            name, 
            email, 
            password, 
            role, 
            avatar: "", 
            bio: "", 
            classes: [], 
            projects: [], 
            badges: [] 
        };
        
        users.push(user);
        saveUsers(users);
        setCurrentUser(user);
        showDashboard(user);
    };

    // Login
    loginForm.onsubmit = function (e) {
        e.preventDefault();
        const email = document.getElementById("login-email").value.trim().toLowerCase();
        const password = document.getElementById("login-password").value;
        
        let users = getUsers();
        let user = users.find(u => u.email === email && u.password === password);
        
        if (!user) {
            alert("Invalid email or password.");
            return;
        }
        
        setCurrentUser(user);
        showDashboard(user);
    };

    // Logout
    logoutBtn.onclick = function () {
        localStorage.removeItem("currentUser");
        dashboard.classList.add("hidden");
        authPage.classList.remove("hidden");
        loginTabBtn.click();
    };

    // Auto-login if already logged in
    const currentUser = getCurrentUser();
    if (currentUser) {
        showDashboard(currentUser);
    } else {
        authPage.classList.remove("hidden");
        dashboard.classList.add("hidden");
        loginTabBtn.click();
    }
});

// =================== DASHBOARD FUNCTIONS ===================
function showDashboard(user) {
    const authPage = document.getElementById("auth-page");
    const dashboard = document.getElementById("dashboard");
    
    authPage.classList.add("hidden");
    dashboard.classList.remove("hidden");
    
    // Update user info in header
    document.getElementById("user-name-display").textContent = user.name;
    document.getElementById("user-role-display").textContent = user.role.charAt(0).toUpperCase() + user.role.slice(1) + " Dashboard";
    document.getElementById("user-class-display").textContent = user.role.charAt(0).toUpperCase() + user.role.slice(1);
    document.getElementById("user-avatar").src = user.avatar || "https://ui-avatars.com/api/?name=" + encodeURIComponent(user.name);
    
    // Setup tabs and render content
    setupTabs();
    renderHomePage(user);
    renderClassesTab(user);
    renderProjectsTab(user);
    renderAnalyticsTab(user);
    renderProfileTab(user);
    renderFeedbackTab(user);
}

// =================== TAB MANAGEMENT ===================
function setupTabs() {
    document.querySelectorAll(".nav-tab").forEach(btn => {
        btn.onclick = function () {
            document.querySelectorAll(".tab-content").forEach(tab => tab.classList.remove("tab-active"));
            document.querySelectorAll(".nav-tab").forEach(tab => tab.classList.remove("active"));
            document.getElementById(btn.getAttribute("data-tab") + "-tab").classList.add("tab-active");
            btn.classList.add("active");
            
            const currentUser = getCurrentUser();
            const tab = btn.getAttribute("data-tab");
            
            switch(tab) {
                case "home":
                    renderHomePage(currentUser);
                    break;
                case "classes":
                    renderClassesTab(currentUser);
                    break;
                case "projects":
                    renderProjectsTab(currentUser);
                    break;
                case "analytics":
                    renderAnalyticsTab(currentUser);
                    break;
                case "profile":
                    renderProfileTab(currentUser);
                    break;
                case "feedback":
                    renderFeedbackTab(currentUser);
                    break;
            }
        };
    });
    
    // Theme toggle
    document.getElementById("theme-toggle").onclick = function () {
        document.body.classList.toggle("dark");
        const icon = this.querySelector("i");
        if (document.body.classList.contains("dark")) {
            icon.setAttribute("data-lucide", "sun");
        } else {
            icon.setAttribute("data-lucide", "moon");
        }
        lucide.createIcons();
    };
}

// =================== CLASSES TAB ===================
function renderClassesTab(user) {
    let classes = getClasses();
    const userClasses = classes.filter(c => c.members && c.members.includes(user.email));
    
    let html = `
        <div class="flex justify-between items-center mb-4">
            <h2 class="text-2xl font-bold text-gray-900">Classes</h2>
            <div>
                ${(user.role === "teacher") ? `
                    <button id="create-class-btn" class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition-smooth shadow-md flex items-center gap-2">
                        <i data-lucide="plus" class="w-5 h-5"></i>Create Class
                    </button>
                ` : ""}
                ${(user.role === "student") ? `
                    <button id="join-class-btn" class="bg-white text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-50 transition-smooth shadow-sm border border-gray-300 flex items-center gap-2">
                        <i data-lucide="users" class="w-5 h-5"></i>Join Class
                    </button>
                ` : ""}
            </div>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            ${userClasses.length ? userClasses.map((c, idx) => `
                <div class="bg-white p-4 rounded-xl shadow-sm border border-gray-200 card-hover">
                    <div class="font-bold text-lg">${c.name}</div>
                    <div class="text-xs text-gray-500">${c.subject} – ${c.grade}</div>
                    <div class="text-sm text-gray-700 mb-2">${c.description || ""}</div>
                    <div class="text-xs text-gray-500 mb-2">Invite Code: <span class="font-mono">${c.code}</span></div>
                    <div class="flex gap-2 flex-wrap mb-2">
                        ${c.members?.map(m => `<span class="bg-blue-100 text-blue-700 px-2 py-1 rounded">${getUsers().find(u => u.email === m)?.name || m}</span>`).join("") || ""}
                    </div>
                    <div class="flex gap-2">
                        <button onclick="openClassChat(${idx})" class="bg-purple-100 text-purple-600 px-2 py-1 rounded">Open Chat</button>
                        <button onclick="openClassProjects(${idx})" class="bg-green-100 text-green-600 px-2 py-1 rounded">Class Projects</button>
                        ${user.role === "teacher" ? `
                            <button onclick="deleteClass('${c.id}')" class="bg-red-100 text-red-600 px-2 py-1 rounded">Delete</button>
                        ` : ''}
                    </div>
                </div>
            `).join("") : `
                <div class="col-span-full text-center py-8 text-gray-400">
                    <i data-lucide="book-open" class="w-8 h-8 mx-auto mb-2"></i>
                    <p>No classes yet</p>
                </div>
            `}
        </div>
    `;
    
    document.getElementById("classes-tab").innerHTML = html;
    
    if (user.role === "teacher") {
        document.getElementById("create-class-btn").onclick = function () {
            showModal(`
                <form id="class-form" class="p-6 space-y-4">
                    <h2 class="text-xl font-bold mb-2">Create New Class</h2>
                    <input type="text" id="class-name" class="w-full px-4 py-2 border rounded" placeholder="Class Name" required>
                    <input type="text" id="class-subject" class="w-full px-4 py-2 border rounded" placeholder="Subject" required>
                    <input type="text" id="class-grade" class="w-full px-4 py-2 border rounded" placeholder="Grade" required>
                    <textarea id="class-description" class="w-full px-4 py-2 border rounded" placeholder="Description"></textarea>
                    <button type="submit" class="bg-blue-600 text-white px-4 py-2 rounded">Create</button>
                </form>
            `);
            
            document.getElementById("class-form").onsubmit = function(e) {
                e.preventDefault();
                let classes = getClasses();
                let code = Math.random().toString(36).substring(2,10).toUpperCase();
                
                classes.push({
                    id: "class" + Date.now(),
                    name: document.getElementById("class-name").value,
                    subject: document.getElementById("class-subject").value,
                    grade: document.getElementById("class-grade").value,
                    description: document.getElementById("class-description").value,
                    code,
                    members: [getCurrentUser().email],
                    chat: [],
                    projects: []
                });
                
                saveClasses(classes);
                closeModal();
                renderClassesTab(getCurrentUser());
            };
        };
    }
    
    if (user.role === "student") {
        document.getElementById("join-class-btn").onclick = function () {
            showModal(`
                <form id="join-class-form" class="p-6 space-y-4">
                    <h2 class="text-xl font-bold mb-2">Join a Class</h2>
                    <input type="text" id="join-class-code" class="w-full px-4 py-2 border rounded" placeholder="Invite Code" required>
                    <button type="submit" class="bg-blue-600 text-white px-4 py-2 rounded">Join</button>
                </form>
            `);
            
            document.getElementById("join-class-form").onsubmit = function(e) {
                e.preventDefault();
                let code = document.getElementById("join-class-code").value.trim();
                let classes = getClasses();
                let found = classes.find(c => c.code === code);
                
                if (!found) {
                    alert("Invalid class code.");
                    return;
                }
                
                if (!found.members.includes(getCurrentUser().email)) {
                    found.members.push(getCurrentUser().email);
                    saveClasses(classes);
                    closeModal();
                    renderClassesTab(getCurrentUser());
                } else {
                    alert("You're already a member of this class.");
                }
            };
        };
    }
}

function deleteClass(classId) {
    if (confirm("Are you sure you want to delete this class?")) {
        let classes = getClasses().filter(c => c.id !== classId);
        saveClasses(classes);
        renderClassesTab(getCurrentUser());
    }
}

// =================== CLASS CHAT ===================
function openClassChat(idx) {
    let classes = getClasses();
    let c = classes[idx];
    
    showModal(`
        <div class="p-6">
            <h2 class="text-xl font-bold mb-2">Class Chat: ${c.name}</h2>
            <div id="class-chat-list" class="class-chat-box mb-4">
                ${(c.chat||[]).map(msg => `
                    <div class="mb-2">
                        <span class="font-bold">${msg.user}:</span> 
                        <span>${msg.text}</span>
                    </div>
                `).join("")}
            </div>
            <form id="class-chat-form" class="flex gap-2">
                <input type="text" id="class-chat-input" class="flex-1 px-4 py-2 border rounded" placeholder="Type a message..." required>
                <button type="submit" class="bg-blue-600 text-white px-4 py-2 rounded">Send</button>
            </form>
        </div>
    `);
    
    document.getElementById("class-chat-form").onsubmit = function(e) {
        e.preventDefault();
        let msg = document.getElementById("class-chat-input").value;
        c.chat = c.chat || [];
        c.chat.push({ 
            user: getCurrentUser().name, 
            text: msg,
            timestamp: new Date().toISOString()
        });
        
        classes[idx] = c;
        saveClasses(classes);
        
        // Update chat display
        document.getElementById("class-chat-list").innerHTML = c.chat.map(msg => `
            <div class="mb-2">
                <span class="font-bold">${msg.user}:</span> 
                <span>${msg.text}</span>
            </div>
        `).join("");
        
        document.getElementById("class-chat-input").value = "";
    };
}

// =================== CLASS PROJECTS ===================
function openClassProjects(idx) {
    let classes = getClasses();
    let c = classes[idx];
    let projects = getProjects();
    
    showModal(`
        <div class="p-6">
            <h2 class="text-xl font-bold mb-2">Projects in ${c.name}</h2>
            ${(getCurrentUser().role === "teacher" || c.members.includes(getCurrentUser().email)) ? `
                <div class="mb-4">
                    <button id="add-class-project-btn" class="bg-blue-600 text-white px-4 py-2 rounded">
                        Add Project to Class
                    </button>
                </div>
            ` : ''}
            <div id="class-projects-list">
                ${(c.projects||[]).map(pid => {
                    let p = projects.find(pr => pr.id === pid);
                    return p ? `
                        <div class="border rounded-lg p-4 mb-2">
                            <div class="font-bold">${p.title}</div>
                            <div class="text-xs text-gray-500">${p.date}</div>
                            <div class="text-sm text-gray-700">${p.description}</div>
                            <div class="mt-2">
                                <button onclick="viewProjectDetail('${p.id}')" class="bg-purple-100 text-purple-600 px-2 py-1 rounded text-sm">
                                    View Details
                                </button>
                                ${getCurrentUser().role === "teacher" ? `
                                    <button onclick="removeProjectFromClass('${c.id}', '${p.id}', ${idx})" class="bg-red-100 text-red-600 px-2 py-1 rounded text-sm ml-2">
                                        Remove
                                    </button>
                                ` : ''}
                            </div>
                        </div>
                    ` : "";
                }).join("") || "<div>No projects yet.</div>"}
            </div>
        </div>
    `);

    if (document.getElementById("add-class-project-btn")) {
        document.getElementById("add-class-project-btn").onclick = function() {
            let availableProjects = getProjects().filter(p => 
                p.creators.includes(getCurrentUser().email) && 
                !c.projects.includes(p.id)
            );
            
            showModal(`
                <div class="p-6">
                    <h2 class="text-xl font-bold mb-2">Add Your Project to ${c.name}</h2>
                    <form id="add-class-project-form">
                        <select id="class-project-select" class="w-full px-4 py-2 border rounded" required>
                            <option value="">Select Project...</option>
                            ${availableProjects.map(p => `
                                <option value="${p.id}">${p.title}</option>
                            `).join("")}
                        </select>
                        <button type="submit" class="bg-blue-600 text-white px-4 py-2 rounded mt-2">
                            Add to Class
                        </button>
                    </form>
                </div>
            `);
            
            document.getElementById("add-class-project-form").onsubmit = function(e) {
                e.preventDefault();
                let pid = document.getElementById("class-project-select").value;
                if (!pid) return;
                
                c.projects = c.projects || [];
                c.projects.push(pid);
                classes[idx] = c;
                saveClasses(classes);
                
                closeModal();
                openClassProjects(idx);
            };
        };
    }
}

function removeProjectFromClass(classId, projectId, classIndex) {
    if (confirm("Are you sure you want to remove this project from the class?")) {
        let classes = getClasses();
        let classObj = classes.find(c => c.id === classId);
        
        if (classObj) {
            classObj.projects = classObj.projects.filter(p => p !== projectId);
            saveClasses(classes);
            openClassProjects(classIndex);
        }
    }
}

// =================== PROJECTS TAB ===================
function renderProjectsTab(user) {
    let projects = getProjects();
    let projectOfMonth = getProjectOfMonth();
    let projectOfMonthData = projects.find(p => p.id === projectOfMonth);
    
    let html = `
        <div class="flex justify-between items-center mb-4">
            <h2 class="text-2xl font-bold text-gray-900">Student Projects</h2>
            <button id="add-project-btn" class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition-smooth shadow-md flex items-center gap-2">
                <i data-lucide="plus" class="w-5 h-5"></i>Add Project
            </button>
        </div>
        
        ${projectOfMonthData ? `
            <div class="mb-6">
                <div class="bg-amber-50 p-4 rounded-xl shadow-sm border border-amber-200 card-hover project-of-month-card mb-4">
                    <div class="flex items-center mb-2">
                        <div class="project-month-badge">Project of the Month</div>
                    </div>
                    <div class="font-bold text-xl">${projectOfMonthData.title}</div>
                    <div class="text-sm text-gray-700 mb-2">${projectOfMonthData.description}</div>
                    <div class="flex gap-2 flex-wrap mb-2">
                        ${projectOfMonthData.creators?.map(t => `
                            <span class="bg-blue-100 text-blue-700 px-2 py-1 rounded">
                                ${getUsers().find(u => u.email === t)?.name || t}
                            </span>
                        `).join("") || ""}
                    </div>
                    <div class="flex gap-2">
                        <button onclick="likeProject('${projectOfMonthData.id}')" class="bg-pink-100 text-pink-600 px-2 py-1 rounded">Like</button>
                        <button onclick="showCommentsModal('${projectOfMonthData.id}')" class="bg-blue-100 text-blue-600 px-2 py-1 rounded">Comments</button>
                        ${(user.role==="teacher") ? `
                            <button onclick="unsetProjectOfMonth()" class="bg-gray-100 text-gray-600 px-2 py-1 rounded">Remove Selection</button>
                        ` : ''}
                    </div>
                </div>
            </div>
        ` : ''}
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            ${projects.length ? projects.map(p => {
                if (p.id === projectOfMonth) return ''; // Skip if it's the project of the month
                return `
                    <div class="bg-white p-4 rounded-xl shadow-sm border border-gray-200 card-hover">
                        <div class="font-bold text-lg">${p.title}</div>
                        <div class="text-xs text-gray-500">${p.date}</div>
                        <div class="text-sm text-gray-700 mb-2">${p.description}</div>
                        <div class="flex gap-2 flex-wrap mb-2">
                            ${p.creators?.map(t => `
                                <span class="bg-blue-100 text-blue-700 px-2 py-1 rounded">
                                    ${getUsers().find(u => u.email === t)?.name || t}
                                </span>
                            `).join("") || ""}
                        </div>
                        <div class="flex gap-2">
                            <button onclick="likeProject('${p.id}')" class="bg-pink-100 text-pink-600 px-2 py-1 rounded">Like</button>
                            <button onclick="showCommentsModal('${p.id}')" class="bg-blue-100 text-blue-600 px-2 py-1 rounded">Comments</button>
                            ${(user.role==="teacher") ? `
                                <button onclick="setProjectOfMonth('${p.id}')" class="bg-yellow-100 text-yellow-600 px-2 py-1 rounded">Select as POM</button>
                            ` : ''}
                            ${p.creators.includes(user.email) || user.role === "teacher" ? `
                                <button onclick="deleteProject('${p.id}')" class="bg-red-100 text-red-600 px-2 py-1 rounded">Delete</button>
                            ` : ''}
                        </div>
                    </div>
                `;
            }).join("") : `
                <div class="col-span-full text-center py-8 text-gray-400">
                    <i data-lucide="folder" class="w-8 h-8 mx-auto mb-2"></i>
                    <p>No projects yet</p>
                </div>
            `}
        </div>
    `;
    
    document.getElementById("projects-tab").innerHTML = html;
    document.getElementById("add-project-btn").onclick = showProjectModal;
}

function likeProject(projectId) {
    let projects = getProjects();
    let project = projects.find(p => p.id === projectId);
    
    if (project) {
        project.likes = (project.likes || 0) + 1;
        saveProjects(projects);
        
        // Refresh display
        renderProjectsTab(getCurrentUser());
    }
}

function showCommentsModal(projectId) {
    let projects = getProjects();
    let project = projects.find(p => p.id === projectId);
    
    if (!project) return;
    
    showModal(`
        <div class="p-6">
            <h2 class="text-xl font-bold mb-2">Comments on ${project.title}</h2>
            <div id="comments-list" class="mb-4 max-h-60 overflow-y-auto">
                ${(project.comments||[]).map(c => `
                    <div class="comment-box mb-2">
                        <div class="font-bold">${c.user}</div>
                        <div>${c.text}</div>
                    </div>
                `).join("")}
            </div>
            <form id="comment-form" class="flex gap-2">
                <input type="text" id="comment-input" class="flex-1 px-4 py-2 border rounded" placeholder="Add a comment..." required>
                <button type="submit" class="bg-blue-600 text-white px-4 py-2 rounded">Post</button>
            </form>
        </div>
    `);
    
    document.getElementById("comment-form").onsubmit = function(e) {
        e.preventDefault();
        let commentText = document.getElementById("comment-input").value.trim();
        
        if (!commentText) return;
        
        project.comments = project.comments || [];
        project.comments.push({
            user: getCurrentUser().name,
            text: commentText,
            timestamp: new Date().toISOString()
        });
        
        saveProjects(projects);
        
        // Refresh comments display
        document.getElementById("comments-list").innerHTML = project.comments.map(c => `
            <div class="comment-box mb-2">
                <div class="font-bold">${c.user}</div>
                <div>${c.text}</div>
            </div>
        `).join("");
        
        document.getElementById("comment-input").value = "";
    };
}

function unsetProjectOfMonth() {
    setProjectOfMonth("");
    renderProjectsTab(getCurrentUser());
}

function showProjectModal() {
    showModal(`
        <form id="project-upload-form" class="p-6 space-y-4">
            <h2 class="text-xl font-bold mb-2">Upload Project</h2>
            <input type="text" id="project-title" class="w-full px-4 py-2 border rounded" placeholder="Project Title" required>
            <input type="url" id="project-link" class="w-full px-4 py-2 border rounded" placeholder="Project URL" required>
            <input type="url" id="project-video" class="w-full px-4 py-2 border rounded" placeholder="Video URL (optional)">
            <textarea id="project-description" class="w-full px-4 py-2 border rounded" placeholder="Project Description" required></textarea>
            <button type="submit" class="bg-blue-600 text-white px-4 py-2 rounded">Upload</button>
        </form>
    `);
    
    document.getElementById("project-upload-form").onsubmit = function(e) {
        e.preventDefault();
        let projects = getProjects();
        let user = getCurrentUser();
        
        let newProject = {
            id: "p" + Date.now(),
            title: document.getElementById("project-title").value.trim(),
            link: document.getElementById("project-link").value.trim(),
            video: document.getElementById("project-video").value.trim() || null,
            description: document.getElementById("project-description").value.trim(),
            creators: [user.email],
            date: new Date().toLocaleDateString(),
            likes: 0,
            views: 0,
            comments: []
        };
        
        if (!newProject.title || !newProject.link || !newProject.description) {
            alert("Please fill all required fields.");
            return;
        }
        
        projects.push(newProject);
        saveProjects(projects);
        
        closeModal();
        renderProjectsTab(user);
    };
}

function deleteProject(projectId) {
    if (confirm("Are you sure you want to delete this project?")) {
        let projects = getProjects().filter(p => p.id !== projectId);
        saveProjects(projects);
        
        // If this was the project of month, unset it
        if (getProjectOfMonth() === projectId) {
            setProjectOfMonth("");
        }
        
        renderProjectsTab(getCurrentUser());
    }
}

// =================== ANALYTICS TAB ===================
function renderAnalyticsTab(user) {
    let projects = getProjects();
    let feedbacks = getFeedbacks();
    
    // Prepare project statistics
    let projectStats = projects.map(p => {
        let likes = p.likes || 0;
        let views = p.views || 0;
        let comments = p.comments ? p.comments.length : 0;
        let feedbacksForProject = feedbacks.filter(f => f.project === p.id);
        let avgRating = feedbacksForProject.length ? 
            feedbacksForProject.reduce((sum, f) => sum + f.rating, 0) / feedbacksForProject.length : 0;
        
        return {
            id: p.id,
            title: p.title,
            likes,
            views,
            comments,
            feedbackCount: feedbacksForProject.length,
            avgRating: avgRating.toFixed(1)
        };
    });
    
    // Sort by most likes first
    projectStats.sort((a, b) => b.likes - a.likes);
    
    let html = `
        <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-200 mb-6">
            <h2 class="text-xl font-bold mb-4 text-gray-900">Engagement Analytics</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                <div>
                    <h3 class="text-lg font-semibold mb-2">Projects by Likes</h3>
                    <canvas id="likes-chart" height="200"></canvas>
                </div>
                <div>
                    <h3 class="text-lg font-semibold mb-2">Projects by Views</h3>
                    <canvas id="views-chart" height="200"></canvas>
                </div>
            </div>
            <div>
                <h3 class="text-lg font-semibold mb-2">Projects Ratings</h3>
                <canvas id="ratings-chart" height="200"></canvas>
            </div>
        </div>
        
        <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-200 mb-6">
            <h2 class="text-xl font-bold mb-4 text-gray-900">Top Projects</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                ${projectStats.slice(0, 6).map(p => {
                    const project = projects.find(proj => proj.id === p.id);
                    return `
                        <div class="border rounded-lg p-4">
                            <div class="font-bold">${project.title}</div>
                            <div class="text-xs text-gray-500">${project.date}</div>
                            <div class="mb-2 mt-1 flex gap-2">
                                <span class="bg-blue-100 text-blue-700 px-2 py-1 rounded text-xs">${p.views} views</span>
                                <span class="bg-pink-100 text-pink-700 px-2 py-1 rounded text-xs">${p.likes} likes</span>
                                <span class="bg-purple-100 text-purple-700 px-2 py-1 rounded text-xs">${p.feedbackCount} reviews</span>
                                <span class="bg-amber-100 text-amber-700 px-2 py-1 rounded text-xs">${p.avgRating}/5</span>
                            </div>
                            <button onclick="viewProjectDetail('${p.id}')" class="w-full bg-blue-100 text-blue-700 px-2 py-1 rounded text-sm mt-2">
                                View Details
                            </button>
                        </div>
                    `;
                }).join("")}
            </div>
        </div>
    `;
    
    document.getElementById("analytics-tab").innerHTML = html;
    
    // Render charts
    renderCharts(projects, projectStats);
}

function renderCharts(projects, projectStats) {
    const likesCtx = document.getElementById("likes-chart").getContext("2d");
    const viewsCtx = document.getElementById("views-chart").getContext("2d");
    const ratingsCtx = document.getElementById("ratings-chart").getContext("2d");
    
    // Sort by likes
    projectStats.sort((a, b) => b.likes - a.likes);
    const topByLikes = projectStats.slice(0, 5);
    
    new Chart(likesCtx, {
        type: "bar",
        data: {
            labels: topByLikes.map(p => projects.find(proj => proj.id === p.id).title),
            datasets: [{
                label: "Likes",
                data: topByLikes.map(p => p.likes),
                backgroundColor: "#3b82f6"
            }]
        },
        options: {
            responsive: true,
            plugins: {
                legend: { display: false }
            },
            scales: {
                y: { beginAtZero: true }
            }
        }
    });
    
    // Sort by views
    projectStats.sort((a, b) => b.views - a.views);
    const topByViews = projectStats.slice(0, 5);
    
    new Chart(viewsCtx, {
        type: "bar",
        data: {
            labels: topByViews.map(p => projects.find(proj => proj.id === p.id).title),
            datasets: [{
                label: "Views",
                data: topByViews.map(p => p.views),
                backgroundColor: "#10b981"
            }]
        },
        options: {
            responsive: true,
            plugins: {
                legend: { display: false }
            },
            scales: {
                y: { beginAtZero: true }
            }
        }
    });
    
    // Sort by rating
    projectStats.sort((a, b) => b.avgRating - a.avgRating);
    const topByRating = projectStats.slice(0, 5).filter(p => p.avgRating > 0);
    
    new Chart(ratingsCtx, {
        type: "bar",
        data: {
            labels: topByRating.map(p => projects.find(proj => proj.id === p.id).title),
            datasets: [{
                label: "Average Rating",
                data: topByRating.map(p => p.avgRating),
                backgroundColor: "#f59e0b"
            }]
        },
        options: {
            responsive: true,
            plugins: {
                legend: { display: false }
            },
            scales: {
                y: { 
                    beginAtZero: true,
                    max: 5
                }
            }
        }
    });
}

// =================== PROFILE TAB ===================
function renderProfileTab(user) {
    let html = `
        <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-200">
            <div class="flex items-center gap-4 mb-4">
                <img id="profile-avatar-display" class="avatar avatar-lg" src="${user.avatar || "https://ui-avatars.com/api/?name=" + encodeURIComponent(user.name)}" alt="user avatar">
                <div>
                    <div class="font-bold text-xl" id="profile-name-display">${user.name}</div>
                    <div class="text-gray-600" id="profile-role-display">${user.role.charAt(0).toUpperCase() + user.role.slice(1)}</div>
                    <div class="text-gray-600" id="profile-email-display">${user.email}</div>
                </div>
            </div>
            
            <div class="mb-4">
                <div class="font-bold mb-1">Bio</div>
                <div id="profile-bio-display">${user.bio || "No bio yet."}</div>
            </div>
            
            <div class="mb-4">
                <div class="font-bold mb-1">Joined Classes</div>
                <div>${getClasses().filter(c => c.members && c.members.includes(user.email)).map(c => c.name).join(", ") || "None"}</div>
            </div>
            
            <div class="mb-4">
                <div class="font-bold mb-1">Uploaded Projects</div>
                <div>${getProjects().filter(p => p.creators.includes(user.email)).map(p => p.title).join(", ") || "None"}</div>
            </div>
            
            <div class="mb-4">
                <div class="font-bold mb-1">Badges</div>
                <div>
                    ${user.badges?.map(b => `<span class="badge">${b}</span>`).join("") || "None"}
                    ${getTopContributor()?.email === user.email ? `<span class="top-contributor-badge">Top Contributor</span>` : ''}
                </div>
            </div>
            
            <button id="edit-profile-btn" class="bg-blue-600 text-white px-4 py-2 rounded">Edit Profile</button>
        </div>
    `;
    
    document.getElementById("profile-tab").innerHTML = html;
    
    document.getElementById("edit-profile-btn").onclick = function() {
        showModal(`
            <form id="profile-form" class="p-6 space-y-4">
                <h2 class="text-xl font-bold mb-2">Edit Profile</h2>
                <input type="text" id="profile-edit-name" class="w-full px-4 py-2 border rounded" value="${user.name}" required>
                <textarea id="profile-edit-bio" class="w-full px-4 py-2 border rounded" placeholder="Bio">${user.bio || ""}</textarea>
                <input type="url" id="profile-edit-avatar" class="w-full px-4 py-2 border rounded" value="${user.avatar}" placeholder="Avatar Image URL">
                <button type="submit" class="bg-blue-600 text-white px-4 py-2 rounded">Save</button>
            </form>
        `);
        
        document.getElementById("profile-form").onsubmit = function(e) {
            e.preventDefault();
            let users = getUsers();
            let userIndex = users.findIndex(u => u.email === user.email);
            
            if (userIndex !== -1) {
                users[userIndex].name = document.getElementById("profile-edit-name").value.trim();
                users[userIndex].bio = document.getElementById("profile-edit-bio").value.trim();
                users[userIndex].avatar = document.getElementById("profile-edit-avatar").value.trim();
                
                saveUsers(users);
                setCurrentUser(users[userIndex]);
                
                closeModal();
                renderProfileTab(users[userIndex]);
                
                // Update header
                document.getElementById("user-name-display").textContent = users[userIndex].name;
                document.getElementById("user-avatar").src = users[userIndex].avatar || 
                    "https://ui-avatars.com/api/?name=" + encodeURIComponent(users[userIndex].name);
            }
        };
    };
}

// =================== FEEDBACK TAB ===================
function renderFeedbackTab(user) {
    let projects = getProjects();
    let feedbacks = getFeedbacks();
    let html = `
        <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-200 mb-6">
            <h2 class="text-xl font-bold mb-4 text-gray-900">Submit Feedback</h2>
            <form id="feedback-form" class="space-y-4">
                <select id="feedback-project-select" class="w-full px-4 py-2 border rounded" required>
                    <option value="">Select Project...</option>
                    ${projects.map(p => `
                        <option value="${p.id}">${p.title}</option>
                    `).join("")}
                </select>
                
                <div class="star-rating">
                    <input type="radio" id="star5" name="rating" value="5">
                    <label for="star5" title="Excellent">5 stars</label>
                    <input type="radio" id="star4" name="rating" value="4">
                    <label for="star4" title="Good">4 stars</label>
                    <input type="radio" id="star3" name="rating" value="3">
                    <label for="star3" title="Average">3 stars</label>
                    <input type="radio" id="star2" name="rating" value="2">
                    <label for="star2" title="Poor">2 stars</label>
                    <input type="radio" id="star1" name="rating" value="1">
                    <label for="star1" title="Very Poor">1 star</label>
                </div>
                
                <textarea id="feedback-comment" class="w-full px-4 py-2 border rounded" placeholder="Your feedback..." required></textarea>
                
                <button type="submit" class="bg-blue-600 text-white px-4 py-2 rounded">Submit Feedback</button>
            </form>
        </div>
        
        <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-200">
            <h2 class="text-xl font-bold mb-4 text-gray-900">Feedback History</h2>
            <div class="space-y-4">
                ${feedbacks.filter(f => f.user === user.email).length ? 
                    feedbacks.filter(f => f.user === user.email).map(f => {
                        let project = projects.find(p => p.id === f.project);
                        return `
                            <div class="border rounded-lg p-4">
                                <div class="flex justify-between items-start mb-2">
                                    <div class="font-bold">${project?.title || "Project"}</div>
                                    <div class="flex gap-1">
                                        ${Array.from({ length: 5 }).map((_, i) => `
                                            <i data-lucide="star" class="w-4 h-4 ${i < f.rating ? 'text-yellow-400 fill-yellow-400' : 'text-gray-300'}"></i>
                                        `).join("")}
                                    </div>
                                </div>
                                <div class="text-gray-700">${f.comment}</div>
                                <div class="text-xs text-gray-500 mt-2">${new Date(f.timestamp || new Date()).toLocaleDateString()}</div>
                            </div>
                        `;
                    }).join("") : `
                        <div class="text-center py-8 text-gray-400">
                            <i data-lucide="message-circle" class="w-8 h-8 mx-auto mb-2"></i>
                            <p>No feedback submitted yet</p>
                        </div>
                    `
                }
            </div>
        </div>
    `;
    
    document.getElementById("feedback-tab").innerHTML = html;
    
    // Submit feedback form
    document.getElementById("feedback-form").onsubmit = function(e) {
        e.preventDefault();
        
        const projectId = document.getElementById("feedback-project-select").value;
        const rating = parseInt(document.querySelector('input[name="rating"]:checked')?.value);
        const comment = document.getElementById("feedback-comment").value.trim();
        
        if (!projectId || !rating || !comment) {
            alert("Please fill all fields and provide a rating.");
            return;
        }
        
        let feedbacks = getFeedbacks();
        feedbacks.push({
            project: projectId,
            rating: rating,
            comment: comment,
            user: user.email,
            timestamp: new Date().toISOString()
        });
        
        saveFeedbacks(feedbacks);
        
        // Reset form
        document.getElementById("feedback-project-select").value = "";
        document.querySelectorAll('input[name="rating"]').forEach(radio => radio.checked = false);
        document.getElementById("feedback-comment").value = "";
        
        // Refresh feedback display
        renderFeedbackTab(user);
        
        // Show success message
        showModal(`
            <div class="p-6 text-center">
                <i data-lucide="check-circle" class="w-12 h-12 text-green-500 mx-auto mb-4"></i>
                <h2 class="text-xl font-bold mb-2">Feedback Submitted</h2>
                <p>Thank you for your feedback!</p>
                <button onclick="closeModal()" class="bg-blue-600 text-white px-4 py-2 rounded mt-4">Close</button>
            </div>
        `);
    };
}

// =================== MODAL FUNCTIONS ===================
function showModal(html) {
    let modal = document.getElementById("modal-container");
    modal.innerHTML = `
        <div class="bg-white rounded-xl shadow-2xl max-w-lg w-full mx-auto overflow-y-auto max-h-[90vh]">
            ${html}
        </div>
    `;
    modal.classList.remove("hidden");
    modal.onclick = function(e) {
        if (e.target === modal) closeModal();
    };
}

function closeModal() {
    let modal = document.getElementById("modal-container");
    modal.classList.add("hidden");
    modal.innerHTML = "";
}

// Initialize icons after DOM loads
window.addEventListener('DOMContentLoaded', function() {
    lucide.createIcons();
});
</script>
</body>
</html>
