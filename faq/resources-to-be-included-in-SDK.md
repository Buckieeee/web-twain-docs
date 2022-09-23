---
layout: default-layout
noTitleIndex: true
needAutoGenerateSidebar: true
title: What resources of the SDK should be included in my web application?
keywords: Dynamic Web TWAIN, Project Deployment and End-user Installation, resources
breadcrumbText: What resources of the SDK should be included in my web application?
description: What resources of the SDK should be included in my web application?
permalink: /faq/resources-to-be-included-in-SDK.html
---

# Project Deployment and End-user Installation

## What resources of the SDK should be included in my web application?

You can include all the files under the Resources folder, but not all are required.

Under the `\addon` folder, you do not need the files for add-ons which are not used by your web application.

Under the `\dist` folder, you can include the installers required per your OS requirements.

Under the `\src` folder, you do not need the wasm files if you are not using camera functionalities.

For more information, please check <a href="{{site.faq}}what-are-the-resources-files.html" target="_blank">What are the Resources files</a> and <a href="{{site.indepth}}features/initialize.html#loading-the-core-js-files" target="_blank">Loading the Resource Files</a>.
