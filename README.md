# Documentation

Here is a **clear summary of everything we discussed** about connecting **Camunda Web Modeler** with your **GitHub** repository.

---

# 🧾 Summary of the Setup Process

## 1️⃣ Create a GitHub App

You need a **GitHub App** so Web Modeler can sync files with your repository.

Steps:

* Go to:

  ```
  https://github.com/settings/apps
  ```

* Click **New GitHub App**

Fill the basic fields:

| Setting      | Example                                                                              |
| ------------ | ------------------------------------------------------------------------------------ |
| App Name     | camunda-web-modeler-sync                                                             |
| Homepage URL | [https://github.com/aalnajour/Camundanzia](https://github.com/aalnajour/Camundanzia) |

---

## 2️⃣ Webhook Configuration

Under **Webhooks**:

| Setting     | Value       |
| ----------- | ----------- |
| Webhook URL | leave empty |
| Secret      | leave empty |
| Active      | ❌ Disabled  |

Webhooks are **not required** for Web Modeler.

---

## 3️⃣ Repository Permissions

Set **Read & Write** permissions for:

| Permission      | Access       |
| --------------- | ------------ |
| Commit statuses | Read & Write |
| Contents        | Read & Write |
| Pull requests   | Read & Write |

Then click **Create GitHub App**.

---

# 🔑 Generate Private Key

After creating the app:

1. Open the GitHub App page
2. Go to **General → Private keys**
3. Click **Generate a private key**

GitHub downloads a `.pem` file like:

```
web-modeler-sync.private-key.pem
```

Open the file and **copy all the content**.

---

# 📦 Install the GitHub App

1. Go to **Install App**
2. Click **Install**
3. Choose:

```
Only select repositories
```

4. Select your repository:

```
Camundanzia
```

---

# 🆔 Get the Installation ID

After installation you will see a URL like:

```
https://github.com/settings/installations/12345678
```

The number at the end is your:

```
Installation ID = 12345678
```

---

# 🆔 Get the Client ID

Open your **GitHub App → General page**

You will see:

```
Client ID: Iv1.xxxxxxxxx
Application ID: 123456
```

Copy the **Client ID**.

---

# 🌿 Find the Branch Name

Open your repository:

```
https://github.com/aalnajour/Camundanzia
```

At the top you will see the branch selector like:

```
main ▼
```

Your branch name is usually:

```
main
```

---

# ⚙️ Configure GitHub in Web Modeler

Inside **Camunda Web Modeler → Connect Repository**

Fill:

| Field               | Value                                                                                |
| ------------------- | ------------------------------------------------------------------------------------ |
| Client ID           | From GitHub App                                                                      |
| Installation ID     | From installation URL                                                                |
| GitHub API Base URL | Leave empty (GitHub Cloud)                                                           |
| Private Key         | Paste content of `.pem`                                                              |
| Repository URL      | [https://github.com/aalnajour/Camundanzia](https://github.com/aalnajour/Camundanzia) |
| Branch name         | main                                                                                 |
| Repository path     | optional                                                                             |

Then click:

```
Open repository
```

If it opens correctly → click **Save Configuration**.

---

# 🗑️ Delete a Repository (if needed)

To delete a repository in **GitHub**:

1. Open the repository
2. Click **Settings**
3. Scroll to **Danger Zone**
4. Click:

```
Delete this repository
```

5. Type the repository name to confirm.

⚠️ This action is **permanent**.

---

# ✅ Final Result

After configuration:

* **Camunda Web Modeler** can push BPMN changes
* Files are stored in **GitHub**
* Changes can be managed via **branches and pull requests**


Client ID: Iv23likxUb0W451asgkn

https://github.com/settings/installations/116759851

-----BEGIN RSA PRIVATE KEY-----
MIIEpQIBAAKCAQEA0mv5hJUlZ4EN25GuCKFAH04xjhxRrQpP4on0Vp3pL5DAYFOB
WT4CrEbEvfo+c3ET/4ha3by+Bc89SzORRRhXEcLix8G3+Bv9oLiddVKiX7JvwZLv
edPsgQc4a3xfDopAjwD0QILHINmqfajan0lrEQVbDjaKoI3oyu7AC3+a+FwP6fmp
RplcSjTA7N89a7aTOCLnfmi05jzHdLbtCRKDcz++oYvOjBtRN5LM1mIsm/g40EiU
CgmX957kxFBfPuNO/D7OD59H5dPASsLxbCc59KnJNYRpxhY3Znpov1wV+hik4SFQ
uR2i4qM04YV10kflPxlwBkse/roD3fOOM8CouQIDAQABAoIBAQDNTcpTIM4w8cra
i4X5J5OPt9RD6r+KDQCqcJ10kXf+D8aTdYZD02v6OMYm8e1S52ZysNCvfkMNGgmc
wQChIMF7M+HestTTgEPzN41x9iE1K708aie7fxlHPws+XEfGwP+CR5UJCFBPbfCZ
0FEWjySmo8oW0QJq6mrS7SV1UpiabjthKKOo1oUSWcx9/Gm1/2qt8OMOEyeKuQBM
vnDfAIJuZXF7rBnulQzy8GJ2W5UqaBGjMy6sUYD7iIRVlgI3HJKVJLGaL/rkhy05
ebEi/AcKEw+JZquQSdZO2ed7ZiJ6jWo+6BFN/zkIObV4FTdHd1Xzlp3m6Pkge+pe
IPmEJlABAoGBAPES6Pi+5J5oAP7t0KS4hS5AwNQOXxFeOm+SUZjpC8vLNKeLfcKB
5sVdfAkvIP8YByK/Yo1GJWq9tCx/KahjMY0+/luj63Q4fMtBTafAUsKJXuBycnhM
xg1uBDshb5uwVUPXL0ya5Q+k5iyQI7ViK044s2T2u9EO8jcsgoYgBM65AoGBAN9z
OF6gk1D6qA7ZgQL4DsnzatTtFpNq3GvjHxqGJtQJvzDppiPbvGay6KAlkSGDQ6Ky
vEMBPcJd7lLTzg5eHYi0oo0lHgRh6ID4kUQo20zrvRWfxRMvHxgHHzD+o7B5QQD1
whWlOR6ZeBmupGTD++IVirS1s0OqaReB8R1znaoBAoGASgsV1TjEfUbSb3pZqA4o
kbE/yKH1Xx9C8XvOZhnGDr0GGiPE55YAbEQvUZ7REqitoGWJ/nw6B9PmX/hasiZt
VMWxWDI7okGrSr5u/IQcpzWMF4HvWLWz6vIMiKDXZ8k8Fw8jrvKwQiLSs4M+BHr3
dBoEN5F01Fwz1vBr0ohJEbkCgYEAsUgdBRapSqpUA9QVQ2HDef6iV+Ty8GrsDrzX
xJeC3uAMzKXTpseDpodzgPvNNaWLV94u94pYkYksuJJK/aM2E2wdO5ajRh7X9NtB
ha5Ur6apEir8lMfiB5I+8QRWooDRTg2turanpttkKhwhWcEUar9kmRM/8wOU9Y2m
2xMLmAECgYEAqkLBTARlG1NVE2HKytobzjYGBLjNT60PAViYTxJCG4cFkcU5FyqY
gcB5f7KZyd1HFn3dJeO2qlBNK/TqN0I3USK1NpWxutOOfrXQGShXvSj6gvJhj0Lw
iTKbyOAeEbWiqn2KmXTELjVv1jfz6L7G3xhaX55rZwk573iP54nJCDE=
-----END RSA PRIVATE KEY-----


