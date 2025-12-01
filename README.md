# TUGAS-4-PWEB-A-BRILIAN
Web Course (Implementation from HTML &amp; CSS)

## Task Description
Tugas kali ini adalah membuat Web Course dengan implementasi HTML & CSS dalam proses pembuatannya.
Ketentuan isi dari Web Course tersebut adalah : 
1. Materi per bab : HTML Dasar, CSS, JavaScript, PHP.
2. Dashboard, Forum Diskusi.

## Kode

index.html : 

```
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web Programming Course - Belajar sampai jago</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <nav class="navbar">
        <div class="logo">CodeWithKubil</div>
        <ul class="nav-links">
            <li><a href="#" class="active">Home</a></li>
            <li><a href="#">Course</a></li>
            <li><a href="#">Dashboard</a></li> <li><a href="#" class="btn-login">Login/Register</a></li>
        </ul>
    </nav>

    <header class="hero">
        <div class="hero-content">
            <h1>Kuasai Web Programming dari Dasar hingga Mahir</h1>
            <p>Pelajari HTML, CSS, PHP, dan JavaScript dengan kurikulum terstruktur. Sertifikat resmi menantimu.</p>
            <a href="#courses" class="btn-cta">Mulai Belajar Sekarang</a>
        </div>
    </header>

    <section id="courses" class="course-section">
        <h2>Materi Pembelajaran</h2>
        <div class="course-grid">
            <div class="card">
                <div class="card-icon">HTML</div>
                <h3>HTML Dasar</h3>
                <p>Struktur dokumen, heading, form, dan tabel.</p>
            </div>
            <div class="card">
                <div class="card-icon">CSS</div>
                <h3>CSS Styling</h3>
                <p>Layout, Flexbox, Grid, dan Box Model.</p>
            </div>
            <div class="card">
                <div class="card-icon">JS</div>
                <h3>JavaScript</h3>
                <p>Interaksi DOM dan logika pemrograman web.</p>
            </div>
            <div class="card">
                <div class="card-icon">PHP</div>
                <h3>PHP Backend</h3>
                <p>Koneksi database dan pengelolaan data server.</p>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 CodeWithKubil Course. All Rights Reserved.</p>
    </footer>

</body>
</html>
```

style.css : 

```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

:root {
    --bg-dark: #0a192f; 
    --bg-card: #112240; 
    --accent-blue: #64ffda; 
    --text-white: #e6f1ff; 
    --text-gray: #8892b0;
}

body {
    background-color: var(--bg-dark); 
    color: var(--text-white);
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 5%;
    background: linear-gradient(to bottom, rgba(10,25,47,0.9) 0%, rgba(10,25,47,0) 100%);
    position: fixed; 
    width: 100%;
    top: 0;
    z-index: 1000;
    transition: background 0.3s;
}


.logo {
    font-size: 1.8rem;
    font-weight: 800;
    color: var(--accent-blue);
    letter-spacing: 1px;
}

.nav-links {
    list-style: none;
    display: flex;
    gap: 30px;
}

.nav-links a {
    text-decoration: none;
    color: var(--text-white);
    font-weight: 500;
    font-size: 0.9rem;
    opacity: 0.8;
    transition: 0.3s;
}

.nav-links a:hover, .nav-links a.active {
    opacity: 1;
    color: var(--accent-blue);
}

.nav-links .btn-login {
    padding: 8px 25px;
    background-color: transparent;
    border: 1px solid var(--accent-blue); 
    color: var(--accent-blue);
    border-radius: 4px;
    font-weight: bold;
}

.nav-links .btn-login:hover {
    background-color: rgba(100, 255, 218, 0.1); 
}

.hero {
    height: 100vh;
    background: linear-gradient(rgba(10,25,47,0.85), rgba(10,25,47,0.95)), url('https://images.unsplash.com/photo-1555066931-4365d14bab8c?q=80&w=2070&auto=format&fit=crop');
    background-size: cover;
    background-position: center;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 0 20px;
    margin-top: -80px;
}

.hero-content {
    max-width: 800px;
}

.hero h1 {
    font-size: 3.5rem;
    font-weight: 800;
    margin-bottom: 20px;
    line-height: 1.2;
}

.hero p {
    font-size: 1.3rem;
    margin-bottom: 40px;
    color: var(--text-gray);
}

.btn-cta {
    display: inline-block;
    padding: 15px 40px;
    background-color: var(--accent-blue); 
    color: var(--bg-dark);
    text-decoration: none;
    font-weight: 800;
    font-size: 1.1rem;
    border-radius: 4px; 
    transition: transform 0.3s, box-shadow 0.3s;
}

.btn-cta:hover {
    transform: scale(1.02);
    box-shadow: 0 0 20px rgba(100, 255, 218, 0.4);
}

.course-section {
    padding: 80px 5%;
    background-color: var(--bg-dark);
}

.course-section h2 {
    color: var(--text-white);
    margin-bottom: 40px;
    font-size: 1.8rem;
    text-align: left; 
    padding-left: 10px;
    border-left: 4px solid var(--accent-blue);
}

.course-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); 
    gap: 25px;
}

.card {
    background: var(--bg-card); 
    padding: 30px;
    border-radius: 8px;
    transition: 0.3s ease-in-out;
    border: 1px solid transparent;
    border-top: none; 
    text-align: left;
}

.card:hover {
    transform: translateY(-5px) scale(1.02); 
    border-color: var(--accent-blue); 
    background-color: #172a45; 
    box-shadow: 0 10px 30px -15px rgba(2, 12, 27, 0.7);
}

.card-icon {
    font-size: 2rem;
    font-weight: 800;
    color: var(--accent-blue);
    margin-bottom: 20px;
    display: inline-block;
}

.card h3 {
    color: var(--text-white);
    margin-bottom: 10px;
    font-size: 1.3rem;
}

.card p {
    color: var(--text-gray);
    font-size: 0.95rem;
    line-height: 1.5;
}

footer {
    background-color: #050d1a; 
    color: var(--text-gray);
    text-align: center;
    padding: 30px;
    margin-top: 50px;
    font-size: 0.9rem;
}

@media (max-width: 768px) {
    .nav-links {
        display: none; 
    }
    .hero h1 {
        font-size: 2.2rem;
    }
    .hero p {
        font-size: 1rem;
    }
    .hero {
        height: 90vh;
    }
}
```


## Hasil 
<img width="2879" height="1439" alt="image" src="https://github.com/user-attachments/assets/2fac93a4-69ee-44dd-b6cb-3ebd56c505d0" />

<img width="2879" height="1153" alt="image" src="https://github.com/user-attachments/assets/84e11099-311a-4f8c-a94e-7c484e14e7fc" />



