<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Navya Vattikuti - Professional Resume</title>
    <style>
        /* ===== RESET & BASE STYLES ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #4361ee;
            --secondary: #3f37c9;
            --accent: #4895ef;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #4cc9f0;
            --warning: #f72585;
            --gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            --card-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            padding: 30px 20px;
            line-height: 1.6;
            color: var(--dark);
        }

        /* ===== CONTAINER ===== */
        .resume-container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 30px;
            box-shadow: var(--shadow);
            overflow: hidden;
            animation: slideUp 0.6s ease;
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* ===== HEADER SECTION ===== */
        .resume-header {
            background: var(--gradient);
            color: white;
            padding: 50px 40px;
            position: relative;
            overflow: hidden;
        }

        .resume-header::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .header-content {
            position: relative;
            z-index: 1;
        }

        .header-content h1 {
            font-size: 3.5em;
            font-weight: 700;
            margin-bottom: 10px;
            letter-spacing: 2px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }

        .contact-info {
            display: flex;
            gap: 30px;
            margin-top: 20px;
            flex-wrap: wrap;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            background: rgba(255,255,255,0.2);
            padding: 10px 20px;
            border-radius: 50px;
            backdrop-filter: blur(10px);
            transition: transform 0.3s ease;
        }

        .contact-item:hover {
            transform: translateY(-3px);
            background: rgba(255,255,255,0.3);
        }

        .contact-item .icon {
            font-size: 1.2em;
        }

        /* ===== MAIN CONTENT ===== */
        .main-content {
            padding: 40px;
        }

        /* ===== SECTION STYLES ===== */
        .section {
            margin-bottom: 40px;
            animation: fadeIn 0.8s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .section-title {
            font-size: 1.8em;
            color: var(--primary);
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 4px;
            background: var(--gradient);
            border-radius: 2px;
        }

        /* ===== PROFILE SUMMARY ===== */
        .profile-summary {
            background: var(--light);
            padding: 25px;
            border-radius: 15px;
            border-left: 4px solid var(--primary);
            box-shadow: var(--card-shadow);
        }

        .profile-summary p {
            color: #555;
            line-height: 1.8;
        }

        /* ===== EDUCATION GRID ===== */
        .education-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .edu-card {
            background: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: var(--card-shadow);
            transition: all 0.3s ease;
            border: 1px solid #eee;
        }

        .edu-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(67, 97, 238, 0.15);
            border-color: var(--primary);
        }

        .edu-card h3 {
            color: var(--primary);
            font-size: 1.3em;
            margin-bottom: 10px;
        }

        .edu-card .institution {
            color: #666;
            margin-bottom: 10px;
            font-size: 1em;
        }

        .edu-card .year {
            color: #999;
            font-size: 0.9em;
            margin-bottom: 10px;
        }

        .edu-card .score {
            display: inline-block;
            background: var(--gradient);
            color: white;
            padding: 5px 15px;
            border-radius: 25px;
            font-size: 0.9em;
            font-weight: 600;
        }

        /* ===== SKILLS SECTION ===== */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }

        .skill-category {
            background: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: var(--card-shadow);
            border: 1px solid #eee;
        }

        .skill-category h3 {
            color: var(--primary);
            font-size: 1.2em;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill-tag {
            background: var(--light);
            color: var(--primary);
            padding: 8px 16px;
            border-radius: 25px;
            font-size: 0.9em;
            font-weight: 500;
            transition: all 0.3s ease;
            cursor: pointer;
            border: 1px solid var(--primary);
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .skill-tag:hover {
            background: var(--gradient);
            color: white;
            transform: scale(1.05);
        }

        .skill-tag .delete-btn {
            opacity: 0;
            transition: opacity 0.3s ease;
            cursor: pointer;
            font-size: 1.1em;
        }

        .skill-tag:hover .delete-btn {
            opacity: 1;
        }

        /* ===== PROJECTS SECTION ===== */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 25px;
        }

        .project-card {
            background: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: var(--card-shadow);
            transition: all 0.3s ease;
            border: 1px solid #eee;
            position: relative;
        }

        .project-card:hover {
            transform: translateX(5px);
            border-left: 4px solid var(--primary);
        }

        .project-card h3 {
            color: var(--primary);
            font-size: 1.3em;
            margin-bottom: 15px;
            padding-right: 30px;
        }

        .project-card p {
            color: #666;
            margin-bottom: 15px;
            line-height: 1.6;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 15px;
        }

        .tech-tag {
            background: var(--light);
            color: var(--secondary);
            padding: 4px 12px;
            border-radius: 15px;
            font-size: 0.85em;
        }

        .project-year {
            position: absolute;
            top: 20px;
            right: 20px;
            background: var(--gradient);
            color: white;
            padding: 4px 12px;
            border-radius: 15px;
            font-size: 0.85em;
        }

        .delete-project {
            position: absolute;
            bottom: 20px;
            right: 20px;
            color: #ff4444;
            cursor: pointer;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .project-card:hover .delete-project {
            opacity: 1;
        }

        /* ===== INFO GRID ===== */
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }

        .info-card {
            background: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: var(--card-shadow);
        }

        .info-card h3 {
            color: var(--primary);
            margin-bottom: 20px;
            font-size: 1.2em;
        }

        .info-list {
            list-style: none;
        }

        .info-list li {
            padding: 8px 0;
            border-bottom: 1px dashed #eee;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .info-list li:last-child {
            border-bottom: none;
        }

        .info-list li::before {
            content: "•";
            color: var(--primary);
            font-weight: bold;
            font-size: 1.5em;
        }

        /* ===== HOBBIES SECTION ===== */
        .hobbies-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }

        .hobby-item {
            background: var(--light);
            padding: 12px 25px;
            border-radius: 30px;
            color: var(--primary);
            font-weight: 500;
            transition: all 0.3s ease;
            border: 1px solid var(--primary);
        }

        .hobby-item:hover {
            background: var(--gradient);
            color: white;
            transform: scale(1.05);
        }

        /* ===== ADMIN PANEL ===== */
        .admin-panel {
            margin-top: 50px;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border-radius: 20px;
            padding: 30px;
            border: 2px dashed var(--primary);
        }

        .admin-title {
            font-size: 1.5em;
            color: var(--primary);
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .admin-forms {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }

        .admin-form {
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: var(--card-shadow);
        }

        .admin-form h4 {
            color: var(--dark);
            margin-bottom: 20px;
            font-size: 1.1em;
        }

        .form-group {
            margin-bottom: 15px;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #eee;
            border-radius: 10px;
            font-size: 1em;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
        }

        .btn {
            background: var(--gradient);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 10px;
            font-size: 1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            width: 100%;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(67, 97, 238, 0.4);
        }

        .btn-secondary {
            background: linear-gradient(135deg, #4cc9f0 0%, #4895ef 100%);
        }

        /* ===== NOTIFICATION ===== */
        .notification {
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 15px 25px;
            border-radius: 10px;
            color: white;
            font-weight: 500;
            z-index: 1000;
            animation: slideIn 0.3s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        .notification.success {
            background: linear-gradient(135deg, #4CAF50 0%, #45a049 100%);
        }

        .notification.error {
            background: linear-gradient(135deg, #f44336 0%, #d32f2f 100%);
        }

        @keyframes slideIn {
            from {
                transform: translateX(100%);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        /* ===== LOADING SPINNER ===== */
        .spinner {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 50px;
            height: 50px;
            border: 5px solid var(--light);
            border-top: 5px solid var(--primary);
            border-radius: 50%;
            animation: spin 1s linear infinite;
            z-index: 1001;
        }

        @keyframes spin {
            0% { transform: translate(-50%, -50%) rotate(0deg); }
            100% { transform: translate(-50%, -50%) rotate(360deg); }
        }

        .overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 1000;
        }

        /* ===== RESPONSIVE DESIGN ===== */
        @media (max-width: 768px) {
            .resume-header {
                padding: 30px 20px;
            }

            .header-content h1 {
                font-size: 2.5em;
            }

            .contact-info {
                flex-direction: column;
                gap: 10px;
            }

            .main-content {
                padding: 20px;
            }

            .section-title {
                font-size: 1.5em;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }
        }

        /* ===== ANIMATIONS ===== */
        .pulse {
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>
    <div class="resume-container">
        <!-- Header Section -->
        <header class="resume-header">
            <div class="header-content">
                <h1 id="name">NAVYA VATTIKUTI</h1>
                <div class="contact-info">
                    <div class="contact-item">
                        <span class="icon">📧</span>
                        <span id="email">navyavattikuti03@gmail.com</span>
                    </div>
                    <div class="contact-item">
                        <span class="icon">📱</span>
                        <span id="phone">9030337686</span>
                    </div>
                </div>
            </div>
        </header>

        <!-- Main Content -->
        <main class="main-content">
            <!-- Profile Summary -->
            <section class="section">
                <h2 class="section-title">PROFILE SUMMARY</h2>
                <div class="profile-summary">
                    <p id="profile-summary">Passionate about sports with enthusiasm for learning new technologies and improving personal and professional skills.</p>
                </div>
            </section>

            <!-- Education Section -->
            <section class="section">
                <h2 class="section-title">EDUCATION</h2>
                <div class="education-grid" id="education-container"></div>
            </section>

            <!-- Technical Skills -->
            <section class="section">
                <h2 class="section-title">TECHNICAL SKILLS</h2>
                <div class="skills-container" id="skills-container"></div>
            </section>

            <!-- Projects -->
            <section class="section">
                <h2 class="section-title">PROJECTS</h2>
                <div class="projects-grid" id="projects-container"></div>
            </section>

            <!-- Soft Skills & Languages -->
            <section class="section">
                <h2 class="section-title">ADDITIONAL INFORMATION</h2>
                <div class="info-grid">
                    <div class="info-card">
                        <h3>Soft Skills</h3>
                        <ul class="info-list" id="soft-skills-list"></ul>
                    </div>
                    <div class="info-card">
                        <h3>Languages</h3>
                        <ul class="info-list" id="languages-list"></ul>
                    </div>
                </div>
            </section>

            <!-- Hobbies -->
            <section class="section">
                <h2 class="section-title">HOBBIES & INTERESTS</h2>
                <div class="hobbies-container" id="hobbies-container"></div>
            </section>

            <!-- Admin Panel -->
            <section class="admin-panel">
                <h3 class="admin-title">⚙️ Admin Panel - Manage Resume</h3>
                
                <div class="admin-forms">
                    <!-- Add Skill Form -->
                    <div class="admin-form">
                        <h4>➕ Add New Skill</h4>
                        <div class="form-group">
                            <select id="skill-category">
                                <option value="programming">Programming Language</option>
                                <option value="web">Web Application</option>
                                <option value="soft">Soft Skill</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <input type="text" id="skill-name" placeholder="Enter skill name (e.g., Python)">
                        </div>
                        <button onclick="addSkill()" class="btn">Add Skill</button>
                    </div>

                    <!-- Add Project Form -->
                    <div class="admin-form">
                        <h4>➕ Add New Project</h4>
                        <div class="form-group">
                            <input type="text" id="project-name" placeholder="Project name">
                        </div>
                        <div class="form-group">
                            <textarea id="project-desc" placeholder="Project description" rows="3"></textarea>
                        </div>
                        <div class="form-group">
                            <input type="text" id="project-tech" placeholder="Technologies (comma separated)">
                        </div>
                        <div class="form-group">
                            <input type="text" id="project-year" placeholder="Year (e.g., 2024)">
                        </div>
                        <button onclick="addProject()" class="btn btn-secondary">Add Project</button>
                    </div>

                    <!-- Update Profile Form -->
                    <div class="admin-form">
                        <h4>📝 Update Profile</h4>
                        <div class="form-group">
                            <textarea id="profile-update" placeholder="New profile summary" rows="3"></textarea>
                        </div>
                        <button onclick="updateProfile()" class="btn">Update Profile</button>
                    </div>
                </div>
            </section>
        </main>
    </div>

    <!-- Notification & Loading -->
    <div id="notification" class="notification" style="display: none;"></div>
    <div id="overlay" class="overlay"></div>
    <div id="spinner" class="spinner"></div>

    <script>
        // ===== UTILITY FUNCTIONS =====
        function showNotification(message, type) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            notification.className = `notification ${type}`;
            notification.style.display = 'block';
            
            setTimeout(() => {
                notification.style.display = 'none';
            }, 3000);
        }

        function showLoading(show) {
            document.getElementById('spinner').style.display = show ? 'block' : 'none';
            document.getElementById('overlay').style.display = show ? 'block' : 'none';
        }

        // ===== LOAD RESUME DATA =====
        async function loadResume() {
            showLoading(true);
            try {
                const response = await fetch('/api/resume');
                const data = await response.json();
                
                // Update header
                document.getElementById('name').textContent = data.name;
                document.getElementById('email').textContent = data.email;
                document.getElementById('phone').textContent = data.phone;
                document.getElementById('profile-summary').textContent = data.profile_summary;
                
                // Update education
                const educationContainer = document.getElementById('education-container');
                educationContainer.innerHTML = '';
                data.education.forEach(edu => {
                    const card = document.createElement('div');
                    card.className = 'edu-card';
                    card.innerHTML = `
                        <h3>${edu.degree}</h3>
                        <div class="institution">${edu.institution}</div>
                        <div class="year">${edu.year || ''}</div>
                        ${edu.score ? `<span class="score">${edu.score}</span>` : ''}
                    `;
                    educationContainer.appendChild(card);
                });
                
                // Update skills
                const skillsContainer = document.getElementById('skills-container');
                skillsContainer.innerHTML = `
                    <div class="skill-category">
                        <h3>💻 Programming Languages</h3>
                        <div class="skill-tags" id="programming-skills">
                            ${data.technical_skills.programming_languages.map(skill => 
                                `<span class="skill-tag" onclick="deleteSkill('programming', '${skill}')">
                                    ${skill}
                                    <span class="delete-btn">✕</span>
                                </span>`
                            ).join('')}
                        </div>
                    </div>
                    <div class="skill-category">
                        <h3>🌐 Web Applications</h3>
                        <div class="skill-tags" id="web-skills">
                            ${data.technical_skills.web_applications.map(skill => 
                                `<span class="skill-tag" onclick="deleteSkill('web', '${skill}')">
                                    ${skill}
                                    <span class="delete-btn">✕</span>
                                </span>`
                            ).join('')}
                        </div>
                    </div>
                `;
                
                // Update projects
                const projectsContainer = document.getElementById('projects-container');
                projectsContainer.innerHTML = '';
                data.projects.forEach(project => {
                    const card = document.createElement('div');
                    card.className = 'project-card';
                    card.innerHTML = `
                        <span class="project-year">${project.year || '2024'}</span>
                        <h3>${project.name}</h3>
                        <p>${project.description}</p>
                        <div class="project-tech">
                            ${(project.technologies || []).map(tech => 
                                `<span class="tech-tag">${tech}</span>`
                            ).join('')}
                        </div>
                        <span class="delete-project" onclick="deleteProject('${project.name}')">🗑️ Delete</span>
                    `;
                    projectsContainer.appendChild(card);
                });
                
                // Update soft skills
                const softSkillsList = document.getElementById('soft-skills-list');
                softSkillsList.innerHTML = '';
                data.soft_skills.forEach(skill => {
                    const li = document.createElement('li');
                    li.innerHTML = `${skill} <span style="margin-left:auto; cursor:pointer; color:#ff4444;" onclick="deleteSkill('soft', '${skill}')">✕</span>`;
                    softSkillsList.appendChild(li);
                });
                
                // Update languages
                const languagesList = document.getElementById('languages-list');
                languagesList.innerHTML = '';
                data.languages.forEach(lang => {
                    const li = document.createElement('li');
                    li.textContent = lang;
                    languagesList.appendChild(li);
                });
                
                // Update hobbies
                const hobbiesContainer = document.getElementById('hobbies-container');
                hobbiesContainer.innerHTML = '';
                data.hobbies.forEach(hobby => {
                    const span = document.createElement('span');
                    span.className = 'hobby-item';
                    span.textContent = hobby;
                    hobbiesContainer.appendChild(span);
                });
                
            } catch (error) {
                showNotification('Error loading resume: ' + error.message, 'error');
            } finally {
                showLoading(false);
            }
        }

        // ===== ADD SKILL =====
        async function addSkill() {
            const category = document.getElementById('skill-category').value;
            const skill = document.getElementById('skill-name').value.trim();
            
            if (!skill) {
                showNotification('Please enter a skill name', 'error');
                return;
            }
            
            showLoading(true);
            try {
                const response = await fetch('/api/resume/skill/add', {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({ category, skill })
                });
                
                const result = await response.json();
                if (result.success) {
                    showNotification(result.message, 'success');
                    document.getElementById('skill-name').value = '';
                    loadResume();
                } else {
                    showNotification(result.message, 'error');
                }
            } catch (error) {
                showNotification('Error adding
