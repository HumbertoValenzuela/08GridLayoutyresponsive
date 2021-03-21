# 08GridLayoutyresponsive
*08 grid layout responsive gap grid-template-areas grid-template-column

```javascript
 .contenedor {
     display: grid;
     margin: 0 auto;
     max-width: 900px;
     background-color: azure;
     height: 100vh;
     grid-template-areas: 
     "header" 
     "navegacion" 
     "izquierda" 
     "principal" 
     "derecha"
     "footer";
     grid-template-columns: 1fr;     
     gap: 1rem;     
 }

 /* Selecciona todos los elementos que contiene contenedor */
 .contenedor > * {
     padding: 2rem;
     font-size: 1.4rem;
 }

 .header {
     background-color: blueviolet;
     grid-area: header;
 }

 .navegacion {
     background-color: brown; 
     grid-area: navegacion;    
 }
 .izquierda {
     background-color: chartreuse;
     grid-area: izquierda;
 }
 .derecha{
     background-color: cornflowerblue;
     grid-area: derecha;
 }
 .contenido-principal {
     background-color: darkgreen;
     grid-area: principal;
 }
 .footer {
     background-color: darkorange;
     grid-area: footer;
 }

 @media screen and (min-width:768px) {
     .contenedor {
         grid-template-areas: 
         "header header header header"
         "izquierda navegacion navegacion navegacion"
         "izquierda principal principal derecha"
         "izquierda principal principal derecha"
         "footer footer footer derecha";
         grid-template-columns: repeat(4, 1fr);
         grid-template-rows: 4rem 4rem auto auto 4rem;
         gap: 1rem;
     }
 }
```
