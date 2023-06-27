# sfe5
sfe five
class User:
    def __init__(self, username, password):
        self.username = username
        self.password = password

class UserManager:
    def __init__(self):
        self.users = []

    def create_user(self, username, password):
        user = User(username, password)
        self.users.append(user)
        print("User created successfully.")

    def verify_user(self, username, password):
        for user in self.users:
            if user.username == username and user.password == password:
                print("User verified.")
                return
        print("Invalid username or password.")

    def display_users(self):
        print("User List:")
        for user in self.users:
            print("Username:", user.username)

# 示例用法
manager = UserManager()
manager.create_user("Alice", "12345")
manager.create_user("Bob", "password")
manager.display_users()
manager.verify_user("Alice", "12345")
manager.verify_user("Eve", "password123")
