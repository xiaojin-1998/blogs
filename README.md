<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Personal Blog</title>
    <style>
        :root {
            --primary-color: #2563eb;
            --text-color: #1f2937;
            --bg-color: #f3f4f6;
            --card-bg: #ffffff;
            --border-color: #e5e7eb;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        /* Top Navigation Bar */
        header {
            background: #ffffff;
            border-bottom: 1px solid var(--border-color);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 2rem;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary-color);
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 1.5rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-color);
            font-weight: 500;
            transition: color 0.2s;
        }

        .nav-links a:hover {
            color: var(--primary-color);
        }

        /* Main Layout: Left Articles, Right Sidebar */
        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 2rem;
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 2rem;
        }

        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
            }
        }

        /* Article List Section */
        .main-content {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .post-card {
            background: var(--card-bg);
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .post-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .post-title {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: #111827;
            text-decoration: none;
            display: block;
        }

        .post-title:hover {
            color: var(--primary-color);
        }

        .post-meta {
            font-size: 0.875rem;
            color: #6b7280;
            margin-bottom: 1rem;
        }

        .post-excerpt {
            color: #4b5563;
            margin-bottom: 1rem;
        }

        .read-more {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 500;
        }

        .read-more:hover {
            text-decoration: underline;
        }

        /* Sidebar Widgets */
        aside {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .sidebar-widget {
            background: var(--card-bg);
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
        }

        .sidebar-widget h3 {
            font-size: 1.2rem;
            margin-bottom: 1rem;
            border-bottom: 2px solid var(--primary-color);
            padding-bottom: 0.3rem;
            display: inline-block;
        }

        .sidebar-widget ul {
            list-style: none;
            padding-left: 0;
        }

        .sidebar-widget li {
            margin-bottom: 0.75rem;
        }

        .sidebar-widget a {
            color: #4b5563;
            text-decoration: none;
            transition: color 0.2s;
        }

        .sidebar-widget a:hover {
            color: var(--primary-color);
        }

        /* Footer */
        footer {
            background: #ffffff;
            border-top: 1px solid var(--border-color);
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
            color: #6b7280;
        }
    </style>
</head>
<body>

    <!-- Navigation Bar -->
    <header>
        <div class="nav-container">
            <a href="#" class="logo">My Personal Blog</a>
            <ul class="nav-links">
                <li><a href="#">Home</a></li>
                <li><a href="#">Articles</a></li>
                <li><a href="#">Categories</a></li>
                <li><a href="#">About</a></li>
            </ul>
        </div>
    </header>

    <!-- Main Content Area -->
    <div class="container">
        <!-- Left Article List -->
        <main class="main-content">
            <article class="post-card">
                <a href="#" class="post-title">How to Build Responsive Web Layouts with Modern CSS</a>
                <div class="post-meta">Published on November 10, 2026 · Category: Web Development</div>
                <p class="post-excerpt">In this article, we dive deep into the core techniques of modern CSS layouts, including Flexbox and Grid, and how to use media queries to effortlessly adapt to any screen size.</p>
                <a href="#" class="read-more">Read More &rarr;</a>
            </article>
            
            <article class="post-card">
                <a href="#" class="post-title">A Beginner's Guide to Asynchronous Programming in Python</a>
                <div class="post-meta">Published on November 2, 2026 · Category: Python</div>
                <p class="post-excerpt">Asynchronous programming is a powerful tool for boosting the performance of I/O-bound applications. This guide walks you through the fundamentals of asyncio from scratch.</p>
                <a href="#" class="read-more">Read More &rarr;</a>
            </article>

            <article class="post-card">
                <a href="#" class="post-title">Key Trends Shaping Artificial Intelligence in 2026</a>
                <div class="post-meta">Published on October 20, 2026 · Category: Artificial Intelligence</div>
                <p class="post-excerpt">With the rapid evolution of large language models and multimodal technologies, AI adoption is accelerating across industries. Here is a roundup of the most impactful trends this year.</p>
                <a href="#" class="read-more">Read More &rarr;</a>
            </article>
        </main>
        
        <!-- Right Sidebar -->
        <aside>
            <div class="sidebar-widget">
                <h3>About Me</h3>
                <p style="color: #4b5563; font-size: 0.95rem;">Hi there! I'm a developer and writer passionate about technology and sharing knowledge. Here I document my learning notes, technical guides, and daily thoughts.</p>
            </div>
            
            <div class="sidebar-widget">
                <h3>Categories</h3>
                <ul>
                    <li><a href="#">Web Development (12)</a></li>
                    <li><a href="#">Python (8)</a></li>
                    <li><a href="#">Artificial Intelligence (5)</a></li>
                    <li><a href="#">Lifestyle & Notes (3)</a></li>
                </ul>
            </div>
            
            <div class="sidebar-widget">
                <h3>Recent Posts</h3>
                <ul>
                    <li><a href="#">How to Build Responsive Web Layouts with Modern CSS</a></li>
                    <li><a href="#">A Beginner's Guide to Asynchronous Programming in Python</a></li>
                    <li><a href="#">Key Trends Shaping Artificial Intelligence in 2026</a></li>
                </ul>
            </div>
        </aside>
    </div>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 My Personal Blog. All Rights Reserved.</p>
    </footer>

</body>
</html>
