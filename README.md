# webhook
**P2pool to Discord**

    Apply webhook to send.py file
    Put desired message into shareBlock.sh
    Change this file to match your p2pool and webhook locations
    Open 2 seperate terminals

**First terminal run**

    tail -f ~/Documents/p2pool/data/litecoin/log | grep --line-buffered 'GOT BLOCK FROM PEER' | tee ~/Documents/p2pool/web-static/blocks.txt

**Second terminal**

    iwatch -e modify -c ~/Documents/webhook/shareBlock.sh ~/Documents/p2pool/web-static/blocks.txt
