Download Link: https://assignmentchef.com/product/solved-cosc2135-assignment-1
<br>
<strong>This assessment requires you to apply various concepts and techniques covered in weeks 1–4 of the course, in order </strong><strong>to assemble a programmatic solution for a problem based on a simulated real-world scenario.</strong>

<strong>An important part of your development as a programmer is the ability to identify and apply appropriate techniques </strong><strong>or programming structures when implementing the various aspects of a programmatic solution to a given problem, </strong><strong>so in addition to the basic functional requirements of this task, you will also be assessed on your ability to select </strong><strong>and utilise appropriate techniques and structures in your solution.</strong>

<strong>This assessment requires you to design and create a Java program to solve analysed stakeholder (user and </strong><strong>supervisor) requirements.</strong>




<strong>Course learning outcomes</strong>

<strong>This assessment is relevant to the following course learning outcomes:</strong>

<ul>

 <li><strong>CLO 1: Solve simple algorithmic computing problems using basic control structures and Object-Oriented </strong><strong>Techniques</strong></li>

 <li><strong>CLO 2: Design and implement computer programs based on analysing and modelling requirements</strong></li>

 <li><strong>CLO 3: Identify and apply basic features of an Object-Oriented programming language through the use of </strong><strong>standard Java (Java SE) language constructs and APIs</strong></li>

 <li><strong>CLO 4: Identify and apply good programming style based on established standards, practices and coding </strong><strong>guidelines</strong></li>

 <li><strong>CLO 5: Devise and apply strategies to test the developed software</strong></li>

</ul>




<table>

 <tbody>

  <tr>

   <td width="745"><strong>Assessment Details</strong><strong>Your task is to produce, using standard Java, a prototype booking management system for ‘Direct Coaches </strong><strong>Australia (DCA)’, a (fictitious) regional coach service.</strong><strong>Edited interviews with Lauren, the manager of DCA and Abhijeet, the booking clerk have been provided. You should analyse the interviews to determine the functional requirements for your program. Your development-team supervisor has provided further requirements. These requirements are set out in the </strong><strong>three stages (A, B and C) below. Since each stage elaborates on the previous one, you only need to submit </strong><strong>one program – the one implementing the highest stage you were able to complete.</strong><strong>The functionality of each stage will be tested on test-case described in TestCases.pdf, which can be found </strong><strong>on the course Canvas under the Assignment 1 link.</strong><strong>For each of the stages A, B and C, complete the steps below based on the Double Diamond process: </strong><strong>Discover</strong><strong>‘Go wide’ in the form of reading and thinking about the supplied stakeholder requirements. Find out what </strong><strong>the current situation is and understand user behaviours and business drivers.</strong><strong>Fill in the supplied ‘Discover and Define’ Word template with a list of different problems that could be </strong><strong>solved.</strong><strong>Define</strong><strong>From your understanding of the overall issues/requirements, narrow down to a single problem and turn that </strong><strong>into a problem statement. The problem statement defines what you will develop, and you may start some </strong><strong>initial coding to start working out if you can create a solution to the problem you defined.</strong><strong>Fill in the supplied ‘Discover and Define’ Word template with a statement of the single problem you will </strong><strong>solve.</strong><strong>Develop</strong><strong>Start coding to create an initial prototype and program logic to address the problem. You may create a few </strong><strong>different iterations to get to the best prototype. This is a phase for trying ideas out to see if they work.</strong><strong>Deliver</strong><strong>Pick the best prototype from the ‘Develop’ phase and create the final version of the code, refining and </strong><strong>making it work. The aim is to create a minimum viable product (MVP) to address the problem you have </strong><strong>identified and defined. The final result of this process at stage C will become your final submission for </strong><strong>assessment 1.</strong><strong>How to use the Double Diamond will be explained in the course webinar, please ask your instructor if you </strong><strong>have any questions.</strong></td>

  </tr>

 </tbody>

</table>




<strong>Stage A – Basic coach booking system</strong>

<strong>Your task here is to discover and define the problem and then develop a console-driven Java program which </strong><strong>implements the functional requirements derived from the interviews and instructions given below.</strong>

<strong>Lauren – DCA Manager</strong>

<strong>“In this initial project we’ll only focus on managing booking for a single coach. The prototype will be </strong><strong>used by myself and the booking clerks. On start-up, the prototype should ask for the number of rows </strong><strong>in the coach, the coach destination, and the seat price category for travelling to that destination. Our </strong><strong>coaches have four seats per row (two on either side of a central isle). There are three price categories</strong>

<strong>for a seat: standard (S) which is full fare, pensioner (P), and discounted frequent customers (F).</strong>

<strong>Once initialised, I’d like the prototype to be able to display the number of available seats on the coach </strong><strong>and also be able to book seats and to refund seats. A booking/refund receipt should be produced </strong><strong>when booking or refunding seats. I’d like the booking/refund receipt format to be the same as what </strong><strong>we currently produce:</strong>

<strong>Receipt ******* Destination : xxxxxxxxxxxxxxx</strong>

