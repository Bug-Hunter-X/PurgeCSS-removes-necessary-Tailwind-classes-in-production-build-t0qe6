# PurgeCSS removes necessary Tailwind classes

This repository demonstrates an uncommon bug where PurgeCSS, used with Tailwind CSS, removes necessary CSS classes during the production build process. This leads to unexpected styling issues, particularly in responsive designs.

## Bug Description

The issue arises when PurgeCSS incorrectly identifies and removes classes that are crucial for specific responsive design elements. Even though these classes are present in the main CSS file and are referenced in components, PurgeCSS still eliminates them.

## Reproduction

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm run build` to build the project.
4. Observe the missing styles in the production build.

## Solution

The provided solution implements a workaround to prevent PurgeCSS from removing the necessary classes. The strategy involves explicitly listing the affected classes in the PurgeCSS configuration or using a more lenient PurgeCSS configuration. 
