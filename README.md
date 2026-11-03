# ប្រព័ន្ធគ្រប់គ្រងសាលារៀន NPIT Smart School

ប្រព័ន្ធគេហទំព័រសាលារៀនដែលត្រូវបានកែលម្អ ដោយប្រើ PHP 8, MySQL និង Bootstrap 5។

## ១. មុខងារដែលមានក្នុងប្រព័ន្ធ

- ប្តូរភាសារវាងភាសាអង់គ្លេស និងភាសាខ្មែរ។
- រក្សាទុកការកំណត់ Dark Mode ជាប្រចាំ។
- គេហទំព័រដើមសាធារណៈរបស់ NPIT។
- បណ្ណាល័យអេឡិចត្រូនិក (e-Library) ពីរភាសា ដែលអាចស្វែងរកសៀវភៅ តម្រៀបតាមប្រភេទ មើលសៀវភៅពេញនិយម សៀវភៅណែនាំ អាន PDF និងទាញយកសៀវភៅ។
- ប្រព័ន្ធគ្រប់គ្រងបណ្ណាល័យសម្រាប់ Admin ដើម្បីគ្រប់គ្រងសៀវភៅ រូបភាពគម្រប PDF អ្នកនិពន្ធ ប្រភេទសៀវភៅ និងស្ថិតិការអាន/ទាញយក។
- ផ្នែកអាហារូបករណ៍ ១០០% រយៈពេល ២ ឆ្នាំ និងការចុះឈ្មោះចូលរៀន។
- បង្ហោះ និងគ្រប់គ្រងជំនាញពិសេស ព្រឹត្តិការណ៍ គម្រោង សេចក្តីជូនដំណឹង និងវិចិត្រសាលរូបភាព។
- កំណត់តួនាទីអ្នកប្រើប្រាស់៖ Admin, Teacher, Student និង Parent។
- ប្រវត្តិរូបសិស្ស និងគ្រូ ដែលអាចបង្ហោះរូបថតបាន។
- ប្រព័ន្ធកត់ត្រាវត្តមានប្រចាំថ្ងៃ។
- ប្រព័ន្ធតាមដានថ្លៃសិក្សា និងវិក្កយបត្រ។
- ការកំណត់ព័ត៌មានផ្លូវការរបស់សាលា ព័ត៌មានទំនាក់ទំនង និងផែនទី តាមរយៈ Admin។
- សុវត្ថិភាពប្រព័ន្ធ រួមមានការអ៊ិនគ្រីបពាក្យសម្ងាត់ (Password Hashing) ការគ្រប់គ្រង Session ការការពារ CSRF និងការប្រើ SQL Prepared Statements។

## ២. កំណត់ត្រាអំពីការកែលម្អថ្មីៗ

### ២.១ ការចុះឈ្មោះគណនី

- នៅពេលចុះឈ្មោះជាសិស្ស ប្រព័ន្ធបង្កើតប្រវត្តិរូបសិស្សភ្ជាប់ជាមួយគណនីដោយស្វ័យប្រវត្តិ និងបង្កើតលេខសម្គាល់សិស្ស (Student ID)។
- នៅពេលចុះឈ្មោះជាអាណាព្យាបាល អាចភ្ជាប់គណនីកូនភ្លាមៗតាមរយៈ Student ID ឬភ្ជាប់នៅពេលក្រោយតាម Portal របស់អាណាព្យាបាល។
- នៅពេល Admin ឬ Teacher បង្កើតប្រវត្តិរូបសិស្ស ប្រព័ន្ធនឹងព្យាយាមភ្ជាប់ទៅគណនីដែលបានចុះឈ្មោះដោយខ្លួនឯង និងមានអ៊ីមែលត្រូវគ្នា។

### ២.២ ទំព័ររបស់សិស្ស និងអាណាព្យាបាល

Portal របស់សិស្ស និងអាណាព្យាបាល បង្ហាញព័ត៌មានពិតប្រាកដជំនួសសារគំរូ រួមមាន៖

