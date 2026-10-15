# CachePulse – Cloud Application Cache Efficiency

## 1. Project Overview

CachePulse is a web-based prototype designed to demonstrate how caching improves application performance by reducing repeated backend requests.

The application simulates cache hits, cache misses, cache expiration, response time, and backend operations. It also compares application behavior with caching enabled and disabled.

## 2. Objectives

- Demonstrate cache HIT and MISS operations.
- Implement a cache using JavaScript Map.
- Configure Time-To-Live (TTL) for cached data.
- Detect expired cache entries.
- Compare requests with caching enabled and disabled.
- Display performance metrics and request history.

## 3. Technologies Used

- **HTML5** – Structure of the application.
- **CSS3** – User interface and styling.
- **JavaScript** – Cache logic and interactive functionality.
- **JavaScript Map** – In-memory cache storage.
- **Performance API** – Measure simulated operation response time.

## 4. Features

- Send a single request.
- Test multiple requests without caching.
- Test multiple requests with caching.
- Simulate TTL expiration.
- Display cache hits and misses.
- Track simulated backend operations.
- View response time and request history.
- Reset the dashboard and statistics.

## 5. Project Structure

```text
CachePulse/
├── index.html
├── style.css
├── script.js
└── README.md
```

## 6. How to Run the Project

1. Download or clone the project repository.
2. Open the `CachePulse` folder in Visual Studio Code.
3. Ensure that `index.html`, `style.css`, and `script.js` are in the same folder.
4. Install the **Live Server** extension in VS Code if it is not already installed.
5. Right-click `index.html`.
6. Select **Open with Live Server**.
7. The CachePulse dashboard will open in your browser.
8. Click the available buttons to test cache behavior.

## 7. How It Works

### Without Cache
Each request is sent to the simulated backend operation. Repeated requests increase the backend operation count.

### With Cache
The first request produces a cache MISS and stores the result. Repeated requests for the same key produce cache HITs until the cached entry expires.

### TTL Expiration
When the configured Time-To-Live expires, the cached entry becomes invalid and a new request produces a cache MISS.

## 8. Expected Results

- Cache MISS occurs when data is not available in the cache.
- Cache HIT occurs when valid data is available in the cache.
- Expired entries require a new simulated backend operation.
- Repeated requests with caching can reduce simulated backend operations.
- The dashboard displays request statistics and response-time measurements.

## 9. Limitations

This is a frontend demonstration prototype. Backend operations and caching behavior are simulated in JavaScript. It does not currently connect to a real cloud server or database. Response times represent local simulated operations and should not be interpreted as real cloud network latency.

## 10. Future Enhancements

- Integrate a real backend API.
- Add Redis or another distributed cache.
- Store performance reports in a database.
- Deploy the application to a cloud platform.
- Add real-time monitoring and analytics.

## 11. Conclusion

CachePulse demonstrates the basic principles of application caching and how cache hits can reduce repeated backend operations. It provides an interactive way to understand cache behavior, TTL expiration, and the potential performance benefits of caching.
