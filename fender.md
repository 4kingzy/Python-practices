import csv

compromised_users = []

with open('password.csv') as password_file:
  password_csv = csv.DictReader(password_file)
  for password_row in password_csv:
    print(password_row)
