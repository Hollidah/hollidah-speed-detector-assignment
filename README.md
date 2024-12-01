        Car Speed and Demerit Points Program

        Description
This program calculates the demerit points of a driver based on their speed. It adheres to the following rules:

1. If the speed is **70 km/h or less**, it prints: `Ok`.
2. For every **5 km/h above the speed limit (70 km/h)**, the program adds **demerit point**
3. If the driver accumulates more than **12 demerit points**, their license is suspended, and the program prints: `License suspended`.

                Code used;
Here is the code in JavaScript:

```javascript
function calculateDemeritPoints(speed) {
    const speedLimit = 70;
    const kmPerPoint = 5;

    if (speed <= speedLimit) {
        console.log("Ok");
        return;
    }

    // Calculate demerit points
    const points = Math.ceil((speed - speedLimit) / kmPerPoint);

    if (points > 12) {
        console.log("License suspended");
    } else {
        console.log(`Points: ${points}`);
    }
}

// Test cases
calculateDemeritPoints(55); // Output: "Ok"
calculateDemeritPoints(80); // Output: "Points: 2"
calculateDemeritPoints(110); // Output: "Points: 10"
calculateDemeritPoints(180); // Output: "License suspended"
