SimplyEdit Attributes
=====================

Fields
------

data-simply-field
~~~~~~~~~~~~~~~~~

::

	<h1 data-simply-field="title">Title</h1>

Makes an HTML element editable in the browser in editmode. It also adds the 
contents to the data store. This means that you can change the contents of
the field in javascript simply by changing the javascript object, like this:

::

	editor.pageData.title.innerHTML = 'New Title';

This attribute can be set on any HTML element. Depending on which HTML element,
it will expect and set different properites:

- ``A``: href, title and innerHTML
- ``IMG``: src, alt and title
- ``INPUT``: value
- ...

Fields may not contain other fields, except when using ``data-simply-content="fixed"``.

Fields with the same name on the same page will always have the same content. Except when the
field is part of a list entry, or if you've specified a different path with ``data-simply-path``.

data-simply-content
~~~~~~~~~~~~~~~~~~~

::

	<a data-simply-field="link" data-simply-content="fixed">
		<img data-simply-field="image">
	</a>

Tells SimplyEdit what kind of content the field may contain. Expects one of
the following values:

- ``fixed``
  Only attributes on the element are editable. The innerHTML will not be set 
  or updated.

- ``attributes``
  Only make the attributes of the element editable. By default all attributes
  will be stored. You can override this with the ``data-simply-attributes`` attribute.

- ``template``
  The value of the field will be used to select a template. The template name
  must match the value of the field. If the field is not available in the data
  store yet, you can set a default value with the ``data-simply-default-value`` attribute.


data-simply-attributes
~~~~~~~~~~~~~~~~~~~~~~

::

	<button data-simply-field="product" data-simply-content="attributes"
		data-simply-attributes="data-item-id data-item-name data-item-price"
	>Buy Now</button>
	<div data-simply-field="product.data-item-id">1</div>
	<div data-simply-field="product.data-item-name">Name</div>
	<div data-simply-field="product.data-item-price">99</div>


data-simply-template
~~~~~~~~~~~~~~~~~~~~

::

	<input type="radio" name="size" value="small" data-simply-field="size">Small
	<input type="radio" name="size" value="large" data-simply-field="size">Large
	<div data-simply-field="size" data-simply-content="template">
		<template data-simply-template="small">
			Small size selected
		</template>
		<template data-simply-template="large">
			Large size selected
		</template>
	</div>



Lists
-----

data-simply-list
~~~~~~~~~~~~~~~~

data-simply-sortable
~~~~~~~~~~~~~~~~~~~~

data-simply-template
~~~~~~~~~~~~~~~~~~~~

data-simply-entry
~~~~~~~~~~~~~~~~~

data-simply-list-item
~~~~~~~~~~~~~~~~~~~~~

Misc
----

data-simply-path
~~~~~~~~~~~~~~~~

data-simply-selectable
~~~~~~~~~~~~~~~~~~~~~~

data-simply-hidden
~~~~~~~~~~~~~~~~~~

data-simply-edit
~~~~~~~~~~~~~~~~

data-simply-default-value
~~~~~~~~~~~~~~~~~~~~~~~~~

Script
------

data-api-key
~~~~~~~~~~~~

data-simply-settings
~~~~~~~~~~~~~~~~~~~~

data-simply-endpoint
~~~~~~~~~~~~~~~~~~~~

data-simply-images
~~~~~~~~~~~~~~~~~~

data-simply-files
~~~~~~~~~~~~~~~~~