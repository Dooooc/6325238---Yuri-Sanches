# 6325238---Yuri-Sanches

db.createCollection("Produtos")

db.produtos.insertOne({
  nome: "Iphone XR",
  categoria: "Eletronico",
  preco: 1499.00,
  marca: "Apple",
  armazenamento: "238GB",
  cor: "Preto"
  
})

db.Produtos.insertMany([{
  nome: "Notebook Ultra X",
  categoria: "Eletronicos",
  preco: 4899.90,
  marca: "Lenovo",
  memoria_ram: "32GB",
  processador: "Intel i7" 
},
  {

  nome: "Smartphone Galaxy A15",

  categoria: "Eletronicos",

  preco: 1299.90,

  marca: "Samsung",

  armazenamento: "128GB",

  cor: "Azul"

}]
   )

   db.Produtos.find()

   db.Produtos.find({ preco: {$gt:100 } })

   db.Produtos.find({ categoria: "Eletronicos" })

   db.produtos.find(
  {},
  { nome: 1, preco: 1, _id: 0 }
)

db.Produtos.updateOne(
  { nome: "Smartphone Galaxy A15" },
  { $set: { preco: 1199.90 } }
)

db.Produtos.updateMany(
  {},
  { $set: { estoque: 0 } }
)

db.Produtos.updateMany(
  { categoria: "Roupas" },
  { $set: { promocao: true } }
)

db.Produtos.deleteOne({ nome: "Smartphone Galaxy A15 " })

db.Produtos.deleteMany(
  { categoria: "Eletronicos" }
)