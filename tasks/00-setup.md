# Vazifa 00: GitHub'ni sozlash

**Natija:** guruh saytida sizning ismingiz va internetda ochiladigan shaxsiy sahifangiz.

## 1. Hisob va dasturlar

1. https://github.com da account oching
2. Git'ni o'rnating: https://git-scm.com
3. VS Code'ni o'rnating: https://code.visualstudio.com
4. Terminalda ismingizni sozlang:

```bash
git config --global user.name "Aziz Karimov"
git config --global user.email "sizning@email.uz"
```

## 2. Fork va clone

1. https://github.com/web-dev-2026/group-208 sahifasida **Fork** tugmasini bosing.
2. Terminalda (`USERNAME` = sizning GitHub nomingiz):

```bash
git clone https://github.com/USERNAME/group-208.git
cd group-208
git remote add upstream https://github.com/web-dev-2026/group-208.git
git checkout -b 00-setup-aziz
```

## 3. O'z papkangiz

1. `students/_template` papkasini nusxalang va nomini o'zgartiring: `students/ism-familiya` (masalan `students/aziz-karimov`).
2. VS Code'da `students/ism-familiya/index.html` faylini oching va ismingizni yozing.

## 4. Topshirish

```bash
git add .
git commit -m "00-setup: shaxsiy papka qo'shildi"
git push -u origin 00-setup-aziz
```

GitHub'da **Compare & pull request** → sarlavha: `[00] Aziz Karimov – Setup` → **Create pull request**.

## 5. Saytingizni yoqing

O'z fork'ingizda: **Settings → Pages → Branch: main → Save**.

O'qituvchi PR'ni qabul qilgandan keyin `main`ni sinxronlang (README'dagi 1-qadam). Saytingiz:
`https://USERNAME.github.io/group-208/students/ism-familiya/`

Guruh sayti: https://web-dev-2026.github.io/group-208/
