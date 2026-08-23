RAM FULL LIVE WEBSITE — PUBLIC + ADMIN + DATABASE

FILES
1. index.html      = public portfolio website
2. admin.html      = full website admin/CMS
3. config.js       = Supabase URL + anon key
4. schema.sql      = database tables + Row Level Security + starter content
5. assets/images   = project images
6. assets/videos   = project videos

SETUP (mobile/Acode friendly)
1. Create a Supabase project.
2. In Supabase SQL Editor, run the complete schema.sql.
3. In Supabase Authentication -> Users, create the admin email/password.
4. Copy that user's UUID.
5. In SQL Editor run:
   insert into public.admin_users(user_id) values ('YOUR_ADMIN_USER_UUID');
6. Open config.js and replace:
   YOUR_SUPABASE_PROJECT_URL
   YOUR_SUPABASE_ANON_KEY
   with your Supabase project URL and anon/public key.
7. Keep index.html, admin.html and config.js in the same folder.
8. Upload the whole folder to your hosting.
9. Public: /index.html
10. Admin: /admin.html

IMPORTANT
- Use only the Supabase anon/public key in config.js.
- NEVER put the Supabase service_role key in browser files.
- The database is not actually live until you create the Supabase project and put its URL/key into config.js.
- Public visitors can submit messages; only an authenticated admin user added to admin_users can modify CMS data.
