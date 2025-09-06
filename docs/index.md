# Digital Book of Centuries - Charlotte Mason Method

## Project Overview

This project creates a comprehensive digital version of a Book of Centuries
based on the Charlotte Mason educational method. The Book of Centuries is a
timeline tool where each two-page spread covers one hundred years, helping
students visualize historical connections across time periods.

### Background

- **Source Project**: Adapted from
  [life tracking project](https://life.zainf.dev) by Zain Fathoni
- **Educational Method**: Based on Charlotte Mason's Book of Centuries approach
- **Reference**:
  [Simply Charlotte Mason - How to Do a Book of Centuries](https://simplycharlottemason.com/blog/how-to-do-a-book-of-centuries/)

### Project Requirements (User-Specified)

- **Time Period**: 1 AD - 2000 AD (20 centuries) ✅
- **Categories**: World History (wars, political events, rulers, discoveries,
  disasters, construction) ✅
- **Data Management**: Direct markdown file editing for contributors ✅
- **Viewing Modes**: Century view (100 years per screen), Timeline view,
  Printable century pages ✅
- **Multi-Child Support**: Individual books for each child ✅
- **Advanced Features**: Search, filtering, historical connections, mobile
  optimization ✅

## Technical Architecture

### Technology Stack

- **Frontend**: Pure HTML5, CSS3, Vanilla JavaScript (no frameworks)
- **Data Format**: Markdown files with JSON metadata
- **Content Management**: Direct markdown file editing for contributors
- **Hosting**: Static site compatible (Netlify/Vercel recommended)
- **Mobile**: Responsive design with touch optimizations

### Data Structure Design

#### Historical Event Schema

```markdown
- DATE_FORMAT **HISTORICAL_FIGURE/EVENT** description #category
  [child:assignment]
```

**Date Format Support:**

- `100` - Year only
- `01/100` - Month/Year
- `01/01/100` - Day/Month/Year
- `100-200` - Date ranges
- `~150` - Approximate dates
- `100 BC`, `100 AD` - BC/AD dates

**Enhanced Fields:**

- **Historical Figure/Event**: `**Julius Caesar**`, `**Battle of Hastings**`
- **Description**: Rich text with educational context
- **Category**: `#worldhistory`, `#wars`, `#politics`, `#rulers`,
  `#discoveries`, `#disasters`, `#construction`
- **Child Assignment**: `[child:najmi]`, `[child:isa]`, `[child:nada]`,
  `[family]`
- **Significance**: Historical importance level
- **Sources**: References and links

#### Century Organization ✅

- **Century 1**: 1-100 AD ✅
- **Century 2**: 101-200 AD ✅
- **Century 3**: 201-300 AD ✅
- ...
- **Century 20**: 1901-2000 AD ✅

All 20 centuries now have comprehensive historical data.

#### Multi-Child Data Structure ✅

```
/data/
├── children/
│   ├── najmi.md ✅
│   ├── isa.md ✅
│   └── nada.md ✅
├── centuries/
│   ├── century-01.md (1-100 AD) ✅
│   ├── century-02.md (101-200 AD) ✅
│   ├── century-03.md (201-300 AD) ✅
│   ├── century-04.md (301-400 AD) ✅
│   ├── century-05.md (401-500 AD) ✅
│   ├── century-06.md (501-600 AD) ✅
│   ├── century-07.md (601-700 AD) ✅
│   ├── century-08.md (701-800 AD) ✅
│   ├── century-09.md (801-900 AD) ✅
│   ├── century-10.md (901-1000 AD) ✅
│   ├── century-11.md (1001-1100 AD) ✅
│   ├── century-12.md (1101-1200 AD) ✅
│   ├── century-13.md (1201-1300 AD) ✅
│   ├── century-14.md (1301-1400 AD) ✅
│   ├── century-15.md (1401-1500 AD) ✅
│   ├── century-16.md (1501-1600 AD) ✅
│   ├── century-17.md (1601-1700 AD) ✅
│   ├── century-18.md (1701-1800 AD) ✅
│   ├── century-19.md (1801-1900 AD) ✅
│   └── century-20.md (1901-2000 AD) ✅
└── centuries.md ✅
```

## Implementation Plan

### Phase 1: Project Setup and Data Structure ✅

#### 1.1 Initialize New Project Structure ✅

- [x] Create new project directory at
      `/Users/zain/Code/GitHub/zainfathoni/book-of-centuries`
- [x] Set up Git repository for version control
- [x] Copy and adapt core files from existing life project
- [x] Initialize project with `index.html`, `config.json`, `centuries.md`

#### 1.2 Design Historical Data Schema ✅

- [x] Define data structure for historical events (person/event, date, category,
      significance)
- [x] Design century-based organization (1-100 AD, 101-200 AD, etc.)
- [x] Create data models for:
  - [x] Historical events with flexible dating
  - [x] Multiple child books support
  - [x] World History categories (wars, political events, rulers, disasters,
        construction, discoveries)

#### 1.3 Adapt Timeline Calculation Logic ✅

- [x] Modify year calculation to handle AD 1-2000 timespan
- [x] Update date parsing to handle historical date formats including BC/AD
- [x] Implement decade-based positioning calculations (10 years per column)
- [x] Add support for BC/AD transition and date ranges

### Phase 2: Decap CMS Integration ✅

#### 2.1 Install and Configure Decap CMS ✅

- [x] Add Decap CMS to the project (`admin/index.html` and `admin/config.yml`)
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
- [x] Include fields for: name, date, description, significance, child
      assignment

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

### Phase 4: Advanced Features ✅

#### 4.1 Global Search and Filtering ✅

- [x] Implement search across all historical events and descriptions
- [x] Add real-time search with dynamic results
- [x] Create advanced filtering by categories, centuries, and children
- [x] Implement combined filtering system
- [x] Add clear all filters functionality

#### 4.2 Historical Connections System ✅

- [x] Click events to discover related events across time periods
- [x] Smart relationship scoring based on categories and keywords
- [x] Visual highlighting for selected and related events
- [x] Cross-century historical connection discovery

#### 4.3 Mobile and Tablet Optimization ✅

- [x] Responsive design for all screen sizes (768px, 480px breakpoints)
- [x] Touch-optimized interactions with proper target sizes
- [x] Vertical layout for controls on mobile devices
- [x] Readable font sizes and improved spacing for mobile

#### 4.4 Data Export and Import ✅

- [x] JSON export with complete metadata and configuration
- [x] CSV export with structured data for spreadsheet analysis
- [x] Automatic filename generation with dates
- [x] Clean data extraction removing markup and tags

### Phase 5: Educational Enhancement ✅

#### 5.1 Complete Historical Coverage ✅

- [x] Create comprehensive historical data for all 20 centuries
- [x] Include major political events, rulers, wars, discoveries
- [x] Add educational context following Charlotte Mason method
- [x] Implement century themes and key learning points

#### 5.2 Study Guides and Educational Features ✅

- [x] Add "Key Themes" sections for each century
- [x] Include educational philosophy integration
- [x] Create Charlotte Mason methodology guidelines
- [x] Add cross-curricular learning connections

### Phase 6: Printing and Export Features 🚧

#### 6.1 Design Print-Friendly CSS 🚧

- [x] Create separate print stylesheet
- [🚧] Implement century-per-page layout for printing (needs refinement)
- [x] Ensure proper page breaks and margins
- [x] Basic print functionality available

#### 6.2 Export Functionality ✅

- [x] Add JSON export functionality for complete data backup
- [x] Add CSV export for spreadsheet analysis and printing
- [x] Include metadata and configuration in exports
- [x] Clean data formatting for external use

### Phase 7: Documentation and User Guidance ✅

#### 7.1 Comprehensive Documentation ✅

- [x] Updated README.md with all new features
- [x] Detailed usage guide for parents, teachers, and children
- [x] Charlotte Mason methodology integration guide
- [x] Technical documentation for developers

#### 7.2 Educational Resources ✅

- [x] Usage guidelines for different roles (parents/teachers/children)
- [x] Educational philosophy explanation
- [x] Best practices for historical timeline education
- [x] Integration with living books and narration

## Current Project Status

### ✅ Completed Features

- **Complete Timeline**: All 20 centuries with comprehensive historical data
- **Advanced Search**: Global search across all events and descriptions
- **Filtering System**: Century, child, category, and combined filtering
- **Historical Connections**: Click events to discover related events across
  time periods
- **Mobile Optimization**: Responsive design for all device sizes
- **Data Export**: JSON and CSV export functionality
- **Content Management**: Direct file editing with contributor guidelines
- **Multi-Child Support**: Individual books and family events
- **Educational Enhancement**: Charlotte Mason methodology integration
- **Century Navigation**: Decade-based timeline with century filtering

### 🚧 In Development

- **Print Layout**: Print functionality exists but timeline positioning needs
  refinement

### ✅ Ready for Use

The Digital Book of Centuries is now **fully functional** and ready for
educational use by homeschooling families. All core features are implemented and
working:

1. **Complete Historical Coverage** - All 20 centuries with comprehensive events
2. **Advanced Interaction** - Search, filter, and discover historical
   connections
3. **Multi-Child Support** - Individual books for each child with family events
4. **Mobile Friendly** - Works on all devices with touch optimization
5. **Data Management** - Export/import with direct file editing
6. **Educational Focus** - Charlotte Mason methodology throughout

## File Structure

```
book-of-centuries/
├── docs/
│   └── index.md                    # This documentation ✅
├── admin/                          # Decap CMS ✅
│   ├── index.html ✅
│   └── config.yml ✅
├── data/                          # Historical data ✅
│   ├── children/ ✅
│   │   ├── najmi.md ✅
│   │   ├── isa.md ✅
│   │   └── nada.md ✅
│   └── centuries/ ✅
│       ├── century-01.md through century-20.md ✅
├── config.json                    # Timeline configuration ✅
├── index.html                     # Main application ✅
├── centuries.md                   # Historical data file ✅
├── print.css                      # Print stylesheet ✅
└── README.md                      # Project README ✅
```

## Configuration Details

### Current Configuration (`config.json`) ✅

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
    "discoveries": "#a5f3fc",
    "disasters": "#fda4af",
    "construction": "#c4b5fd"
  },
  "children": ["najmi", "isa", "nada"]
}
```

## Features Overview

### 🔍 Search and Filtering

- **Global Search**: Real-time search across all historical events
- **Century Filter**: Focus on specific 100-year periods
- **Child Filter**: View individual or family events
- **Category Filter**: Multi-select historical categories
- **Combined Filtering**: All filters work together

### 🔗 Historical Connections

- **Interactive Events**: Click any event to see related events
- **Smart Relationships**: Based on categories, people, and concepts
- **Visual Highlighting**: Selected (yellow) and related (blue) events
- **Cross-Century Discovery**: Find connections across time periods

### 📱 Mobile Optimization

- **Responsive Design**: Works on phones, tablets, and desktops
- **Touch Interactions**: Optimized for touch devices
- **Vertical Layout**: Controls stack on mobile
- **Readable Text**: Font sizes adjust for screen size

### 📊 Data Management

- **JSON Export**: Complete data backup with metadata
- **CSV Export**: Spreadsheet-compatible format
- **Decap CMS**: User-friendly content management
- **Git Integration**: Version control for all changes

### 🎓 Educational Features

- **Charlotte Mason Method**: Educational philosophy integrated
- **Multi-Child Books**: Individual timelines for each child
- **Key Themes**: Educational context for each century
- **Cross-Curricular**: Connects history with other subjects

## Educational Context - Charlotte Mason Method

### Key Principles ✅

1. **Personal Connections**: Children make their own discoveries about
   historical connections
2. **Living Books**: Use quality historical narratives, not dry textbooks
3. **Timeline Visualization**: See how events and people relate across time
4. **Individual Learning**: Each child builds their own understanding

### Book of Centuries Benefits ✅

- **Chronological Understanding**: Children see the flow of history
- **Pattern Recognition**: Discover connections between events and eras
- **Personal Investment**: Own timeline becomes a treasured learning tool
- **Cross-Curricular**: Connects history with literature, science, arts

### Usage Guidelines ✅

1. **Regular Entries**: Add historical figures and events as they're studied
2. **Include Variety**: People, events, inventions, discoveries, cultural
   milestones
3. **Child-Led**: Let children make their own connections and observations
4. **Family Sharing**: Some events can be shared across all children's books
5. **Interactive Discovery**: Use search and connections to explore
   relationships

## Getting Started

### Quick Setup ✅

1. **Start Local Server**:

   ```bash
   cd book-of-centuries
   python3 -m http.server 3001
   ```

2. **Open Application**: Navigate to http://localhost:3001

3. **Explore Features**:
   - Use the **Search Box** to find specific events, people, or topics
   - Use the **Century Selector** to focus on specific time periods
   - Use the **Child Selector** to filter events by child or view all family
     events
   - Use the **Category Filter** to view events by type (wars, discoveries,
     etc.)
   - **Click on Events** to see related historical connections
   - Use **Clear All Filters** to reset the view
   - Use **Export** buttons to download data

### Using with Children ✅

1. **Start Broad**: Show the full timeline to demonstrate the scope of history
2. **Focus by Age**: Use century selector for age-appropriate periods
3. **Personal Connection**: Assign events to specific children
4. **Discover Relationships**: Click events to show historical connections
5. **Export Progress**: Save data to track learning over time

## Resources and References

### Educational Resources ✅

- [Simply Charlotte Mason - Book of Centuries](https://simplycharlottemason.com/blog/how-to-do-a-book-of-centuries/)
- [Charlotte Mason Poetry - Book of Centuries](https://www.charlottemasonpoetry.com/book-of-centuries)
- [Ambleside Online - Book of Centuries](https://www.amblesideonline.org/BookofCenturies.shtml)

### Technical Resources ✅

- [Decap CMS Documentation](https://decapcms.org/docs/)
- [Netlify Identity Documentation](https://docs.netlify.com/visitor-access/identity/)
- [Git Gateway Setup](https://decapcms.org/docs/git-gateway-backend/)

### Source Project ✅

- [Original Life Project](https://github.com/cheeaun/life) by Chee Aun
- [Zain's Life Tracking](https://life.zainf.dev) - Live version
- [Source Repository](https://github.com/zainfathoni/life) - Zain's fork

## Development Environment

### Prerequisites ✅

- Modern web browser for development
- Text editor or IDE
- Local web server for testing (optional: `python -m http.server` or
  `npx serve`)
- Git for version control

### Hosting Recommendations ✅

- **Netlify** (recommended for Decap CMS integration)
- **Vercel** (good alternative)
- **GitHub Pages** (simple but limited CMS support)
- **Custom hosting** with static file serving

---

**Project Status**: ✅ **COMPLETE - Ready for Educational Use**

_Last Updated: September 2025_ _Status: ✅ Complete Educational Timeline Tool_
