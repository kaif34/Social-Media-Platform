<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Social Media Platform</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <style>body {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        line-height: 1.6;
        margin: 0;
        padding: 0;
        background: linear-gradient(135deg, #f5f7fa, #e4e7eb);
        color: #333;
        transition: all 0.3s ease;
    }
    
    header {
        background: linear-gradient(135deg, #2b5876, #4e4376);
        color: #fff;
        text-align: center;
        padding: 2rem;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
        position: sticky;
        top: 0;
        z-index: 1000;
        animation: slideDown 0.6s ease;
    }
    
    @keyframes slideDown {
        from {
            transform: translateY(-100%);
        }
        to {
            transform: translateY(0);
        }
    }
    
    header h1 {
        margin: 0;
        font-size: 2.8em;
        font-weight: 700;
        text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.3);
        animation: fadeIn 1.2s ease;
        letter-spacing: 1px;
    }
    
    @keyframes fadeIn {
        from {
            opacity: 0;
            transform: translateY(-10px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
    
    nav {
        margin-top: 2rem;
        display: flex;
        justify-content: center;
        gap: 1.5rem;
        flex-wrap: wrap;
    }
    
    button {
        background: linear-gradient(135deg, #667eea, #764ba2);
        border: none;
        color: white;
        padding: 14px 28px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 4px 2px;
        cursor: pointer;
        border-radius: 30px;
        transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        position: relative;
        overflow: hidden;
        font-weight: 600;
        letter-spacing: 0.5px;
    }
    
    button:before {
        content: '';
        position: absolute;
        top: 0;
        left: -100%;
        width: 100%;
        height: 100%;
        background: linear-gradient(120deg, transparent, rgba(255, 255, 255, 0.4), transparent);
        transition: 0.6s;
    }
    
    button:hover:before {
        left: 100%;
    }
    
    button:hover {
        background: linear-gradient(135deg, #5a67d8, #6b46c1);
        transform: translateY(-3px) scale(1.05);
        box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
    }
    
    main {
        padding: 3rem;
        max-width: 1200px;
        margin: 0 auto;
        animation: fadeInUp 0.8s ease;
    }
    
    @keyframes fadeInUp {
        from {
            opacity: 0;
            transform: translateY(30px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
    
    form {
        background: rgba(255, 255, 255, 0.95);
        padding: 2.5rem;
        border-radius: 25px;
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.12);
        transition: all 0.5s ease;
        backdrop-filter: blur(20px);
        border: 1px solid rgba(255, 255, 255, 0.2);
    }
    
    form:hover {
        transform: translateY(-10px);
        box-shadow: 0 15px 35px rgba(0, 0, 0, 0.18);
    }
    
    input,
    textarea {
        width: 100%;
        padding: 1.2rem;
        margin-bottom: 1.5rem;
        border: 2px solid #e2e8f0;
        border-radius: 20px;
        transition: all 0.4s ease;
        font-size: 1.1rem;
        background: rgba(255, 255, 255, 0.95);
        box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.06);
    }
    
    input:focus,
    textarea:focus {
        border-color: #667eea;
        box-shadow: 0 0 0 4px rgba(102, 126, 234, 0);
        outline: none;
        transform: scale(1.02);
    }
    
    .post {
        background: linear-gradient(135deg, #ffffff, #f8fafc);
        border: none;
        border-radius: 25px;
        padding: 2.5rem;
        margin-bottom: 2.5rem;
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.12);
        transition: all 0.5s ease;
        animation: slideIn 0.6s ease;
        backdrop-filter: blur(20px);
        border: 1px solid rgba(255, 255, 255, 0);
    }
    
    @keyframes slideIn {
        from {
            opacity: 0;
            transform: translateX(-30px);
        }
        to {
            opacity: 1;
            transform: translateX(0);
        }
    }
    
    .post:hover {
        transform: translateY(-10px) scale(1.02);
        box-shadow: 0 15px 35px rgba(0, 0, 0, 0.18);
        background: linear-gradient(135deg, #f8fafc, #f1f5f9);
    }
    
    .post-actions {
        margin-top: 2rem;
        display: flex;
        gap: 20px;
        flex-wrap: wrap;
    }
    
    .post-actions button {
        flex: 1;
        min-width: 140px;
        font-size: 1rem;
        padding: 12px 24px;
        background: linear-gradient(135deg, #ff6b6b, #f03e3e);
    }
    
    .comment {
        background-color: #f8fafc;
        border-left: 5px solid #667eea;
        border-radius: 0 20px 20px 0;
        padding: 1.5rem;
        margin-top: 1.2rem;
        transition: all 0.4s ease;
        animation: slideInRight 0.4s ease;
        box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
    }
    
    @keyframes slideInRight {
        from {
            opacity: 0;
            transform: translateX(30px);
        }
        to {
            opacity: 1;
            transform: translateX(0);
        }
    }
    
    .comment:hover {
        background-color: #f1f5f9;
        transform: translateX(10px);
        box-shadow: 4px 6px 20px rgba(0, 0, 0, 0.12);
    }
    
    .profile-header {
        background: linear-gradient(135deg, #ffffff, #f8fafc);
        padding: 3rem;
        border-radius: 30px;
        margin-bottom: 3rem;
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.12);
        backdrop-filter: blur(20px);
        border: 1px solid rgba(255, 255, 255, 0.2);
        animation: fadeInDown 0.6s ease;
    }
    
    @keyframes fadeInDown {
        from {
            opacity: 0;
            transform: translateY(-30px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
    
    .profile-stats {
        display: flex;
        justify-content: space-around;
        margin: 2.5rem 0;
        gap: 2rem;
    }
    
    .stat-box {
        text-align: center;
        padding: 2rem;
        background: linear-gradient(135deg, #f8fafc, #f1f5f9);
        border-radius: 20px;
        min-width: 180px;
        transition: all 0.4s ease;
        box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
    }
    
    .stat-box:hover {
        transform: translateY(-8px) scale(1.05);
        box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        background: linear-gradient(135deg, #f1f5f9, #e2e8f0);
    }
    
    #theme-toggle {
        position: fixed;
        bottom: 40px;
        right: 40px;
        z-index: 1000;
        padding: 25px;
        border-radius: 50%;
        background: linear-gradient(135deg, #667eea, #764ba2);
        animation: pulse 2.5s infinite;
        box-shadow: 0 6px 20px rgba(0, 0, 0, 0.2);
    }
    
    @keyframes pulse {
        0% {
            box-shadow: 0 0 0 0 rgba(102, 126, 234, 0.5);
        }
        70% {
            box-shadow: 0 0 0 15px rgba(102, 126, 234, 0);
        }
        100% {
            box-shadow: 0 0 0 0 rgba(102, 126, 234, 0);
        }
    }
    
    .upload-preview {
        max-width: 400px;
        max-height: 400px;
        object-fit: cover;
        margin-top: 1.5rem;
        border-radius: 15px;
        display: none;
        box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
        transition: all 0.4s ease;
    }
    
    img {
        max-width: 100%;
        height: auto;
        border-radius: 15px;
        margin: 1.5rem 0;
        box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
        transition: all 0.4s ease;
    }
    
    img:hover {
        transform: scale(1.02);
        box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
    }</style>
</head>

<body>
    <header>
        <h1><i class="fas fa-globe"></i> Social Media Platform</h1>
        <nav id="nav-menu">
            <button id="home-btn"><i class="fas fa-home"></i> Home</button>
            <button id="profile-btn"><i class="fas fa-user"></i> Profile</button>
            <button id="login-btn"><i class="fas fa-sign-in-alt"></i> Login</button>
            <button id="register-btn"><i class="fas fa-user-plus"></i> Register</button>
            <button id="logout-btn" style="display: none;"><i class="fas fa-sign-out-alt"></i> Logout</button>
            <button id="notifications-btn"><i class="fas fa-bell"></i></button>
        </nav>
    </header>

    <main id="main-content">
        <section id="login-section" style="display: none;">
            <h2><i class="fas fa-sign-in-alt"></i> Login</h2>
            <form id="login-form">
                <input type="text" id="login-username" placeholder="Username" required>
                <input type="password" id="login-password" placeholder="Password" required>
                <button type="submit"><i class="fas fa-lock-open"></i> Login</button>
            </form>
        </section>

        <section id="register-section" style="display: none;">
            <h2><i class="fas fa-user-plus"></i> Register</h2>
            <form id="register-form">
                <input type="text" id="register-username" placeholder="Username" required>
                <input type="password" id="register-password" placeholder="Password" required>
                <input type="email" id="register-email" placeholder="Email" required>
                <button type="submit"><i class="fas fa-user-check"></i> Register</button>
            </form>
        </section>

        <section id="home-section" style="display: none;">
            <h2><i class="fas fa-stream"></i> Home</h2>
            <form id="post-form">
                <textarea id="post-content" placeholder="What's on your mind?" required></textarea>
                <div class="post-actions">
                    <button type="button" id="emoji-btn"><i class="far fa-smile"></i></button>
                    <div class="upload-btn-wrapper">
                        <button type="button"><i class="far fa-image"></i> Upload Image</button>
                        <input type="file" id="image-upload" accept="image/*" onchange="previewImage(event)">
                    </div>
                    <button type="submit"><i class="fas fa-paper-plane"></i> Post</button>
                </div>
                <img id="upload-preview" class="upload-preview">
            </form>
            <div id="posts-container"></div>
            <div class="loading-spinner">
                <i class="fas fa-spinner fa-spin fa-2x"></i>
            </div>
        </section>

        <section id="profile-section" style="display: none;">
            <div class="profile-header">
                <h2><i class="fas fa-user-circle"></i> Profile</h2>
                <div id="user-info"></div>
                <div class="profile-stats">
                    <div class="stat-box">
                        <h3>Posts</h3>
                        <div id="posts-count">0</div>
                    </div>
                    <div class="stat-box">
                        <h3>Following</h3>
                        <div id="following-count">0</div>
                    </div>
                    <div class="stat-box">
                        <h3>Followers</h3>
                        <div id="followers-count">0</div>
                    </div>
                </div>
            </div>

            <div class="following-list">
                <h3>Following</h3>
                <div id="following-list"></div>
            </div>

            <div class="followers-list">
                <h3>Followers</h3>
                <div id="followers-list"></div>
            </div>

            <h3>My Posts</h3>
            <div id="user-posts"></div>
        </section>
    </main>

    <script>
        // DOM Elements
        const mainContent = document.getElementById('main-content');
        const navMenu = document.getElementById('nav-menu');
        const loginSection = document.getElementById('login-section');
        const registerSection = document.getElementById('register-section');
        const homeSection = document.getElementById('home-section');
        const profileSection = document.getElementById('profile-section');
        const postsContainer = document.getElementById('posts-container');
        const userInfo = document.getElementById('user-info');
        const userPosts = document.getElementById('user-posts');

        // Event Listeners
        document.getElementById('home-btn').addEventListener('click', showHome);
        document.getElementById('profile-btn').addEventListener('click', showProfile);
        document.getElementById('login-btn').addEventListener('click', showLogin);
        document.getElementById('register-btn').addEventListener('click', showRegister);
        document.getElementById('logout-btn').addEventListener('click', logout);
        document.getElementById('login-form').addEventListener('submit', login);
        document.getElementById('register-form').addEventListener('submit', register);
        document.getElementById('post-form').addEventListener('submit', createPost);

        // Image preview function
        function previewImage(event) {
            const preview = document.getElementById('upload-preview');
            const file = event.target.files[0];
            const reader = new FileReader();

            reader.onload = function() {
                preview.src = reader.result;
                preview.style.display = 'block';
            }

            if (file) {
                reader.readAsDataURL(file);
            }
        }

        // Global Variables
        let currentUser = null;

        // Helper Functions
        function showSection(section) {
            loginSection.style.display = 'none';
            registerSection.style.display = 'none';
            homeSection.style.display = 'none';
            profileSection.style.display = 'none';
            section.style.display = 'block';
        }

        function updateNavMenu() {
            const loginBtn = document.getElementById('login-btn');
            const registerBtn = document.getElementById('register-btn');
            const logoutBtn = document.getElementById('logout-btn');
            const profileBtn = document.getElementById('profile-btn');

            if (currentUser) {
                loginBtn.style.display = 'none';
                registerBtn.style.display = 'none';
                logoutBtn.style.display = 'inline-block';
                profileBtn.style.display = 'inline-block';
            } else {
                loginBtn.style.display = 'inline-block';
                registerBtn.style.display = 'inline-block';
                logoutBtn.style.display = 'none';
                profileBtn.style.display = 'none';
            }
        }

        // Main Functions
        function showHome() {
            if (!currentUser) {
                showLogin();
                return;
            }
            showSection(homeSection);
            loadPosts();
        }

        function showProfile() {
            if (!currentUser) {
                showLogin();
                return;
            }
            showSection(profileSection);
            loadUserProfile();
        }

        function showLogin() {
            showSection(loginSection);
        }

        function showRegister() {
            showSection(registerSection);
        }

        function login(e) {
            e.preventDefault();
            const username = document.getElementById('login-username').value;
            const password = document.getElementById('login-password').value;
            const users = JSON.parse(localStorage.getItem('users')) || [];
            const user = users.find(u => u.username === username && u.password === password);
            if (user) {
                currentUser = user;
                updateNavMenu();
                showHome();
            } else {
                alert('Invalid username or password');
            }
        }

        function register(e) {
            e.preventDefault();
            const username = document.getElementById('register-username').value;
            const password = document.getElementById('register-password').value;
            const email = document.getElementById('register-email').value;
            const users = JSON.parse(localStorage.getItem('users')) || [];
            if (users.some(u => u.username === username)) {
                alert('Username already exists');
                return;
            }
            const newUser = {
                username,
                password,
                email,
                posts: [],
                following: [],
                followers: [],
                bio: '',
                joinDate: new Date().toISOString()
            };
            users.push(newUser);
            localStorage.setItem('users', JSON.stringify(users));
            currentUser = newUser;
            updateNavMenu();
            showHome();
        }

        function logout() {
            currentUser = null;
            updateNavMenu();
            showLogin();
        }

        function createPost(e) {
            e.preventDefault();
            const content = document.getElementById('post-content').value;
            const preview = document.getElementById('upload-preview');
            const post = {
                id: Date.now(),
                content,
                author: currentUser.username,
                likes: 0,
                dislikes: 0,
                comments: [],
                image: preview.style.display === 'block' ? preview.src : null,
                timestamp: new Date().toISOString()
            };
            currentUser.posts.unshift(post);
            const users = JSON.parse(localStorage.getItem('users'));
            const userIndex = users.findIndex(u => u.username === currentUser.username);
            users[userIndex] = currentUser;
            localStorage.setItem('users', JSON.stringify(users));

            // Reset form
            document.getElementById('post-content').value = '';
            preview.src = '';
            preview.style.display = 'none';
            document.getElementById('image-upload').value = '';

            loadPosts();
        }

        function loadPosts() {
            const users = JSON.parse(localStorage.getItem('users'));
            const allPosts = users.flatMap(u => u.posts);
            allPosts.sort((a, b) => b.id - a.id);
            postsContainer.innerHTML = allPosts.map(post => createPostHTML(post)).join('');
            addPostEventListeners();
        }

        function loadUserProfile() {
            const users = JSON.parse(localStorage.getItem('users'));
            const user = users.find(u => u.username === currentUser.username);
            const followers = users.filter(u => u.following.includes(currentUser.username));

            // Update profile header
            userInfo.innerHTML = `
                <h3>${user.username}</h3>
                <p><i class="fas fa-envelope"></i> ${user.email}</p>
                <p><i class="fas fa-calendar-alt"></i> Joined ${new Date(user.joinDate).toLocaleDateString()}</p>
                <p>${user.bio || 'No bio yet'}</p>
            `;

            // Update stats
            document.getElementById('posts-count').textContent = user.posts.length;
            document.getElementById('following-count').textContent = user.following.length;
            document.getElementById('followers-count').textContent = followers.length;

            // Update following list
            document.getElementById('following-list').innerHTML = user.following.map(username => `
                <div class="user-card">
                    <div class="user-avatar">${username[0].toUpperCase()}</div>
                    <div>
                        <h4>${username}</h4>
                        <button class="unfollow-btn">Unfollow</button>
                    </div>
                </div>
            `).join('');

            // Update followers list
            document.getElementById('followers-list').innerHTML = followers.map(follower => `
                <div class="user-card">
                    <div class="user-avatar">${follower.username[0].toUpperCase()}</div>
                    <div>
                        <h4>${follower.username}</h4>
                        ${!user.following.includes(follower.username) ? 
                            `<button class="follow-btn">Follow Back</button>` : 
                            `<button class="unfollow-btn">Unfollow</button>`}
                    </div>
                </div>
            `).join('');

            // Update user posts
            userPosts.innerHTML = user.posts.map(post => createPostHTML(post)).join('');
            addPostEventListeners();
        }

        // Modified createPostHTML function
        function createPostHTML(post) {
            const isFollowing = currentUser.following.includes(post.author);
            return `
                <div class="post" data-post-id="${post.id}">
                    <p><strong>${post.author}</strong></p>
                    <p>${post.content}</p>
                    ${post.image ? `<img src="${post.image}" alt="Post Image" class="image-preview">` : ''}
                    <div class="post-actions">
                        <button class="like-btn">${post.likes} Likes</button>
                        <button class="dislike-btn">${post.dislikes} Dislikes</button>
                        <button class="comment-btn">Comment</button>
                        ${currentUser.username !== post.author ? 
                            `<button class="${isFollowing ? 'unfollow-btn' : 'follow-btn'}">
                                ${isFollowing ? 'Unfollow' : 'Follow'} ${post.author}
                            </button>` : 
                            `<button class="delete-btn">Delete Post</button>`}
                    </div>
                    <div class="comments">
                        ${post.comments.map(comment => `<div class="comment"><strong>${comment.author}</strong>: ${comment.content}</div>`).join('')}
                    </div>
                    <form class="comment-form">
                        <input type="text" class="comment-input" placeholder="Add a comment" required>
                        <button type="submit">Submit</button>
                    </form>
                </div>
            `;
        }
        
        function addPostEventListeners() {
            document.querySelectorAll('.like-btn').forEach(btn => btn.addEventListener('click', likePost));
            document.querySelectorAll('.dislike-btn').forEach(btn => btn.addEventListener('click', dislikePost));
            document.querySelectorAll('.comment-btn').forEach(btn => btn.addEventListener('click', toggleCommentForm));
            document.querySelectorAll('.follow-btn').forEach(btn => btn.addEventListener('click', followUser));
            document.querySelectorAll('.unfollow-btn').forEach(btn => btn.addEventListener('click', unfollowUser));
            document.querySelectorAll('.comment-form').forEach(form => form.addEventListener('submit', addComment));
            document.querySelectorAll('.delete-btn').forEach(btn => btn.addEventListener('click', deletePost));
        }
        
        function likePost(e) {
            const postId = parseInt(e.target.closest('.post').dataset.postId);
            const users = JSON.parse(localStorage.getItem('users'));
            const post = findPost(users, postId);
            post.likes++;
            localStorage.setItem('users', JSON.stringify(users));
            loadPosts();
        }

        function dislikePost(e) {
            const postId = parseInt(e.target.closest('.post').dataset.postId);
            const users = JSON.parse(localStorage.getItem('users'));
            const post = findPost(users, postId);
            post.dislikes++;
            localStorage.setItem('users', JSON.stringify(users));
            loadPosts();
        }
        
        function toggleCommentForm(e) {
            const form = e.target.closest('.post').querySelector('.comment-form');
            form.style.display = form.style.display === 'none' ? 'block' : 'none';
        }
        
        function addComment(e) {
            e.preventDefault();
            const postId = parseInt(e.target.closest('.post').dataset.postId);
            const content = e.target.querySelector('.comment-input').value;
            const users = JSON.parse(localStorage.getItem('users'));
            const post = findPost(users, postId);
            post.comments.push({ author: currentUser.username, content });
            localStorage.setItem('users', JSON.stringify(users));
            loadPosts();
        }
        
        function followUser(e) {
            const authorToFollow = e.target.textContent.replace('Follow ', '').trim();
            if (!currentUser.following.includes(authorToFollow)) {
                currentUser.following.push(authorToFollow);
                const users = JSON.parse(localStorage.getItem('users'));
                const userIndex = users.findIndex(u => u.username === currentUser.username);
                users[userIndex] = currentUser;
                localStorage.setItem('users', JSON.stringify(users));
                loadPosts();
                if (profileSection.style.display === 'block') {
                    loadUserProfile();
                }
            }
        }

        function unfollowUser(e) {
            const authorToUnfollow = e.target.textContent.replace('Unfollow ', '').trim();
            const index = currentUser.following.indexOf(authorToUnfollow);
            if (index > -1) {
                currentUser.following.splice(index, 1);
                const users = JSON.parse(localStorage.getItem('users'));
                const userIndex = users.findIndex(u => u.username === currentUser.username);
                users[userIndex] = currentUser;
                localStorage.setItem('users', JSON.stringify(users));
                loadPosts();
                if (profileSection.style.display === 'block') {
                    loadUserProfile();
                }
            }
        }
        
        function findPost(users, postId) {
            for (const user of users) {
                const post = user.posts.find(p => p.id === postId);
                if (post) return post;
            }
        }

        function deletePost(e) {
            const postId = parseInt(e.target.closest('.post').dataset.postId);
            const users = JSON.parse(localStorage.getItem('users'));
            const userIndex = users.findIndex(u => u.username === currentUser.username);
            const postIndex = users[userIndex].posts.findIndex(p => p.id === postId);
            
            if (postIndex > -1) {
                users[userIndex].posts.splice(postIndex, 1);
                localStorage.setItem('users', JSON.stringify(users));
                currentUser = users[userIndex];
                loadPosts();
                if (profileSection.style.display === 'block') {
                    loadUserProfile();
                }
            }
        }
        
        // Initialize the application
        updateNavMenu();
        showLogin();
    </script>
</body>

</html>