- ភាគរយវត្តមាន។
- ថ្លៃសិក្សាដែលនៅជំពាក់។
- ព័ត៌មានប្រវត្តិរូប។

### ២.៣ វិចិត្រសាលរូបភាពនៅគេហទំព័រដើម

គេហទំព័រដើមមាន Bootstrap Carousel ដែលបង្ហាញរូបភាព និងវីដេអូដែលបានផ្សព្វផ្សាយដោយស្វ័យប្រវត្តិ។ វាក៏រួមបញ្ចូលមាតិកាប្រភេទ Gallery ដែលពីមុនមិនទាន់បង្ហាញជាសាធារណៈផងដែរ។

### ២.៤ បណ្ណាល័យអេឡិចត្រូនិក (e-Library)

- តារាងសៀវភៅ អ្នកនិពន្ធ និងប្រភេទសៀវភៅ ត្រូវបានបង្កើតដោយស្វ័យប្រវត្តិពី `database/schema.sql`។
- Admin អាចគ្រប់គ្រងសៀវភៅតាមរយៈ **Dashboard → e-Library management**។
- ឯកសារ PDF ដែលបង្ហោះ ត្រូវតែជាឯកសារ PDF ត្រឹមត្រូវ និងមានទំហំមិនលើស 100 MB។
- ត្រូវកំណត់ PHP និង Web Server ឱ្យអនុញ្ញាតការបង្ហោះឯកសារទំហំប៉ុណ្ណោះ។
- ការអាន PDF តាមអ៊ីនធឺណិត ប្រើកម្មវិធីអាន PDF ដែលមានស្រាប់ក្នុង Browser។

### ២.៥ រចនាប័ទ្ម Glassmorphism

កាតមាតិកា កាតមុខងារ កាតស្ថិតិ និងកាតប្រកាស ប្រើរចនាប័ទ្មកញ្ចក់ស្រអាប់ (Frosted Glass) ដោយមានផ្ទៃថ្លា និងបែបផែន `backdrop-filter`។

- មានពណ៌ផ្ទៃជំនួសសម្រាប់ Browser ចាស់ៗ។
- គាំទ្រទាំង Light Mode និង Dark Mode។
- ប្រើ Flexbox ដើម្បីឱ្យកាតមានកម្ពស់ស្មើគ្នា និងអាចរៀបចំឡើងវិញតាមទំហំអេក្រង់។

### ២.៦ ចលនា និងការផ្លាស់ប្តូររូបរាង

CSS និង JavaScript រួមគ្នាបន្ថែម៖

- ចលនាបង្ហាញមាតិកានៅពេលវាចូលក្នុងតំបន់មើលរបស់អេក្រង់។
- ចលនាបង្ហាញមាតិកាបន្តបន្ទាប់គ្នា។
- បែបផែនពេលដាក់ Mouse លើធាតុ។
- គាំទ្រទំព័រសាធារណៈ បណ្ណាល័យ និង Portal។
- គោរពការកំណត់ `prefers-reduced-motion` សម្រាប់អ្នកប្រើដែលចង់កាត់បន្ថយចលនា។
- មាតិកានៅតែអាចមើលឃើញ ប្រសិនបើ Browser មិនគាំទ្រមុខងារចលនាមួយចំនួន។

### ២.៧ ប្រព័ន្ធរចនាប៊ូតុង

ប៊ូតុង Bootstrap ត្រូវបានកែសម្រួលឱ្យមានរចនាប័ទ្មស្របគ្នា ដូចជា៖

- ប៊ូតុងពណ៌ Gradient។
- ប៊ូតុងប្រភេទ Outline។
- ប៊ូតុងបែប Glass។
- ប៊ូតុងដែលមានពណ៌តាមមុខងារ។
- បែបផែនពេលដាក់ Mouse និងពេលចុច។
- ការគាំទ្រការប្រើ Keyboard។
- ទំហំប៊ូតុងតូច និងទំហំងាយចុចលើអេក្រង់ Touch។
- ស្ថានភាព Loading និង Disabled។

