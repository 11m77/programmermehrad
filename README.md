<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>برنامه نویسی مهراد</title>

<style>
:root{--bg:#fff;--text:#000000;--card:#f4f4f4;--primary:#4e89ff}
[data-theme=dark]{--bg:#000000;--text:#eee;--card:#1e1e1e}

*{margin:0;padding:0;box-sizing:border-box;font-family:tahoma,Arial}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--text);transition:.4s}

/* هدر */
header{position:fixed;top:0;inset-inline:0;height:64px;background:var(--card);
display:flex;align-items:center;justify-content:space-between;padding:0 1.2rem;
box-shadow:0 2px 10px #0003;z-index:30}
.logo{font-weight:900;font-size:1.5rem;color:var(--primary)}
nav{display:flex;gap:1.5rem}
nav a{color:var(--text);text-decoration:none;font-weight:600}
nav a:hover{color:var(--primary)}
#themeBtn{background:var(--primary);border:none;color:#fff;border-radius:22px;
padding:.5rem 1.2rem;font-size:.85rem;cursor:pointer}
#themeBtn:hover{background:#234ebd}

/* منوی موبایل */
.hb{display:none;flex-direction:column;gap:5px;cursor:pointer}
.hb span{width:26px;height:3px;background:var(--text);transition:.3s}
.hb.open span:nth-child(1){transform:translateY(7px) rotate(45deg)}
.hb.open span:nth-child(2){opacity:0}
.hb.open span:nth-child(3){transform:translateY(-7px) rotate(-45deg)}
.menu{display:none;flex-direction:column;gap:1.2rem;position:fixed;top:64px;right:0;width:70%;height:calc(100% - 64px);
background:var(--card);padding:1.8rem;box-shadow:-4px 0 12px #0004;z-index:25}
.menu.show{display:flex}
.menu a{color:var(--text);text-decoration:none;font-weight:600}
.menu a:hover{color:var(--primary)}

/* HERO */
.hero{display:flex;align-items:center;justify-content:center;flex-wrap:wrap;gap:2.5rem;
min-height:100vh;padding:5rem 2rem;background:linear-gradient(135deg,#4e89ff,#234ebd);color:#fff}
.hero-content{flex:1 1 320px;display:flex;flex-direction:column;gap:1.3rem}
.hero-content h1{font-size:3.2rem;font-weight:900;line-height:1.2}
.hero-content p{font-size:1.25rem;line-height:1.7}
.hero-content button{align-self:flex-start;background:#fff;color:#4e89ff;border:none;padding:1rem 2.6rem;
border-radius:32px;font-weight:700;cursor:pointer;transition:.3s;box-shadow:0 8px 24px #0003}
.hero-content button:hover{background:#234ebd;color:#fff}
.hero-img{flex:1 1 320px;display:flex;justify-content:center}
.hero-img img{width:100%;max-width:920px;border-radius:24px;box-shadow:0 14px 40px #0005}

/* سکشن عمومی */
section{padding:4.5rem 1.5rem}
section:nth-of-type(even){background:var(--card)}
.section-title{font-size:2.2rem;font-weight:900;text-align:center;margin-bottom:1.8rem}

/* کارت‌ها */
.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:2.2rem;max-width:1200px;margin:auto}
.card{background:var(--card);border-radius:18px;padding:1.5rem;box-shadow:0 10px 22px #0002;position:relative;
display:flex;flex-direction:column;align-items:center;gap:1rem;transform-style:preserve-3d;transition:.6s}
.card:hover{transform:rotateY(15deg) translateZ(30px) scale(1.06)}
.card img{width:100%;border-radius:14px;box-shadow:0 8px 22px #0003}

/* فرم ورود */
.login-box{background:var(--card);width:100%;max-width:450px;margin:auto;padding:2.5rem 3rem;border-radius:22px;
box-shadow:0 14px 32px #0004;display:flex;flex-direction:column;gap:1.4rem}
.login-box h2{margin-bottom:.4rem}
.login-box input{padding:1rem;border:2px solid var(--primary);border-radius:12px;font-size:1rem;background:var(--bg);color:var(--text)}
.login-box input:focus{outline:none;border-color:#234ebd}
.login-box button{background:var(--primary);border:none;color:#fff;padding:.9rem;border-radius:26px;font-weight:0;cursor:pointer}
.login-box button:hover{background:#234ebd}
.login-box a{align-self:flex-end;font-size:.85rem;color:var(--primary);text-decoration:none}
.login-box a:hover{text-decoration:underline}

/* فوتر */
footer{text-align:center;padding:2rem;color:var(--text);background:var(--card);font-size:.9rem}

/* ریسپانسیو */
@media(max-width:768px){
  nav{display:none}.hb{display:flex}
  .hero{flex-direction:column-reverse;text-align:center}
  .hero-content button{align-self:center}
}
</style>
</head>
<body data-theme="light">

<header>
  <div class="logo">برنامه نویسی مهراد </div>
  <nav>
    <a href="#hero">خانه</a><a href="#works">آموزش ها </a><a href="#login">تماس</a><a href="#login"></a>
  </nav>
  <button id="themeBtn">حالت شب</button>
  <div class="hb" id="hb"><span></span><span></span><span></span></div>
  <div class="menu" id="menu">
    <a href="#hero">خانه</a><a href="#works">آموذش ها </a><a href="#login">تماس</a><a href="#login"></a>
  </div>
</header>

<main style="padding-top:64px">

  <!-- HERO -->
  <section id="hero" class="hero">
    
    <div class="hero-content">
      
      <h1>برنامه نویسی مهراد</h1>
      <p>طراحی، توسعه برنامه نویسی برای رشد کسب‌وکار شما</p>
      <button onclick="document.getElementById('login').scrollIntoView({behavior:'smooth'})">تماس با ما</button>
    </div>
    <div class="hero-img">
      <b></b><b></b><b></b><b></b>
      <img src="md.jpg" alt="تصویر مرد" style="width: 70%;border-radius: 20px;box-shadow:30px 20px 70px 10px #000000;border-color: rgba(red, green, blue, alpha);border-width: 190px;">
    </div>
    
  </section>



  
  <!-- نمونه کارها -->
  <section id="works">
    
    <h2 class="section-title">آموزش ها</h2>
    <table>
      <tr>
        <td><img src="mmd.jpg" alt="" style="width: 70%;height: 70%;border-radius: 50%;"></td>
        <td><h1>تیم برنامه‌نویسی مهراد با تخصص در طراحی وب‌سایت، آماده است تا به رشد و دیده‌شدن کسب‌وکار شما در فضای آنلاین کمک کند.
ما علاوه بر اجرای پروژه با کیفیت بالا، آموزش‌های لازم را نیز در اختیارتان قرار می‌دهیم تا مدیریت وب‌سایت برایتان ساده و مؤثر باشد.</h1></td>

      </tr>
    </table>
    <a href="https://t.me/programmingmehrad" style="text-decoration: none;">
    <center><div ><h3 style="color: #04ff00;">  برای رزرو پروژه هاوآموزش ها با ما در ارتباط باشید</h3><img src="tl.jpg" alt="" style="width: 40px;height: 40px;border-radius: 50%;"></div></center>
   </a>
  
    <div class="banner">
      <div class="slider" style="--quantity: 10">
          
        <div class="item" style="--position: 1"><img src="bak1.jpg" alt=""></div>
            <div class="item" style="--position: 2"><img src="bak2.jpg" alt="" style="width: 100%;"></div>
            <div class="item" style="--position: 3"><img src="bak3.jpg" alt="" style="width: 100%;"></div>
            <div class="item" style="--position: 4"><img src="bak4.jpg" alt="" style="width: 100%;"></div>
            <div class="item" style="--position: 5"><img src="bak5.jpg" alt="" style="width: 100%;"></div>
            <div class="item" style="--position: 6"><img src="bak7.jpg" alt="" style="width: 100%;"></div>
            <div class="item" style="--position: 7"><img src="bak8.jpg" alt="" style="width: 100%;"></div>
            <div class="item" style="--position: 8"><img src="bak9.jpg" alt="" style="width: 100%;"></div>
            <div class="item" style="--position: 9"><img src="bak10.jpg" alt="" style="width: 100%;"></div>
            <div class="item" style="--position: 10"><img src="bak11.jpg" alt="" style="width: 100%;"></div>
      </div>
      <div class="content">
          <h1 data-content="">
              
          </h1>
          <div class="author">
              <h2></h2>
              <p><b></b></p>
              <p>
                  
              </p>
          </div>
          <div class="model"></div>
      </div>
  </div>

  




  <style>
    @import url('https://fonts.cdnfonts.com/css/ica-rubrik-black');
@import url('https://fonts.cdnfonts.com/css/poppins');

.banner{
    width: 100%;
    height: 100vh;
    text-align: center;
    overflow: hidden;
    position: relative;
}
.banner .slider{
    position: absolute;
    width: 200px;
    height: 250px;
    top: 10%;
    left: calc(50% - 100px);
    transform-style: preserve-3d;
    transform: perspective(1000px);
    animation: autoRun 20s linear infinite;
    z-index: 2;
}
@keyframes autoRun{
    from{
        transform: perspective(1000px) rotateX(-16deg) rotateY(0deg);
    }to{
        transform: perspective(1000px) rotateX(-16deg) rotateY(360deg);
    }
}

.banner .slider .item{
    position: absolute;
    inset: 0 0 0 0;
    transform: 
        rotateY(calc( (var(--position) - 1) * (360 / var(--quantity)) * 1deg))
        translateZ(550px);
}
.banner .slider .item img{
    width: 60%;
    height: 100%;
    object-fit: cover;
}
.banner .content{
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: min(1400px, 100vw);
    height: max-content;
    padding-bottom: 100px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    z-index: 1;
}
.banner .content h1{
    font-family: 'ICA Rubrik';
    font-size: 16em;
    line-height: 1em;
    color: #25283B;
    position: relative;
}
.banner .content h1::after{
    position: absolute;
    inset: 0 0 0 0;
    content: attr(data-content);
    z-index: 2;
    -webkit-text-stroke: 2px #d2d2d2;
    color: transparent;
}
.banner .content .author{
    font-family: Poppins;
    text-align: right;
    max-width: 200px;
}
.banner .content h2{
    font-size: 3em;
}
.banner .content .model{
    background-image: url(images/model.png);
    width: 50%;
    height: 75vh;
    position: absolute;
    bottom: 0;
    left: 0;
    background-size: auto 130%;
    background-repeat: no-repeat;
    background-position: top center;
    z-index: 1;
}
@media screen and (max-width: 1023px) {
    .banner .slider{
        width: 160px;
        height: 200px;
        left: calc(50% - 80px);
    }
    .banner .slider .item{
        transform: 
            rotateY(calc( (var(--position) - 1) * (360 / var(--quantity)) * 1deg))
            translateZ(300px);
    }
    .banner .content h1{
        text-align: center;
        width: 100%;
        text-shadow: 0 10px 20px #000;
        font-size: 7em;
    }
    .banner .content .author{
        color: #fff;
        padding: 20px;
        text-shadow: 0 10px 20px #000;
        z-index: 2;
        max-width: unset;
        width: 100%;
        text-align: center;
        padding: 0 30px;
    }
}
@media screen and (max-width: 767px) {
    .banner .slider{
        width: 100px;
        height: 150px;
        left: calc(50% - 50px);
    }
    .banner .slider .item{
        transform: 
            rotateY(calc( (var(--position) - 1) * (360 / var(--quantity)) * 1deg))
            translateZ(180px);
    }
    .banner .content h1{
        font-size: 5em;
    }
}
</style>

    <div class="cards">
      
      <div class="card">
        <a href="https://t.me/programmingmehrad" style="color: red;text-decoration: none;"><img src="a1.jpg" alt="">
        قیمت دوره  4000000تومان</a>
      </div>
      <div class="card">
        <a href="https://t.me/programmingmehrad" style="color: red;text-decoration: none;"><img src="a2.jpg" alt="">
        قیمت دوره  800تومان</a>
      </div>
      <div class="card">
        <a href="https://t.me/programmingmehrad" style="color: red;text-decoration: none;"><img src="a3.jpg" alt="">
       قیمت دوره  400تومان</a>
      </div>
      <div class="card">
        <a href="https://t.me/programmingmehrad" style="color: red;text-decoration: none;"><img src="a4.jpg" alt="">
        قیمت آموزش نصب 150تومان</a>
      </div>
      <div class="card">
        <a href="https://t.me/programmingmehrad" style="color: red;text-decoration: none;"><img src="a5.jpg" alt="">
        قیمت دوره 950تومان</a>
      </div>
      <div class="card">
        <a href="https://t.me/programmingmehrad" style="color: red;text-decoration: none;"><img src="a6.jpg" alt="">
        قیمت آموزش نصب 200تومان</a>
      </div>
      <div class="card">
        <a href="https://t.me/programmingmehrad" style="color: red;text-decoration: none;"><img src="a7.jpg" alt="">
        قیمت دوره 500تومان</a>
      </div>
      <div class="card">
        <a href="https://t.me/programmingmehrad" style="color: red;text-decoration: none;"><img src="a8.jpg" alt="">
        قیمت دوره 500تومان</a>
      </div>
      <div class="card">
        <a href="https://t.me/programmingmehrad" style="color: red;text-decoration: none;"><img src="a9.jpg" alt="">
        قیمت دوره 650تومان</a>
      </div>
      <div class="card">
        <a href="https://t.me/programmingmehrad" style="color: red;text-decoration: none;"><img src="a10.jpg" alt="">
        قیمت دوره650تومان</a>
      </div>
    </div>
  </section>






















  


  <!-- فرم ورود -->
  <section id="login">
    <h2 class="section-title">فرم تماس </h2>
    <div class="login-box">
      <h2>حساب کاربری</h2>
      <input type="email" placeholder="ایمیل">
      <input type="password" placeholder="رمز عبور">
      
      <a href="tel:9809054062592"><button>تماس با ما</button></a>
    </div>
  </section>
</main>







<center>


<h1 style="color: #004b95;border-width:10px;border-color: #fff;">نظر ها</h1>

</center>






<style>
    

  .container {
    width: 80%;
    max-width: 550px;
    padding: 20px;
    box-sizing:30%;
  }

  h2, h3 {
    text-align: center;
    color: #1e3a8a;
    margin-bottom: 20px;
  }

  .comment-box {
    background-color: white;
    padding: 25px;
    border-radius: 18px;
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
    animation: fadeIn 0.7s ease;
  }

  input, textarea {
    width: 90%;
    padding: 14px;
    margin-bottom: 9px;
    border: 1px solid #ccc;
    border-radius: 12px;
    font-size: 16px;
    outline: none;
    transition: border 0.3s ease;
    box-sizing: border-box;
  }

  input:focus, textarea:focus {
    border-color: #3b82f6;
  }

  button {
    position: relative;
    overflow: hidden;
    background: linear-gradient(to right, #3b82f6, #6366f1);
    color: white;
    padding: 12px 24px;
    border: none;
    border-radius: 12px;
    font-size: 16px;
    cursor: pointer;
    transition: transform 0.2s ease, box-shadow 0.3s;
   
  }

  button:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 12px rgba(0,0,0,0.2);
  }

  button::after {
    content: "";
    position: absolute;
    background: rgba(255, 255, 255, 0.4);
    width: 100px;
    height: 100px;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0);
    border-radius: 50%;
    opacity: 0;
    transition: transform 0.5s, opacity 1s;
  }

  button:active::after {
    transform: translate(-50%, -50%) scale(2.5);
    opacity: 0;
  }

  .error {
    color: red;
    font-size: 14px;
    margin-bottom: 10px;
  }

  #comments {
    margin-top: 30px;
  }

  .comment {
    display: flex;
    align-items: flex-start;
    gap: 15px;
    background-color: #eef2ff;
    padding: 15px;
    border-radius: 14px;
    margin-bottom: 15px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    animation: fadeInUp 0.5s ease forwards;
    opacity: 0;
    transform: translateY(20px);
    position: relative;
  }

  .profile-pic {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-image: url('https://cdn-icons-png.flaticon.com/512/149/149071.png');
    background-size: cover;
    background-position: center;
    flex-shrink: 0;
  }

  .comment-text {
    flex-grow: 1;
  }

  .comment-author {
    font-weight: bold;
    color: #1d4ed8;
    margin-bottom: 5px;
  }

  .comment-actions {
    position: absolute;
    top: 10px;
    left: 10px;
    display: flex;
    gap: 8px;
  }

  .comment-actions button {
    background: transparent;
    border: none;
    cursor: pointer;
    color: #3b82f6;
    font-size: 14px;
    padding: 4px 6px;
    border-radius: 6px;
    transition: background-color 0.3s;
  }

  .comment-actions button:hover {
    background-color: #bfdbfe;
  }

  @keyframes fadeInUp {
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: scale(0.95);
    }
    to {
      opacity: 1;
      transform: scale(1);
    }
  }

  @media (max-width: 600px) {
    .container {
      padding: 10px;
    }

    .comment-box {
      padding: 20px;
    }

    input, textarea {
      font-size: 15px;
    }

    button {
      font-size: 15px;
    }
  }
</style>
<center>
 
  <br>
  <br>

<div class="container">
  <h2>دوست عزیز نظر خود را درباره سایت و آموزش ها  با مادرمیان بگذارید.</h2>
  <div class="comment-box">
    <input type="text" id="username" placeholder="نام شما">
    <textarea id="commentInput" rows="4" placeholder="نظر خود را بنویسید..."></textarea>
    <div id="error" class="error"></div>
    <button onclick="submitComment()">ارسال نظر</button>
  </div>
</center>
  <div id="comments" style="color: #1d4ed8;">
    <h3>نظرات کاربران:</h3>
  </div>
</div>

<script>
  let comments = [];

  // بارگذاری نظرات از localStorage
  function loadComments() {
    const saved = localStorage.getItem('comments');
    if (saved) {
      comments = JSON.parse(saved);
    } else {
      comments = [];
    }
    renderComments();
  }

  // ذخیره نظرات در localStorage
  function saveComments() {
    localStorage.setItem('comments', JSON.stringify(comments));
  }

  // نمایش نظرات
  function renderComments() {
    const container = document.getElementById('comments');
    container.innerHTML = '<h3>نظرات کاربران:</h3>';

    comments.forEach((c, index) => {
      const commentDiv = document.createElement('div');
      commentDiv.className = 'comment';

      const profile = document.createElement('div');
      profile.className = 'profile-pic';

      const textDiv = document.createElement('div');
      textDiv.className = 'comment-text';

      const author = document.createElement('div');
      author.className = 'comment-author';
      author.textContent = c.name;

      const message = document.createElement('div');
      message.textContent = c.text;

      // دکمه‌های ویرایش و حذف
      const actions = document.createElement('div');
      actions.className = 'comment-actions';

      const editBtn = document.createElement('button');
      editBtn.textContent = '';
      editBtn.onclick = () => editComment(index);

      const deleteBtn = document.createElement('button');
      deleteBtn.textContent = '';
      deleteBtn.onclick = () => deleteComment(index);

      actions.appendChild(editBtn);
      actions.appendChild(deleteBtn);

      textDiv.appendChild(author);
      textDiv.appendChild(message);
      commentDiv.appendChild(profile);
      commentDiv.appendChild(textDiv);
      commentDiv.appendChild(actions);

      container.appendChild(commentDiv);

      // انیمیشن نمایش
      setTimeout(() => {
        commentDiv.style.opacity = '1';
        commentDiv.style.transform = 'translateY(0)';
      }, 50);
    });
  }

  // ارسال نظر جدید یا ذخیره ویرایش
  function submitComment() {
    const nameInput = document.getElementById('username');
    const commentInput = document.getElementById('commentInput');
    const error = document.getElementById('error');

    const name = nameInput.value.trim();
    const comment = commentInput.value.trim();

    if (!name || !comment) {
      error.textContent = "لطفاً نام و نظر خود را وارد کنید.";
      return;
    }

    error.textContent = "";

    if (submitComment.editIndex !== undefined) {
      // ویرایش نظر موجود
      comments[submitComment.editIndex] = {name, text: comment};
      submitComment.editIndex = undefined;
    } else {
      // افزودن نظر جدید
      comments.push({name, text: comment});
    }

    saveComments();
    renderComments();

    nameInput.value = '';
    commentInput.value = '';
    submitComment.editIndex = undefined;
  }

  
  window.onload = loadComments;
</script>
























<script >
const body=document.body,
      themeBtn=document.getElementById('themeBtn'),
      hb=document.getElementById('hb'),
      menu=document.getElementById('menu');

themeBtn.onclick=()=>{
  const dark = body.dataset.theme==='dark';
  body.dataset.theme= dark ? 'light' : 'dark';
  themeBtn.textContent= dark ? 'حالت شب' : 'حالت روز';
};

hb.onclick=()=>{
  hb.classList.toggle('open');
  menu.classList.toggle('show');
};

</script>




</body>
</html>
<br>
<br>








































