# Stm32f103_PinRead
Sequel to my previous baremetal attemt to blink leds to the bluepill board. This time i tried reading a pin state (PB12) and used the result to toggle an led (PA3). Although i'd seen tutorials doing this with A0 or B0 or C0. However, i wanted to choose an arbitrary pin to read because in real life, that's what you may need to do from time to time. So i figured out that instead of sending one bit (0X1) to the IDR to read PB12, all i had to do was send 4 bits instead (0x1000) or (1 << 12) to a uint16 pinStatus variable. Using uint8 didnt work as it only parsed one bit so i switched to uint16 to achieve this. Please find the pics and video for this attempt below. Thanks!!!

![photo_2023-03-16_10-41-12](https://user-images.githubusercontent.com/103900270/225577409-b19d6478-6f3e-4363-a7d7-d103c011fe4d.jpg)


![photo_2023-03-16_10-41-06](https://user-images.githubusercontent.com/103900270/225577429-eb0a2ec8-4ae8-46f1-b452-46c8ca8f4b27.jpg)




https://user-images.githubusercontent.com/103900270/225577506-288388aa-7bcd-4a97-9108-c9c2377bed76.mp4

