
● Cree una base de datos NoSQL.
● Cree una colección de datos llamada “parque”.
● Inserte cinco (5) documentos con la estructura JSON Creada.
● Actualizar los datos del primer y último registro.
● Liste la colección completa.
● Borre el tercer documento de la colección parque.
● Liste la colección de datos completa. 
● Cree la sentencia que permita obtener un documento según el número de placa del documento.



use('nuevadb');
db.createCollection('parque');




db.parque.insertMany(
[
{
_id:1,
placa: "lth456",
numero: 54346283928,
serie: "spg12894834934894380",
modelo: "hylux",
marca: "toyota",
kilometraje: 40.000,
tipo: "camioneta platon"
},
{
_id:2,
placa: "cvx345",
numero: 89846283928,
serie: "hjf2894834934894380",
modelo: "txl",
marca: "toyota",
kilometraje: 10.000,
tipo: "camioneta"
},
{
_id:3,
placa: "lps958",
numero: 95346283928,
serie: "asd42894834934894380",
modelo: "onix",
marca: "renault",
kilometraje: 40.000,
tipo: "sedan"
},
{
_id:4,
placa: "ytr534",
numero: 98746283928,
serie: "4682894834934894380",
modelo: "spark",
marca: "chebrolet",
kilometraje: 60.000,
tipo: "turismo"
},
{
_id:5,
placa: "clx987",
numero: 92246283928,
serie: "ttl22894834934894380",
modelo: "benz",
marca: "mercedez",
kilometraje: 50.000,
tipo: "deportivo"
}
]
);



db.parque.updateOne(
    {_id: 1},
    [{$set:{
        placa: "kñp765",
        numero: 34562789000,
        serie: "hhh56432897282",
        modelo: "fiesta",
        marca: "ford",
        kilometraje: 1.000,
        tipo: "sedan"
    }}]
)

db.parque.updateOne(
    {_id: 5},
    [{$set:{
        placa: "zlz098",
        numero: 977366252514,
        serie: "lki097265153777",
        modelo: "f160",
        marca: "ford",
        kilometraje: 80.000,
        tipo: "camioneta platon"
    }}]
)

db.parque.deleteOne({_id:3})


db.parque.find({placa:"zlz098"})