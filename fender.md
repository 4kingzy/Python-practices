import csv
import json

# 1 using passwords.csv file and printing all the users in compromised_users list via .append function
compromised_users = []
with open('passwords.csv') as password_file:
  password_csv = csv.DictReader(password_file)
  for password_row in password_csv:
    compromised_users.append(password_row['Username'])

# 2 write all the files from compromised_users list in 'compromised_users.txt.'

with open('compromised_users.txt', 'w') as compromised_user_file:
  for compromised_user in compromised_users:
    compromised_user_file.write(compromised_user)

# 3 import json and open json file, make dictionary and write it in .json file 
with open('boss_message.json', 'w') as boss_message:
  boss_message_dict = {
    'recipient' : 'The Boss',
    'message' : 'Mission Success'
  }
  json.dump(boss_message_dict, boss_message)
  
# 4 making a new variable password 
with open('new_passwords.csv', 'w') as new_passwords_obj:
  slash_null_sig = '''  

 _  _     ___   __  ____             
/ )( \   / __) /  \(_  _)            
) \/ (  ( (_ \(  O ) )(              
\____/   \___/ \__/ (__)             
 _  _   __    ___  __ _  ____  ____  
/ )( \ / _\  / __)(  / )(  __)(    \ 
) __ (/    \( (__  )  (  ) _)  ) D ( 
\_)(_/\_/\_/ \___)(__\_)(____)(____/ 
        ____  __     __   ____  _  _ 
 ___   / ___)(  )   / _\ / ___)/ )( \
(___)  \___ \/ (_/\/    \\___ \) __ (
       (____/\____/\_/\_/(____/\_)(_/
 __ _  _  _  __    __                
(  ( \/ )( \(  )  (  )               
/    /) \/ (/ (_/\/ (_/\             
\_)__)\____/\____/\____/

'''
  new_passwords_obj.write(slash_null_sig)

