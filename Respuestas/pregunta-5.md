db.productos.aggregate([
  {
    $group: {
      _id: "$categoria",
      stock_total: { $sum: "$stock" }
    }
  }
]) 
