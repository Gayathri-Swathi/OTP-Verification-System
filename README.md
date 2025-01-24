# OTP-Verification-System
import random 
import smtplib 
MYEMAIL = "YOUR EMAIL" # replace with your email address
PASSWORD = 'APP PASSWORD' # replace with your password
USER_EMAIL = "USER EMAIL" # user email address
# To generate 6-digit number.

def generate_otp():
  rand_num = random.randint(100000,999999)
  return rand_num

# To send the OTP to the users email address.

def send_otp_to_email(otp):
  with smtplib.SMTP('smtp.gmail.com') as connection:
    connection.starttls()
    connection.login(MYEMAIL,PASSWORD)
    connection.sendmail(
        from_addr=MYEMAIL,
        to_addrs=USER_EMAIL,
        msg=f"Subject:OTP Sent Successfully\n\nYour otp is {otp}"
    )

# entered OTP is Correct or not.

def otp_verification():
    otp = generate_otp()
    send_otp_to_email(otp)
    attempts = 0
    max_attempts = 2
    while attempts < max_attempts:
        user_input = input("Enter Your OTP: ")
  # Check the OTP is not entered ask again please enter your OTP.
        if not user_input:
            print("Please Enter Your OTP ")
  # Check if OTP is valid (e.g., 6 digits).
        elif not user_input.isdigit() or len(user_input) != 6:
            print("Invalid OTP format. Please enter a 6-digit number.")
  # Check the user input is equal to OTP.
        elif int(user_input) == otp:
            print("OTP Verified Successfully\nYour access should be granted")
            break
  # Check if the OTP is entered wrongly, then give a chance to enter again, and it will give attempts reaches to its maximum.
        else:
            print(f"Your Entered Invalid OTP, Please try again")
            attempts += 1
            if attempts == max_attempts:
                print(f"You Reached {max_attempts} maximum attempts.\nYour access should be denied")

# Call the otp_verification function
otp_verification()
