# -souqna
سوقنا للإعلانات ودليل الشركات والأنشطة التجارية في السودان

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 18px;
    }

    .card {
      background: white;
      padding: 22px;
      border-radius: 10px;
      box-shadow: 0 2px 9px rgba(0,0,0,0.08);
      text-align: center;
    }

    .card h3 {
      color: #1769aa;
      margin-top: 0;
    }

    .card p {
      line-height: 1.8;
    }

    .button {
      display: inline-block;
      padding: 10px 18px;
      background: #1769aa;
      color: white;
      text-decoration: none;
      border-radius: 6px;
      margin-top: 8px;
    }

    .add-business {
      background: #eaf4fb;
      padding: 30px 20px;
      text-align: center;
      border-radius: 12px;
    }

    footer {
      margin-top: 40px;
      background: #1769aa;
      color: white;
      text-align: center;
      padding: 25px 15px;
    }

    @media (max-width: 600px) {
      header h1 {
        font-size: 26px;
      }

      .search {
        flex-direction: column;
      }

      .search button {
        width: 100%;
      }
    }
  </style>
</head>

<body>

  <header>
    <h1>سوقنا</h1>
    <p>للإعلانات ودليل الشركات والأنشطة التجارية في السودان</p>
  </header>

  <nav>
    <a href="#home">الرئيسية</a>
    <a href="#companies">الشركات</a>
    <a href="#ads">الإعلانات</a>
    <a href="#add">أضف نشاطك</a>
  </nav>

  <section class="hero" id="home">
    <h2>مرحباً بكم في سوقنا</h2>
    <p>
      منصة سودانية للإعلانات ودليل الشركات والأنشطة التجارية،
      تساعدك في الوصول إلى الخدمات والمنتجات والشركات في السودان.
    </p>

    <div class="search">
      <input type="text" id="searchInput" placeholder="ابحث عن شركة أو نشاط تجاري">
      <button onclick="searchCompanies()">بحث</button>
    </div>
  </section>

  <section class="section" id="companies">
    <h2>الشركات والأنشطة التجارية</h2>

    <div class="cards" id="companyCards">

      <div class="card company">
        <h3>شركة النحلة</h3>
        <p>خدمات ومنتجات متنوعة</p>
        <p>📍 الشمالية - مروي</p>
        <a class="button" href="#">عرض التفاصيل</a>
      </div>

      <div class="card company">
        <h3>شركة زين</h3>
        <p>اتصالات وإنترنت</p>
        <p>📍 الشمالية - مروي</p>
        <a class="button" href="#">عرض التفاصيل</a>
      </div>

      <div class="card company">
        <h3>سوداني</h3>
        <p>اتصالات وإنترنت في السودان</p>
        <p>📍 الشمالية - مروي</p>
        <a class="button" href="#">عرض التفاصيل</a>
      </div>

    </div>
  </section>

  <section class="section" id="ads">
    <h2>الإعلانات</h2>

    <div class="cards">
      <div class="card">
        <h3>أعلن معنا في سوقنا</h3>
        <p>
          يمكنك عرض شركتك أو نشاطك التجاري والوصول إلى العملاء
          من خلال منصة سوقنا.
        </p>
        <a class="button" href="#add">أضف إعلانك</a>
      </div>

      <div class="card">
        <h3>دليل الأنشطة التجارية</h3>
        <p>
          اكتشف الشركات والخدمات والأنشطة التجارية الموجودة
          في مختلف مناطق السودان.
        </p>
      </div>
    </div>
  </section>

  <section class="section" id="add">
    <div class="add-business">
      <h2>أضف نشاطك التجاري</h2>
      <p>
        هل لديك شركة أو متجر أو نشاط تجاري؟
        أضفه إلى سوقنا ليظهر للعملاء.
      </p>

      <a class="button" href="mailto:info@souqna.com">
        تواصل معنا لإضافة نشاطك
      </a>
    </div>
  </section>

  <footer>
    <p>© 2026 سوقنا - جميع الحقوق محفوظة</p>
    <p>الإعلانات ودليل الشركات والأنشطة التجارية في السودان</p>
  </footer>

  <script>
    function searchCompanies() {
      const input = document.getElementById("searchInput").value.trim().toLowerCase();
      const companies = document.querySelectorAll(".company");

      companies.forEach(function(company) {
        const text = company.innerText.toLowerCase();

        if (input === "" || text.includes(input)) {
          company.style.display = "block";
        } else {
          company.style.display = "none";
        }
      });
    }
  </script>

</body>
</html>
