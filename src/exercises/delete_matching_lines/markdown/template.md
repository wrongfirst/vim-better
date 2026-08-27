function calculateTotal(items) {
  console.log("Starting calculation...");
  let total = 0;
  for (const item of items) {
    console.log("Processing item:", item);
    total += item.price;
  }
  console.log("Finished:", total);
  return total;
}
