# Insertion des liens
Pour insérer des liens vers des pages web dans LaTeX,
il existe plusieurs méthodes :

1. Méthode simple avec le package `hyperref` :
```latex
\usepackage{hyperref}

% Dans le texte :
\url{https://www.example.com}
% ou
\href{https://www.example.com}{Texte cliquable}
```

2. Personnalisation de l'apparence des liens :
```latex
\usepackage{hyperref}
\hypersetup{
    colorlinks=true,
    linkcolor=blue,
    filecolor=magenta,      
    urlcolor=cyan
}
```

3. Pour un lien sans soulignement :
```latex
\href{https://www.example.com}{\nolinkurl{Texte du lien}}
```

4. Pour les liens contenant des caractères spéciaux :
```latex
\href{https://www.example.com/page\%20with\%20spaces}{Texte du lien}
```

Le package `hyperref` doit généralement être chargé en dernier dans le préambule
pour éviter les conflits avec d'autres packages.
