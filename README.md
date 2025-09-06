# Digital Book of Centuries - Charlotte Mason Method

A digital timeline tool for homeschooling families, implementing the Charlotte
Mason Book of Centuries method for historical education.

## Overview

This project adapts the timeline concept from
[life tracking](https://life.zainf.dev) to create an educational tool for
children to visualize and connect historical events across 20 centuries (1-2000
AD).

## Features

- **✅ Century View**: Timeline organized by decades (10 years per column) for
  better historical overview
- **✅ Individual Books**: Separate event filtering for each child (Najmi, Isa,
  Nada)
- **✅ Multi-Child Support**: Events can be assigned to specific children or
  shared with family
- **✅ Historical Categories**: Color-coded categories (#worldhistory, #wars,
  #politics, #rulers, #discoveries, #disasters, #construction)
- **✅ BC/AD Date Support**: Handles historical dates including BC dates and
  date ranges
- **✅ Decap CMS Integration**: User-friendly content management system for
  adding historical events
- **🚧 Print Support**: Basic print functionality (print layout needs
  refinement)

## Educational Philosophy

Based on Charlotte Mason's approach where children:

- Make personal connections with historical figures
- Discover chronological relationships naturally
- Build their own understanding through living books
- Create a lifelong learning artifact

## Getting Started

### Quick Setup

1. **Start Local Server**:

   ```bash
   cd book-of-centuries
   python3 -m http.server 3001
   ```

2. **Open Application**: Navigate to http://localhost:3001

3. **Explore Timeline**:
   - Use the **Century Selector** to focus on specific time periods
   - Use the **Child Selector** to filter events by child or view all family
     events
   - Scroll horizontally to explore the timeline

### Current Historical Data

The application includes sample historical events from:

- **Century 1 (1-100 AD)**: Roman Empire, Jesus Christ, early Christianity
- **Century 2 (101-200 AD)**: Trajan, Hadrian's Wall, Marcus Aurelius
- **Century 9 (801-900 AD)**: Charlemagne, Viking raids
- **Century 11 (1001-1100 AD)**: Battle of Hastings, First Crusade
- Additional centuries with key historical events

### Adding Historical Events

Historical events follow this format in `centuries.md`:

```markdown
- DATE **HISTORICAL_FIGURE/EVENT** Description #category [child:assignment]
```

**Examples**:

```markdown
- 27 BC-14 AD **Augustus Caesar** First Roman Emperor, establishes Pax Romana
  #rulers [family]
- 1066 AD **Battle of Hastings** Norman conquest of England changes history
  #wars [isa]
- ~1440 AD **Gutenberg Printing Press** Revolutionizes learning and knowledge
  #discoveries [family]
```

**Date Formats Supported**:

- `100` - Year only
- `01/100` - Month/Year
- `01/01/100` - Day/Month/Year
- `100-200` - Date ranges
- `~150` - Approximate dates
- `100 BC`, `100 AD` - BC/AD dates

## Content Management

### Using Decap CMS (Optional)

For user-friendly content management:

1. **Setup Required**: Deploy to a platform with Git integration (Netlify
   recommended)
2. **Access CMS**: Navigate to `/admin/` after deployment
3. **Add Events**: Use the rich text interface to add historical events
4. **Manage Children**: Create and manage child profiles
5. **Categories**: Organize events by historical categories

## Technology

- Pure HTML/CSS/JavaScript (no frameworks)
- Markdown for data storage
- Decap CMS for content management
- Static site hosting (Netlify/Vercel recommended)

## Development Status

### ✅ Completed Features

- Historical timeline with decade-based columns
- Multi-child event filtering and assignment
- BC/AD date parsing and display
- Historical category color coding
- Decap CMS integration for content management
- Century-based navigation and filtering
- Sample historical data across multiple centuries

### 🚧 In Development

- **Print Layout**: Print functionality exists but timeline positioning needs
  refinement
- **Additional Historical Data**: Expanding coverage across all 20 centuries
- **Enhanced Mobile Support**: Optimizing for tablet and phone use

### 🎯 Future Enhancements

- PDF export with proper timeline formatting
- Blank century page templates for printing
- Enhanced search and cross-referencing
- Community historical data sharing
- Enhanced visual themes and customization

## Related Projects

- [Original Life Project](https://github.com/cheeaun/life) by Chee Aun
- [Zain's Life Tracking](https://life.zainf.dev) - Source inspiration

## Educational Resources

- [Simply Charlotte Mason - Book of Centuries](https://simplycharlottemason.com/blog/how-to-do-a-book-of-centuries/)
- [Charlotte Mason Poetry - Book of Centuries](https://www.charlottemasonpoetry.com/book-of-centuries)
- [Ambleside Online - Book of Centuries](https://www.amblesideonline.org/BookofCenturies.shtml)

---

**Current Status**: ✅ **Fully Functional Digital Timeline** - Ready for
educational use with basic print support

_For detailed technical documentation, see [docs/index.md](docs/index.md)_
