# Unit 16: Veb-sayt dizayni va ishlab chiqish — Guruh 208

**Guruh sayti:** https://web-dev-2026.github.io/group-208/

Bu repozitoriyda har bir talabaning o'z papkasi bor. Har bir yangi mavzu uchun papkangiz ichida yangi papka yaratasiz. Ishingizni **Pull Request (PR)** orqali topshirasiz, o'qituvchi tekshirib qabul qiladi (merge). Qabul qilingan ishlar guruh saytida avtomatik paydo bo'ladi.

## Papkalar tuzilishi

```
students/
└── aziz-karimov/            ← sizning papkangiz
    ├── index.html           ← sizning bosh sahifangiz (barcha mavzularga havolalar)
    ├── 01-html-basics/
    │   ├── index.html
    │   ├── css/style.css
    │   └── images/
    └── 02-tables/
        ├── index.html
        └── css/style.css
```

## Qoidalar

1. Faqat **o'z papkangizdagi** fayllarni o'zgartiring: `students/ism-familiya/`.
2. Har bir mavzu uchun **yangi papka**: `01-html-basics`, `02-tables`, ... Nomi `tasks/` papkasidagi vazifa fayli bilan bir xil bo'lsin.
3. Nomlarda faqat kichik lotin harflari, raqamlar va chiziqcha (`-`). **Bo'sh joy ishlatmang.**
4. Har bir mavzu papkasida `index.html` bo'lishi shart.
5. Ishni boshlashdan oldin har doim **sinxronlang** (pastdagi 1-qadam).
6. Bitta vazifa = bitta branch = bitta Pull Request.
7. Har yangi mavzudan keyin o'z bosh sahifangizga (`students/ism-familiya/index.html`) unga havola qo'shing.

## Bir martalik sozlash

To'liq ko'rsatma: [tasks/00-setup.md](tasks/00-setup.md)

1. Shu sahifaning yuqori o'ng burchagidagi **Fork** tugmasini bosing.
2. Terminalda (`USERNAME` o'rniga o'z GitHub nomingizni yozing):

```bash
git clone https://github.com/USERNAME/group-208.git
cd group-208
git remote add upstream https://github.com/web-dev-2026/group-208.git
```

3. `students/_template` papkasini nusxalang va `students/ism-familiya` deb nomlang (masalan `students/aziz-karimov`).
4. O'z fork'ingizda: **Settings → Pages → Branch: main → Save**. 1–2 daqiqadan keyin saytingiz ochiladi:
   `https://USERNAME.github.io/group-208/students/ism-familiya/`

## Har bir vazifa uchun ish tartibi

```bash
# 1. O'qituvchining repozitoriyasidan yangiliklarni olish
git checkout main
git pull upstream main
git push origin main

# 2. Vazifa uchun yangi branch
git checkout -b 02-tables-aziz

# 3. Ishlash: students/aziz-karimov/02-tables/ papkasida

# 4. Saqlash (tez-tez commit qiling)
git add .
git commit -m "02-tables: dars jadvali va havolalar qo'shildi"

# 5. Fork'ingizga yuklash
git push -u origin 02-tables-aziz
```

6. GitHub'da **Compare & pull request** tugmasini bosing. Sarlavha: `[02] Aziz Karimov – Tables`
7. O'qituvchi izoh qoldirsa: tuzating, yana `commit` va `push` qiling. PR o'zi yangilanadi.

## Avvalgi ishni qayta ishlash

Vazifa eski ishingizni yaxshilash bo'lsa (masalan, Flexbox bilan bosh sahifa):

1. Eski papkani yangi nom bilan nusxalang va **hech narsani o'zgartirmasdan** commit qiling:
   `git commit -m "09-flexbox-homepage: 01-html-basics dan nusxa"`
2. O'zgartirishlarni keyingi commit'larda qiling.

Shunda PR'da nima o'zgarganini aniq ko'rish mumkin, eski versiya esa saytda saqlanib qoladi.

## Tez-tez uchraydigan muammolar

| Muammo | Yechim |
|---|---|
| Push qilganda `Permission denied` | `upstream`ga emas, `origin`ga push qiling |
| Conflict chiqdi | Faqat o'z papkangizni o'zgartirganingizni tekshiring |
| Sayt ochilmayapti (404) | Pages yoqilganini tekshiring, 1–2 daqiqa kuting, papkada `index.html` borligini tekshiring |
| Rasm yoki CSS ishlamayapti | Yo'l (path) va fayl nomidagi katta-kichik harflarni tekshiring: `Image.png` va `image.png` har xil |