<strong>Number of seats booked : x</strong>

<table>

 <tbody>

  <tr>

   <td width="181"><strong>xx *</strong></td>

   <td width="73"><strong>Standard</strong></td>

   <td width="74"><strong>@ $xx.xx</strong></td>

   <td width="21"><strong>=</strong></td>

   <td width="15"><strong>$</strong></td>

   <td width="351"><strong>xx.xx</strong></td>

  </tr>

  <tr>

   <td width="181"><strong>xx *</strong></td>

   <td width="73"><strong>Pensioner</strong></td>

   <td width="74"><strong>@ $xx.xx</strong></td>

   <td width="21"><strong>=</strong></td>

   <td width="15"><strong>$</strong></td>

   <td width="351"><strong>xx.xx</strong></td>

  </tr>

  <tr>

   <td width="181"><strong>xx *</strong></td>

   <td width="73"><strong>Frequent</strong></td>

   <td width="74"><strong>@ $xx.xx</strong></td>

   <td width="21"><strong>=</strong></td>

   <td width="15"><strong>$</strong></td>

   <td width="351"><strong>xx.xx</strong></td>

  </tr>

 </tbody>

</table>




<strong>Total : $xxx.xx</strong>

<strong>I’d also like to be able to produce a statistics report detailing the number of seats booked, the </strong><strong>percentage of seats booked and the average price of the booked seats.</strong>

<strong>I’d like to be able to keep selecting from these options until I choose to exit the system.”</strong>

<strong>Abhijeet – DCA Booking Clerk</strong>

<strong>“I take seat bookings and provide refunds from cancellations. All I need to know for booking a seat is </strong><strong>the number of seats required, and the price category for each seat (standard, pensioner or frequent </strong><strong>traveller). I have to be careful to ensure there are enough seats available on the coach to fulfil the </strong><strong>booking so it would be good if the system could automate that.</strong>

<strong>Refunds are similar to booking, as I need to enter the number of seats to refund and, for each seat,</strong>

<strong>what price to refund (standard, pensioner or frequent traveller). Although I’m referring to the customer’s hard-copy receipt while doing this, it would still help if the system could automatically</strong>

<strong>check that the quantity of each seat category being claimed for refund isn’t more than the total number of that seat type currently booked. For example, if the coach has 3 pensioner bookings in </strong><strong>total, a customer shouldn’t be able to claim a refund for 4 pensioner seats.”</strong>

<strong>Supervisor directives</strong>

<table>

 <tbody>

  <tr>

   <td width="164">

    <table width="100%">

     <tbody>

      <tr>

       <td></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<strong>Your supervisor advises that your program should prompt the user to enter the required information in a</strong>




<strong>user-friendly manner, read those values in from the console and store the corresponding values in variables </strong><strong>of appropriate types. Displayed output should be neatly tabulated.</strong>

<strong>Your program for this stage should be implemented as a single class. You will have the opportunity to implement an Object-Oriented design in stage C. Please note that ArrayLists and other Java Collection </strong><strong>Framework classes are not permitted and only concepts covered from weeks 1..3 should be utilised.</strong>

<strong>Stage B – Booking System tracking individual coach seats</strong>

<strong>Your task here is to extend your console-driven Java program to implement the functional requirements </strong><strong>derived from the interviews and instructions given below.</strong>

<strong>Lauren – DCA Manager</strong>

<strong>“For this stage I’d like the prototype to be able to display the status of individual coach seats, in </strong><strong>addition to giving the number of available seats. For each seat, I’d like the seat number and status </strong><strong>(one of ‘-‘ for not booked, ‘B’ for booked) to be displayed. Our seat numbering is simply an integer, </strong><strong>starting at zero from the front left-hand (looking out of the coach) window seat and incrementing</strong>

<strong>across each row. For example, our smaller coach of 5 rows (i.e. 20 seats) with only seat 6 booked </strong><strong>should have a display of:</strong>

<table>

 <tbody>

  <tr>

   <td width="156"><strong>0:-</strong></td>

   <td width="36"><strong>1:-</strong></td>

   <td width="37"><strong>2:-</strong></td>

   <td width="485"><strong>3:-</strong></td>

  </tr>

  <tr>

   <td width="156"><strong>4:-</strong></td>

   <td width="36"><strong>5:-</strong></td>

   <td width="37"><strong>6:B</strong></td>

   <td width="485"><strong>7:-</strong></td>

  </tr>

  <tr>

   <td width="156"><strong>8:-</strong></td>

   <td width="36"><strong>9:-</strong></td>

   <td width="37"><strong>10:-</strong></td>

   <td width="485"><strong>11:-</strong></td>

  </tr>

  <tr>

   <td width="156"><strong>12:-</strong></td>

   <td width="36"><strong>13:-</strong></td>

   <td width="37"><strong>14:-</strong></td>

   <td width="485"><strong>15:-</strong></td>

  </tr>

  <tr>

   <td width="156"><strong>16:-</strong></td>

   <td width="36"><strong>17:-</strong></td>

   <td width="37"><strong>18:-</strong></td>

   <td width="485"><strong>19:-</strong></td>

  </tr>

 </tbody>

