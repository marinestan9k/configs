# Source 1 games on Linux

### For base Fedora or something
To fix the SELinux thing while running a Source 1 game, run this command in the terminal listed here and in this screenshot.<br>
<img width="721" height="106" alt="image" src="https://github.com/user-attachments/assets/730fd143-36fa-48c2-8a6a-f8587e020ac1" /><br>
`sudo ausearch -c 'hl2_linux' --raw | audit2allow -M my-hl2linux`

Afterwards, run this command listed here and in this screenshot.<br>
<img width="558" height="196" alt="image" src="https://github.com/user-attachments/assets/bde3e6a3-1562-4ec3-a986-3213b5a465d7" /><br>
`sudo semodule -X 300 -i my-hl2linux.pp`

Hopefully it shouldn't bother you anymore. Enjoy!

### Vulkan (any distro)

Steam's overlay will look pretty funny since its running with OpenGL by default (at least in my experience). This will be the thing for those that are bothered by it.

First, make sure the Steam client is open. Then in your library, right click on any Source 1 game and click "Properties..."<br>
<img width="265" height="205" alt="image" src="https://github.com/user-attachments/assets/ecdec55c-faac-4aec-b5d8-41041f444e93" /><br>

Under "Launch Options", put in `-vulkan`.<br>
<img width="836" height="595" alt="image" src="https://github.com/user-attachments/assets/f53a8480-4611-4334-bbea-92c21dc6c3a6" /><br>

### Proton (any distro)

Alternatively, you can force the Source 1 game to run via a version of Proton.<br>
<img width="836" height="595" alt="image" src="https://github.com/user-attachments/assets/d71bc969-e540-4822-ba8a-1ca894e8ddde" />
