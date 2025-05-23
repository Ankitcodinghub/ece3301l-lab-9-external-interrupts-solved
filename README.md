# ece3301l-lab-9-external-interrupts-solved
**TO GET THIS SOLUTION VISIT:** [ECE3301L LAB 9-External Interrupts Solved](https://www.ankitcodinghub.com/product/ece3301l-lab-9-external-interrupts-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;91475&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE3301L LAB 9-External Interrupts Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Experiment 9 External Interrupts

</div>
</div>
<div class="layoutArea">
<div class="column">
The purpose of this lab is to get the student to be familiar with the concept of system interrupt and in particular the external interrupts.

PART A) External Interrupts

A hardware interrupt is a signal generated by a special function device to indicate to the CPU that an event has happened and the CPU needs to temporary leave what it is working on so it can go to process the needs of that event. There are some procedures to ensure that the CPU remembers the location where it leaves before it goes away to process the interrupt. The new location where the CPU jumps to take care of the interrupt is called an Interrupt Service Routine (ISR). The CPU will enter the ISR routine when the interrupt occurs and when the task in that routine is completed, the CPU will perform a Return from Interrupt (RETI) in order to return to the main program at the location where the CPU was interrupted.

The advantage for an interrupt is that the CPU does not have to constantly wait for a hardware event to happen. It just needs to perform any task that it needs to take care or sitting idle doing nothing and then when an interrupt happens, the CPU just jumps to the ISR to handle that interrupt.

To allow interrupts to be able to be processed by the CPU, each hardware device that is capable to generate an interrupt has an ‘Interrupt Enable’ (IE) bit associated with it. When to set 1, the IE will allow an interrupt to happen. In addition, an ‘Interrupt Flag’ (IF) bit is set when an interrupt event happens. If the IE is on and when IF is also set, then the interrupt has occurred. When an interrupt is processed by the CPU, the IF has to be cleared to allow the next interrupt event to happen. If IF is not cleared, no further interrupt can be generated.

In addition, a ‘Global Interrupt Enable’ (GIE) bit is a general control bit that will allow any interrupt to be generated to the CPU when that bit is set to 1. This GIE has to be turned on in order for interrupts to happen.

Refer to chapter 10 ‘Interrupts’ of the PIC18F460 datasheets to see all the control bits for the interrupt functions of the hardware devices.

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
External interrupt is a type of interrupt when an input changes from a logic level to the other level. The edge transitioning from a selectable low-to-high or high-to-low transition will in fact generate an interrupt. There are three pins on the PIC18F4620 that can be used for such operation. They are called by the name INTx where x can be 0, 1 or 2. Here are the registers associated with these pins:

</div>
</div>
<div class="layoutArea">
<div class="column">
INTCONbits.GIE=1;

<ol>
<li>1) &nbsp;Interrupt Enable bits: INTCONbits.INT0IE ;
INTCON3bits.INT1IE; INTCON3bits.INT2IE;
</li>
<li>2) &nbsp;Interrupt Flag bits: INTCONbits.INT0IF ;
INTCON3bits.INT1IF; INTCON3bits.INT2IF;
</li>
<li>3) &nbsp;Interrupt Edge Select bits: INTCON2bits.INTEDG0 ;
INTCON2bits.INTEDG1; INTCON2bits.INTEDG2;
</li>
</ol>
</div>
<div class="column">
// Set the Global Interrupt Enable

// INT0 IE is in INTCON // INT1 IE is in INTCON3 // INT2 IE is in INTCON3

// INT0 IF is in INTCON // INT1 IF is in INTCON3 // INT2 IF is in INTCON3

// INT0 EDGE is in INTCON2 // INT1 EDGE is in INTCON2 // INT2 EDGE is in INTCON2

</div>
</div>
<div class="layoutArea">
<div class="column">
The INTxIE must be set to logic 1 to enable the associated INTx signal to generate an interrupt when it transitions with the type of edge specified by the INTEDGx bit (see below).

The INTxIF bit is set to 1 when the associated INTx signal has made the edge transition that would cause a subsequent interrupt. This bit needs to be cleared once the interrupt has been processed in order to allow the next interrupt to occur again. Leaving that bit to logic 1 will prevent further interrupt.

A INTEDGx bit when set to 0 indicates that an interrupt is to be generated when the logic transition goes from high-to-low (falling edge) and the other way when it is set to 1.

Here is an example to test the external interrupts: int INT0_flag, INT1_flag, INT2_flag = 0;

