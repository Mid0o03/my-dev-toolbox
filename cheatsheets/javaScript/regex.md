# Regex (Expressions Régulières)

Les expressions régulières sont utilisées pour la recherche et le remplacement de motifs dans les chaînes de caractères.

## 🛠️ Syntaxe de base
- `/motif/drapeaux` : Structure de base.
- `.` : N'importe quel caractère (sauf nouvelle ligne).
- `^` : Début de la chaîne.
- `$` : Fin de la chaîne.
- `*` : 0 ou plus.
- `+` : 1 ou plus.
- `?` : 0 ou 1.
- `\d` : Chiffre.
- `\w` : Caractère de mot (alphanumérique + underscore).
- `\s` : Espace blanc.
- `[abc]` : N'importe quel caractère entre les crochets.
- `[^abc]` : N'importe quel caractère SAUF ceux entre les crochets.
- `(abc)` : Groupe de capture.

## 🚩 Drapeaux (Flags)
- `g` : Global (ne s'arrête pas au premier match).
- `i` : Insensible à la casse.
- `m` : Multi-ligne.

## 📝 Exemples courants en JS
```javascript
// Tester un email
const emailRegex = /^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$/;
emailRegex.test("test@example.com"); // true

// Extraire des chiffres
const str = "L'ID est 12345";
const id = str.match(/\d+/)[0]; // "12345"

// Remplacer du texte
const result = "C'est mal".replace(/mal/g, "bien");
```

## 🔍 Méthodes JavaScript
- `regex.test(str)` : Retourne true/false.
- `str.match(regex)` : Retourne un tableau de résultats.
- `str.replace(regex, replacement)` : Remplace les matchs.
- `str.search(regex)` : Retourne l'index du premier match.
