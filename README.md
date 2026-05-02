# BusHub - Bus Booking Application

A modern bus booking web application built with Next.js, React Leaflet, and Tailwind CSS.

## Features

✨ **Modern UI/UX**
- Clean, intuitive interface with gradient backgrounds
- Responsive design (works on desktop and tablet)
- Real-time search and filtering

🗺️ **Interactive Map**
- Leaflet-powered interactive map
- Real-time bus route visualization
- Color-coded markers (green for start, red for end)
- Polyline routes with distance calculation

🔍 **Smart Filtering**
- Filter by price range
- Filter by bus type (AC/Non-AC)
- Live search with suggestions
- Date selection

🚌 **Bus Information**
- Operator details with ratings
- Departure and arrival times
- Distance calculation using Haversine formula
- Available seats information
- Bus type and amenities

## Setup & Installation

### Prerequisites
- Node.js 16+
- npm or yarn

### Installation Steps

```bash
# Clone the repository
git clone <your-repo-url>
cd bus-app

# Install dependencies
npm install

# or
yarn install
```

### Running the Application

```bash
# Development mode
npm run dev

# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) to see the application.

### Build for Production

```bash
npm run build
npm start

# or
yarn build
yarn start
```

## Project Structure

```
bus-app/
├── app/
│   ├── components/
│   │   ├── SearchBar.tsx      # Search input component
│   │   ├── BusCard.tsx        # Individual bus listing card
│   │   ├── FilterPanel.tsx    # Filter options panel
│   │   └── MapView.tsx        # Interactive map component
│   ├── globals.css            # Global styles & Tailwind
│   ├── layout.tsx             # Root layout
│   ├── page.tsx               # Home page
│   └── page.tsx               # Main application logic
├── public/                    # Static assets
├── package.json              # Dependencies
├── tailwind.config.ts        # Tailwind configuration
├── tsconfig.json             # TypeScript configuration
├── next.config.js            # Next.js configuration
└── postcss.config.js         # PostCSS configuration
```

## Technologies Used

- **Framework**: Next.js 14
- **UI Library**: React 18
- **Styling**: Tailwind CSS 3
- **Maps**: Leaflet & React-Leaflet
- **Language**: TypeScript
- **Build Tools**: PostCSS, Autoprefixer

## Key Features Explained

### Distance Calculation
Uses the Haversine formula to calculate accurate distances between coordinates:
```typescript
distance = 2 * R * atan2(√a, √(1−a))
```
where R is Earth's radius (6371 km)

### Dynamic Filtering
- Real-time price range filtering
- Bus type selection (AC/Non-AC/All)
- Instant results update

### Responsive Design
- Mobile-optimized layout with stacked cards
- Tablet view with side-by-side layout
- Desktop view with full map display

## Future Enhancements

- 🔐 User authentication & booking history
- 💳 Payment gateway integration
- 📱 Mobile app version
- 🔔 Real-time notifications
- ⭐ User reviews & ratings
- 🌙 Dark mode
- 🌍 Multi-language support
- 📊 Analytics dashboard

## API Integration

Currently using mock data. To integrate with a real API:

1. Create an API service file: `app/services/busApi.ts`
2. Replace static `routes` array with API calls
3. Update filter logic to handle dynamic data
4. Add loading states and error handling

## Performance Optimization

- ✅ Dynamic imports for map component (SSR disabled)
- ✅ Image optimization with Next.js Image component
- ✅ Code splitting for better performance
- ✅ CSS-in-JS with Tailwind for minimal bundle

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

MIT

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository
2. Create a feature branch
3. Commit changes
4. Push to the branch
5. Open a pull request

## Support

For issues or questions, please open an issue on the repository.

---

**Made with ❤️ for seamless bus travel**
