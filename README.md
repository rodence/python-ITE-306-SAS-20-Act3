# python-ITE-306-SAS-20-Act3
Simple flask website 


## Source Code:
  
  app.py
  
  
    from flask import *
    app = Flask(__name__)

    @app.route('/')
    def message():
      return render_template('message.html')

    @app.route('/table/<int:num>')
    def table(num):
      return render_template('print-table.html',n=num)
    if __name__ == '__main__':
    app.run(debug = True)
    
    
    
   message.html
   
   
   
       <html>
       <head>
       <title>Message</title>
       <link rel="stylesheet" href="{{ url_for('static', filename='css/style.css') }}">
       </head>
       <body>
       <h1>Welcome to my website using Python Flask</h1>
       </body>
       </html>
       
       
       
  print-table.html
     
     
     
     
          <html>
          <head>
          <title>print table</title>
          </head>
          <body>
          <h2> printing table of {{n}}</h2>
          {% for i in range(1,11): %}
          <h3>{{n}} X {{i}} = {{n * i}} </h3>
          {% endfor %}
          </body>
          </html>
          
 ## Documentations:         
![Screenshot (13)](https://user-images.githubusercontent.com/113341443/194837911-a0c0ded5-aa8f-468a-b552-a036e98696ff.png)
![Screenshot (14)](https://user-images.githubusercontent.com/113341443/194837918-5518b512-14f0-4013-977a-c31049837311.png)
![Screenshot (15)](https://user-images.githubusercontent.com/113341443/194837920-9ef98a48-111e-4862-8232-12d81fee1287.png)

### Run the url in the browser  `http://127.0.0.1:5000/`
![Screenshot (16)](https://user-images.githubusercontent.com/113341443/194837923-2c307eb2-4b50-4bce-866e-cb7e40c8a7e8.png)
### Run the url in the browser  `http://127.0.0.1:5000/table/30`
![Screenshot (17)](https://user-images.githubusercontent.com/113341443/194837929-4b4969a3-5d69-43d7-8958-e6d72f502acf.png)

          
  
