# 402final

import mysql.connector

mydb = mysql.connector.connect( host="localhost", user="root", password="YU_oppdivide!20" )

mycursor = mydb.cursor()

mycursor.execute("CREATE DATABASE menagerie ")

import mysql.connector

mydb = mysql.connector.connect( host="localhost", user="root", password="YU_oppdivide!20" )

mycursor = mydb.cursor()

mycursor.execute("CREATE TABLE pets (name VARCHAR(20), owner VARCHAR(20), species VARCHAR(20), sex CHAR(1), birth DATE, death Date")

import mysql.connector

mydb = mysql.connector.connect( host="localhost", user="root", password="YU_oppdivide!20" )

mycursor = mydb.cursor()

mycursor.execute("DESCRIBE pets")

for x in mycursor: print(x)

import mysql.connector

mydb = mysql.connector.connect( host="localhost", user="root", password="YU_oppdivide!20" )

mycursor = mydb.cursor()

mycursor.execute("SELECT name, birtj FROM pets")

myresult = mycursor.fetchall()

for x in myresult: print(x)

import mysql.connector

mydb = mysql.connector.connect( host="localhost", user="root", password="YU_oppdivide!20" )

mycursor = mydb.cursor()

mycursor.execute("SELECT owner, COUNT(*) FROM pets GROUP BY owner")

myresult = mycursor.fetchall()

for x in myresult: print (x)

import mysql.connector

mydb = mysql.connector.connect( host="localhost", user="root", password="YU_oppdivide!20" )

mycursor = mydb.cursor()

mycursor.execute("SELECT name, birth, MONTH(birth)FROM pets ")

myresult = mycursor.fetchall()

for x in myresult: print(x)
