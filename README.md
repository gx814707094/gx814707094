- 👋 Hi, I’m @gx814707094
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
gx814707094/gx814707094 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
Exception in thread "main" net.schmizz.sshj.transport.TransportException: Unable to reach a settlement of Client2ServerCipherAlgorithms: [aes128-cbc, aes128-ctr, aes128-gcm@openssh.com, blowfish-cbc, cast128-cbc, cast128-ctr, idea-cbc, idea-ctr, serpent128-cbc, serpent128-ctr, 3des-cbc, 3des-ctr, twofish128-cbc, twofish128-ctr, arcfour, arcfour128] and [aes256-cbc, aes256-ctr]

Hello, I reported an error in using sftpexample

  final SSHClient ssh = new SSHClient();
        ssh.loadKnownHosts();
        ssh.connect("xxx.xxx.com");
        try {
            ssh.authPassword("xxx","xxx");
            final SFTPClient sftp = ssh.newSFTPClient();
            try {
                sftp.get("test_file", new FileSystemFile("/tmp"));
            } finally {
                sftp.close();
            }
        } finally {
            ssh.disconnect();
        }
