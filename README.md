<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>김문기 - 개인 포트폴리오</title>
    <style>
        :root {
            --primary-color: #118c74;
            --secondary-color: #f8d45c;
            --accent-color: #ff9d8a;
            --text-color: #333;
            --light-gray: #f5f5f5;
            --medium-gray: #e0e0e0;
            --dark-gray: #555;
            --font-main: 'Pretendard', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: var(--font-main);
            color: var(--text-color);
            line-height: 1.6;
        }
        
        a {
            text-decoration: none;
            color: var(--primary-color);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            padding: 1.5rem 0;
            border-bottom: 1px solid var(--medium-gray);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-weight: bold;
            font-size: 1.5rem;
            color: var(--text-color);
        }
        
        .nav-links {
            display: flex;
            gap: 2rem;
        }
        
        .nav-links a {
            color: var(--text-color);
            font-weight: 500;
        }
        
        /* Hero Section */
        .hero {
            display: flex;
            align-items: center;
            padding: 5rem 0;
            gap: 2rem;
        }
        
        .hero-content {
            flex: 1;
        }
        
        .hero-title {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 1rem;
            line-height: 1.2;
        }
        
        .hero-subtitle {
            color: var(--dark-gray);
            margin-bottom: 1.5rem;
        }
        
        .hero-visual {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .visual-container {
            position: relative;
            width: 100%;
            height: 300px;
        }
        
        .circle-main {
            width: 200px;
            height: 200px;
            background-color: var(--primary-color);
            border-radius: 50%;
            position: absolute;
            top: 0;
            right: 40px;
        }
        
        .circle-accent {
            width: 100px;
            height: 100px;
            background-color: var(--accent-color);
            border-radius: 50%;
            position: absolute;
            top: 50px;
            right: 90px;
            opacity: 0.8;
        }
        
        .circle-large {
            width: 240px;
            height: 240px;
            border: 15px solid var(--secondary-color);
            border-radius: 50%;
            position: absolute;
            bottom: 0;
            right: 0;
        }
        
        .star {
            position: absolute;
            bottom: 50px;
            left: 30px;
            color: var(--secondary-color);
            font-size: 2rem;
        }
        
        /* Clients/Logos Section */
        .clients {
            padding: 2rem 0;
            border-top: 1px solid var(--medium-gray);
            border-bottom: 1px solid var(--medium-gray);
        }
        
        .client-logos {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 2rem;
            filter: grayscale(100%);
            opacity: 0.7;
        }
        
        .client-logo {
            font-weight: bold;
            font-size: 1.2rem;
        }
        
        /* Skills Section */
        .skills {
            padding: 5rem 0;
        }
        
        .skills-container {
            display: flex;
            justify-content: space-between;
            gap: 2rem;
        }
        
        .skill-card {
            flex: 1;
            background-color: var(--light-gray);
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
        }
        
        .skill-icon {
            width: 80px;
            height: 80px;
            background-color: #ddd;
            border-radius: 10px;
            margin: 0 auto 1.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .skill-title {
            font-weight: 600;
            margin-bottom: 0.5rem;
        }
        
        .skill-description {
            font-size: 0.9rem;
            color: var(--dark-gray);
        }
        
        /* Experience Section */
        .experience {
            padding: 5rem 0;
        }
        
        .section-title {
            font-size: 2rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .experience-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .experience-card {
            border-radius: 10px;
            overflow: hidden;
        }
        
        .exp-image {
            width: 100%;
            height: 200px;
            background-color: var(--light-gray);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .exp-content {
            padding: 1.5rem 0;
        }
        
        .exp-title {
            font-weight: 600;
            margin-bottom: 0.3rem;
        }
        
        .exp-company {
            color: var(--dark-gray);
            font-size: 0.9rem;
        }
        
        /* Education Section */
        .education {
            padding: 5rem 0;
            background-color: var(--light-gray);
        }
        
        .education-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .education-card {
            background-color: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }
        
        .stars {
            color: var(--secondary-color);
            margin-bottom: 1rem;
        }
        
        .reviewer {
            display: flex;
            align-items: center;
            margin-top: 1rem;
        }
        
        .reviewer-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: #ddd;
            margin-right: 1rem;
        }
        
        .reviewer-info h4 {
            font-weight: 600;
            margin-bottom: 0.2rem;
        }
        
        .reviewer-company {
            font-size: 0.8rem;
            color: var(--dark-gray);
        }
        
        /* Contact Section */
        .contact {
            padding: 5rem 0;
        }
        
        .contact-container {
            display: flex;
            gap: 4rem;
        }
        
        .contact-info {
            flex: 1;
        }
        
        .contact-title {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
        }
        
        .contact-text {
            margin-bottom: 2rem;
            color: var(--dark-gray);
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
        }
        
        .social-icon {
            width: 40px;
            height: 40px;
            border-radius: 5px;
            background-color: var(--light-gray);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .contact-form {
            flex: 1;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-input {
            width: 100%;
            padding: 1rem;
            border: 1px solid var(--medium-gray);
            border-radius: 5px;
            font-family: inherit;
        }
        
        textarea.form-input {
            min-height: 150px;
            resize: vertical;
        }
        
        .submit-btn {
            background-color: #333;
            color: white;
            border: none;
            padding: 1rem 2rem;
            border-radius: 5px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .submit-btn:hover {
            background-color: #000;
        }
        
        /* Footer */
        footer {
            padding: 2rem 0;
            background-color: var(--light-gray);
            text-align: center;
            color: var(--dark-gray);
            font-size: 0.9rem;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .hero {
                flex-direction: column;
                text-align: center;
            }
            
            .visual-container {
                height: 250px;
            }
            
            .skills-container, .contact-container {
                flex-direction: column;
            }
            
            .client-logos {
                flex-wrap: wrap;
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">김문기</div>
                <div class="nav-links">
                    <a href="#about">소개</a>
                    <a href="#work">경력</a>
                    <a href="#contact">연락처</a>
                </div>
            </nav>
        </div>
    </header>
    
    <!-- Hero Section -->
    <section class="hero container" id="about">
        <div class="hero-content">
            <div class="hero-subtitle">개발자 | 데이터 분석가</div>
            <h1 class="hero-title">성장에 목마른 도전자</h1>
            <p>저는 성장에 목마른 사람입니다. 대학원 과정을 거치며 리액트를 이수하고, 파이썬을 독학했습니다. '다시 해보자'라는 도전의식을 불러일으킵니다. 팀에서 저는 팔로워 역할에 강합니다. 말이 많지 않아도 할 일은 확실히 해내는 타입입니다. 업무 마감 시간은 지키는 것이 아니라 앞당기는 것입니다. 실무에서 저는 AI를 활용해 신기술을 빠르게 캐치합니다.</p>
        </div>
        <div class="hero-visual">
            <div class="visual-container">
                <div class="circle-main"></div>
                <div class="circle-accent"></div>
                <div class="circle-large"></div>
                <div class="star">★</div>
            </div>
        </div>
    </section>
    
    <!-- Clients/Logos Section -->
    <section class="clients">
        <div class="container">
            <div class="client-logos">
                <div class="client-logo">JAVA</div>
                <div class="client-logo">Spring</div>
                <div class="client-logo">React</div>
                <div class="client-logo">MySQL</div>
                <div class="client-logo">AWS</div>
            </div>
        </div>
    </section>
    
    <!-- Skills Section -->
    <section class="skills">
        <div class="container">
            <div class="skills-container">
                <div class="skill-card">
                    <div class="skill-icon">
                        <svg width="40" height="40" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M10 20L14 4M18 8L22 12L18 16M6 16L2 12L6 8" stroke="#333" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>
                    </div>
                    <h3 class="skill-title">백엔드 개발</h3>
                    <p class="skill-description">Java, Spring Boot, JPA, MySQL, Docker, AWS 등을 활용한 백엔드 서비스 개발</p>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <svg width="40" height="40" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M4 3H20C21.1046 3 22 3.89543 22 5V19C22 20.1046 21.1046 21 20 21H4C2.89543 21 2 20.1046 2 19V5C2 3.89543 2.89543 3 4 3Z" stroke="#333" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            <path d="M9 9H15M9 13H15M9 17H12" stroke="#333" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>
                    </div>
                    <h3 class="skill-title">데이터 분석</h3>
                    <p class="skill-description">Python, R, QGIS, 태블로 등을 활용한 데이터 분석 및 시각화</p>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <svg width="40" height="40" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="#333" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            <path d="M2 17L12 22L22 17" stroke="#333" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            <path d="M2 12L12 17L22 12" stroke="#333" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>
                    </div>
                    <h3 class="skill-title">프론트엔드 개발</h3>
                    <p class="skill-description">HTML, CSS, JavaScript, React를 활용한 웹 UI/UX 개발</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Experience Section -->
    <section class="experience" id="work">
        <div class="container">
            <h2 class="section-title">경력 및 학력</h2>
            <div class="experience-grid">
                <div class="experience-card">
                    <div class="exp-image" style="background-color: #ff9d8a;">
                        <svg width="60" height="60" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M22 10V15C22 20 20 22 15 22H9C4 22 2 20 2 15V9C2 4 4 2 9 2H14" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            <path d="M22 10H18C15 10 14 9 14 6V2L22 10Z" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>
                    </div>
                    <div class="exp-content">
                        <h3 class="exp-title">시립대학교 도시과학대학원 조경학과</h3>
                        <p class="exp-company">석사 연구원 (Research Studio)</p>
                    </div>
                </div>
                <div class="experience-card">
                    <div class="exp-image" style="background-color: #f8d45c;">
                        <svg width="60" height="60" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M21 10H3M21 10V16C21 19 19.5 20 17 20H7C4.5 20 3 19 3 16V10M21 10V8C21 5 19.5 4 17 4H7C4.5 4 3 5 3 8V10M7.5 15H9.5M14.5 15H16.5" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>
                    </div>
                    <div class="exp-content">
                        <h3 class="exp-title">서울시립대학교 도시과학대학 조경학과</h3>
                        <p class="exp-company">석사수료 - 졸업예정 (2022 - 2025)</p>
                    </div>
                </div>
                <div class="experience-card">
                    <div class="exp-image" style="background-color: #118c74;">
                        <svg width="60" height="60" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            <path d="M7.99998 3H8.99998C7.04998 8.84 7.04998 15.16 8.99998 21H7.99998" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            <path d="M15 3C16.95 8.84 16.95 15.16 15 21" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            <path d="M3 16V15C8.84 16.95 15.16 16.95 21 15V16" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            <path d="M3 9.0001C8.84 7.0501 15.16 7.0501 21 9.0001" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>
                    </div>
                    <div class="exp-content">
                        <h3 class="exp-title">연암대학교 스마트원예(IoT)계열</h3>
                        <p class="exp-company">원예학과 전문학사 졸업 (2018 - 2019)</p>
                    </div>
                </div>
                <div class="experience-card">
                    <div class="exp-image" style="background-color: #6c757d;">
                        <svg width="60" height="60" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M22 8V13C22 17 20 19 16 19H15.5C15.19 19 14.89 19.15 14.7 19.4L13.2 21.4C12.54 22.28 11.46 22.28 10.8 21.4L9.3 19.4C9.14 19.18 8.77 19 8.5 19H8C4 19 2 18 2 13V8C2 4 4 2 8 2H12" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            <path d="M15.2 4.62002C14.87 3.73002 15.26 2.66002 16.34 2.33002C16.9 2.14002 17.6 2.26002 18.1 2.76002C18.6 2.26002 19.3 2.14002 19.85 2.33002C20.93 2.66002 21.32 3.73002 20.99 4.62002C20.48 6.00002 18.1 7.00002 18.1 7.00002C18.1 7.00002 15.73 6.01002 15.2 4.62002Z" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            <path d="M15.9965 11H16.0054M11.9955 11H12.0045M7.99451 11H8.00349" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>
                    </div>
                    <div class="exp-content">
                        <h3 class="exp-title">숭실대학교 정보통계 보험수리학과</h3>
                        <p class="exp-company">이학사 졸업 (2007 - 2012)</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Education/Certification Section -->
    <section class="education">
        <div class="container">
            <h2 class="section-title">교육 및 자격증</h2>
            <div class="education-container">
                <div class="education-card">
                    <div class="stars">★★★★★</div>
                    <p>Java 기반 DevOps 개발자 양성과정 (JAVA, MySQL, Javascript, Servlet, Spring, React, Docker, AWS, CI/CD)</p>
                    <div class="reviewer">
                        <div class="reviewer-avatar"></div>
                        <div class="reviewer-info">
                            <h4>2025.02 ~ 현재</h4>
                            <p class="reviewer-company">진행중</p>
                        </div>
                    </div>
                </div>
                <div class="education-card">
                    <div class="stars">★★★★★</div>
                    <p>(서울대 LH) LH-서울대학교 COMPAS 도시 데이터 분석 학교</p>
                    <div class="reviewer">
                        <div class="reviewer-avatar"></div>
                        <div class="reviewer-info">
                            <h4>2025-02-17 ~ 2025-03-03</h4>
                            <p class="reviewer-company">수료</p>
                        </div>
                    </div>
                </div>
                <div class="education-card">
                    <div class="stars">★★★★★</div>
                    <p>LG CNS AM Inspire Camp (HTML/CSS, JavaScript / React)</p>
                    <div class="reviewer">
                        <div class="reviewer-avatar"></div>
                        <div class="reviewer-info">
                            <h4>2024-12 ~ 2025-01-13</h4>
                            <p class="reviewer-company">수료</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills List Section -->
    <section class="container" style="padding: 5rem 0;">
        <h2 class="section-title">기술 스킬</h2>
        <div style="columns: 2; column-gap: 3rem; margin-top: 2rem;">
            <div style="margin-bottom: 1rem;">1. Java Programming</div>
            <div style="margin-bottom: i1rem;">2. DataBase (mySQL)</div>
            <div style="margin-bottom: 1rem;">3. JDBC API</div>
            <div style="margin-bottom: 1rem;">4. HTML, CSS</div>
            <div style="margin-bottom: 1rem;">5. Javascript</div>
            <div style="margin-bottom: 1rem;">6. Servlet</div>
            <div style="margin-bottom: 1rem;">7. JSP</div>
            <div style="margin-bottom: 1rem;">8. Spring Framework</div>
            <div style="margin-bottom: 1rem;">9. Spring Boot</div>
            <div style="margin-bottom: 1rem;">10. ORM – JPA</div>
            <div style="margin-bottom: 1rem;">11. React</div>
            <div style="margin-bottom: 1rem;">12. Docker</div>
            <div style="margin-bottom: 1rem;">13. AWS(EC2,RDS)</div>
            <div style="margin-bottom: 1rem;">14. CI/CD</div>
        </div>
    </section>
    
    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="contact-container">
                <div class="contact-info">
                    <h2 class="contact-title">연락 가능한 방법</h2>
                    <p class="contact-text">새로운 기술을 배우고 이를 실무에 적용하는 과정에 관심이 많습니다. 함께 일하고 싶으시다면 연락주세요.</p>
                    <div>
                        <strong>김문기</strong><br>
                        전화번호: 010-7907-8282<br>
                        LinkedIn: <a href="http://www.linkedin.com/in/mgkim2025/" target="_blank">www.linkedin.com/in/mgkim2025/</a>
                    </div>
                    <div class="social-links">
                        <a href="#" class="social-icon">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 22H15C20 22 22 20 22 15V9C22 4 20 2 15 2H9C4 2 2 4 2 9V15C2 20 4 22 9 22Z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                                <path d="M12 15.5C13.933 15.5 15.5 13.933 15.5 12C15.5 10.067 13.933 8.5 12 8.5C10.067 8.5 8.5 10.067 8.5 12C8.5 13.933 10.067 15.5 12 15.5Z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                                <path d="M17.636 7H17.648" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>
                        </a>
                        <a href="#" class="social-icon">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M14 9.3V12.2H16.6C16.8 12.2 16.9 12.4 16.9 12.6L16.5 14.5C16.5 14.6 16.3 14.7 16.2 14.7H14V22H11V14.8H9.3C9.1 14.8 9 14.7 9 14.5V12.6C9 12.4 9.1 12.3 9.3 12.3H11V9C11 7.3 12.3 6 14 6H16.7C16.9 6 17 6.1 17 6.3V8.7C17 8.9 16.9 9 16.7 9H14.3C14.1 9 14 9.1 14 9.3Z" stroke="currentColor" stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="round"/>
                            </svg>
                        </a>
                        <a href="#" class="social-icon">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M16 4H8C6.34315 4 5 5.34315 5 7V17C5 18.6569 6.34315 20 8 20H16C17.6569 20 19 18.6569 19 17V7C19 5.34315 17.6569 4 16 4Z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                                <path d="M9 12L15 12" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                                <path d="M12 15L12 9" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>
                        </a>
                        <a href="http://www.linkedin.com/in/mgkim2025/" target="_blank" class="social-icon">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M7 10V17" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                                <path d="M11 13V17" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                                <path d="M11 13C11 11.3431 12.3431 10 14 10C15.6569 10 17 11.3431 17 13V17" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                                <path d="M7 7.01L7.01 6.99889" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>
                        </a>
                    </div>

# portfolio

# 김문기 - 개인 포트폴리오 웹사이트

## 📜 프로젝트 설명

본 프로젝트는 개발자이자 데이터 분석가인 김문기의 개인 포트폴리오 웹사이트입니다. 자신을 "성장에 목마른 도전자"로 소개하며, 보유 기술, 경력, 학력 및 교육 사항을 상세히 보여줍니다. 이 웹사이트는 잠재적인 고용주나 협업자에게 자신의 역량을 효과적으로 전달하기 위해 제작되었습니다.

## ✨ 주요 기능

* **헤더 및 내비게이션**: 사이트의 주요 섹션(소개, 경력, 연락처)으로 빠르게 이동할 수 있는 내비게이션 바를 포함합니다.
* **Hero 섹션**: 방문자를 맞이하는 자기소개와 시선을 사로잡는 시각적 요소로 구성되어 있습니다.
* **기술 스택 로고**: 사용 가능한 주요 기술(JAVA, Spring, React, MySQL, AWS 등)을 로고 형태로 보여줍니다.
* **기술 역량**: 백엔드 개발, 데이터 분석, 프론트엔드 개발 등 주요 기술 역량을 아이콘과 함께 설명합니다.
* **경력 및 학력**: 주요 경력 사항과 학력 정보를 카드 형태로 제공합니다.
* **교육 및 자격증**: 이수한 교육 과정 및 자격증 정보를 보여줍니다.
* **상세 기술 스킬 목록**: Java, Spring Boot, React, Docker, AWS, Python 등 보유하고 있는 구체적인 기술 스킬들을 나열합니다.
* **연락처**: 전화번호, 이메일(HTML에는 없으나 일반적으로 포함), LinkedIn 프로필 링크 등 연락 가능한 방법을 안내합니다.
* **반응형 웹 디자인**: 다양한 화면 크기(데스크톱, 태블릿, 모바일)에 최적화된 레이아웃을 제공합니다.

## 🛠️ 사용 기술

* **프론트엔드**:
    * HTML5
    * CSS3 (CSS Variables, Flexbox, Grid, 반응형 웹 디자인)
    * JavaScript (웹사이트 인터랙션 및 동적 기능 구현에 사용될 수 있음)
* **주요 언급 기술 (포트폴리오 내용 기반)**:
    * **백엔드**: Java, Spring, Spring Boot, JPA, Servlet, JSP
    * **데이터베이스**: MySQL
    * **데이터 분석**: Python, R, QGIS, 태블로
    * **프론트엔드 라이브러리/프레임워크**: React
    * **클라우드 및 DevOps**: AWS (EC2, RDS), Docker, CI/CD

## 🚀 웹사이트 보는 방법

1.  이 프로젝트의 모든 파일 (HTML, CSS, 이미지 등)을 다운로드합니다.
2.  `250513 portfolio.html` (또는 `index.html`로 이름을 변경한 경우 해당 파일)을 웹 브라우저에서 엽니다. (예: Chrome, Firefox, Safari, Edge 등)

* *참고: 이 웹사이트가 GitHub Pages, Netlify, Vercel 등과 같은 호스팅 플랫폼에 배포된 경우, 해당 라이브 URL을 여기에 추가할 수 있습니다.*
    * 예시: `https://your-username.github.io/portfolio/`

## 📞 연락처 정보

* **이름**: 김문기
* **전화
