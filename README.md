# webhook
**P2pool to Discord**

    Open send.py in editor and replace Discord webhook url with your own    
    Open shareBlock.sh in editor and put desired message in for when block is found.
    Change the lines below in this readme to match your p2pool and webhook locations
    Open 2 seperate terminals

**First terminal run**

    tail -f ~/Documents/p2pool/data/litecoin/log | grep --line-buffered 'GOT BLOCK FROM PEER' | tee ~/Documents/p2pool/web-static/blocks.txt

**Second terminal**

    iwatch -e modify -c ~/Documents/webhook/shareBlock.sh ~/Documents/p2pool/web-static/blocks.txt
