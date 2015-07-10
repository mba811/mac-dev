### 配置

Sublime Text 并不提供专门的配置界面，而是通过 JSON 文件来放置各种配置信息。而每种配置信息都分为 `Default` 和 `User` 两个版本，即 `Default` 为默认配置，因此不建议直接修改`Default` 配置文件，而是在 `User` 文件中放置自己的个性化配置。

比如我的部分配置：

~~~
{
    "color_scheme": "Packages/Theme - Spacegray/base16-ocean.dark.tmTheme",
    "enable_tab_scrolling": false,
    "ignored_packages":
    [
        "RestructuredText",
        "Markdown",
        "Vintage"
    ],
    "spacegray_sidebar_font_large": true,
    "spacegray_sidebar_font_normal": true,
    "spacegray_sidebar_font_small": true,
    "spacegray_sidebar_font_xlarge": true,
    "spacegray_sidebar_tree_large": true,
    "spacegray_sidebar_tree_normal": true,
    "spacegray_sidebar_tree_small": true,
    "spacegray_sidebar_tree_xlarge": true,
    "spacegray_sidebar_tree_xsmall": true,
    "spacegray_tabs_auto_width": true,
    "spacegray_tabs_font_large": true,
    "spacegray_tabs_font_normal": true,
    "spacegray_tabs_font_small": true,
    "spacegray_tabs_font_xlarge": true,
    "spacegray_tabs_large": true,
    "spacegray_tabs_normal": true,
    "spacegray_tabs_small": true,
    "spacegray_tabs_xlarge": true,
    "theme": "Spacegray.sublime-theme"
}
~~~
