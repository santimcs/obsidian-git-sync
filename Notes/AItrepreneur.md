cd comfyui[RunPod - The Cloud Built for AI](https://www.runpod.io/)
Choose RTX 3090
Change template
Select AItrepreneur
Edit template and change to 80,120 GB
Click Deploy On-Demand
Click Port 8888

Go to ComfyUI folder
Drag "C:\Users\User\Dropbox\My PC (DESKTOP-AVATU0N)\Downloads\ULTIMATE-FLUX_AUTO_INSTALL-RUNPOD.sh"  to ComfyUI folder
chmod +x ULTIMATE-FLUX_AUTO_INSTALL-RUNPOD.sh
./ULTIMATE-FLUX_AUTO_INSTALL-RUNPOD.sh

Drag EP08.sh
chmod +x EP08.sh
./ EP08.sh

Click Port 3000
cd /workspace/logs/
tail -f comfyui.log
