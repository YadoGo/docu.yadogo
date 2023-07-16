---
sidebar_label: 'Arquitectura'
sidebar_position: 2
---

# Arquitectura de una Aplicación Frontend en Angular
Angular utiliza una arquitectura basada en componentes y un patrón de diseño llamado Model-View-Controller (MVC) o Model-View-ViewModel (MVVM) para organizar y gestionar la estructura de la aplicación. La arquitectura de una aplicación Angular típica consta de los siguientes elementos:

## Módulos
Los módulos son bloques de construcción fundamentales en una aplicación Angular. Representan una funcionalidad o característica específica y agrupan componentes, servicios y otros elementos relacionados. Cada aplicación Angular tiene al menos un módulo raíz, conocido como el módulo principal (app.module.ts), que importa otros módulos y define los componentes principales de la aplicación.

## Componentes
Los componentes son unidades independientes y reutilizables que manejan la lógica de presentación y la interacción con el usuario. Cada componente está formado por una plantilla HTML que define la vista y una clase TypeScript que contiene la lógica y los datos del componente. Los componentes se pueden anidar y se comunican entre sí mediante propiedades de entrada y eventos de salida.

## Plantillas HTML
Las plantillas HTML definen la estructura y el contenido visual de los componentes. Utilizan directivas de Angular para controlar el flujo de la aplicación y para interactuar con el modelo de datos.

## Servicios
Los servicios son clases que contienen lógica compartida y datos que pueden ser utilizados por varios componentes. Estos servicios proporcionan funcionalidades como obtener datos de un servidor, manejar la lógica de negocios y gestionar el estado de la aplicación.

## Directivas
Las directivas son instrucciones en el DOM que extienden el comportamiento de los elementos HTML. Angular ofrece directivas incorporadas, como ngIf, ngFor y ngStyle, y también permite crear directivas personalizadas para extender la funcionalidad de los elementos HTML.

## Enrutamiento
El enrutamiento en Angular permite navegar entre diferentes vistas y componentes en una aplicación de página única (SPA). Utiliza un enrutador que mapea URL a componentes específicos y permite la navegación mediante enlaces y redireccionamientos.

## Inyección de Dependencias
Angular utiliza el patrón de inyección de dependencias para proporcionar instancias de clases necesarias a otros componentes o servicios. Esto facilita la creación y gestión de instancias y ayuda a mantener la modularidad y la reutilización de código.

## Data Binding
Angular ofrece una variedad de formas de enlazar datos entre la vista y el modelo de datos. El data binding bidireccional permite que los cambios en la vista se reflejen automáticamente en el modelo y viceversa.

En resumen, la arquitectura de una aplicación frontend en Angular se basa en componentes reutilizables, enrutamiento para la navegación, inyección de dependencias para la gestión de objetos y servicios para compartir la lógica común. Estos conceptos trabajan juntos para crear aplicaciones web eficientes y mantenibles.




