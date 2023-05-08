<!-- markdownlint-disable MD033 MD041 -->

<div align="center">
  <a href="https://plotly.com/graphing-libraries/">
    <picture>
      <source width="400px" media="(prefers-color-scheme: light)"
        srcset="assets/plotly_logo/plotly_logo_light_mode.png">
      <source width="400px" media="(prefers-color-scheme: dark)"
        srcset="assets/plotly_logo/plotly_logo_dark_mode.png">
      <img width="400px" alt="Shows Plotly logo in light mode"
        src="https://raw.githubusercontent.com/congineer/plotly-export-and-quick-edit-techdemo/master/assets/plotly_logo/plotly_logo_light_mode.png"
      >
    </picture>
  </a>
</div>

<h1 align="center">TECH DEMO</h1>

# Advanced [Plotly.js](https://plotly.com/javascript/) in-plot State Hydration <br> for custom ModeBar Button Modes

- Multi Export to Vector SVG, PDF, and Alpha Channel WEBP, PNG;
- Quick Edit of Title, Axes, Ranges, Legend position and Legend items;
- Modes-aware Light Mode Toggle;

---

## Licensing

- Code (scripts and compiled code) under [MIT](LICENSE) license.
- Plotly brand assets (icons, logos) under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license. Copyright by [Plotly, Inc.](https://plotly.com)
- Brand assets (icons, logos) under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license. Copyright by [CONGINEER Ltd.](https://congineer.com)
- Media assets (video, audio, graphics, animations) under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license. Copyright by [CONGINEER Ltd.](https://congineer.com)

---

## Context

The below demonstrated functionality is a recent development effort towards the CemGEMS application release v0.8.0 [cemgems.app](https://cemgems.app)

The goals of the v0.8.0 release are set to be an implementation of:

- a maximum achievable responsiveness of data input tables and interactive charts/plots;
- a statefull "quick" and/or "full" editability of interactive charts/plots.

All charts have been rewritten from pure [D3.js](https://github.com/d3/d3) and/or [DC.js](https://github.com/dc-js/dc.js) to [Plotly.js](https://github.com/plotly/plotly.js/).

A framework-agnostic state hydration architecture has been experimented on, found, and implemented for the custom functionality Plotly ModeBar buttons.

---

### Plotly Alpha Export Tidbits

    - PNG and WEBP Export is always transparent, i.e. has no background
    - Light Mode Export transparency is achieved via white background outside of Plotly graph div

![Plotly Alpha Export Techdemo](assets/plotly_export_to_alpha/Plotly_demo_alpha_export_Recording_2023-05-08_at_19.04.40.gif)

Lookup exports:

- [Light mode PNG](assets/plotly_export_to_alpha/CemGEMS_PlotView_CEM-IV-A_min_4a_Hydration-MPK_Time-log_tlog__default_Time-log_Aqueous-totals_CompositeLines_lightMode_1938x1400px.png)
- [Dark mode WEBP](assets/plotly_export_to_alpha/CemGEMS_PlotView_CEM-IV-A_min_4a_Hydration-MPK_Time-log_tlog__default_Time-log_Aqueous-totals_CompositeLines_darkMode_1938x1400px.webp)

---

### Plotly Vector Export Tidbits

    - SVG Export is always transparent, i.e. has no background
    - PDF Export in dark mode is set to pick the app background (no background in light mode)
    - Export and Light Modes are set to persist on any layout or data change, e.g. axis, chart type, etc.

![Plotly Vector Export Techdemo](assets/plotly_export_to_vector/Plotly_demo_vector_export_Recording_2023-05-06_at_17.36.49.gif)

Lookup exports:

- [Light mode SVG](assets/plotly_export_to_vector/CemGEMS_PlotView_CEM-IV-A_min_4a_Ingress_Add-Salts_carbonation__default_Lead-linear_Masses_StackedAreas_lightMode_1938x1400px.svg)
- [Dark mode PDF](assets/plotly_export_to_vector/CemGEMS_PlotView_CEM-IV-A_min_4a_Ingress_Add-Salts_carbonation__default_Lead-linear_Masses_StackedAreas_darkMode_678x490px.pdf)
- [More area SVG](assets/plotly_export_to_vector/_more_of_light_mode/CemGEMS_PlotView_CEM-IV-A_min_4a_Leaching_Add-Water_lwater__default_Lead-linear_Aqueous-totals_CompositeLines_lightMode_1938x1400px.svg)
- [Legend in place SVG](assets/plotly_export_to_vector/_more_of_light_mode/CemGEMS_PlotView_CEM-IV-A_min_4a_Hydration-MPK_Time-log_tlog__default_Time-log_Volumes_StackedAreas_lightMode_1950x1400px.svg)

---

### Plotly Quick Edit Tidbits

    - Quick Edit Mode light/dark theme is aware of Light Mode switch
    - Quick Edit Mode is set to auto-deactivate on any significant change, e.g. axis, chart type, etc.

![Plotly Quick Edit Techdemo](assets/plotly_quick_edit/Plotly_demo_quick_edit_Recording_2023-05-08_at_19.22.55.gif)

Lookup exports:

- [Light mode PDF](assets/plotly_quick_edit/CemGEMS_PlotView_CEM-IV-A_min_4a_Leaching_Add-Water_lwater__default_Lead-log_Volumes_StackedAreas_lightMode_678x490px.pdf)
