Futura PT is a licensed, commercial typeface and its font files are not
included in this project (they were not supplied and cannot be redistributed).

The site instead uses this fallback stack, declared in css/style.css:

  font-family: "Futura PT", Futura, "Century Gothic", Arial, Helvetica, sans-serif;

Century Gothic ships with Windows by default and is the closest common match
to Futura's geometric look, so most Windows visitors will already see a very
close approximation with zero setup.

If you purchase Futura PT (e.g. from MyFonts / fonts.com), drop the .woff2 files
in this folder and add an @font-face block at the top of css/style.css:

  @font-face {
    font-family: "Futura PT";
    src: url("../fonts/FuturaPT-Book.woff2") format("woff2");
    font-weight: 400; font-display: swap;
  }
  /* repeat per weight: Medium (500), Demi/Bold (600-700) */