តំណភ្ជាប់ Form និងសកម្មភាពប៊ូតុងដែលមានស្រាប់ នៅតែដំណើរការដដែល។

### ២.៨ ការកែសម្រួលព័ត៌មានណែនាំខ្លួន

អ្នកប្រើប្រាស់អាចកែសម្រួលអត្ថបទណែនាំខ្លួន (Bio) ដែលមានប្រវែងអតិបរមា ២,០០០ តួអក្សរ នៅក្នុងការកំណត់ប្រវត្តិរូប។

អត្ថបទនេះនឹងបង្ហាញជាសាធារណៈជំនួសអត្ថបទគំរូពីមុន។ ប្រព័ន្ធក៏អាចបន្ថែមវាល `users.bio` ដោយស្វ័យប្រវត្តិទៅក្នុងមូលដ្ឋានទិន្នន័យចាស់ តាមរយៈការត្រួតពិនិត្យភាពឆបគ្នារបស់ Schema។

### ២.៩ ការកែកំហុសក្នុង Teacher Attendance

បានកែសម្រួលលក្ខខណ្ឌដែលមិនអាចដំណើរការពិតបាននៅក្នុង `teacher/attendance.php`។ លក្ខខណ្ឌ `'student'==='teacher'` ដែលនៅសេសសល់ពីការចម្លងកូដរបស់ Admin ត្រូវបានកែតម្រូវ។

## ៣. របៀបដំឡើងប្រព័ន្ធ (Install)

អនុវត្តតាមជំហានខាងក្រោម ដើម្បីដំណើរការគេហទំព័រនៅលើកុំព្យូទ័ររបស់អ្នក។

1. ចម្លង Folder គម្រោងទៅក្នុងថត `htdocs` របស់ Apache/PHP ក្នុង XAMPP។
2. បង្កើត Database ឬ Import ឯកសារ `database/schema.sql` ទៅក្នុង MySQL។
3. កំណត់អថេរបរិស្ថាន Database (Database Environment Variables) ឬកែសម្រួលឯកសារ `config/config.php`។
4. ប្រសិនបើអ្នកកំពុងធ្វើបច្ចុប្បន្នភាពគម្រោងចាស់ សូមដំណើរការ `database/migrate.php` ម្តង។ កម្មវិធីក៏ព្យាយាមធ្វើ Migration ដោយស្វ័យប្រវត្តិផងដែរ។
5. ដំណើរការ `database/seed_admin.php` ម្តង តាម Browser ឬ Command Line។
6. បន្ទាប់ពីបង្កើតគណនី Admin ដំបូងរួច សូមលុបឯកសារ `database/seed_admin.php` ចេញ។
7. ត្រូវប្រាកដថា PHP មានសិទ្ធិសរសេរទិន្នន័យទៅក្នុង `uploads/` និង Folder រងទាំងអស់របស់វា។

### គណនី Admin លំនាំដើម

- **អ៊ីមែល:** `admin@example.com`
- **ពាក្យសម្ងាត់:** `Admin@12345`

**សំខាន់៖** សម្រាប់ការដាក់ឱ្យប្រើប្រាស់ជាក់ស្តែង សូមប្តូរពាក្យសម្ងាត់នេះភ្លាមៗ និងកំណត់ HTTPS ដើម្បីការពារទិន្នន័យ។

## ៤. ដោះស្រាយបញ្ហា `Unknown column 'published_at'`

បញ្ហានេះកើតឡើងនៅពេលប្រព័ន្ធកំពុងប្រើតារាង `content_items` ចាស់ ដែលមិនទាន់មាន Column `published_at`។

កំណែនេះអាចបន្ថែម Column `published_at` និង `status` ដោយស្វ័យប្រវត្តិ។

ប្រសិនបើអ្នកប្រើ MySQL មិនមានសិទ្ធិកែប្រែតារាងដោយស្វ័យប្រវត្តិទេ៖

