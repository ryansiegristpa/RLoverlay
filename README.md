# RLoverlay
Real-time updating broadcast overlay featuring a custom scoreboard, player statistic meters, and a post-match display for Epic Games’ video game Rocket League. Written in React for use with https://gitlab.com/bakkesplugins/sos

![maxresdefault](https://github.com/ryansiegristpa/RLoverlay/assets/135390943/858557a7-c236-43cb-a182-b0319847dc1f)

# Features
- Displays real-time Rocket League match data
- Easy to configure and customize
- Works with OBS for streaming overlays
- Includes controller UI for starting matches and updating dashboard
  
# Getting Started
To run the overlay locally:
1. Clone the repository
2. Run `yarn install` to install dependencies
3. Run `yarn start` to start the dev server
4. Open http://localhost:3000 to view the overlay

# To build for production:
`yarn build`
This will generate optimized production assets in the build folder.

# Configuration
The overlay fetches real-time state from a local Node.js server. Start the server with:
`nodemon controller.js`

This will serve data from state.json. See state.example.json for the expected format.
The React app polls this API every 1000ms to update the overlay.

# Customizing

To replace the logo, swap out logo.svg in src/ with your own SVG file. You may need to update the import path in the code as well.
The controller UI is available at http://localhost:3000/controller for starting matches and updating the dashboard.

# OBS Integration
To use the overlay in OBS, add a Browser source pointing to http://localhost:3000.
