Simple CLI app that generates tokens compatible with Google Authenticator. I implemented this mainly to understand how it works, you should probably not use this.

Example output:

```sh
$ go run main.go "<your key>"
934523 (17 second(s) remaining)
```

Relevant RFCs:

* http://tools.ietf.org/html/rfc4226
* http://tools.ietf.org/html/rfc6238

---
- It's based [robbiev/two-factor-auth](https://github.com/robbiev/two-factor-auth).
- It has compiled with name `main` file, just exec the `login_blj` file to login.
- It is depend on `sshpass`(If you want replace it as `ssh` and modify the expect script.) `expect` and you should down the [Authenticator Extension](https://github.com/Authenticator-Extension)'s backup file. (The point is your secret key).

[中文](https://github.com/hereTac/blj-two-factor-auth/blob/main/README.zh-CN.md)
1. In some enterprise scenarios, there will be bastion hosts (which may have different names such as jump servers) and other jump servers for transfer, which allow technical personnel in the office environment (usually positions that need to perform operation and maintenance work) to remotely access certain servers in the online self-owned computer room through the bastion host. The bastion host usually uses 2FA technology verification.
2. In some enterprise scenarios, each employee usually has his own domain account, which is used as the account and password login for corporate mailboxes, corporate OA, corporate office computers, corporate internal systems, etc. If necessary, the domain account system is usually connected to allow technical personnel to log in to certain online servers
3. In the above two scenarios, technical personnel need one account and two passwords to log in to the online server. The account is the domain account, the first is the password of the domain account, and the second password is the 2FA dynamic verification code of the bastion host.
4. [hereTac/blj-two-factor-auth](https://github.com/hereTac/blj-two-factor-auth) is a small tool for automatically filling in the above two-stage passwords.
