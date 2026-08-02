## Docker-এ Node.js Container চালানো

## ধাপ ১: Docker Desktop-এ Node.js Image খোঁজা

Docker Desktop ওপেন করে সার্চ বারে লিখতে হবে **node**।

![Search node](https://imgur.com/DC7ispP.png)

## ধাপ ২: Image Pull করা

**node** অপশনে ক্লিক করে **Pull** বাটনে ক্লিক করতে হবে।

অথবা, PowerShell-এ নিচের command দিয়েও pull করা যায়:

```bash
docker pull node
```

![Pull node](https://imgur.com/B7Z1535.png)

Download শেষ হলে image-টি Docker Desktop-এর Images লিস্টে যোগ হয়ে যাবে।

![Image added](https://imgur.com/nbdqqe2.png)

## ধাপ ৩: Container-এ Terminal Open করে Run করা

Containers ট্যাব থেকে terminal open করে নিচের command দিতে হবে:

```bash
docker run -it node /bin/bash
```

![Run container](https://imgur.com/Xidcsyt.png)

## ধাপ ৪: Node Version চেক করা

```bash
node -v
```

![Node version](https://imgur.com/PgZCWyY.png)

## গুরুত্বপূর্ণ নোট

Local machine-এর Node version আর Docker-এর ভেতরের Node version একই হবে না। PowerShell-এ `node -v` command দিলে সেটা machine-এর version দেখাবে, আর Docker container-এর ভেতরে একই command দিলে সেটা container-এর নিজস্ব version দেখাবে — দুটো ভিন্ন হতে পারে।
