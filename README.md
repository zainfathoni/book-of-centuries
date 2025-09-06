# Digital Book of Centuries - Charlotte Mason Method

A comprehensive digital timeline tool for homeschooling families, implementing the Charlotte Mason Book of Centuries method for historical education.

## Overview

This project adapts the timeline concept from [life tracking](https://life.zainf.dev) to create an educational tool for children to visualize and connect historical events across 20 centuries (1-2000 AD). The application now includes advanced filtering, search capabilities, and educational features designed specifically for the Charlotte Mason methodology.

## Features

### ✅ Core Timeline Features
- **Century View**: Timeline organized by decades (10 years per column) for better historical overview
- **Complete Historical Coverage**: All 20 centuries (1-2000 AD) with comprehensive historical events
- **BC/AD Date Support**: Handles historical dates including BC dates and date ranges
- **Individual Books**: Separate event filtering for each child (Najmi, Isa, Nada)
- **Multi-Child Support**: Events can be assigned to specific children or shared with family

### ✅ Advanced Features
- **🔍 Global Search**: Search across all historical events and descriptions
- **🏷️ Advanced Filtering**: Filter by categories, centuries, children, and combinations
- **🔗 Historical Connections**: Click events to discover related events across time periods
- **📱 Mobile Optimized**: Responsive design for tablets and mobile devices
- **📊 Data Export**: Export timeline data as JSON or CSV for analysis
- **🎨 Category System**: Color-coded categories (worldhistory, wars, politics, rulers, discoveries, disasters, construction)

### ✅ Content Management
- **Direct Markdown Editing**: Simple file-based content management for contributors
- **Clear Filters**: Reset all filters with one click
- **Print Support**: Basic print functionality (print layout needs refinement)

## Educational Philosophy

Based on Charlotte Mason's approach where children:

- **Make Personal Connections**: Events can be assigned to specific children for personalized learning
- **Discover Relationships**: Historical connections system shows related events across centuries
- **Build Understanding**: Visual timeline helps children see chronological relationships
- **Create Learning Artifacts**: Each child builds their own book of centuries over time

## Getting Started

### Quick Setup

1. **Start Local Server**:
   ```bash
   cd book-of-centuries
   python3 -m http.server 3001
   ```

2. **Open Application**: Navigate to http://localhost:3001

3. **Explore Timeline**:
   - Use the **Search Box** to find specific events, people, or topics
   - Use the **Century Selector** to focus on specific time periods
   - Use the **Child Selector** to filter events by child or view all family events
   - Use the **Category Filter** to view events by type (wars, discoveries, etc.)
   - **Click on Events** to see related historical connections
   - Use **Clear All Filters** to reset the view

### Using the Timeline

#### Search and Filtering
- **Global Search**: Type in the search box to find events containing specific words
- **Century Filter**: Select a specific century for focused study
- **Child Filter**: View events assigned to specific children or family events
- **Category Filter**: Multi-select categories to see specific types of events
- **Combined Filters**: All filters work together for precise event discovery

#### Historical Connections
- **Click any event** to highlight related events across the timeline
- **Related events** are shown in blue highlighting
- **Selected events** are shown in yellow highlighting
- **Connections are based on**: Common categories, people, places, and concepts

#### Data Export
- **Export JSON**: Complete data export with metadata for backup or analysis
- **Export CSV**: Spreadsheet-compatible format for data analysis or printing

### Current Historical Data

The application includes comprehensive historical events covering all 20 centuries:

- **Century 1 (1-100 AD)**: Roman Empire, Jesus Christ, early Christianity
- **Century 2 (101-200 AD)**: Trajan, Hadrian's Wall, Marcus Aurelius
- **Centuries 3-10**: Late Roman Empire, early Christianity, Byzantine Empire
- **Centuries 11-13**: Crusades, medieval kingdoms, Mongol conquests
- **Centuries 14-16**: Renaissance, Reformation, Age of Exploration
- **Centuries 17-19**: Enlightenment, revolutions, industrial age
- **Century 20**: Modern era (1901-2000 AD)

Each century includes major political events, discoveries, rulers, wars, and cultural developments appropriate for the Charlotte Mason method.

### Adding Historical Events

Historical events follow this format in century files:

```markdown
- DATE **HISTORICAL_FIGURE/EVENT** Description #category [child:assignment]
```

**Examples**:
```markdown
- 27 BC-14 AD **Augustus Caesar** First Roman Emperor, establishes Pax Romana #rulers [family]
- 1066 AD **Battle of Hastings** Norman conquest of England changes history #wars [child:isa]
- ~1440 AD **Gutenberg Printing Press** Revolutionizes learning and knowledge #discoveries [family]
```

**Date Formats Supported**:
- `100` - Year only
- `01/100` - Month/Year  
- `01/01/100` - Day/Month/Year
- `100-200` - Date ranges
- `~150` - Approximate dates
- `100 BC`, `100 AD` - BC/AD dates

**Categories Available**:
- `#worldhistory` - Major world events
- `#wars` - Battles and conflicts
- `#politics` - Political changes and treaties
- `#rulers` - Kings, emperors, and leaders
- `#discoveries` - Scientific and technological advances
- `#disasters` - Natural disasters and tragedies
- `#construction` - Major building projects

**Child Assignments**:
- `[family]` - Event for all children
- `[child:najmi]` - Assigned to Najmi
- `[child:isa]` - Assigned to Isa
- `[child:nada]` - Assigned to Nada

## Content Management

### Direct File Editing

For adding or editing historical events:

1. **Edit Century Files**: Modify individual century files in `data/centuries/`
2. **Edit Main Timeline**: Update `centuries.md` for main historical events
3. **Edit Child Profiles**: Update files in `data/children/`
4. **Follow Format**: Use the established markdown format for consistency

### Manual Editing

Events are stored in:
- `centuries.md` - Main historical data file
- `data/centuries/century-XX.md` - Individual century files
- `data/children/` - Child profile files

## Mobile and Tablet Use

The application is optimized for mobile devices:

- **Responsive Design**: Adapts to different screen sizes
- **Touch Interactions**: Optimized for touch devices
- **Vertical Layout**: Controls stack vertically on mobile
- **Readable Text**: Font sizes adjust for smaller screens
- **Touch Targets**: Buttons and controls sized for fingers

## Technology

- **Frontend**: Pure HTML/CSS/JavaScript (no frameworks)
- **Data Storage**: Markdown files for version control and simplicity
- **Content Management**: Direct markdown file editing for contributors
- **Hosting**: Static site compatible (Netlify/Vercel recommended)
- **Mobile**: Responsive CSS with touch optimizations

## Development Status

### ✅ Completed Features

- **Complete Timeline**: All 20 centuries with comprehensive historical data
- **Advanced Search**: Global search across all events and descriptions
- **Filtering System**: Century, child, category, and combined filtering
- **Historical Connections**: Click events to discover related events
- **Mobile Optimization**: Responsive design for all device sizes
- **Data Export**: JSON and CSV export functionality
- **Content Management**: Direct file editing with contributor guidelines
- **Multi-Child Support**: Individual books and family events

### 🚧 In Development

- **Print Layout**: Print functionality exists but timeline positioning needs refinement
- **Study Guides**: Century summaries and key themes for educational enhancement

### 🎯 Future Enhancements

- **PDF Export**: Enhanced PDF export with proper timeline formatting
- **Import Functionality**: Ability to import historical data from CSV/JSON
- **Enhanced Search**: Advanced search with date ranges and boolean operators
- **Educational Resources**: Integrated study guides and discussion questions
- **Community Features**: Share and discover historical data from other families

## Educational Usage Guide

### For Parents/Teachers

1. **Start with Overview**: Begin with "All Centuries" view to show the scope of history
2. **Focus by Century**: Use century selector for age-appropriate time periods
3. **Personal Connections**: Assign events to specific children for ownership
4. **Cross-References**: Use the connections system to show historical relationships
5. **Regular Review**: Use search to review and reinforce learning

### For Children

1. **Explore Freely**: Click events to discover connections across time
2. **Search Interests**: Use search to find topics that interest you
3. **Build Your Book**: Focus on events assigned to you with child filter
4. **Make Connections**: See how events relate across centuries
5. **Export Progress**: Export your timeline data to track learning progress

### Charlotte Mason Method Integration

- **Living Books**: Events provide starting points for living book selections
- **Narration**: Events can be used for oral and written narration practice  
- **Timeline Work**: Visual representation supports chronological thinking
- **Personal Connection**: Child assignments create ownership and engagement
- **Cross-Curricular**: Connects history with geography, science, and literature

## Related Projects

- [Original Life Project](https://github.com/cheeaun/life) by Chee Aun
- [Zain's Life Tracking](https://life.zainf.dev) - Source inspiration

## Educational Resources

- [Simply Charlotte Mason - Book of Centuries](https://simplycharlottemason.com/blog/how-to-do-a-book-of-centuries/)
- [Charlotte Mason Poetry - Book of Centuries](https://www.charlottemasonpoetry.com/book-of-centuries)
- [Ambleside Online - Book of Centuries](https://www.amblesideonline.org/BookofCenturies.shtml)

---

**Current Status**: ✅ **Complete Educational Timeline Tool** - Ready for comprehensive historical education with advanced features

_For detailed technical documentation, see [docs/index.md](docs/index.md)_