1. បើកឯកសារ `database/migrate.php`។
2. ដំណើរការឯកសារនេះម្តង។
3. ត្រឡប់ទៅទំព័រគ្រប់គ្រងមាតិកា Admin ហើយ Refresh ទំព័រឡើងវិញ។

## ៥. ប្រព័ន្ធបង្ហោះវីដេអូ (Video Publishing)

Admin និង Teacher អាចបង្ហោះវីដេអូតាមរយៈ **Content & photos**។

មុខងារនេះគាំទ្រ៖

- បង្ហោះវីដេអូ MP4, WebM ឬ OGG ដោយផ្ទាល់ ដែលមានទំហំអតិបរមា 8 GB រួមទាំងឯកសារវីដេអូប្រភពកម្រិត 8K។
- បង្ហោះរូបភាព JPG, PNG ឬ WebP ដែលមានទំហំអតិបរមា 50 MB។
- មើលវីដេអូជាមុននៅពេលកែសម្រួល។
- បន្ថែមតំណភ្ជាប់ YouTube, Vimeo ឬ URL វីដេអូផ្សេងទៀត។
- ចាក់វីដេអូជាសាធារណៈតាមរយៈ HTML5។

### ៥.១ ការកំណត់ Server សម្រាប់ឯកសារធំ

គម្រោងនេះមានឯកសារ `.user.ini` និង `.htaccess` សម្រាប់កំណត់ការបង្ហោះឯកសារធំ។

ការកំណត់ Server ដែលមានប្រសិទ្ធភាព ត្រូវអនុញ្ញាតយ៉ាងហោចណាស់៖

| ការកំណត់ | តម្លៃ |
|---|---:|
| `upload_max_filesize` | `8G` |
| `post_max_size` | `9G` ឬខ្ពស់ជាងនេះ |
| `max_execution_time` | `3600` |
| `max_input_time` | `3600` |

ចំណាំ៖ Hosting Provider, Reverse Proxy, CDN ឬ Web Server អាចមានការកំណត់កំណត់ទំហំឯកសារបន្ថែម។

ការបង្ហោះឯកសារទំហំ 8 GB ត្រូវការទំហំផ្ទុកគ្រប់គ្រាន់ ហើយអាចចំណាយពេលយូរ ប្រសិនបើការតភ្ជាប់អ៊ីនធឺណិតយឺត។

### ៥.២ ចលនា Loader ពេលបើកទំព័រ

គេហទំព័រនេះប្រើ Loader ដែលមានការ៉េចំនួន 3 × 3 ដើម្បីបង្ហាញចលនាកំពុងផ្ទុក នៅពេល៖

- បើកទំព័រ។
- ផ្លាស់ប្តូរទំព័រនៅក្នុងគេហទំព័រដដែល។
- បញ្ជូន Form។

## ៦. របៀបបើកគម្រោងពី Desktop

កម្មវិធី Shortcut នៅលើ Desktop នឹង៖

1. ចាប់ផ្តើម MariaDB Server របស់ XAMPP ប្រសិនបើវាមិនទាន់ដំណើរការ។
2. បើក Folder គម្រោងពេញលេញនៅក្នុង VS Code។
3. មិនដំឡើង Database ឡើងវិញ និងមិន Reset Database ចាស់ទេ។

MariaDB រក្សាទុកឯកសារទិន្នន័យនៅក្នុង៖

`C:\xampp\mysql\data`

ដូច្នេះ ទិន្នន័យសាលារៀនដែលបានរក្សាទុក នឹងនៅតែមាននៅលើ Disk បន្ទាប់ពីបិទ Windows។

### ៦.១ របៀបដំណើរការគេហទំព័រ

បន្ទាប់ពីបើកគម្រោងក្នុង VS Code៖