</table>




<strong>Number of available seats: 19</strong>

<strong>“</strong>

<strong>Abhijeet – DCA Booking Clerk</strong>

<strong>“We’ve experienced several cases where a refund for a cheaper seat type has accidently been put </strong><strong>through as a higher-priced seat type. Now that the prototype will track the state of individual seats,</strong>

<strong>I’d like to change how refunds are performed. Instead of me and other booking clerks having to </strong><strong>enter the seat type being refunded, I’d like to just enter the number of the seat and have the system </strong><strong>work out how much to refund. For example if seat number 6 had been booked as a Standard seat, </strong><strong>then requesting to refund seat 6 should automatically refund the price for the Standard seat type.</strong>

<strong>I’d also find it helpful if the booking/refund receipt displayed the seat number(s) being </strong><strong>booked/refunded. For example, if a booking for 3 seats had seats 6 and 7 booked as type Standard </strong><strong>and seat 5 as Frequent Traveller, the receipt format should be:</strong>




<table>

 <tbody>

  <tr>

   <td width="215">

    <table width="100%">

     <tbody>

      <tr>

       <td><strong>Receipt</strong><strong>*******</strong><strong>Destination : xxxxxxxxxxxxxxx</strong><strong>Number of seats booked : x</strong><strong>2 * Standard @ $xx.xx</strong><strong>0 * Pensioner @ $xx.xx</strong><strong>1 * Frequent @ $xx.xx</strong></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<table>

 <tbody>

  <tr>

   <td width="305">

    <table width="100%">

     <tbody>

      <tr>

       <td>


        <table>

         <tbody>

          <tr>

           <td width="25"><strong>= $= $= $</strong></td>

           <td width="48"><strong>xx.xxxx.xxxx.xx</strong></td>

           <td width="68"><strong>seat(s):seat(s):seat(s):</strong></td>

           <td width="22"><strong>6,5,</strong></td>

           <td width="138"><strong>7,</strong></td>

          </tr>

         </tbody>

        </table> </td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>




<strong>Total : $xxx.xx</strong>

<strong>“</strong>

<strong>Supervisor directives</strong>

<strong>Your supervisor advises that your program </strong><strong><u>must</u></strong><strong> utilise a 1D array called seats of char type for storing the </strong><strong>status of the coach seats, with ‘not booked’ being indicated with ‘-‘, ‘booked Standard’ with ‘S’, ‘booked </strong><strong>Pensioner’ with ‘P’ and ‘booked Frequent Traveller’ with ‘F’. Please note that ArrayLists and other Java </strong><strong>Collection Framework classes are not permitted and only concepts covered from weeks 1..3 should be </strong><strong>utilised.</strong>

<strong>The lists of booked or refunded seat(s) displayed on the receipt must be implemented as a string for each </strong><strong>seat type. For example, the receipt example given in stage B would have a single string “6, 7,” representing </strong><strong>the Standard seats, a single empty string “” representing the Pensioner seats and a single string “5,” </strong><strong>representing the Frequent seats.</strong>

<strong>You program for this stage should be implemented as a single class. You will have the opportunity to </strong><strong>implement an Object-Oriented design in stage C.</strong>

<strong>Stage C – Object-Oriented implementation of the booking system</strong>

<strong>Supervisor directives</strong>

<strong>Your supervisor advises that you should remodel your stage B Java program to use two classes, StageC and </strong><strong>Coach, to provide the functionality specified in stage B.</strong>

<strong>Class StageC implements the main method. It collects user information and calls methods in the Coach class </strong><strong>to implement the functionality of stage B. Note that StageC is obtains all responses from the user. If the</strong>

<strong>Coach class requires user input, the StageC class must collect the input from the user and pass it to the Coach </strong><strong>via arguments to Coach methods.</strong>

<strong>Class Coach contains the seats array and stores and manipulates all information about the state of the coach. </strong><strong>It hides this information, providing methods for manipulating or displaying the data without revealing the </strong><strong>underlying data structures. It also provides methods for calculating and displaying the receipts and statistics </strong><strong>report.</strong>

<strong>For the purposes of this stage, object oriented technique involves satisfying all the following criteria:</strong>

<ul>

 <li><strong>Appropriate choice of classes and methods as per good object-oriented programming practice</strong></li>

 <li><strong>Appropriate private instance variables and/or constants defined for all required values</strong></li>

 <li><strong>Variables required only within a method are defined locally</strong></li>

 <li></li>

</ul>

<table>

 <tbody>

  <tr>

   <td width="164">

    <table width="100%">

     <tbody>

      <tr>

       <td></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<ul>

 <li><strong>Visibility of instance variables set to private as per good object-oriented programming practice</strong></li>

</ul>




<strong>Please note that ArrayLists and other Java Collection Framework classes are not permitted and only concepts </strong><strong>covered from weeks 1..3 should be utilised.</strong>