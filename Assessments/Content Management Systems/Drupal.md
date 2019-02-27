# Drupal

Evaluated Drupal 8 WxT variant

| Guideline                                                    | Assessment against guideline       | Met |
|--------------------------------------------------------------|---|---------------------------------|
|**Open Standard**|||
|• Code base is available for re-use in a common code repository under an open licence | Codebase for Drupal 8 Core is [licensed GPL2](https://www.drupal.org/about/licensing). All contrib modules are also licensed similarly. | Y  |
|• Content is easy to migrate to another platform | Many methods to migrate data including using contributed (contib) modules [Views data export](https://www.drupal.org/project/views_data_export). Full access to Database is also possible. Custom exporters can also be written against the [Database API](https://www.drupal.org/docs/8/api/database-api) or [RESTful Web Services API](https://www.drupal.org/docs/8/api/restful-web-services-api). Lots of tools have been written to migrate to standard competitors including [WordPress](https://wordpress.org/plugins/fg-drupal-to-wp/) | Y |
|• Content is easy to migrate from another platform | Using [migrate](https://www.drupal.org/docs/8/api/migrate-api/migrate-api-overview) (core), [migrate_plus](https://www.drupal.org/project/migrate_plus) and [migrate_tools](https://www.drupal.org/project/migrate_tools) contrib modules | Y |
|• Code is freely available | All code is available to download and view view [git source control](https://www.drupal.org/project/drupal/git-instructions). Dependency resolution can also be resolved via [composer](https://www.drupal.org/docs/develop/using-composer). | Y |
|**Strong and Robust Community**| ||
|• Community is active and diverse| Drupal is one of the most active open source projects of all time and is extremely diverse and [committed to diversity](https://www.drupaldiversity.com/) For [example](https://dri.es/who-sponsors-drupal-development-2018), "In the 12-month period between July 1, 2017 and June 30, 2018, 7,287 different individuals and 1,002 different organizations contributed code to Drupal.org" including employees from the Government of Canada through Drupal WxtT. | Y |
|• Community is present in more than one region| "When measuring geographic diversity, we saw individual contributors from 6 different continents and 123 different countries" [link](https://dri.es/who-sponsors-drupal-development-2018) | Y |
|• There is a governance model present for how changes are made| Drupal Core: https://www.drupal.org/governance<br />Drupal WxT stack:<br />• [Lightning](https://www.drupal.org/project/lightning): Light governance via [issue queue](https://www.drupal.org/project/issues/lightning) and decisions done by [corporate sponsor Acquia](https://lightning.acquia.com/)<br />• Drupal [Bootstrap](https://www.drupal.org/project/bootstrap/) module: Light governance via issue queue and its maintainer team. Inherits efforts also from the [Government of Canada's wet-boew](https://wet-boew.github.io/wet-boew/index-en.html) and [Bootstrap](https://getbootstrap.com/docs/3.4/about/)<br />• WxT itself: Light governance via [various](https://github.com/drupalwxt/wxt/issues) [issue](https://www.drupal.org/project/issues/search/wxt) queues and decisions done by sponsor and Drupal centre of excellence Statistics Canada. Currently runs TBS' https://open.canada.ca/en wesbite<br /><br />Note: See also Drupal 7 distribution https://www.drupal.org/project/wetkit which is more mature and has [more use](https://www.drupal.org/project/usage/wetkit) (we are early on with the Drupal 8 migration push) | Y |
|• Technical roadmap is publicly available| Drupal Core: https://www.drupal.org/core/roadmap | Y |
|**Customizable**| | |
|• Ability to serve multiple use cases| Multiple ways of using Drupal including:<br />• Traditional Drupal: [case study](https://www.lullabot.com/articles/announcing-new-lullabotcom)<br />• Decoupled Drupal: [analysis of state of art in 2019](https://dri.es/how-to-decouple-drupal-in-2019)<br /> | Y |
|• Tool is adaptable and compatible with existing and custom extensions| Tens of thousands of modules have been made (and also licesned as per GPL2) as seen [here](https://www.drupal.org/project/project_module).<br />Thousands of themes have been made as seen [here](https://www.drupal.org/project/project_theme).<br />A government of Canada theme implementation has been made for [Drupal 7](https://www.drupal.org/project/wetkit_bootstrap) and  [Drupal 8](https://www.drupal.org/project/wxt_bootstrap)  including for the new [GCWeb](https://wet-boew.github.io/themes-dist/GCWeb/gcweb-theme/index.html) v5 spec; see work-in-progress branch for [D8](https://github.com/drupalwxt/wxt_bootstrap/tree/feat-gcweb-spec-v1.5). | Y |
|**Usability**|  | |
|• Has capacity to meet [Government of Canada Standard on Web Usability](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=24227)| Due to implementation of [wet-boew](https://github.com/wet-boew/wet-boew), the Drupal WxT meets the standard as wet-boew is compliant. | Y |
|• Has capacity to meet [Government of Canada Standard on Web Usability](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=24227)| Due to implementation of [wet-boew](https://github.com/wet-boew/wet-boew), the Drupal WxT meets the standard as wet-boew is compliant. | Y |
|**Accessibility**| | |
|• Has capacity to meet [Government of Canada Standard on Web Accessibility](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=23601)| Due to implementation of [wet-boew](https://github.com/wet-boew/wet-boew), the Drupal WxT meets the standard as wet-boew is compliant. | Y |
|**Interoperability**| | Y |
|• Meets [Government of Canada Web Interoperability Standards](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=25875)| Due to implementation of [wet-boew](https://github.com/wet-boew/wet-boew), the Drupal WxT meets the standard as wet-boew is compliant. | |
|**Multilingual**| | |
|• Has capacity to meet [Directive on the Implementation of the Official Languages (Communications with and Services to the Public) Regulations](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=26163)| Support multilingual out of the box with [4 core modules](https://www.acquia.com/blog/managing-multilingual-sites-drupal-8). Drupal WxT has even been used to support languages other than left-right such as inuitiktut | |
|| | |
|**Compatibility**| | |
|• Code base is compatible with security tools| | |
|• Code base is compatible with analytics tools| | |
|• Code base is compatible with search engines| | |
|**Content and style**| | |
|• Must be built on the [HTML5 framework](https://www.w3.org/TR/html5/)| | |
|• Must be built using [Cascading Style Sheets](https://www.w3.org/Style/CSS/Overview.en.html)| | |
|**Ease of use**| | |
|• Language and existing code base and extensions are easy to use| | |