1. បើកឯកសារ `index.php`។
2. ចុចប៊ូតុង **PHP Server: Serve project** នៅក្នុងកម្មវិធីកែសម្រួល ឬស្វែងរក Command នេះតាម Command Palette។
3. ប្រព័ន្ធប្រើ PHP របស់ XAMPP ដែលគាំទ្រ `pdo_mysql`។
4. បើក Browser ហើយចូលទៅកាន់អាសយដ្ឋាន៖

`http://127.0.0.1:8002`

### ៦.២ នៅពេលបើកកុំព្យូទ័រឡើងវិញ

បន្ទាប់ពី Restart Windows៖

1. ចុចពីរដងលើ Shortcut នៅលើ Desktop។
2. វានឹងចាប់ផ្តើម MariaDB និងបើកគម្រោងឡើងវិញ។
3. នៅពេលអ្នកប្រើប្រាស់រួច សូមបញ្ឈប់ PHP Server តាមរយៈ Command Palette។
4. ការបិទ VS Code ក៏នឹងបញ្ឈប់ PHP Server របស់វាផងដែរ។

## សេចក្តីសន្និដ្ឋាន

ប្រព័ន្ធ NPIT Smart School នេះ ជាគម្រោងគ្រប់គ្រងសាលារៀនដែលប្រើ PHP 8, MySQL និង Bootstrap 5។ វារួមបញ្ចូលប្រព័ន្ធគ្រប់គ្រងអ្នកប្រើប្រាស់ វត្តមាន ថ្លៃសិក្សា បណ្ណាល័យអេឡិចត្រូនិក រូបភាព វីដេអូ និងការកំណត់សុវត្ថិភាព។

សម្រាប់អ្នកដែលប្រើ VS Code និង XAMPP ជំហានសំខាន់បំផុតគឺ ត្រូវប្រាកដថា Database ត្រូវបានបង្កើតត្រឹមត្រូវ កំណត់ព័ត៌មានភ្ជាប់ Database ឱ្យបានត្រឹមត្រូវ និងដំណើរការ PHP Server មុនបើកគេហទំព័រ។

# NPIT Smart School Management System
Improved PHP 8 + MySQL + Bootstrap 5 school portal.

## Includes
- EN / Khmer language switch
- Persistent dark mode
- Public NPIT landing site
- Bilingual e-Library with searchable books, categories, featured/popular/recommended collections, PDF reading and downloads
- Admin library management for books, covers/PDFs, authors, categories and reading/download statistics
- 2-year 100% scholarship and enrollment section
- Majors, events, projects, announcements and gallery publishing
- Admin / teacher / student / parent roles
- Student and teacher profiles with photo upload
- Daily attendance
- Fee/invoice tracking
- Admin site settings for official school/contact/map information
- Password hashing, sessions, CSRF protection, prepared SQL statements

## Changelog (this update)
- **Registration is now fully wired up**: signing up as a Student auto-creates a linked
  student profile (with a generated Student ID) instead of leaving accounts unlinked.
  Signing up as a Parent can request a child link by Student ID; an administrator must approve
  the request. Admin/teacher-created student profiles auto-link to a matching
  self-registered account by email.
- **Student & Parent portals** now show real attendance %, fees due and profile info
  instead of a placeholder message.
- **Public gallery carousel**: a Bootstrap carousel-with-indicators section on the
  homepage automatically pulls published photos and videos (including the "Gallery"
  content type, which previously had no public display) from across the site.
- **e-Library**: book, author and category tables are created automatically from
  `database/schema.sql`. Administrators can manage the catalog at **Dashboard →
  e-Library management**. PDF uploads must be valid PDF files no larger than 100 MB;
  ensure PHP and the web server allow uploads of that size. Online reading uses the
  browser's built-in PDF viewer.
- **Glassmorphism**: content/feature/stat/post cards use a frosted-glass style
  (`backdrop-filter`, translucent surfaces) with a solid-color fallback for older
  browsers, in both light and dark mode. Public item grids use flexbox so cards stay
  equal height and reflow responsively.
