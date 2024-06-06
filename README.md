# Philippine Phone Prefix Checker

This Nuxt.js application helps you quickly identify the network (Globe, TM, Smart, or DITO) associated with a Philippine mobile phone number prefix.

## Features

- **Simple Input:** Enter the first 4 digits of a phone number to check its network.
- **Instant Results:** Get the network name instantly if it's found in our database.
- **Error Handling:**  Provides feedback if the prefix is invalid or not found.
- **Offline Ready:** Works offline thanks to the locally stored prefix data.

## How to Use

1. **Clone the Repository:**
   ```bash
   git clone
   ```

2. **Install Dependencies:**
   ```bash
   cd philippine-prefix-checker
   npm install 
   ```

3. **Start the Development Server:**
   ```bash
   npm run dev
   ```

4. **Open in Browser:** Navigate to `http://localhost:3000` (or the port specified in your console).

5. **Enter Prefix:** Type the first 4 digits of the phone number in the input field and click "Check Network".

## How it Works

- The app loads a JSON file (`prefix-data.json`) containing Philippine phone prefixes and their corresponding networks.
- When you enter a prefix, the app searches through this data to find a match.
- If found, the network name is displayed; otherwise, an error message is shown.

## Data Source

The prefix data is sourced from a comprehensive list of Philippine mobile networks and their prefixes. While we strive to keep the data accurate, mobile carriers may change their prefix assignments over time.

## Contributing

Contributions are welcome! If you notice any incorrect or outdated information, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the `LICENSE.md` file for details.


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run dev
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See Configuration Reference [invalid URL removed].
