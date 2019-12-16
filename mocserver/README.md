# HDMI2USB-litex-firmware/mocserver setup

1. install dependencies
1. create opsis_hdmi2usb_lm32.json
1. run server(s)

# dependencies
1. git clone https://github.com/CarlFK/HDMI2USB-litex-firmware
1. git clone https://github.com/CarlFK/litex-renode --branch feature/regval
1. git clone https://github.com/tac-tics/hdmi2usb-viewer
1. sudo apt install nodejs npm
1. cd hdmi2usb-viewer
1. npm i

# opsis_hdmi2usb_lm32.json

HDMI2USB-litex-firmware/build/opsis_hdmi2usb_lm32/test/csr.csv is an artifact of the firmware build process.  If you don't have that, then use the supplied one and hope that is up to date.

otherwise:
`python3 ../litex-renode/generate-mocserver-json.py ../HDMI2USB-litex-firmware/build/opsis_hdmi2usb_lm32/test/csr.csv --json-file opsis_hdmi2usb_lm32.json`


# servers

1. cd HDMI2USB-litex-firmware/mocserver
1. python3 moc-server.py
1.
1. cd hdmi2usb-viewer
1. yarn start

browse http://localhost:8087

