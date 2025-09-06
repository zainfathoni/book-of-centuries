# Digital Book of Century - Charlotte Mason Method

## Project Overview

This project creates a digital version of a Book of Century based on the Charlotte Mason educational method. The Book of Century is a timeline tool where each two-page spread covers one hundred years, helping students visualize historical connections across time periods.

### Background
- **Source Project**: Adapted from [life tracking project](https://life.zainf.dev) by Zain Fathoni
- **Educational Method**: Based on Charlotte Mason's Book of Centuries approach
- **Reference**: [Simply Charlotte Mason - How to Do a Book of Centuries](https://simplycharlottemason.com/blog/how-to-do-a-book-of-centuries/)

### Project Requirements (User-Specified)
- **Time Period**: 1 AD - 2000 AD (20 centuries)
- **Categories**: World History (wars, political events)
- **Data Management**: Decap CMS for user-friendly editing interface
- **Viewing Modes**: Century view (100 years per screen), Timeline view, Printable century pages
- **Multi-Child Support**: Individual books for each child

## Technical Architecture

### Technology Stack
- **Frontend**: Pure HTML5, CSS3, Vanilla JavaScript (no frameworks)
- **Data Format**: Markdown files with JSON metadata
- **CMS**: Decap CMS for content management
- **Authentication**: Git Gateway with Netlify Identity
- **Styling**: CSS with Google Fonts (Open Sans)
- **Build**: Static site generation (no compilation required)

### Data Structure Design

#### Historical Event Schema
```markdown
- DATE_FORMAT **HISTORICAL_FIGURE/EVENT** description #worldhistory [child:name]
```

**Date Format Support:**
- `100` - Year only
- `01/100` - Month/Year  
- `01/01/100` - Day/Month/Year
- `100-200` - Date ranges
- `~150` - Approximate dates
- `100-~` - Ongoing events

**Enhanced Fields:**
- **Historical Figure/Event**: `**Julius Caesar**`, `**Battle of Hastings**`
- **Description**: Rich text with educational context
- **Category**: `#worldhistory`, `#wars`, `#politics`, `#rulers`
- **Child Assignment**: `[child:Najmi]`, `[child:Isa]`, `[family]`
- **Significance**: Historical importance level
- **Sources**: References and links

#### Century Organization
- **Century 1**: 1-100 AD
- **Century 2**: 101-200 AD
- **Century 3**: 201-300 AD
- ...
- **Century 20**: 1901-2000 AD

#### Multi-Child Data Structure
```
/data/
├── children/
│   ├── najmi.md
│   ├── isa.md
│   └── nada.md
├── centuries/
│   ├── century-01.md (1-100 AD)
│   ├── century-02.md (101-200 AD)
│   └── ...
└── shared/
    └── family-events.md
```

## Implementation Plan

### Phase 1: Project Setup and Data Structure ✅

#### 1.1 Initialize New Project Structure ✅
- [x] Create new project directory at `/Users/zain/Code/GitHub/zainfathoni/book-of-centuries`
- [x] Set up Git repository for version control
- [x] Copy and adapt core files from existing life project
- [x] Initialize project with `index.html`, `config.json`, `life.example.md`

#### 1.2 Design Historical Data Schema ✅
- [x] Define data structure for historical events (person/event, date, category, significance)
- [x] Design century-based organization (1-100 AD, 101-200 AD, etc.)
- [x] Create data models for:
  - [x] Historical events with flexible dating
  - [x] Multiple child books support
  - [x] World History categories (wars, political events, rulers, disasters, construction, discoveries)

#### 1.3 Adapt Timeline Calculation Logic ✅
- [x] Modify year calculation to handle AD 1-2000 timespan
- [x] Update date parsing to handle historical date formats including BC/AD
- [x] Implement decade-based positioning calculations (10 years per column)
- [x] Add support for BC/AD transition and date ranges

### Phase 2: Decap CMS Integration ✅

#### 2.1 Install and Configure Decap CMS ✅
- [x] Add Decap CMS to the project (`admin/index.html` and `config.yml`)
- [x] Configure authentication (Git Gateway with Netlify Identity)
- [x] Set up admin interface for content management

#### 2.2 Create CMS Collection Schema ✅
- [x] Design collections for:
  - [x] Historical events/people
  - [x] Child profiles
  - [x] Century overviews
  - [x] Site settings
- [x] Configure rich text editing for event descriptions
- [x] Set up media management for historical images/artifacts

#### 2.3 Design User-Friendly Forms ✅
- [x] Create intuitive forms for adding historical entries
- [x] Implement date pickers with historical date support
- [x] Add category selection with predefined World History categories
- [x] Include fields for: name, date, description, significance, child assignment

### Phase 3: User Interface Development ✅

#### 3.1 Adapt Timeline Visualization ✅
- [x] Modify existing timeline code for century-based display
- [x] Implement horizontal scrolling across centuries
- [x] Add century headers and navigation
- [x] Update styling for historical content vs. personal gadgets

#### 3.2 Implement Century View Mode ✅
- [x] Create century-focused display (decade-based columns)
- [x] Add decade subdivisions within each century
- [x] Implement century filtering and navigation
- [x] Update timeline headers for historical periods

#### 3.3 Create Individual Child Book Support ✅
- [x] Implement child profile selection
- [x] Filter events by assigned child
- [x] Add family events that appear in all children's books
- [x] Create child-specific navigation and personalization

### Phase 4: Printing and Export Features 🚧

#### 4.1 Design Print-Friendly CSS 🚧
- [x] Create separate print stylesheet
- [🚧] Implement century-per-page layout for printing (needs refinement)
- [x] Ensure proper page breaks and margins
- [x] Optimize typography for printed output
- [ ] Optimize typography for printed output

#### 4.2 Implement Century Export
- [ ] Add functionality to export individual centuries
- [ ] Support PDF generation for offline use
- [ ] Include century overview and timeline visualization
- [ ] Maintain formatting consistency with digital version

#### 4.3 Create Book Assembly Tools
- [ ] Generate complete book PDFs for each child
- [ ] Include title pages and century navigation
- [ ] Add print preparation guidelines for parents

### Phase 5: Enhanced Features

#### 5.1 Search and Filter Capabilities
- [ ] Implement search across all historical entries
- [ ] Add filtering by category, time period, and child
- [ ] Create cross-referencing for related events
- [ ] Enable discovery of historical connections

#### 5.2 Educational Enhancements
- [ ] Add suggested historical figures by century
- [ ] Include timeline context for major historical periods
- [ ] Implement suggested connections between events
- [ ] Create study guides for each century

#### 5.3 Data Import and Sharing
- [ ] Create templates for bulk historical data import
- [ ] Add export functionality for sharing between families
- [ ] Implement backup and restore capabilities
- [ ] Support for community-shared historical datasets

### Phase 6: Testing and Documentation

#### 6.1 User Testing
- [ ] Test with homeschooling families
- [ ] Verify educational effectiveness
- [ ] Gather feedback on user interface
- [ ] Test printing functionality across different devices

#### 6.2 Documentation Creation
- [ ] Write user guide for parents and children
- [ ] Create setup instructions for Decap CMS
- [ ] Document data entry best practices
- [ ] Include Charlotte Mason method educational context

#### 6.3 Deployment and Distribution
- [ ] Set up hosting solution (Netlify/Vercel recommended)
- [ ] Configure domain and SSL
- [ ] Create deployment automation
- [ ] Establish update and maintenance procedures

## Current Project Status

### ✅ Completed Features
- Historical timeline with decade-based columns
- Multi-child event filtering and assignment
- BC/AD date parsing and display
- Historical category color coding
- Decap CMS integration for content management
- Century-based navigation and filtering
- Sample historical data across multiple centuries

### 🚧 In Development
- **Print Layout**: Print functionality exists but timeline positioning needs refinement
- **Additional Historical Data**: Expanding coverage across all 20 centuries
- **Enhanced Mobile Support**: Optimizing for tablet and phone use

### 🎯 Next Steps
1. **Refine Print Layout** - Fix timeline positioning issues in print mode
2. **Expand Historical Data** - Add comprehensive coverage for all 20 centuries
3. **Mobile Optimization** - Enhance responsiveness for touch devices
4. **User Testing** - Test with homeschool families for feedback

## File Structure

```
book-of-centuries/
├── docs/
│   └── index.md                    # This documentation
├── admin/                          # Decap CMS (to be created)
│   ├── index.html
│   └── config.yml
├── data/                          # Historical data (to be created)
│   ├── children/
│   ├── centuries/
│   └── shared/
├── assets/                        # Images and media (to be created)
├── config.json                    # Timeline configuration
├── index.html                     # Main application
├── centuries.md                   # Historical data file
└── README.md                      # Project README (to be created)
```

## Configuration Details

### Current Configuration (`config.json`)
```json
{
  "customStylesheetURL": null,
  "yearLength": 120,
  "hideAge": false
}
```

### Planned Book of Centuries Configuration
```json
{
  "customStylesheetURL": null,
  "yearLength": 120,
  "hideAge": true,
  "timeRange": {
    "start": 1,
    "end": 2000
  },
  "centuryView": true,
  "defaultChild": null,
  "categories": {
    "worldhistory": "#fef08a",
    "wars": "#fca5a5",
    "politics": "#a7f3d0",
    "rulers": "#ddd6fe",
    "discoveries": "#a5f3fc"
  }
}
```

## Educational Context - Charlotte Mason Method

### Key Principles
1. **Personal Connections**: Children make their own discoveries about historical connections
2. **Living Books**: Use quality historical narratives, not dry textbooks
3. **Timeline Visualization**: See how events and people relate across time
4. **Individual Learning**: Each child builds their own understanding

### Book of Centuries Benefits
- **Chronological Understanding**: Children see the flow of history
- **Pattern Recognition**: Discover connections between events and eras
- **Personal Investment**: Own timeline becomes a treasured learning tool
- **Cross-Curricular**: Connects history with literature, science, arts

### Usage Guidelines
1. **Regular Entries**: Add historical figures and events as they're studied
2. **Include Variety**: People, events, inventions, discoveries, cultural milestones
3. **Child-Led**: Let children make their own connections and observations
4. **Family Sharing**: Some events can be shared across all children's books

## Technical Implementation Notes

### Timeline Calculation Adaptations Needed
- **Year Range**: Change from personal lifespan (1990-2025) to historical (1-2000 AD)
- **Century Headers**: Group by 100-year periods instead of individual years
- **Date Parsing**: Handle historical date formats and approximations
- **Scale Adjustment**: Optimize for 2000-year span vs. 35-year span

### Key Files to Modify
1. **`index.html`** - Main application interface
   - Update title and branding
   - Modify timeline rendering logic
   - Add century view controls
   - Implement child selection

2. **`config.json`** - Timeline and display configuration  
   - Adjust year range and scaling
   - Add historical categories
   - Configure century view settings

3. **Data files** - Convert from `life.md` to historical format
   - Create century-based data organization
   - Design child-specific data structure
   - Implement historical event schema

4. **CSS** - Add century-view styling and print support
   - Century navigation styling
   - Print-friendly layouts
   - Historical category colors
   - Child selection interface

5. **JavaScript** - Adapt timeline logic for historical dates
   - Century-based calculations
   - Child filtering logic
   - Enhanced date parsing
   - Print functionality

### Decap CMS Integration Plan

#### Collections Schema
```yaml
collections:
  - name: "historical-events"
    label: "Historical Events"
    folder: "data/events"
    create: true
    slug: "{{year}}-{{slug}}"
    fields:
      - {label: "Title", name: "title", widget: "string"}
      - {label: "Date", name: "date", widget: "string"}
      - {label: "End Date", name: "endDate", widget: "string", required: false}
      - {label: "Description", name: "description", widget: "markdown"}
      - {label: "Category", name: "category", widget: "select", options: ["worldhistory", "wars", "politics", "rulers"]}
      - {label: "Child", name: "child", widget: "select", options: ["family", "najmi", "isa", "nada"]}
      - {label: "Significance", name: "significance", widget: "select", options: ["high", "medium", "low"]}
  
  - name: "children"
    label: "Children"
    folder: "data/children"
    create: true
    slug: "{{slug}}"
    fields:
      - {label: "Name", name: "name", widget: "string"}
      - {label: "Birth Year", name: "birthYear", widget: "number"}
      - {label: "Color Theme", name: "colorTheme", widget: "select"}
```

## Resources and References

### Educational Resources
- [Simply Charlotte Mason - Book of Centuries](https://simplycharlottemason.com/blog/how-to-do-a-book-of-centuries/)
- [Charlotte Mason Poetry - Book of Centuries](https://www.charlottemasonpoetry.com/book-of-centuries)
- [Ambleside Online - Book of Centuries](https://www.amblesideonline.org/BookofCenturies.shtml)

### Technical Resources
- [Decap CMS Documentation](https://decapcms.org/docs/)
- [Netlify Identity Documentation](https://docs.netlify.com/visitor-access/identity/)
- [Git Gateway Setup](https://decapcms.org/docs/git-gateway-backend/)

### Source Project
- [Original Life Project](https://github.com/cheeaun/life) by Chee Aun
- [Zain's Life Tracking](https://life.zainf.dev) - Live version
- [Source Repository](https://github.com/zainfathoni/life) - Zain's fork

## Development Environment

### Prerequisites
- Modern web browser for development
- Text editor or IDE
- Local web server for testing (optional: `python -m http.server` or `npx serve`)
- Git for version control

### Development Workflow
1. **Edit files locally** using preferred text editor
2. **Test locally** using web server or file:// protocol
3. **Commit changes** using Git
4. **Deploy** to hosting platform (Netlify/Vercel)

### Hosting Recommendations
- **Netlify** (recommended for Decap CMS integration)
- **Vercel** (good alternative)
- **GitHub Pages** (simple but limited CMS support)
- **Custom hosting** with static file serving

---

*Last Updated: January 2025*
*Status: Planning and Initial Setup Phase*