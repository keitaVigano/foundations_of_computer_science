# foundations_of_computer_science

- Extract all trips with `trip_distance` larger than 50.
- Extract all trips where `payment_type` is missing.
- For each `(PULocationID, DOLocationID)` pair, determine the number of trips.
- Save all rows with missing `VendorID`, `passenger_count`, `store_and_fwd_flag`, or `payment_type` in a new dataframe called `bad`, and remove those rows from the original dataframe.
- Add a `duration` column storing how long each trip has taken (use `tpep_pickup_datetime`, `tpep_dropoff_datetime`).
- For each pickup location, determine how many trips have started there.
- Cluster the pickup time of the day into 30-minute intervals (e.g., from 02:00 to 02:30).
- For each interval, determine the average number of passengers and the average fare amount.
- For each payment type and each interval, determine the average fare amount.
- For each payment type, determine the interval when the average fare amount is maximum.
- For each payment type, determine the interval when the overall ratio between the tip and the fare amounts is maximum.
- Find the location with the highest average fare amount.
- Build a new dataframe (called `common`) where, for each pickup location, we keep all trips to the 5 most common destinations (i.e., each pickup location can have different common destinations).
- On the `common` dataframe, for each payment type and each interval, determine the average fare amount.
- Compute the difference of the average fare amount computed in the previous point with those computed in point 9.
- Compute the ratio between the differences computed in the previous point and those computed in point 9. Note: you have to compute a ratio for each pair `(payment type, interval)`.
- Build chains of trips. Two trips are consecutive in a chain if:
  - (a) they have the same `VendorID`,
  - (b) the pickup location of the second trip is also the dropoff location of the first trip,
  - (c) the pickup time of the second trip is after the dropoff time of the first trip, and
  - (d) the pickup time of the second trip is at most 2 minutes later than the dropoff time of the first trip.
- Hint: Add a column `chain` to the dataset. A chain can have more than two trips.
