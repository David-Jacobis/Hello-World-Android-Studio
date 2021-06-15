
1)	O que é uma activity?
Activity é uma tela na aplicação, nela é responsável por definir e exibir um Layout com componentes de interface de usuário, por exemplo: Imagens, botões e textos.

2)	O que é um filtro de intenção (Intent, filter Intent)
Basicamente é um objeto de mensagem que basicamente solicita uma ação de outro componente do aplicativo. São responsáveis por facilitar a comunicação entre os componentes por diversas formas.

3)	Crie um repositório no GitHub e crie o código de Hello World do site: https://developer.android.com/training/basics/firstapp

4)	O que está contido nos arquivos 
a)	app > java > com.example.myfirstapp > MainActivity
package com.example.myfirstapp;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
}






b)	app > res > layout > activity_main.xml


c)	app > manifests > AndroidManifest.xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.myfirstapp">

    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.MyFirstApp">
        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>



d)	Gradle Scripts > build.gradle
Project:
// Top-level build file where you can add configuration options common to all sub-projects/modules.
buildscript {
    repositories {
        google()
        mavenCentral()
    }
    dependencies {
        classpath "com.android.tools.build:gradle:4.2.1"

        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
}

allprojects {
    repositories {
        google()
        mavenCentral()
        jcenter() // Warning: this repository is going to shut down soon
    }
}

task clean(type: Delete) {
    delete rootProject.buildDir
}











Module:

plugins {
    id 'com.android.application'
}

android {
    compileSdkVersion 30
    buildToolsVersion "30.0.3"

    defaultConfig {
        applicationId "com.example.myfirstapp"
        minSdkVersion 16
        targetSdkVersion 30
        versionCode 1
        versionName "1.0"

        testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
    }

    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
        }
    }
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
}

dependencies {

    implementation 'androidx.appcompat:appcompat:1.2.0'
    implementation 'com.google.android.material:material:1.2.1'
    implementation 'androidx.constraintlayout:constraintlayout:2.0.1'
    testImplementation 'junit:junit:4.+'
    androidTestImplementation 'androidx.test.ext:junit:1.1.2'
    androidTestImplementation 'androidx.test.espresso:espresso-core:3.3.0'
}








5)	Execute o guia 2, executando seu app.
a)	Cole aqui um print do aplicativo sendo executado em um simulador.
 

6)	Execute o tutorial de Criar um IU
a)	Cole um print da primeira construção
b)	Cole um print do código gerado
c)	Cole um print da execução final da sua interface.

7)	Execute o tutorial Criar uma Nova Atividade e mostre o aplicativo rodando.
8)	O que mudou? Como as atividades se relacionam?
9)	Quais recursos estão disponíveis e foram utilizados?
10)	 Qual a configuração do seu arquivo de Manifesto e Por quê?
