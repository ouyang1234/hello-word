# hello-word
July another repository
void Init_Gpio_Mode(GPIO_TypeDef* GPIOx,uint32_t RCC_APB2Periph_GPIOx,uint16_t GPIO_Pin_x,GPIOMode_TypeDef GPIO_Mode)//,GPIOMode_TypeDef GPIO_Mode
{
	GPIO_InitTypeDef GPIO_InitStructure;					//定义一个GPIO结构体变量

	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOx,ENABLE);	//使能端口时钟
	
	GPIO_InitStructure.GPIO_Pin = GPIO_Pin_x; 											//
  GPIO_InitStructure.GPIO_Mode = GPIO_Mode;	   	//选择GPIO模式
  GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;	   	//
  GPIO_Init(GPIOx, &GPIO_InitStructure);	
}
