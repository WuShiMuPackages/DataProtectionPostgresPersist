# DataProtectionPostgresPersist


This project is a sava DataProtection Persist Key in postgres .

> Install-Package DataProtectionPostgresPersist -Version 1.0.3

  ```C#
       public void ConfigureServices(IServiceCollection services)
        {
            services.Configure<CookiePolicyOptions>(options =>
            {
                options.CheckConsentNeeded = context => true;
                options.MinimumSameSitePolicy = SameSiteMode.None;
            });
            //add Postgres DataProtection
            services.AddDataProtection().PersistKeysToPostgres(Configuration.GetConnectionString("Postgre"));

            services.AddMvc().SetCompatibilityVersion(CompatibilityVersion.Version_2_2);
        }
 ```
