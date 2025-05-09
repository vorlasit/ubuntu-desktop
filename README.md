Install Odoo 18 on Desktop (Ubuntu/Linux) 24.04 
1. Update and install dependencies:  
  sudo apt update && sudo apt upgrade -y   
  sudo apt install git python3-pip build-essential wget python3-dev libpq-dev \ 
    libxml2-dev libxslt1-dev zlib1g-dev libsasl2-dev libldap2-dev \ 
    libjpeg-dev libpq-dev libffi-dev libtiff5-dev libopenjp2-7 \ 
    liblcms2-dev libwebp-dev libharfbuzz-dev libfribidi-dev \ 
    libxcb1-dev libpq-dev libssl-dev curl -y 

2. Install PostgreSQL :   
  sudo apt install postgresql -y  
  sudo -u postgres createuser -s $USER 
3. Install Python 3.10+ and pip packages  
  sudo apt install python3.12 python3.12-venv python3.12-dev -y   
  sudo apt install python3-pip -y   
4. Install wkhtmltopdf (for PDF support)   
  sudo apt install wkhtmltopdf -y   
5. Clone Odoo 18 (dev version)   
  git clone https://www.github.com/odoo/odoo --depth 1 --branch master odoo18   
6. Install Python dependencies   
  cd odoo18   
  pip3 install -r requirements.txt   
7. Run Odoo   
  ./odoo-bin -d odoo18db -r odoo --addons-path=addons    

You should now be able to access Odoo at:  
http://localhost:8069
