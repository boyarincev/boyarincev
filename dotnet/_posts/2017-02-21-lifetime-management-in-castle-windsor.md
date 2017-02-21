---
layout: post
title: Управление жизненным циклом объектов в Castle Windsor
tags: castle-windsor
published: false
---

Возможно, наиболее непонимаемая вещь в Castle Windsor - это его система управления жизненным циклом объектов.

# Почему Castle Windsor хранит ссылки на созданные им объекты?

Одна из ключевых обязанностей IoC-контейнера - это управление жизненным циклом, создаваемых им объектов. Контейнер создает объект, 
настраивает его и отдаем его вам, так что вы можете использовать его, а когда он становится больше не нужен - уничтожает его.
Для того, чтобы определить какие объекты он должен уничтожить, когда приходит их время и получить к ним доступ, 
хранятся ссылки на все создаваемые объекты.

# Уничтожение объектов
