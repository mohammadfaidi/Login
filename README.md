# Login

import 'package:flutter/material.dart';
 
void main() => runApp(MyHomePage());
 
	
 
class MyHomePage extends StatefulWidget {
  

  @override
  _MyHomePageState createState() => _MyHomePageState();
}
 
class _MyHomePageState extends State<MyHomePage> {
   var emailController = TextEditingController();
  var passwordController = TextEditingController();
  @override
  Widget build(BuildContext context) {
    return MaterialApp(home: Scaffold(
      appBar: AppBar(
        title: Text("Hack"),

      ),
  body: Container(
    child:Padding(
      padding: const EdgeInsets.all(20.0),
      child: Center(
        child: SingleChildScrollView(
                child: Column(
            crossAxisAlignment: CrossAxisAlignment.start,
            children: <Widget>[
             Text("Login",style: TextStyle(fontSize: 30.0,fontWeight: FontWeight.bold),),
            SizedBox(height:40.0),
            TextFormField(
              controller: emailController,
              keyboardType:TextInputType.emailAddress,
              onFieldSubmitted: (String value){
                print(value);

              },
              onChanged: (String value ){
print(value);
              },
              decoration: InputDecoration(
                labelText: "Email Address",
                prefix: Icon(Icons.email),
                border: OutlineInputBorder(),
              
              ),
            ),
            SizedBox(height:15.0),
            TextFormField(
              controller: passwordController,
 keyboardType:TextInputType.visiblePassword,
 obscureText: true,
              onFieldSubmitted: (String value){
                print(value);

              },
              onChanged: (String value ){
print(value);
              },
              decoration: InputDecoration(
                labelText: "Password",
                prefix: Icon(Icons.lock),
                suffix: Icon(Icons.remove_red_eye),
                border: OutlineInputBorder(),
              
              ),
            ),
            SizedBox(height:15.0),
            Container(
              width: double.infinity,
              color: Colors.blue,

              child: MaterialButton(onPressed: (){
               print(emailController.text);
               print(passwordController.text);
              },
               child:Text('LOGIN',
               style: TextStyle(color: Colors.white),
               ),
              ),
            ),
            SizedBox(height:10.0),

Row(
  mainAxisAlignment: MainAxisAlignment.center,
children: [
Text('Don\'t have an account?',),
TextButton(onPressed: (){}
, child: 
Text("Register Now ")),

],

),
            ],

          ),
        ),
      ),
    ),
  
  
  ),
    ),



    );
 }

}




