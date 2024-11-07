#### How to show a Loading Message when Fetching Data 
```
import React, { useState, useEffect } from 'react';

function MyComponent() {
  const [isLoading, setIsLoading] = useState(false);
  const [data, setData] = useState([]);

  useEffect(() => {
    setIsLoading(true);
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => {
        setData(data);
        setIsLoading(false);
      });
  }, []);

  return (
    <div>
      {isLoading ? <p>Loading...</p> : null}
      {/* Render the fetched data here */}
    </div>
  );
}
```
