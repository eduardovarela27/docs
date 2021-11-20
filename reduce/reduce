const users = [
    { id: 1, name: "eduardo", lastName: "varela" },
    { id: 2, name: "fernando", lastName: "varela" },
    { id: 3, name: "fernando", lastName: "varela" },
    { id: 4, name: "fernando", lastName: "varela" },
];



let cuenta = users.map(user => user.id).reduce((acc, el) => acc + el);
console.log(cuenta);

let miCarrito = [
    { "id_producto": 2, "nombre": "Bombilla individual GU10", "cantidad": 1, "precio": 20 },
    { "id_producto": 3, "nombre": "Bombilla individual GU10", "cantidad": 1, "precio": 20 },
    { "id_producto": 2, "nombre": "Bombilla individual GU10", "cantidad": 1, "precio": 20 },
    { "id_producto": 2, "nombre": "Bombilla individual GU10", "cantidad": 1, "precio": 20 },
    { "id_producto": 3, "nombre": "Bombilla individual GU10", "cantidad": 1, "precio": 20 },
    { "id_producto": 4, "nombre": "Bombilla individual GU10", "cantidad": 1, "precio": 20 },
    { "id_producto": 5, "nombre": "Bombilla individual GU10", "cantidad": 1, "precio": 20 },
    { "id_producto": 4, "nombre": "Bombilla individual GU10", "cantidad": 1, "precio": 20 },


];
const miCarrito2 = [];
let y = 1;
miCarrito.forEach(pro => {//recorro cada objeto del arreglo
    for (let i = y; i < miCarrito.length; i++) {//lo comparo con el siguiente
        const element = miCarrito[i];
        if (pro.id_producto === element.id_producto) {
            let comp = miCarrito2.find(p => p.id_producto === element.id_producto) ?? null;
            if (comp === null) {
                element.cantidad += pro.cantidad;
                miCarrito2.push({ ...element });
                element.cantidad = 0;
            } else if (comp) {
                miCarrito2.forEach(m => {
                    if (m.id_producto === comp.id_producto) {
                        m.cantidad += element.cantidad;
                        element.cantidad = 0;
                    }
                });
            }
        } else if (!miCarrito2.find(pro => pro.id_producto === element.id_producto)) {
            miCarrito2.push(element);
        }
    }
    y++;
});
console.log(miCarrito2);