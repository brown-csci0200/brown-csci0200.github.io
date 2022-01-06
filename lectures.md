---
layout: default
title: Lectures
permalink: /lectures/
---

# {{ page.title }}

This is a test for using yaml to specify lecture content. This page is generated using a loop in the Liquid language used by Jekyll. It reads from the file in `_tables/lectures_table.md`.

Behind the scenes, the configuration automatically applies the "generated_table" layout (`_layouts/generated_table`) to any file in the `_tables` collection. A helper function in `table_helper.html` finds and displays the correct table on any site.

{% include table_helper.html name="lectures_table" %}