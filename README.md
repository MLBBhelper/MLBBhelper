- 👋 Hi, I’m @XZ
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
DEVELOPER/EZ is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html ng-app="blog">

<head>
  <meta charset="UTF-8">
  <!-- Open Graph Meta Tags -->
  <meta property="og:title" content="Htet Ko Ko - Blog">
  <meta property="og:description" content="Personal - Profile,Blog and About Me.....">
  <meta property="og:image" content="/images/cover.jpg">
  <meta property="og:url" content="https://htetkokoblog.vercel.app">
  <meta property="og:type" content="website">
  <meta content="Htet Ko Ko,Myanmar,Blog,Coding,Poem" name="keywords">
  <!---favicon add--->
  <link rel="shortcut icon" href="/images/favicon.ico" type="image/x-icon">
  <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
  <link rel="apple-touch-icon" href="/images/favicon.ico">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Htet Ko Ko - Blog</title>
  <!---Icon Font--->
  <script type="module" src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js"></script>
  <script nomodule src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.js"></script>
  <!---Font Add--->
  <link href="https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,200..1000;1,200..1000&family=Roboto+Condensed:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">
  <!---Angular Js & Tailwind--->
  <script src="/main/angular1.8.3.min.js"></script>
  <script src="/main/tailwind.config.js"></script>
  <script src="/main/request.js"></script>
  
</head>

<body class="bg-gray-100 px-3" ng-controller="myblog">
  <!---Profile--->
  <div class="w-full bg-white rounded-lg shadow-md gird justify-center items-center p-4 mb-10 mt-3">
    <div class="flex md:flex-col items-center px-6 py-4 mb-4">
    <img class="w-32 h-32 md:w-52 md:h-52 rounded-full object-cover flex-2 md:mb-3" src="images/profile.png" alt="Avatar">
    <div class="ml-4 flex-2 md:text-center md:mb-1">
      <h1 class="text-2xl font-bold md:text-4xl">Htet Ko Ko</h1></h1>
      <p class="text-gray-600 text-sm md:text-lg md:mb-5" style="font-family: Nunito;">Junier Web Developer &lt;/&gt;</p>
    </div>
  </div>
  <div class="flex justify-center items-center justify-evenly md:mb-5">
      <ion-icon name="logo-facebook" size="large" onclick="location.href='https://www.facebook.com/fb.htetkoko'"></ion-icon>
      <ion-icon name="logo-github" size="large" onclick="location.href='https://github.com/htetkokoblog'"></ion-icon>
      <ion-icon name="navigate-circle" size="large" onclick="location.href='https://t.me/htetkokotelegram'"></ion-icon>
    </div>
  </div>
  <div class="w-full bg-white rounded-lg shadow-md gird items-center p-4 mb-10" style="font-family: Nunito;">
    <div class="text-lg font-bold justify-start mb-1">About Me</div>
    <div class="text-md ms-3 text-gray-700 mb-3 px-3">
      My name is Htet Ko Ko. I was born on November, 2006, in Sagaing Region, Myanmar. I am currently residing in Mandalay City. I have completed high school education and am currently working as a Customer Service representative and Junior Web Developer.
    </div>
  </div>
  <!---Personal Blog--->
  <div class="text-gray-700 text-xl text-start font-bold mb-4">
    Personal - Blog
  </div>
 <div ng-repeat="item in data">
<div class="w-full bg-white rounded-lg shadow-lg overflow-hidden mb-8" ng-attr-id="{{ item.id }}">
  <div class="flex items-center px-6 py-4">
    <img class="w-12 h-12 rounded-full object-cover" src="images/profile.png" alt="Avatar">
    <div class="ml-3">
      <h1 class="text-lg font-bold">Htet Ko Ko</h1>
      <div class="text-gray-600 text-sm flex items-center">
        <ion-icon name="calendar-outline" class="me-1"></ion-icon>
        {{ item.date }}
        </div>
    </div>
  </div>
  <div class="px-6 mb-4">
    <p class="text-gray-700 text-base"  ng-bind-html="renderHtml(item.description)">
      {{ item.description }}
    </p>
  </div>
  <div class="px-6 mb-2 max-w-md" ng-if="item.photo">
    <img ng-src="{{ item.photo}}" alt="cover" class="w-full h-1/2 me-5 rounded-lg">
  </div>
  <div class="px-6 py-4">
    <div class="text-gray-500 text-sm flex items-center justify-end">
      <ion-icon name="time-outline"></ion-icon>
      {{ item.time }}
    </div>
  </div>
</div>
</div>
<div class="w-full flex justify-center items-center p-5 mb-10">
  <p class="text-gray-600 text-md">Copyright&copy; 2024</p>
</div>
<div class="w-full bg-gray-900 flex justify-start items-center p-2 fixed bottom-0 left-0 right-0">
  <p class="text-gray-400 text-sm ps-4" style="font-family: Nunito;">Personal Profile, Personal - Blog and About Me.......</p>
</div>
</body>
  </html>
  
