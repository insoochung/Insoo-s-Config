Created: `$= dv.current().file.ctime`
Last modified: `$= dv.current().file.mtime`

Status: #mature 

Tags: [[habits]] 

## Wellness

```dataviewjs
dv.span("**Exercise 🏋️**")

const calendarData = {
	colors: "green",
    defaultEntryIntensity: 0,
    intensityScaleStart: 0,
    intensityScaleEnd: 100,
	entries: []
}

for(let page of dv.pages('"0 - Daily Notes"').where(p=>p.exerciseMinutes)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.exerciseMinutes,
        content: await dv.span(`[](${page.file.name})`),
    })
       
}

renderHeatmapCalendar(this.container, calendarData)
```
```dataviewjs
dv.span("**Mood 😹**")

const calendarData = {
	colors: "green",
    defaultEntryIntensity: 5,
    intensityScaleStart: 0,
    intensityScaleEnd: 10,

	entries: []
}

for(let page of dv.pages('"0 - Daily Notes"').where(p=>p.mood)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.mood,
        content: await dv.span(`[](${page.file.name})`),
    })
       
}

renderHeatmapCalendar(this.container, calendarData)
```
---
## Studies

```dataviewjs
dv.span("**AIML 🤖 + Math 🎲**")

const calendarData = {
	colors: "blue",
    defaultEntryIntensity: 0,
    intensityScaleStart: 0,
    intensityScaleEnd: 100,
	entries: []
}

for(let page of dv.pages('"0 - Daily Notes"').where(p=>p.mathMinutes || p.aimlMinutes)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: (page.mathMinutes || 0) + (page.aimlMinutes || 0),
        content: await dv.span(`[](${page.file.name})`),
    })
       
}

renderHeatmapCalendar(this.container, calendarData)
```
```dataviewjs
dv.span("**Leetcode 💻 + System Design 🏗️**")

const calendarData = {
	colors: "blue",
    defaultEntryIntensity: 0,
    intensityScaleStart: 0,
    intensityScaleEnd: 100,
	entries: []
}

for(let page of dv.pages('"0 - Daily Notes"').where(p=>p.leetcodeMinutes || p.designMinutes)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: (page.leetcodeMinutes || 0) + (page.designMinutes || 0),
        content: await dv.span(`[](${page.file.name})`),
    })
       
}

renderHeatmapCalendar(this.container, calendarData)
```
---
## Literacy

```dataviewjs
dv.span("**Language 💬**")

const calendarData = {
	colors: "pink",
    defaultEntryIntensity: 0,
    intensityScaleStart: 0,
    intensityScaleEnd: 100,
	entries: []
}

for(let page of dv.pages('"0 - Daily Notes"').where(p=>p.languageMinutes)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.languageMinutes,
        content: await dv.span(`[](${page.file.name})`),
    })
       
}

renderHeatmapCalendar(this.container, calendarData)
```
```dataviewjs
dv.span("**Reading 📖**")

const calendarData = {
	colors: "pink",
    defaultEntryIntensity: 0,
    intensityScaleStart: 0,
    intensityScaleEnd: 100,
	entries: []
}

for(let page of dv.pages('"0 - Daily Notes"').where(p=>p.readingPages)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.readingPages,
        content: await dv.span(`[](${page.file.name})`),
    })
       
}

renderHeatmapCalendar(this.container, calendarData)
```
```dataviewjs
dv.span("**Writing ✍️**")

const calendarData = {
	colors: "pink",
    defaultEntryIntensity: 0,
    intensityScaleStart: 0,
    intensityScaleEnd: 500,
	entries: []
}

for(let page of dv.pages('"0 - Daily Notes"').where(p=>p.writingWords)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.writingWords,
        content: await dv.span(`[](${page.file.name})`),
    })
       
}

renderHeatmapCalendar(this.container, calendarData)
```
---
## Vice

```dataviewjs
  
dv.span("**Alcohol 🍺**")

const calendarData = {
    colors: "red",
    defaultEntryIntensity: 0,
    intensityScaleStart: 0,
    intensityScaleEnd: 6,
	entries: []
}

for(let page of dv.pages('"0 - Daily Notes"').where(p=>p.alcoholBeers)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.alcoholBeers,
        content: await dv.span(`[](${page.file.name})`),
    })
       
}

renderHeatmapCalendar(this.container, calendarData)

```