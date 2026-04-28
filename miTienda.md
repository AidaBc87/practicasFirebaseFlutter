import 'package:flutter/material.dart';

void main() => runApp(MiTienda());
class MiTienda extends StatelessWidget {
  const MiTienda({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home:Scaffold( //armazón
        appBar: AppBar( //barra superior

        leading: Icon(Icons.account_circle_rounded),
          elevation: 15,
          title: Text('Mi tienda abby C87'),
          actions: [
              Icon(Icons.more_vert),
                    ],
          
          backgroundColor: const Color.fromARGB(255, 154, 76, 243),
        ),
        body: Center(// cuerpo
          child: Text("Lista de productos disponibles"),//texto en el centro

        ),

      )
    );
    
  }
}
