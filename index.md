---
layout: default
title: Bienvenido a Mi Tienda
---
<section class="portada">
  <div class="overlay"></div>
  <img src="{{ site.baseurl }}/img/portada.jpg" alt="Imagen de portada" class="portada-img" />
  <div class="portada-texto">
    <h1>Bienvenido a Mi Tienda</h1>
    <p>Encuentra los mejores productos seleccionados para ti.</p>
    <a href="{{ site.baseurl }}/tienda" class="btn-explorar">Explorar productos</a>
  </div>
</section>
<section class="productos-destacados">
  <h2>Explora nuestros productos</h2>
  <ul class="product-list">
    {% for post in site.posts %}
      <li class="product-item">
        <a href="{{ site.baseurl }}{{ post.url }}">
          <img src="{{ site.baseurl }}{{ post.image }}" alt="{{ post.title }}" />
          <h3>{{ post.title }}</h3>
        </a>
        <p class="price">Precio: ${{ post.price }}</p>
        <p>{{ post.excerpt }}</p>
      </li>
    {% endfor %}
  </ul>
</section>
