---
layout: default
title: Bienvenido a Mi Tienda
---

<section class="portada">
  <div class="overlay"></div>
  <img src="/img/portada.jpg" alt="Imagen de portada" class="portada-img" />
  <div class="portada-texto">
    <h1>Bienvenido a Mi Tienda</h1>
    <p>Encuentra los mejores productos seleccionados para ti.</p>
    <a href="/tienda" class="btn-explorar">Explorar productos</a>
    <link rel="stylesheet" href="/css/style.css" />
  </div>
</section>

<section class="productos-destacados">
  <h2>Explora nuestros productos</h2>
  <ul class="product-list">
    {% for post in site.posts %}
      <li class="product-item">
        <a href="{{ post.url }}">
          <img src="{{ post.image }}" alt="{{ post.title }}" />
          <h3>{{ post.title }}</h3>
        </a>
        <p class="price">Precio: ${{ post.price }}</p>
        <p>{{ post.excerpt }}</p>
      </li>
    {% endfor %}
  </ul>
</section>






