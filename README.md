# Project Name: Apna-CheckUp

## Domain : Healthcare

## About the Project
We have designed a CAD system/Disease Prediction system where users can get to know whether they are infected with a particular disease or not based on the input in the form of report or X-Ray/MRI Image.

Because of COVID, it is now unsafe to go to the hospital every time we feel ill since there is a risk of getting affected with COVID in the hospital. So, our project aims to not only effectively connect doctors and patients virtually but incase if a patient recognises the symptoms, then he/she can know what disease he/she is likely to be infected with and what precautionary measures can be taken.

## Getting Started

**Step 1. Clone the repository into a new folder and then switch to code directory**

```
git clone https://github.com/gautamgc17/Apna-CheckUp
cd Apna-CheckUp
```

**Step 2. Create a Virtual Environment and install Dependencies.**

```
pip install virtualenv
```

Create a new Virtual Environment for the project and activate it.

```
virtualenv env
env\Scripts\activate
```
Once the virtual environment is activated, the name of your virtual environment will appear on left side of terminal.

Next, we need to install the project dependencies in this virtual environment, which are listed in `requirements.txt`.

```
pip install -r requirements.txt
```

**Step3 . Download the trained models and include them in models directory of the application.**

The trained deep learning models can be downloaded from [here](https://drive.google.com/drive/folders/1W99hOStpzLc_Dw_RgtDGxdLPJC_M_kf2?usp=sharing).

**Step 4. Set up Amazon Transcribe API for speech to text conversion**

- Sign in to your Amazon console and create a _S3 bucket_ and give it a unique name. Note your AWS region as it will be required later.
- Go to _IAM dashboard_, add a new User. Then click on add permissions and grant the following two permissions - _AmazonTranscribeFullAccess_ and _AmazonS3FullAccess_.
- Then under Security Credentials, click on _Create access key_ to get your credentials i.e,  'aws_access_key_id' and 'aws_secret_access_key'.


**Step 5. Update environment variables.**

To run the project, you need to configure the application to run locally. This will require updating a set of environment variables specific to your environment.

In the same directory, create a local environment file

_Now You have to simply duplicate the __.env.sample__ file and just insert your credentials._

In the file _.env_ , 
- store your aws credentials i.e aws region, unique bucket name, language code, aws access key id and secret key in following variables:

```
AWS_ACCESS_KEY_ID = ''
AWS_SECRET_KEY = ''
MY_REGION = ''
BUCKET_NAME = ''
```

**Step 6. Run Django Project.**
- Make Migrations
```
python manage.py makemigrations
python manage.py migrate
```

- Create a superuser if you wish
```
python manage.py createsuperuser
```

- Run the server code
```
python manage.py runserver
```