</div>
</div>
<div class="layoutArea">
<div class="column">
void Do_Init() {

Init_Uart(); Init_ADC();

OSCCON=0x70;

</div>
<div class="column">
// Initialize the ports

// Initialize the uart

// Initiailize the ADC with the // programming of ADCON1

// Set oscillator to 8 MHz

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
TRISB = 0x??

INTCONbits.INT0IF = 0 ; INTCON3bits.INT1IF = 0; INTCON3bits.INT2IF =0;

INTCON2bits.INTEDG0=0 ; INTCON2bits.INTEDG1=0; INTCON2bits.INTEDG2=1;

INTCONbits.INT0IE =1; INTCON3bits.INT1IE=1; INTCON3bits.INT2IE=1;

INTCONbits.GIE=1;

void interrupt high_priority chkisr() {

if (INTCONbits.INT0IF == 1) INT0_ISR();

if (INTCON3bits.INT1IF == 1) INT1_ISR();

if (INTCON3bits.INT2IF == 1) INT2_ISR(); }

void INT0_ISR() {

INTCONbits.INT0IF=0; INT0_flag = 1;

void INT1_ISR() {

INTCON3bits.INT1IF=0; INT1_flag = 1;

void INT2_ISR() {

INTCON3bits.INT2IF=0; INT2_flag = 1;

</div>
</div>
<div class="layoutArea">
<div class="column">
}

</div>
</div>
<div class="layoutArea">
<div class="column">
}

</div>
<div class="column">
// Clear the interrupt flag // set software INT0_flag

// Clear the interrupt flag // set software INT1_flag

// Clear the interrupt flag // set software INT2_flag

</div>
</div>
<div class="layoutArea">
<div class="column">
}

</div>
</div>
<div class="layoutArea">
<div class="column">
}

</div>
</div>
<div class="layoutArea">
<div class="column">
// Configure the PORTB to make sure // that all the INTx pins are

// inputs

// Clear INT0IF // Clear INT1IF // Clear INT2IF

// INT0 EDGE falling // INT1 EDGE falling // INT2 EDGE rising

// Set INT0 IE // Set INT1 IE // Set INT2 IE

// Set the Global Interrupt Enable

</div>
</div>
<div class="layoutArea">
<div class="column">
// check if INT0 // has occured

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
void main() {

Do_Init(); while (1) {

if (INT0_flag == 1) {

INT0_flag = 0;

printf (“INT0 interrupt pin detected \r\n”);

// print a message that INT0 has // occurred

}

if (INT1_flag == 1) {

INT1_flag = 0;

printf (“INT1 interrupt pin detected \r\n”);

</div>
</div>
<div class="layoutArea">
<div class="column">
} }

}

</div>
</div>
<div class="layoutArea">
<div class="column">
// Initialization // Do nothing,

</div>
</div>
<div class="layoutArea">
<div class="column">
// clear the flag

</div>
</div>
<div class="layoutArea">
<div class="column">
// clear the flag

</div>
</div>
<div class="layoutArea">
<div class="column">
// print a message that INT1 has // occurred

INT2_flag = 0;

printf (“INT2 interrupt pin detected \r\n”);

// print a message that INT2 has // occurred

</div>
</div>
<div class="layoutArea">
<div class="column">
}

if (INT2_flag == 1) {

</div>
</div>
<div class="layoutArea">
<div class="column">
Each time when either push-button SW2, SW3 or SW4 (see schematics) is pressed down, the interrupt INT0, INT1 or INT2 will be generated. The associated INT0_ISR(), INT1_ISR() or INT2_ISR() will be executed to service the interrupt. In each routine, the associated hardware INTxIF will be cleared to allow the next interrupt to be generated. Next, the associated variable INT0_flag, INT1_flag or INT2_flag will be to 1.

In the main program, the three variables INT0_flag, INT1_flag, INT2_flag will be constanstly monitored. When either one flag is detected to be 1, that variable will be cleared and a message will be printed to show the corresponding push-button switch has been pressed.

Complete the above program and run it. Push each button associated with the INT line and see on the screen that a message showing that the INT pin has been pressed.

</div>
</div>
<div class="layoutArea">
<div class="column">
// clear the flag

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
PART B) Use of external interrupts in the Traffic Controller Design

We will now use the external interrupts to trigger the requests for pedestrian accesses on the North-South and East-West directions. We will not use the DIP switches for the Pedestrian requests as in Lab 8. We will use instead the two push-buttons SW2 and SW3 that are hooked to the signals INT0 and INT1 (PORT B bit 0 and PORTB Bit 1 respectively).

