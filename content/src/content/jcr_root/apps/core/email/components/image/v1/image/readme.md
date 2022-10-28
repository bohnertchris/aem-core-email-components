<!--
Copyright 2021 Adobe

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->
# Image Component
Extensible image component for the Core Email Components for composing campaign content written in HTL and based on the [Image Core Component](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/image/v3/image)

## Features
* Linkable to content pages, external URLs or page anchors
* Allows an icon identifier to be configured for rendering an icon
* Personalization fields from Adobe Campaign
* Ability to define image width

## Technical Details

This component inherits its structure and behavior from the [Image (v3) component of the `core.wcm.component` package.](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/image/v3/image)

The changes are:

* Addition of the numeric field **Fixed width (px)** on the **Metadata** tab of the edit dialog, which defines the width (in pixels) of the image
* Addition of the checkbox **Scale image to available width** on the **Metadata** tab of the edit dialog, which forces the image to be displayed in full screen mode
* Addition of the numeric field **Default width (px)** in the edit template dialog, which defines the default value for **Fixed width (px)** field when no value is present
* The image URL in the `src` HTML attribute is now absolute (see [UrlMapperService](https://github.com/adobe/aem-core-email-components/wiki/UrlMapperService:-Technical-documentation) for details)

## Best Practices for Email Image Sizes

According to [statcounter,](https://gs.statcounter.com/screen-resolution-stats#monthly-202201-202203) the most common resolutions (across all platforms) between January and March 2022 are 1920x1080 (9.04% to 9.43%) and 1366x768 (7.35% to 7.57%). Therefore the default width of the Image component is 1280.

## Tests and Coverage

The `ImageIT` class is the Selenium test class. It verifies that the image renders correctly when a fixed width is selected and when the scale is set to full size. In both cases, it checks that the `src` HTML attribute of the image contains an absolute URL.

## Information
* **Vendor**: Adobe
* **Version**: v1
* **Compatibility**: AEM 6.5
* **Status**: production-ready
* **User Documentation**: [https://www.adobe.com/go/aem_cmp_email_button_v1](https://www.adobe.com/go/aem_cmp_email_button_v1)
* **Authors**: 