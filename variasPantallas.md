import 'package:flutter/material.dart';

void main() => runApp(MiAppRegistro());

class MiAppRegistro extends StatelessWidget {
  const MiAppRegistro({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      title: "Registro Aída C87",
      theme: ThemeData(primarySwatch: Colors.blue),
      // Rutas nombradas
      initialRoute: '/',
      routes: {
        '/': (context) => const PantallaBienvenida(),
        '/datos': (context) => const PantallaDatos(),
        '/final': (context) => const PantallaFinal(),
      },// fin rutas
    );
  } // fin widget build
}// fin clase MiAppRegistro

class PantallaBienvenida extends StatelessWidget {
  const PantallaBienvenida({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Bienvenido'),
        backgroundColor: const Color.fromARGB(255, 168, 188, 243),
      ),
     body: Center(
        child: Column(
            mainAxisAlignment: MainAxisAlignment.center, // Centra verticalmente
            children: <Widget>[
              const Text('Aída Bolívar CETis 87',
                style: TextStyle(fontSize: 24),
              ),
              const SizedBox(height: 20), // Espacio entre texto y botón
              ElevatedButton(
                onPressed: () => Navigator.pushNamed(context, '/datos'),
          child: Text("Iniciar Registro"),
              ),
            ],
          ),
        ),
      
       );
  }
}// fin pantalla binvenida

class PantallaDatos extends StatelessWidget {
  const PantallaDatos({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Datos Personales'),
        backgroundColor: const Color.fromARGB(255, 211, 117, 187),
      ),
      body: Center(
        child: ElevatedButton(
          onPressed: () => Navigator.pushNamed(context, '/final'),
          child: Text("Finalizar Registro"),
        ),
  
      ),
    );
  }
}// fin pantalla datos

class PantallaFinal extends StatelessWidget {
  const PantallaFinal({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Final'),
        backgroundColor: const Color.fromARGB(255, 243, 234, 101),
      ),
      body:
      Center(
        child: ElevatedButton(
          onPressed: () => Navigator.pushNamed(context, '/'),
          child: Text("Gracias por participar.. regresa a Bienvenida"),
        )
          

      )
    );
  }
}
