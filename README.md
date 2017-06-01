# TOC Project 2017

Template Code for TOC Project 2017

A telegram bot based on a finite state machine

## Setup

### Prerequisite
* Python 3

#### Install Dependency
```sh
pip install -r requirements.txt
```

* pygraphviz (For visualizing Finite State Machine)
    * [Setup pygraphviz on Ubuntu](http://www.jianshu.com/p/a3da7ecc5303)

### Secret Data

`API_TOKEN` and `WEBHOOK_URL` in app.py **MUST** be set to proper values.
Otherwise, you might not be able to run your code.

### Run Locally
You can either setup https server or using `ngrok` as a proxy.

**`ngrok` would be used in the following instruction**

```sh
ngrok http 5000
```

After that, `ngrok` would generate a https URL.

You should set `WEBHOOK_URL` (in app.py) to `your-https-URL/hook`.

#### Run the sever

```sh
python3 app.py
```

## Finite State Machine
![fsm](./img/show-fsm.png)

## Usage

初始狀態為user
1.當使用者位於user
a.輸入go to state1 跳到 state1 chatbot回答I'm entering state1

b.輸入go to state2 跳到 state2 chatbot回答I'm entering state2

c.輸入go to state3 跳到 state3 chatbot回答I'm entering state3

2.當使用者位於state3

a.輸入go to state4 跳到 state4 chatbot回答I'm entering state4

3.當使用者位於state4

a.輸入go to state5 跳到 state5 chatbot回答I'm entering state5

