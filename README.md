# Automatically file taxes in Paraguay

As a Paraguay tax resident (having a Tax ID) you have to file VATs (form 211) once a month and sometimes even the summary of receipts (even if you never claimed any). This script files all necessary taxes for you (in case of VAT it files 0 guarani tax).

> :warning: **Don't use the script if your VAT is not 0!**

The script also automatically updates your profile information which is usually requested once a year (in August).

Feel free to [support me](#support-me) if you find this helpful. Thank you!

[<img src="https://i.imgur.com/kI1J5wP.png" alt="drawing" height="60"/>](#support-me)

## 1) Dependencies (choose one)

You need these two packages to parse json and html: `jq`, `xmllint`

### 1.1) Install on Mac

Install [brew](https://brew.sh/) first if you haven't done so already.

Now install `jq` and `wget`:

```
brew install jq wget
```

`xmllint` is installed by default on MacOS Ventura (and perhaps older).

### 1.2) Install on Debian based distros

Update repo and install the packages:

```
sudo apt update && sudo apt install jq libxml2-utils
```

### 1.3) Install on RedHat-based distros

Install the packages:

```
sudo dnf install jq libxml2
```

## 2) Basic Setup

Go to a directory of your choice and clone the repo:

```
git clone https://github.com/stitch-05/file-taxes-paraguay.git && cd file-taxes-paraguay
```

Create a `.env` or `.env.local` file by copying the provided template:

```
cp .env.example .env
```

or

```
cp .env.example .env.local
```

Your env files stay local and are ignored by git.

Do NOT change `.env.example` or you'll run into issues when updating the repo.

Either fill in your login information (`USERNAME` and `PASSWORD`) in your local env file or use script arguments.

For more information on how to use script arguments see `./file-taxes.sh --help`.

## 3) Run

```
./file-taxes.sh
```

It may take up to a minute for the script to finish because of random pauses between each request. Let it finish.

## 4) Setup cron job (optional)

You can use cron to run the script automatically on the 2nd day of each month at 3am of your local time.

Open crontab for editing:

```
crontab -e
```

and add the following:

```
0 3 2 \* \* /home/<user>/<path to script/file-taxes.sh >/dev/null 2>&1
```

## 5) Receive Notifications (optional)

Receive a notification every time the script fails or succeeds to file VAT.

### 5.0) Notification Prefix

To customize the prefix displayed before notification messages, add the following to your local env file (`.env` or `.env.local`) or use script argument `--message-prefix`:

```
export MESSAGE_PREFIX="🇵🇾 taxes"$'\n'
```

Leave empty for no prefix.

### 5.1) Pushover

To use [Pushover](https://pushover.net/) as your notification service, create your pushover token and add the following to your env file (`.env` or `.env.local`) or use the relevant script arguments:

```
NOTIFICATION_SERVICE="pushover"

PUSHOVER_TOKEN=<your pushover token>
PUSHOVER_USER=<your pushover user>
```

### 5.2) Signal

To use [Signal](https://signal.org) as your notification service, install [signal-cli](https://github.com/asamk/signal-cli) (beyond the scope of this tutorial) and add the following to your env file (`.env` or `.env.local`) or use the relevant script arguments:

```
NOTIFICATION_SERVICE="signal"

SIGNAL_USER=<your signal phone number>
SIGNAL_RECIPIENT=<recipient signal phone number>
```

### 5.3) Email

Use SMTP to receive email notifications. Requires python3 installed. Add the following to your env file (`.env` or `.env.local`) or use the relevant script arguments.
Below example uses SMTP submission feature from proton mail.

```
NOTIFICATION_SERVICE="email"

export SMTP_HOST="smtp.protonmail.ch"
export SMTP_PORT="587"
export SMTP_ADDR="mypytax@pm.me"
export SMTP_PWD="g1df65gdf51g1gf65dg1df5g16d5fg1d2615dgfg"

# actual receiver/s of email notifications (';' separated string)

export SMTP_RECV="email0@pm.me;email1@gmail.com"
```

## 6) Download Statements (optional)

You can download statements of filed taxes in HTML format by adding the following to your local env file (`.env` or `.env.local`) or using the relevant script arguments:

```
DOWNLOAD_STATEMENTS="TRUE"
```

You can also specify the download directory (default is `statements` in the script directory):

```
DOWNLOAD_DIR="/path/to/download/directory"
```

## Common issues

If you run into any issues with the script, please make the script more verbose by changing `WGET_OUTPUT` in your local env file (`.env` or `.env.local`) to the following and running the script again:

```
WGET_OUTPUT="" # or "-d" for even more verbosity
```

You can also run the script with `--wget-output ""` argument.

The 2 most common issues are SSL issues related to the old server certificate and login captcha.

### SSL

If `wget` outputs an SSL error, you have several options of **trying** to fix it none of which can be covered in detail as they vary based on the OS version.

Your best bet is to uncomment the following line in your local env file (`.env` or `.env.local`) or add it if it doesn't exist and run the script again:

```
WGET_FLAGS="--secure-protocol tlsv1"
```

You can also run the script with `--wget-flags "--secure-protocol tlsv1"` argument.

If it doesn't help, you will have to play with the flag (google is your friend).

Another option is to lower your SSL security settings in `/etc/ssl/openssl.cnf`, which is NOT RECOMMENDED! Again, it depends on the version of your OS and openssl library.

### Captcha

You may be required to solve captcha. The script is currently unable to do so, but you can work around this issue by solving it in the browser first and running the script again. You will see a captcha-related error in the console with the link where you can solve it first.

### No pending actions

If you see a "no pending actions" message then it most likely means there's no form to fill out. Keep the script running in a cron and it will fill out known tax forms as soon as they are available.

## Support me

I spent a lot of time figuring out Paraguay's tax portal (kudos to Paraguay gov for making it fairly hard to automatize) and making it work.

If you find this script helpful, your Bitcoin, Monero or Litecoin donation is very much appreciated:

#### Donate Bitcoin

[![Pay with BTCPay](https://lnnet.work/img/paybutton/pay.svg)](https://lnnet.work/apps/2rmW6V8D4ZQjAx5G75wqTAJkE82H/pos)

or

```
bc1qxwuj3rty9krmtaf6tvah6cktkaktfgx0jagtva
```

![qr-btc](https://user-images.githubusercontent.com/104267488/199220610-878b531d-5387-4fa3-b99c-702d83dbe717.png)

#### Donate Monero

```
87D74aNPpJs6cfJJStv9yj7LYaAW4oJcQX1YqzpvaGokYd2dhMeYzhPNHBrBUdzKrvW9LyFkL2xVBTrhT9rpNocAAH1Z2Qt
```

![qr-xmr](https://user-images.githubusercontent.com/104267488/199220635-ae90a9cd-e4d4-4e34-b6ec-502c6f3b0517.png)

#### Donate Litecoin

```
ltc1qf0lferevscf4ag8vqck5n0nuvnnwdm0g6l9yfk
```

![qr-ltc](https://user-images.githubusercontent.com/104267488/260294867-a60652f2-2209-4e57-862b-33fb5b2d90c2.png)

# Thank you!
