# velocity
/**
 * Calculates velocity given distance and time.
 * 
 * @param {number} distance - The distance traveled.
 * @param {number} time - The time taken to travel the distance.
 * @returns {number} The velocity calculated by dividing distance by time.
 */
function calculateVelocity(distance, time) {
  try {
    // Check if both arguments are numbers
    if (typeof distance !== 'number' || typeof time !== 'number') {
      throw new TypeError('Both arguments must be numbers');
    }
    
    // Check if time is greater than zero
    if (time <= 0) {
      throw new Error('Time must be greater than zero');
    }
    
    // Calculate and return velocity
    return distance / time;
  } catch (error) {
    // Log the error
    console.error('Error:', error.message);
    return null;
  }
}
