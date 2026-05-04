```
/*------------------------------------------------------------------------------

                     Daily Note Themes by CyanVoxel v1.0.5

  

These are a set of 7 main CSS classes that can be used to apply individual color

schemes to daily notes for each day of the week.

To customize the colors for each day, just swamp out the colors values under

the main "day of the week" classes.

  

NOTE: By default, this snippet relies on the "Bai Jamjuree" or

"JetBrainsMono Nerd Font Mono" fonts. If you don't wish to use these, then just

change or remove those font-family lines from this snippet.

------------------------------------------------------------------------------*/

:root {

  --highlight: #ffffff;

  --primary: #aaaaaa;

  --dark: #333333;

}

  

/* 柔和的默认配色 */

.daily {

  --dark: #4a4a4a;

  color: var(--highlight);

  background-color: var(--dark);

  --text-normal: var(--highlight);

  --text-muted: var(--highlight);

  --text-faint: var(--highlight);

  --checklist-done-color: var(--highlight);

  --metadata-label-text-color: var(--highlight);

  --metadata-input-text-color: var(--highlight);

  --tag-color: var(--dark);

  --tag-background: var(--primary);

  --hr-color: var(--primary);

  --blockquote-border-color: var(--primary);

  --interactive-accent: var(--primary);

  --collapse-icon-color-collapsed: var(--primary);

  --checkbox-color: var(--primary);

  --checkbox-marker-color: var(--dark);

  --checkbox-color-hover: var(--highlight);

  --checkbox-border-color: var(--highlight);

  --list-marker-color: var(--highlight);

  --code-background: black;

  --code-normal: var(--primary);

  

  --background-modifier-border-focus: var(--primary);

  --background-modifier-border: color-mix(in srgb, var(--highlight) 60%, transparent);

  --background-modifier-hover: color-mix(in srgb, var(--highlight) 60%, transparent);

  --pill-cover-hover: color-mix(in srgb, var(--highlight) 60%, transparent);

}

  

.daily {

  --dark: var(--dark);

  color: var(--highlight);

  background-color: var(--dark);

  --text-normal: var(--highlight);

  --text-muted: var(--highlight);

  --text-faint: var(--highlight);

  --checklist-done-color: var(--highlight);

  --metadata-label-text-color: var(--highlight);

  --metadata-input-text-color: var(--highlight);

  --tag-color: var(--dark);

  --tag-background: var(--primary);

  --hr-color: var(--primary);

  --blockquote-border-color: var(--primary);

  --interactive-accent: var(--primary);

  --collapse-icon-color-collapsed: var(--primary);

  --checkbox-color: var(--primary);

  --checkbox-marker-color: var(--dark);

  --checkbox-color-hover: var(--highlight);

  --checkbox-border-color: var(--highlight);

  --list-marker-color: var(--highlight);

  --code-background: black;

  --code-normal: var(--primary);

  

  --background-modifier-border-focus: var(--primary);

  --background-modifier-border: color-mix(in srgb, var(--highlight) 60%, transparent);

  --background-modifier-hover: color-mix(in srgb, var(--highlight) 60%, transparent);

  --pill-cover-hover: color-mix(in srgb, var(--highlight) 60%, transparent);

}

  

.sunday,

.Sunday,

.星期日,

.周日 {

  --highlight: #f8c5d1;

  --primary: #e89db8;

  --dark: #7a3d52;

}

  

.monday,

.Monday,

.星期一,

.周一 {

  --highlight: #f8c5d1;

  --primary: #e89898;

  --dark: #7a3d42;

}

  

.tuesday,

.Tuesday,

.星期二,

.周二 {

  --highlight: #c5e1f8;

  --primary: #87b8e8;

  --dark: #3d527a;

}

  

.wednesday,

.Wednesday,

.星期三,

.周三 {

  --highlight: #fff8c5;

  --primary: #e8d087;

  --dark: #7a6b3d;

}

  

.thursday,

.Thursday,

.星期四,

.周四 {

  --highlight: #f8d1c5;

  --primary: #e89870;

  --dark: #7a523d;

}

  

.friday,

.Friday,

.星期五,

.周五 {

  --highlight: #f0c7d3;

  --primary: #dc9fb3;

  --dark: #6b3a4d;

}

  

.saturday,

.Saturday,

.星期六,

.周六 {

  --highlight: #f39caa;

  --primary: #e22c3c;

  --dark: #100305;

}

  

.daily :is(h1, .HyperMD-header.HyperMD-header-1) {

  color: var(--primary);

  text-align: center;

  font-size: 60px;

  font-family: "Bai Jamjuree", "JetBrainsMono Nerd Font Mono", "JetBrains Mono";

  padding: 0 !important;

}

  

.daily :is(h2, .HyperMD-header.HyperMD-header-2) {

  color: var(--highlight);

  text-align: center;

  font-size: 30px;

  font-family: "Bai Jamjuree", "JetBrainsMono Nerd Font Mono", "JetBrains Mono";

  font-style: italic;

  padding: 0 !important;

}

  

.daily :is(h3, .HyperMD-header.HyperMD-header-3) {

  color: var(--primary);

  text-align: center;

  

  font-size: 32px;

  font-family: "Bai Jamjuree", "JetBrainsMono Nerd Font Mono", "JetBrains Mono";

  padding-top: 0;

}

  

.daily :is(h4, .HyperMD-header.HyperMD-header-4) {

  background-color: var(--primary);

  color: var(--dark);

  /* border-color: var(--primary); */

  /* font-family: "JetBrainsMono Nerd Font Mono", "JetBrains Mono", monospace; */

  font-weight: 900;

  margin-bottom: 0;

  padding-top: 0;

  font-size: 20px;

  width: fit-content;

  padding-left: 6px;

  padding-right: 6px;

  /* border: solid; */

  border-radius: 8px;

  /* border-width: 2px; */

  word-wrap: normal;

}

  

.daily :is(h5, .HyperMD-header.HyperMD-header-5) {

  color: var(--primary);

  text-align: center;

  margin-bottom: 0;

  padding-top: 0;

}

  

.daily p {

  margin-top: 4px;

  margin-bottom: 4px;

}

  

.daily :is(a:link, .cm-hmd-internal-link) {

  color: var(--primary);

}

  

.daily :is(a:hover, .cm-hmd-internal-link:hover) {

  color: var(--highlight);

}

  

.daily hr {

  margin-top: 20px !important;

  margin-bottom: 20px !important;

}

  

.daily img {

  display: block !important;

  margin-left: auto !important;

  margin-right: auto !important;

}

  

:is(.sunday, .Sunday,

  .monday, .Monday,

  .tuesday, .Tuesday,

  .wednesday, .Wednesday,

  .thursday, .Thursday,

  .friday, .Friday,

  .saturday, .Saturday) svg {

  color: color-mix(in srgb, var(--highlight) 60%, transparent);

}
```