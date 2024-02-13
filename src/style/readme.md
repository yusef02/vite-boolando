```css
/* RESET */

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: Arial, Helvetica, sans-serif;
}

/* debug */

/* * {
  border: 1px dashed black;
} */

/* GENERICS */

.container {
  width: 1080px;
  height: 100%;
  margin: 0 auto;
  padding: 0 20px;
}

.wrapper {
  font-size: 0;
}

.w-100 {
  width: 100%;
}

.small {
  font-size: 0.8rem;
}

/* HEADER */

.hdrpage {
  padding: 10px 0;
  color: white;
  background-color: #ff6900;
  /* posizionamento fisso del header */
  position: sticky;
  top: 0;
  z-index: 1;
  /* debug */
  /* height: 100px; */
}

.hdrpage .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.hdrpage .hdr--nav > ul {
  list-style: none;
}

.hdrpage .hdr--nav li {
  display: inline-block;
  padding: 5px;
  margin: 5px;
}

.hdrpage .hdr--nav a {
  color: white;
  text-decoration: none;
}

.hdrpage .logo {
  width: 150px;
}

.hdrpage .hdr--links * {
  display: inline-block;
  margin: 5px;
}

/* MAIN */

main {
  padding: 40px 0;
}

main .container {
  display: flex;
  flex-wrap: wrap;
}

main .container .article {
  width: calc(100% / 3 - 20px);
  margin: 10px;
  /* debug */
  /* min-height: 400px;
  background-color: bisque; */
}

.article {
  position: relative;
}

/* sezione etichette e sconti */
/* ho preso l'iniziativa di creare delle classi per sconti o spciali creando il contenuto qua sul css e affisarli sul div, anziche aggiungere degli span a qust ultimo. sono conscio che questo è il modo più errato per fare un esperimento del genere dato si può manipolare il contenuto in js */

.sale-30::before {
  content: "30%";
  color: white;
  background-color: red;
  padding: 2px 5px;
  margin-right: 3px;
}

.sale-50::before {
  content: "50%";
  color: white;
  background-color: red;
  padding: 2px 5px;
  margin-right: 3px;
}

.sostenibile::after {
  content: "sostenibilità";
  color: white;
  background-color: green;
  padding: 2px 5px;
}

.article .tagged {
  position: absolute;
  top: 80%;
}

/* bottone mi piace */
.article .article--like-btn {
  display: inline-block;
  width: 3rem;
  height: 3rem;
  font-size: 1.5rem;
  line-height: 3rem;
  text-align: center;
  vertical-align: middle;
  background-color: lightgrey;
  position: absolute;
  top: 10px;
  right: 10px;
}

/* descrizione articolo */
.article .article--desc span {
  display: inline-block;
  margin-right: 0.5rem;
}

.article .article--desc .current-price {
  color: red;
}

.article .article--desc .previous-price {
  color: rgb(68, 68, 68);
  text-decoration: line-through;
}

/* FOOTER */

.ftrpage {
  /* debug */
  background-color: #1a1a1a;
  height: 100px;
  color: white;
}

.ftrpage .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: white;
}

/* footer infos */
h1 {
  font-size: 1.2rem;
}

.ftrpage .ftr--info a {
  display: inline-block;
  color: white;
  text-decoration: none;
  margin-right: 5px;
}

/* footer socials */
.ftrpage .ftr--socials i {
  display: inline-block;
  padding: 3px;
}

/* BONUS */
/* aggiungo qui in fondo l'effeto hover dagli articolo che cambiano immagine */
.article img[src$="b.webp"] {
  display: none;
}
.article:hover img:first-of-type {
  display: none;
}
.article:hover img:last-of-type {
  display: inline-block;
}
/* ho inserito le imagini a seguire delle prime nel html e settato il display a none, quando poi si fa hover sull'articolo si toglie la prima con un display non e con un altro selettore far ricomparire l'altra */
```
