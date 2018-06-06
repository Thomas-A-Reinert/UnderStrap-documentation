---
layout: docs
title: WordPress Menus
description: UnderStrap supports only a primary menu with two levels, means just a single submenu level.
group: getting-started
toc: false
---

## Adding Icons to the Menu

If you want to prepend an icon to any of your menu items, you can use any of [FontAwesome 4.7]({{ site.baseurl }}/docs/{{ site.docs_version }}/extend/fontawesome-4/)´s icons that come along with UnderStrap. To get an overview of all FontAwesome icons that ship with UnderStrap have a look at their [675 icons](https://fontawesome.com/v4.7.0/icons/){:target="_blank"}.

<figure class="mb-5">
  <img src="{{ site.baseurl }}/assets/img/menu-icons-with-text.jpg" alt="" class="img-fluid">
</figure>

As you can see in the image above you can add custom classes (e.g. `fa fa-home`) to any menu item.{ .mb-5}

{% capture callout %}
You cannot see a `CSS Classes (optional)` field?

Check the upper right corner of that page and click `Screen Options` - toggle `CSS` on and your good to go.
{% endcapture %}
{% include callout.html content=callout type="warning" %}

## Adding Social Media Icons and hiding the text from non visually impaired users

If you want to add social media icons for example but respect [WCAG 2.0 guidelines](https://www.w3.org/TR/WCAG20/){:target="_blank"} you´ll need to provide some assistive text for visually impaired users. But most problably you´ll not want to show it to non visually impaired users.

<figure class="mb-5">
  <img src="{{ site.baseurl }}/assets/img/menu-icons-without-text.jpg" alt="" class="img-fluid">
</figure>

This will render the following HTML:
{%- highlight html -%}
<li itemscope="itemscope" itemtype="https://www.schema.org/SiteNavigationElement" id="menu-item-1713" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-1713 nav-item">
  <a title="Visit us on Github" href="https://github.com/understrap" class="nav-link">
    <i class="fa fa-github" aria-hidden="true"></i>
    <span class="sr-only">Visit us on Github</span>
  </a>
</li>
{%- endhighlight -%}

As you can see the icon will get automatically hidden for visually impaired users by the `aria-hidden="true"` attribute while the text will get wrapped by a `<span class="sr-only">` which will only be "shown" to screenreaders.

## Adding more Menus

If you want to add more menus please see [Extend &raquo; Custom Menus and Menu Areas]({{ site.baseurl }}/docs/{{ site.docs_version }}/extend/custom-menus-and-menu-areas/).