When a push-button is pressed, this will set a flag to indicate that a request for the pedestrian access. When it is the time to do the handling of a pedestrian access, the flag will be checked. If it is not set to 1, then no pedestrian access will be performed. If it is set 1, then the pedestrian process will be performed. When done, the flag will be cleared so that on the next pass no new access will be performed again unless the push-button switch is pressed again in-between.

Use the setup on the program above, do the following:

<ul>
<li>copy the code to initialize the INTCON registers (the code in bold)</li>
<li>copy the ‘void interrupt high_priority chkisr()’ routine</li>
<li>copy the INT0_ISR(), INT1_ISR() and INT2_ISR() routines
Next, take care of the following steps:

<ol>
<li>1) &nbsp;Remove the definitions for the signals: a. NS_PED_SW
b. EW_PED_SW

We no longer use these switches to detect the pedestrian requests
</li>
<li>2) &nbsp;Create two variables with the same name:
<ol>
<li>char NS_PED_SW</li>
<li>char EW_PED_SW</li>
</ol>
</li>
<li>3) &nbsp;Replace in the INT0_ISR() and INT1_ISR() the variables INT0_flag and INT1_flag respectively by those two variables</li>
<li>4) &nbsp;This substitution will allow each pedestrian request to activated when the INT0 or INT1 push-button switch is pressed down.</li>
<li>5) &nbsp;Use the main routine from lab 8 (don’t use the main routine from the example above)</li>
<li>6) &nbsp;When the program runs properly, the NSP and EWP fields on the TFT panel will show a ‘1’ when the INT0 or INT1 switch is pressed. The pedestrian process will</li>
</ol>
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
be handled as usual. However, make sure to add one extra step in the PED_control routine to clear the NS_PED_SW or EW_PED_SW variable to 0 so that the pedestrian countdown does not get executed again unless the associated push-button is pressed in-between.

<ol start="7">
<li>7) &nbsp;In addition, in the interrupt service routine ISR(), add code to check what mode the INTx has occurred. If the mode is in day mode, then proceed as normal to set the variable NS_PED_SW or EW_PED_SW. However, if the mode is in night more, do not set the variable to 1 because no pedestrian access is allowed in that mode.</li>
<li>8) &nbsp;When switching from day mode to night mode, make sure to clear both NS_PED_SW and EW_PED_SW variables to prevent any pedestrian process to be handled in night mode.</li>
</ol>
If the implementation is done properly, the ‘NSP’ and ‘EWP’ display on the screen should have a ‘0’ shown most of the time. When a push-button either at INT0 or INT1 is pressed, then a ‘1’ will show up accordingly and stays at ‘1’ until the pedestrian process in the proper direction is completed. The ‘1’ should be changed to ‘0’ and stays at ‘0’ until the next time the push-buttton is pressed again.

PART C) Implementation of Flashing Mode

Use the INT2 associated with the push-button SW4 to initiate an RED light flashing request. When the INT2 occurs, it will set a flag variable called FLASHING_REQUEST to logic ‘1’. When the traffic controller has finished to execute a sequence either in Day mode or in Night mode (depending on the Photo-resistor), the program does return back to the main program. The next task is to check the logic of this FLASHING _REQUEST flag. If 0, then no request is asked. If 1, then the program will reset the FLASHING_REQUEST flag to 0 and then call a routine called Do_Flashing() whereas the following steps must be executed:

<ol>
<li>1) &nbsp;Set the FLASHING variable to 1</li>
<li>2) &nbsp;A while loop waiting for the variable FLASHING to be cleared to 0 (while (FLASHING == 1))</li>
<li>3) &nbsp;Inside the while loop, a check of the variable FLASHING _REQUEST must be performed</li>
<li>4) &nbsp;If FLASHING _REQUEST is 1, then clear that variable FLASHING _REQUEST to 0 and clear the variable FLASHING to 0. This will force the</li>
</ol>
</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
exit out of the while loop. This is to detect when the user presses on the INT2 switch to request to exit out of the emergency mode.

5) If FLASHING _REQUEST is 0, then we are still in flashing mode. Therefore, we need to set all the four directions with the RED color, then do WAIT_ONE_SECOND(), clear all the four directions with the OFF color, and do another WAIT_ONE_SECOND(). This will create the effect of flashing the RED color in all directions.

That completes the implementation of the Do_Flashing() routine.

In addition, to update the status of the ‘FR’ and ‘FS’ fields on the LCD, add the following lines in the update_LCD_misc() routine:

if (FLASHING _REQUEST == 0) FlashingR_Txt[0] = ‘0’; else FlashingR_Txt[0] = ‘1’; if (FLASHING == 0) FlashingS_Txt[0] = ‘0’; else FlashingS_Txt[0] = ‘1’;

</div>
</div>
</div>
