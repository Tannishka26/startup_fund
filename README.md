# Startup Funding Detection Dashboard

A professional, real-time SaaS dashboard for discovering and tracking Indian startup funding activity. Monitor newly funded startups, identify hiring opportunities, and access enriched company data all in one place.

## Features

### Dashboard Overview
- **Real-Time Data**: Displays 25+ startups funded in the last 30 days across India
- **Live Updates**: Automatically refreshes every 5 minutes for the latest funding announcements
- **Professional UI**: Enterprise-grade design with modern gradient interface and responsive layout

### Key Sections

#### 1. Recent Funded Startups Table
Comprehensive view of all recently funded startups with:
- Company Name
- Funding Amount (in Indian Rupees)
- Funding Round (Seed, Series A/B/C, Pre-Seed)
- Lead Investor Information
- Announcement Date
- City/Location
- Hiring Status (Yes/No with color coding)
- LinkedIn Profile Links
- Company Website
- Key Decision-Makers

**Features:**
- Sort by any column (click column headers)
- Search and filter by company name
- Direct links to LinkedIn and websites
- Color-coded funding rounds for easy identification

#### 2. Hiring Alerts Section
Dedicated panel highlighting actively hiring startups with:
- Companies actively recruiting talent
- Job roles they are hiring for
- Quick action buttons to view opportunities
- Real-time alert badges

#### 3. Analytics Dashboard
Advanced metrics and visualizations:
- **Key Metrics Cards**
  - Total Startups: Count of funded companies
  - Total Funding: Sum of all funding amounts
  - Hiring Companies: Number actively recruiting
  - Average Funding: Mean funding per startup

- **Charts & Visualizations**
  - Funding Distribution by Round (Bar Chart)
  - City-wise Funding Breakdown (Bar Chart)
  - Hiring Status Overview (Pie Chart)
  - Recent Funding Timeline (Line Chart)
  - Round Distribution Analysis (Pie Chart)
  - Monthly Funding Trends (Bar Chart)

#### 4. Data Export
- **Export to CSV**: Download all startup data in standard CSV format
- Includes all columns: Company, Funding, Round, Investor, Location, Hiring Status, Date, Website, LinkedIn, Contacts
- One-click export with automatic file download

#### 5. Settings & Preferences
- **Auto-Refresh Toggle**: Enable/disable automatic data updates
- **Email Alerts**: Toggle email notifications for new funding announcements
- **Notification Bell**: View real-time alerts and updates

## How to Use

### Getting Started
1. Open the dashboard in your browser
2. The application automatically loads all startup data from the last 30 days
3. Data refreshes every 5 minutes automatically

### Navigating the Dashboard
- **Sidebar Navigation**: Click menu items to switch between Overview, Hiring Alerts, and Analytics
- **Search**: Use the search box in the data table to find specific companies
- **Sort**: Click any column header in the table to sort by that field
- **Filter**: Use the filter dropdowns to narrow results by funding round or city

### Exporting Data
1. Click the "Export Data" button in the top right
2. Your browser will download a CSV file with all startup information
3. Open in Excel, Google Sheets, or any spreadsheet application

### Using Analytics
1. Navigate to the "Analytics" tab in the sidebar
2. View key metrics at the top
3. Scroll through interactive charts for deeper insights
4. Charts automatically update with new data

### Accessing Company Information
- **LinkedIn Profiles**: Click the LinkedIn icon/link in any row to visit the company's LinkedIn page
- **Company Website**: Click the website link to visit the company's official website
- **Decision-Makers**: View key contacts and founders in the table for outreach

## Data Structure

Each startup entry contains:
\`\`\`json
{
  "id": "unique_identifier",
  "name": "Company Name",
  "fundingAmount": 1500000000,
  "fundingRound": "Series A",
  "investor": "Investor Name",
  "city": "Bangalore",
  "hiringStatus": true,
  "dateAnnounced": "2024-11-10",
  "linkedInUrl": "https://linkedin.com/company/...",
  "websiteUrl": "https://company.com",
  "keyContacts": "Founder Name, CTO Name"
}
\`\`\`

## Funding Rounds Explained

- **Pre-Seed**: Initial funding, < ₹50 Lakhs
- **Seed**: Early stage, ₹50 Lakhs - ₹2 Crores
- **Series A**: Growth stage, ₹2 - ₹10 Crores
- **Series B**: Expansion stage, ₹10 - ₹50 Crores
- **Series C+**: Scale stage, ₹50+ Crores

## API Integration

The dashboard uses mock data by default. To integrate with real startup data APIs:

### Option 1: NewsData.io
1. Get API key from https://newsdata.io
2. Add to environment: `NEWSDATA_API_KEY=your_key`
3. Update `/app/api/startups/fetch/route.ts`

### Option 2: Product Hunt
1. Register at https://producthunt.com/api
2. Get API credentials
3. Update `/app/api/startups/fetch/route.ts`

### Option 3: Crunchbase
1. Subscribe to Crunchbase API
2. Add credentials to environment variables
3. Update `/app/api/startups/fetch/route.ts`

## Settings & Preferences

### Auto-Refresh
When enabled (default), the dashboard automatically fetches new data every 5 minutes. Disable to reduce API calls or when working offline.

### Email Alerts
Enable to receive email notifications when:
- New startups matching your criteria are funded
- Your target companies announce funding
- Key decision-makers change roles

### Notification Bell
Shows real-time alerts and updates. Click to view:
- Recent funding announcements
- Companies started hiring
- Important sector updates

## Tips & Best Practices

1. **Regular Monitoring**: Check the dashboard daily for the latest funding activity
2. **Use Hiring Alerts**: Prioritize outreach to companies actively recruiting
3. **Export for CRM**: Export data and import into your CRM for campaign management
4. **Set Preferences**: Configure auto-refresh and email alerts based on your needs
5. **Sort by Recent**: Always sort by date announced to see the most recent funding

## Troubleshooting

### Data Not Loading
- Refresh the page (Ctrl+R or Cmd+R)
- Clear browser cache
- Check internet connection

### Export Not Working
- Try a different browser
- Disable browser extensions that might interfere
- Check browser console for errors

### Charts Not Displaying
- Ensure JavaScript is enabled
- Try a different browser
- Clear cache and reload

### Slow Performance
- Disable auto-refresh in settings
- Close other browser tabs
- Use a more recent browser version

## Browser Compatibility

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Keyboard Shortcuts

- `Ctrl/Cmd + K`: Open search
- `Ctrl/Cmd + E`: Export data
- `Ctrl/Cmd + R`: Refresh data
- `ESC`: Close dropdowns

## Support

For issues or feature requests, please check:
1. The troubleshooting section above
2. Browser console for error messages
3. Verify all data is loading correctly from the API

## License

This dashboard is provided as-is for business intelligence purposes.

---

**Last Updated**: November 2024
**Version**: 1.0
**Dashboard Type**: Real-Time Funding Intelligence
