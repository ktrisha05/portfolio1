import 'package:flutter/material.dart';

void main() => runApp(MyPortfolioApp());

class MyPortfolioApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Trisha\'s Portfolio',
      theme: ThemeData(
        primarySwatch: Colors.blueGrey,
        scaffoldBackgroundColor: Colors.grey[200],
        textTheme: TextTheme(
          bodyText1: TextStyle(color: Colors.black87),
          bodyText2: TextStyle(color: Colors.black87),
          headline6: TextStyle(color: Colors.black87),
        ),
        colorScheme: ColorScheme.fromSwatch(
          primarySwatch: Colors.blueGrey,
          accentColor: Colors.amber,
          backgroundColor: Colors.grey[200],
          errorColor: Colors.redAccent,
        ),
      ),
      home: MyPortfolioPage(),
    );
  }
}

class MyPortfolioPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Trisha\'s Portfolio'),
      ),
      body: Center(
        child: Container(
          padding: EdgeInsets.all(20.0),
          child: SingleChildScrollView(
            child: Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                CircleAvatar(
                  radius: 80,
                  backgroundImage: AssetImage(
                      'image/trisha.JPG'),
                ),
                SizedBox(height: 20.0),
                Text(
                  'Hello, I\'m Trisha Khandelwal,',
                  textAlign: TextAlign.center,
                  style: TextStyle(
                    fontSize: 28.0,
                    fontWeight: FontWeight.bold,
                    color: Colors.black87,
                  ),
                ),
                SizedBox(height: 10.0),
                Text(
                  'I am currently pursuing a BA program (Computer Applications+Economics) from Mata Sundri College for Women, University of Delhi.',
                  textAlign: TextAlign.center,
                  style: TextStyle(
                    fontSize: 20.0,
                    color: Colors.black87,
                  ),
                ),
                SizedBox(height: 10.0),
                Text(
                  'My passion lies in coding languages such as C++, Python, and Java. Recently, I embarked on a journey into app development using the Flutter Dart language, which has captivated my interest.',
                  textAlign: TextAlign.center,
                  style: TextStyle(
                    fontSize: 20.0,
                    color: Colors.black87,
                  ),
                ),
                SizedBox(height: 20.0),
                Text(
                  'Skills:',
                  textAlign: TextAlign.center,
                  style: TextStyle(
                    fontSize: 22.0,
                    fontWeight: FontWeight.bold,
                    color: Colors.black87,
                  ),
                ),
                SizedBox(height: 10.0),
                Row(
                  mainAxisAlignment: MainAxisAlignment.center,
                  children: [
                    _buildSkillChip('Python'),
                    SizedBox(width: 10.0),
                    _buildSkillChip('C++'),
                    SizedBox(width: 10.0),
                    _buildSkillChip('Graphic Design'),
                  ],
                ),
                SizedBox(height: 20.0),
                Text(
                  'Contact Me:',
                  textAlign: TextAlign.center,
                  style: TextStyle(
                    fontSize: 22.0,
                    fontWeight: FontWeight.bold,
                    color: Colors.black87,
                  ),
                ),
                SizedBox(height: 10.0),
                Text(
                  'Email: khandelwaltrisha08@gmail.com',
                  textAlign: TextAlign.center,
                  style: TextStyle(
                    fontSize: 18.0,
                    color: Colors.black87,
                  ),
                ),
                SizedBox(height: 10.0),
                Text(
                  'Phone: 9871698563',
                  textAlign: TextAlign.center,
                  style: TextStyle(
                    fontSize: 18.0,
                    color: Colors.black87,
                  ),
                ),
              ],
            ),
          ),
        ),
      ),
    );
  }

  Widget _buildSkillChip(String skill) {
    return Chip(
      label: Text(
        skill,
        style: TextStyle(
          fontSize: 16.0,
          fontWeight: FontWeight.bold,
          color: Colors.white,
        ),
      ),
      backgroundColor: Color(0xff597a8b),
    );
  }
}
