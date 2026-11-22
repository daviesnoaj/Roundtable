drop policy if exists "read posts" on posts;
drop policy if exists "read chat" on chat;
drop policy if exists "read profiles" on profiles;
create policy "read posts" on posts for select to anon, authenticated using (true);
create policy "read chat" on chat for select to anon, authenticated using (true);
create policy "read profiles" on profiles for select to anon, authenticated using (true);
grant select on posts, chat, profiles to anon;
