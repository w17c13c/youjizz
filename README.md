### [👉👉👉♥♥点此进入♥观看入口👈👈👈](https://mrddrm.github.io/jizz.html)
<br></br><br></br><br></br>
 user_id = str(len(self.users) + 1)
        self.users[user_id] = {
            'username': username,
            'password': password,  # 实际应用中应加密存储
            'age': age,
            'weight': weight,
            'height': height,
            'records': [],  # 饮用记录
            'health_metrics': []  # 健康指标记录
        }
        self.save_data()
        return True, "注册成功"
    
    def login(self, username: str, password: str):
        """用户登录"""
        for user_id, user_data in self.users.items():
            if user_data['username'] == username and user_data['password'] == password:
                self.current_user = user_id
                return True, "登录成功"
        return False, "用户名或密码错误"
