# lamina1
echo "deb [trusted=yes arch=amd64] https://snapshotter.lamina1.global/ubuntu jammy main"  > /etc/apt/sources.list.d/lamina1.list &&  apt update &&  apt install lamina1-node
lamina1.check-bootstrap.sh
lamina1.get_my_nodeid.sh
sudo journalctl -u lamina1-node.testnet -f -o cat
systemctl stop lamina1
systemctl disable lamina1
rm -rf ~/lamina1 ~/.lamina1 /etc/systemd/system/lamina1.service
