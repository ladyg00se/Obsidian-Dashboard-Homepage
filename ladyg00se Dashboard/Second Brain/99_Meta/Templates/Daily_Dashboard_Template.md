---
banner: "![[99_Meta/38a8c66883cc912d73b4b29050f76941.webp]]"
banner-x: 54
banner-y: 21
banner-height: 300
pixel-banner-flag-color: bee
tags:
  - Daily
content-start: 191
---
> [!note]
> If you have any wishes for the Dashboard, please let me know. Also if you like it, would love to hear your feedback! ~ ladyg00se
```widgets
type: clock
format: "24hr"
```
🎯 #My #Goals #To #Follow
> [!multi-column]
>
> > [!blank-container|wide-1]
> >### 📂 Task List
> >
> >
> > - #### 📅 [[Todo]] <span class="chip success">Today</span>  #mcl/list-card
> >
> >   ```dataview
> >   TASK
> >   FROM "01_Personal/Todo" OR "03_Projects/Master_WI" OR "99_Meta/DB/Birthdays"
> >   WHERE section = [[Todo#📅 Todos]] OR section = [[Master_WI#📅 Todos]] OR section = [[Birthdays#Birthdays]]
> >   AND !completed
> >   AND due = date(today) OR due = date(none)
> >   SORT checked asc, text asc
> >   ```
>
> > [!blank-container|wide-2]
> >
> > ### 📂 Aktuelle Projekte
> >
> > - [[Master|🎓 Master ]] #mcl/list-card
> >   - Studies
> > - [[03_Projects/Learning|Learning]]
> >   - Learning
> > - [[03_Projects/Shopping List| Shopping List]]
> >   - Shopping List
> >

---
# ✨ ᴅᴀʏ ᴘʟᴀɴɴᴇʀ ✨ (Example [[Day-Planner]])
- [ ] 08:00 - 09:00 Frühstück & Morgenroutine 🌿  
- [ ] 09:00 - 10:30 Lernen: Master WI 📚  
- [ ] 10:30 - 11:00 Spaziergang ☘️  
- [ ] 11:00 - 12:30 Projektarbeit Cyber Security 🛡️  
- [ ] 12:30 - 13:30 Mittagessen 🥗  
- [ ] 13:30 - 15:00 Wohnung planen 🏡  
- [ ] 15:00 - 15:30 Kaffee & kurze Pause ☕  
- [ ] 15:40 - 16:30 TÜV Auto 🚗  
- [ ] 16:30 - 18:00 Shopping 🛍️  
- [ ] 18:00 - 19:00 Fitnessstudio 🏋️  
- [ ] 19:00 - 20:00 Abendessen 🍲  
- [ ] 20:00 - 21:00 Lesen & Duolingo 📖🦉  

---
#  ✳️ ᴛᴏ ᴅᴏ ✳️ (Shows all Todos from [[Todo]])

> [!multi-column]
>
> > [!blank-container|wide-1]
> >
> > - #### 📅 Next 7 days <span class="chip info">Week</span> #mcl/list-card
> >
> >   ```dataview
> >   TASK
> >   FROM "01_Personal/Todo" OR "03_Projects/Master_WI"
> >   WHERE !completed
> >   AND due != null
> >   AND due >= date(today)
> >   AND due <= date(today) + dur(7 days)
> >   SORT due asc, text asc
> >   ```
> >
> > - #### 📅 Next 30 days <span class="chip warn">Month</span> #mcl/list-card
> >
> >   ```dataview
> >   TASK
> >   FROM "01_Personal/Todo" OR "03_Projects/Master_WI"
> >   WHERE !completed
> >   AND due != null
> >   AND due > date(today) + dur(7 days)
> >   AND due <= date(dateformat(date(today), "yyyy-MM") + "-31")
> >   SORT due asc, text asc
> >   ```
> >
> > - #### 📅 Later <span class="chip success">Future+</span> #mcl/list-card
> >
> >   ```dataview
> >   TASK
> >   FROM "01_Personal/Todo" OR "03_Projects/Master_WI"
> >   WHERE !completed
> >   AND due != null
> >   AND due > date(dateformat(date(today), "yyyy-MM") + "-31")
> >   SORT due asc, text asc
> >   ```

---
# 🌱 ʟɪɴᴋs (All the other important Stuff, next to Main Projects)

> [!multi-column]
>
> > [!blank-container|wide-1]
> >
> > 
> >
> > - [[Braindump]] #mcl/list-card
> >   - To unload the brain
> > - [[News Dashbaord]]
> >   - RSS Feed
> > - [[🍰 Recipes]]
> >   - Enjoying the food
> > - [[Links to remember]]
> >   - All the pages and videos i want to watch
> > - [[Books & Animes]]
> >   - Too read and shop
> > - [[Wishlist]]
> >   - All the stuff i want, but don't have money for
> > - [[Archived]]
> >   - All the finished projects
>    
> > [!blank-container|wide-1]
> > 
> > 
> > 
> > ![[38a8c66883cc912d73b4b29050f76941.webp]]
> 

---
# 🌿 ᴛᴏᴅᴀʏ ɴᴏᴛᴇs 🌿 (Useful for daily Journaling ;)
```handwritten-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Writing/2025.8.22 - 21.48pm.writing"
}
```

---
# 🎂 ʙɪʀᴛʜᴅᴀʏs ✨ (Just add to [[Birthdays]] and [[Presents]])

> [!multi-column]
>
> > [!blank-container|wide-1]
> >
> > - #### 📅 [[Birthdays|Next 30 days]] <span class="chip info">Month</span> #mcl/list-card
> >
> >   ```dataview
> >   TASK
> >   FROM "98_Database/Birthdays"
> >   WHERE !completed
> >   AND due >= date(today)
> >   AND due <= date(today) + dur(30 days)
> >   SORT due asc, text asc
> >   ```
> >
> > - #### [[Presents|🎁 Present Ideas]]<span class="chip warn">Shopping</span> #mcl/list-card
> >
> >   ```dataview
> >   TASK
> >   FROM "98_Database/Presents"
> >   WHERE !completed
> >   SORT due asc, text asc
> >   ```
> >
> > - #### 📅 Later <span class="chip success">Future+</span> #mcl/list-card
> >
> >   ```dataview
> >   TASK
> >   FROM "98_Database/Birthdays"
> >   WHERE !completed
> >   AND due > date(dateformat(date(today), "yyyy-MM") + "-31")
> >   SORT due asc, text asc
> >   ```

---



