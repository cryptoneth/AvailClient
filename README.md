sudo apt update && sudo apt upgrade -y

sudo apt install curl tar wget clang pkg-config protobuf-compiler libssl-dev jq build-essential protobuf-compiler bsdmainutils git make ncdu gcc git jq chrony liblz4-tool -y

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

***press 1 , press enter

source ~/.cargo/env

rustup default stable

rustup update

rustup update nightly

rustup target add wasm32-unknown-unknown --toolchain nightly

apt install snapd 

***press y , press enter

snap install rustup --classic

apt  install cargo

***press y , press enter

git clone https://github.com/availproject/avail-light.git

cd avail-light

cargo build --release

wait 20 Min to finish

20 دقیقه وایسید حدودی تموم شه . شاید زودتر 


حالا میخوایم ولت قبلی رو ایمپورت کنیم

touch identity.toml

nano identity.toml


----------------------------

***** avail_secret_seed_phrase = 'Your Seed'

paste your key

press crtl + x
press y
press enter

-------------------------------




sudo tee /etc/systemd/system/availightd.service > /dev/null <<EOF

[Unit]
Description=Avail Light Client
After=network.target
StartLimitIntervalSec=0
[Service]
User=root
ExecStart=ExecStart=$(which avail-light) --identity '~/avail-light/identity.toml' --network goldberg 
Restart=always
RestartSec=120
[Install]
WantedBy=multi-user.target
EOF


-------------------------
این کد رو نمیخواد بزنید 
nano /etc/systemd/system/availightd.service

-------------------------

apt install screen
screen -S client

sudo systemctl daemon-reload
sudo systemctl enable availightd.service


sudo systemctl start availightd.service


sudo systemctl status availightd.service

press crtl + C

curl -sL1 avail.sh | bash

اون پابلیک کی رو یه جا سیو کنید

ما نود رو رو اسکرین ران کردیم الان 

Crtl + A + D

بزنید بیاید بیرون

کارمون تمومه


ولتی که میخواید رو یا همون ولت قدیمی رو فایل 
json

رو تو ولت پلکا دات بیارید بالا


https://lightclient.availproject.org/

اون پابلیک کی که داد رو اونجا کپی کنید


باقی مراحل سوشیال رو هم برید بعد ان اف تیشو مینت کنید

نود هم همونجا ران هست
