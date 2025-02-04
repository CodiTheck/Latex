# Figure

## Problème de positionnement d'une figure
Ce problème est très courant avec LaTeX car par défaut, il utilise un positionnement
flottant pour les figures. Voici plusieurs solutions pour mieux contrôler le placement :

1. Modifier les paramètres de placement dans l'environnement figure :
```latex
\begin{figure}[!htb]
```
où :
- `h` : ici (here)
- `t` : haut de page (top)
- `b` : bas de page (bottom)
- `!` : force LaTeX à respecter plus strictement vos préférences

2. Pour forcer encore plus le placement, utilisez [H] :
```latex
\usepackage{float}
\begin{figure}[H]
```
Cela force la figure à apparaître exactement à l'endroit spécifié.

3. Ajustez les paramètres de flottants :
```latex
\setcounter{topnumber}{2}
\setcounter{bottomnumber}{2}
\setcounter{totalnumber}{4}
\renewcommand{\topfraction}{0.85}
\renewcommand{\bottomfraction}{0.85}
\renewcommand{\textfraction}{0.15}
\renewcommand{\floatpagefraction}{0.7}
```

4. Une autre approche est d'utiliser le package `placeins` :
```latex
\usepackage{placeins}
\FloatBarrier
```
Placez `\FloatBarrier` là où vous voulez empêcher les figures de "flotter" plus loin.

La solution la plus simple et souvent la plus efficace est d'utiliser `[H]` avec le package float.
C'est généralement suffisant pour la plupart des cas.