- **Motion and transitions**: shared CSS and JavaScript add viewport-triggered
  reveals, staggered content, and restrained hover feedback across public, library,
  and portal pages. Animations use transforms and opacity, respect
  `prefers-reduced-motion`, and leave content visible when motion APIs are unavailable.
- **Button design system**: shared Bootstrap button styles add consistent gradient,
  outline, glass, and semantic variants with hover/press feedback, keyboard focus,
  compact and touch-friendly sizing, and loading/disabled states. Existing links,
  forms, and button actions remain unchanged; motion respects reduced-motion settings.
- **Editable profile bio**: users can update a 2,000-character bio in their profile
  settings; it is displayed publicly in place of the previous sample text. New
  installations create the `users.bio` field, and existing installations add it
  through the normal automatic schema compatibility check.
- Fixed a dead/always-false conditional in `teacher/attendance.php` (`'student'==='teacher'`)
  left over from a copy-paste of the admin version.

## Install
1. Copy to Apache/PHP `htdocs`.
2. Create/import `database/schema.sql` into MySQL.
3. Configure DB environment variables, or edit `config/config.php`.
4. If upgrading an older copy of this project, run `database/migrate.php` once from the XAMPP Shell/CLI (the application also attempts compatibility migrations automatically).
5. Set `NPIT_ADMIN_PASSWORD` to a unique password of at least 16 characters, then run `database/seed_admin.php` once from the XAMPP Shell/CLI. For example, in PowerShell: `$env:NPIT_ADMIN_PASSWORD='use-a-unique-password-here'; php .\database\seed_admin.php`.
6. Delete `database/seed_admin.php` after creating the first admin.
7. Ensure `uploads/` and its subfolders are writable by PHP.

The seed script creates/checks `admin@example.com`; it never uses a built-in password.
Existing installations should immediately replace any administrator password that
was previously set to the old documented default.

For production, change that password immediately and configure HTTPS.

## Fix for `Unknown column 'published_at'`

That error happens when an older `content_items` table is still being used. This version automatically adds the missing `published_at` and `status` columns. If your MySQL user cannot ALTER tables automatically, run `php database/migrate.php` from the XAMPP Shell, then reload the admin content page.

## Video publishing

Admins and teachers can publish videos from **Content & photos**. The form supports:
- Direct MP4, WebM, or OGG video uploads up to **4 GB**
- JPG, PNG, or WebP photo uploads up to **100 MB**
- Video preview when editing
- Optional YouTube/Vimeo/video URL
- Public HTML5 video playback

### Large upload server settings
The project includes `.user.ini` and Apache `.htaccess` settings for large uploads. The effective PHP configuration must allow at least:

- `upload_max_filesize = 4G`
- `post_max_size = 0` (unlimited request body; PHP's `0` value is intentional)
- `max_execution_time = 7200`
- `max_input_time = 7200`
- `memory_limit = 512M`
- Enable `fileinfo`, `mbstring`, `gd`, and `pdo_mysql` in XAMPP's active `php.ini`.

Apache must allow request bodies of the required size (`LimitRequestBody 0` means
unlimited; it is the Apache default). A hosting provider, reverse proxy, or web
server can impose additional limits. A 4 GB upload also requires enough disk space
and can take a long time on a slow connection.

### Page Loader
The site now uses the supplied 3x3 square animated loader on page load, same-origin navigation, and form submission.

## Open locally from the Desktop

The Desktop launcher starts the existing XAMPP MariaDB server if it is stopped, then opens this full project folder in VS Code. It does not reinstall or reset the database. MariaDB keeps its files under `C:\xampp\mysql\data`, so the saved school records remain on disk when Windows is shut down.

After opening the project, open `index.php` and click the **PHP Server: Serve project** editor button, or run that command from the Command Palette. The workspace config uses XAMPP PHP (with `pdo_mysql`) and serves on `http://127.0.0.1:8002`.

After restarting Windows, double-click the Desktop launcher again to start MariaDB and reopen the project. Stop the PHP Server extension from the Command Palette when you are finished; closing VS Code also stops its PHP server.
