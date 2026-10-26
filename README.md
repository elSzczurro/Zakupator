# Strona pobierania Zakupatora (GitHub Pages)

## 1. Wrzuć stronę na GitHub
1. Utwórz repozytorium, np. `zakupator`, i wgraj do niego wszystkie pliki z tego folderu (`index.html`, `icon.png`, `favicon.png`, `.nojekyll`).
2. Wejdź w **Settings → Pages**. W **Source** wybierz **Deploy from a branch**, gałąź `main` i folder `/ (root)`.
3. Po minucie strona działa pod adresem `https://TWOJ-LOGIN.github.io/zakupator/`.

## 2. Dodaj plik do pobrania
1. Zbuduj aplikację: `eas build -p android --profile preview` (w `eas.json` ustaw dla `preview` `"android": { "buildType": "apk" }`).
2. W repozytorium wejdź w **Releases → Draft a new release**, nadaj tag `v1.0.0`.
3. Wgraj plik APK pod nazwą **zakupator.apk** i opublikuj.

Przycisk „Pobierz na Androida" zawsze wskazuje najnowsze wydanie, a numer wersji na przycisku pobiera się sam.

## 3. iPhone
Pliku `.ipa` nie da się zainstalować bezpośrednio ze strony. Gdy będziesz mieć link TestFlight lub App Store, wpisz go w `index.html` w polu `iosUrl` w obiekcie `CONFIG`.

## Własna domena lub inna nazwa repozytorium
Wpisz `user` i `repo` w obiekcie `CONFIG` na początku skryptu w `index.html`.
