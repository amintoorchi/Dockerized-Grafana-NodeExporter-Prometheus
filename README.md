Grafana / NodeExporter / Prometheus Dockerized

This project provides a Dockerized setup for monitoring your system with Prometheus, Node Exporter, and Grafana. It's designed for easy deployment and visualization of system metrics.
Features

Prometheus: For collecting and storing metrics.
Node Exporter: Exposes hardware and OS metrics from your host system.
Grafana: Beautiful dashboards for visualizing the collected data.
Persistent storage for Prometheus data and Grafana configurations.
Simple Docker Compose setup for quick start.

Getting Started
Prerequisites

Docker and Docker Compose installed on your machine.

Installation

Clone the repository:
git clone https://github.com/username/repo-name.git
cd repo-name


Start the containers:
docker compose up -d



Access the Services

Prometheus: http://localhost:9090
Grafana: http://localhost:3000 (Default credentials: admin/admin)

Important Notes

Data for Prometheus is stored in ./prom_data/ and for Grafana in ./grafana-storage/. These directories are ignored in .gitignore and will be created automatically on first run.
Docker Compose version is set to "3.18" for compatibility with recent Docker versions.
Network mode is set to "host" for Node Exporter and Prometheus to access host metrics directly. If you need portability across different systems, consider switching to a bridge network.
Ensure ./prom_data and ./grafana-storage are added to .gitignore before pushing to GitHub to avoid uploading unnecessary data.

Configuration

The docker-compose.yml file is pre-configured. You can customize ports or volumes as needed.
Grafana dashboards can be imported or created manually after login.

Troubleshooting

If containers fail to start, check Docker logs: docker compose logs.
Ensure no port conflicts on 9090 or 3000.

Contributing
Feel free to fork this repository and submit pull requests for improvements!
License
This project is licensed under the MIT License.

Grafana / NodeExporter / Prometheus Dockerized

این پروژه یک راه‌اندازی Dockerized برای مانیتورینگ سیستم با Prometheus، Node Exporter و Grafana ارائه می‌دهد. طراحی شده برای استقرار آسان و visualization متریک‌های سیستم.
ویژگی‌ها

Prometheus: برای جمع‌آوری و ذخیره متریک‌ها.
Node Exporter: نمایش متریک‌های سخت‌افزار و سیستم عامل از هاست.
Grafana: داشبوردهای زیبا برای visualization داده‌های جمع‌آوری‌شده.
ذخیره‌سازی پایدار برای داده‌های Prometheus و تنظیمات Grafana.
راه‌اندازی ساده با Docker Compose برای شروع سریع.

شروع به کار
پیش‌نیازها

Docker و Docker Compose روی ماشین شما نصب شده باشد.

نصب

کلون کردن مخزن:
git clone https://github.com/username/repo-name.git
cd repo-name


بالا آوردن کانتینرها:
docker compose up -d



دسترسی به سرویس‌ها

Prometheus: http://localhost:9090
Grafana: http://localhost:3000 (نام کاربری و رمز پیش‌فرض: admin/admin)

نکات مهم

داده‌های Prometheus در ./prom_data/ و Grafana در ./grafana-storage/ ذخیره می‌شوند. این دایرکتوری‌ها در .gitignore نادیده گرفته شده‌اند و در اولین اجرا به طور خودکار ایجاد می‌شوند.
نسخه Docker Compose روی "3.18" تنظیم شده برای سازگاری با نسخه‌های جدید Docker.
حالت شبکه روی "host" برای Node Exporter و Prometheus تنظیم شده تا مستقیماً به متریک‌های هاست دسترسی داشته باشند. اگر نیاز به قابلیت حمل بین سیستم‌های مختلف دارید، از شبکه bridge استفاده کنید.
قبل از push به GitHub، مطمئن شوید ./prom_data و ./grafana-storage به .gitignore اضافه شده‌اند تا داده‌های غیرضروری آپلود نشود.

پیکربندی

فایل docker-compose.yml از قبل پیکربندی شده است. می‌توانید پورت‌ها یا volumeها را طبق نیاز تغییر دهید.
داشبوردهای Grafana را می‌توانید پس از ورود import کنید یا به صورت دستی بسازید.

عیب‌یابی

اگر کانتینرها شروع نشدند، لاگ‌های Docker را چک کنید: docker compose logs.
مطمئن شوید تداخل پورتی روی 9090 یا 3000 وجود ندارد.

مشارکت
از fork کردن این مخزن و ارسال pull request برای بهبودها استقبال می‌شود!
لایسنس
این پروژه تحت لایسنس MIT منتشر شده است.
