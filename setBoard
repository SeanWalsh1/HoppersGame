import java.applet.*;
import java.awt.*;
import javax.swing.*;
import java.util.*;
import java.lang.String;
import javax.swing.JCheckBox;
import java.awt.event.MouseEvent;
import java.awt.event.*;
import javax.swing.*;
import javax.swing.JApplet;
import java.util.ArrayList;

/**
 * This class is used in order to set the board
 * based upon the users input. It references the
 * other classes in order to get the starting board
 * states, as well as the solver in order to determine
 * possible and legal jumps.
 * 
 * @author Sean Walsh, Kevin Conner
 * @author Andrew Ashline, Kaitlyn Boomhower 
 * @version 1.0
 */
public class setBoard extends JApplet implements
MouseListener, MouseMotionListener
{
    //creates images for the frogs to be placed
    Image image, image0, image1, image2, image3,
    image4, image5, image6, image7, image8, image9,
    image10, image11, image12;

    //creates images for the lily pads
    Image pad0, pad1, pad2, pad3, pad4, pad5, pad6,
    pad7, pad8, pad9, pad10, pad11, pad12; 

    //instance of checkBox
    checkBox checkB = new checkBox();

    //int arrays used to set the board
    private int[] numOfFrogs;
    private int[] board;

    //instances of playBoard
    private playBoard pBoard = new playBoard();
    private playBoard Mboard = new playBoard();

    //instance of Point called p
    private Point p;
    
    //boolean variable if the player has won
    private boolean win = false;
    
    //int variables to set the board and user action
    private int clicked = 0;
    private int first, last;
    private int red;
    private int numHop;

    //String arraylist done
    private ArrayList<String> done;
    //FrogSound soundfile
    private String soundfile = "frogSound.wav";
    /**
     * This method is used in order to show the
     * applet to the user. It references checkBoxes
     * as well as methods in the playBoard class.
     * It also adds the mouseListener and sets the
     * size of the applet window.
     */
    public void init()
    {
        //reference to checkBoxes class
        numOfFrogs = checkB.checkBoxes();

        //reference to the playBord class
        board = pBoard.doBoard(numOfFrogs);

        addMouseListener(this); 

        setSize(562,750); 
    }

    /**
     * This method is used to create all the graphics
     * as well as set the board with the red and green
     * frog images as well as the lily pad images.
     * 
     * @param Graphics reference
     */
    public void paint(Graphics g )
    {
        //gets the background image and draws the image on
        image = getImage(getCodeBase(),
            "HoppersBoard.png");
        g.drawImage(image,0,0,this);

        //reference to playBoard
        numOfFrogs = pBoard.swap(board);

        //int variables used for incrementing
        int count = 0;
        int counter =0;

        //counts the number of frogs in numOfFrogs
        for(int i = 0; i< numOfFrogs.length; i++){
            if ( numOfFrogs[i] != -1){
                count++;
            }
        }

        //sets numHop to the count
        numHop = count;

        //if statement to determine if user has won
        if(count==1)
        {
            win = true;
            JOptionPane.showMessageDialog(null,
                "You Win!", "End Game",
                JOptionPane.PLAIN_MESSAGE);
                
        }

        //for loop used to set the board with frogs
        for(int i = 0; i < numOfFrogs.length; i++){
            if( numOfFrogs[1] == -1)
            {
                continue;
            }
            else if( numOfFrogs [i] == 0 ){
                counter++;
                if (counter != count){
                    image0 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image0,45,30,this); 
                }
                else{
                    red = i;
                    image0 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image0,45,30,this); 
                }
            }
            else if( numOfFrogs [i] == 1){
                counter++;
                if (counter != count){
                    image1 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image1,224,28,this);
                }
                else{

                    image1 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image1,224,30,this);
                }
            }
            else if( numOfFrogs [i] == 2){
                counter++;
                if (counter != count){
                    image2 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image2,415,30,this); 
                }
                else{
                    image2 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image2,415,30,this); 
                }
            }
            else if( numOfFrogs [i] == 3){
                counter++;
                if (counter != count){
                    image3 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image3,129,157,this); 
                }
                else{
                    image3 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image3,129,157,this); 
                }
            }
            else if( numOfFrogs [i] == 4){
                counter++;
                if (counter != count){
                    image4 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image4,330,160,this);
                }
                else{
                    image4 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image4,330,160,this);
                }
            }
            else if( numOfFrogs [i] == 5){
                counter++;
                if (counter != count){
                    image5 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image5,25,280,this); 
                }
                else{
                    image5 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image5,25,280,this);
                }
            }
            else if( numOfFrogs [i] == 6){
                counter++;
                if (counter != count){
                    image6 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image6,228,280,this);
                }
                else{
                    image6 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image6,228,280,this);
                }
            }
            else if( numOfFrogs [i] == 7){
                counter++;
                if (counter != count){
                    image7 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image7,434,282,this);
                }
                else{
                    image7 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image7,434,282,this);
                }
            }
            else if( numOfFrogs [i] == 8){
                counter++;
                if (counter != count){
                    image8 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image8,119, 424,this);
                }
                else{
                    image8 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image8,119, 424,this);
                }

            }
            else if( numOfFrogs [i] == 9){
                counter++;
                if (counter != count){
                    image9 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image9,333, 424,this);
                }
                else{
                    image9 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image9,333, 424,this); 
                }
            }
            else if( numOfFrogs [i] == 10){
                counter++;
                if (counter != count){
                    image10 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image10, 41, 562,this);
                }
                else{
                    image10 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image10, 41, 562,this);
                }
            }
            else if( numOfFrogs [i] == 11){
                counter++;
                if (counter != count){
                    image11 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image11, 240, 566,this);
                }
                else{
                    image11 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image11, 240, 566,this);
                }
            }
            else if( numOfFrogs [i] == 12){
                counter++;
                if (counter != count){
                    image12 = getImage(getCodeBase(),
                        "greenFrogcopy.png");
                    g.drawImage(image12, 422, 568,this);
                }
                else{
                    image12 = getImage(getCodeBase(),
                        "redFrogcopy.png");
                    g.drawImage(image12, 422, 568,this);
                }
            }
        }

        //hint for users next move
        g.drawString("Click Me For A Good Move",0, 750);
        showStatus(("I Wonder What To Do? Is There Even A Solution"));

        //method call to possibleM
        possibleM();
    }

    /**
     * This method is used in order to help
     * determine whether or not a move is possible
     * and is used in order to help create a hint
     * for the user if wanted.
     */
    public void possibleM()
    {
        //boolean variable initialized to false
        boolean movesLeft = false;

        //for loop to check possible moves
        for(int i = 0; i<13; i++)
        {
            for(int j = 0; j<13; j++)
            {
                movesLeft = pBoard.isPossible(pBoard.board, i, j);
                if(movesLeft == true)
                {
                    break;
                }
            }
            if(movesLeft == true)
            {
                break;
            }
        }

        //if no possible moves tell user they have lost
        if((movesLeft == false)&&(!win))
        {
            JOptionPane.showMessageDialog(null,
                "You Lost!", "End Game",
                JOptionPane.PLAIN_MESSAGE);
        }
    }

    /**
     * This method is used when
     * the mouse has been pressed
     * in the window.
     * 
     * @param MouseEvent e used for mouseListener
     */
    public void mousePressed(MouseEvent e){}

    /**
     * This method is used when
     * the mouse exits the window.
     * 
     * @param MouseEvent e used for mouseListener
     */
    public void mouseExited(MouseEvent e){}

    /**
     * This method is used when
     * the mouse is dragged in the window.
     * 
     * @param MouseEvent e used for mouseListener
     */
    public void mouseDragged(MouseEvent e){}

    /**
     * This method is used when
     * the mouse is moved in the window.
     * 
     * @param MouseEvent e used for mouseListener
     */
    public void mouseMoved(MouseEvent e){}

    /**
     * This method is used when
     * the mouse has entered the window.
     * 
     * @param MouseEvent e used for mouseListener
     */
    public void mouseEntered (MouseEvent e){} 

    /**
     * This method is used when
     * the mouse has been clicked.It gets the 
     * coordinates of the click and based off
     * of that point, it will reference the 
     * click method and increment a counter or
     * it will get the next suggested move. Another
     * point to make is that a right click will 
     * reset the click counter to 0 if the user has
     * accidently clicked in the wrong location.
     * 
     * @param MouseEvent e used for mouseListener
     */
    public void mouseClicked (MouseEvent e) 
    {
        //if point within bounds gets next
        //possible move
        if (e.getX()<80 && e.getY()>710  ){
            done = Mboard.getSolution(Mboard.doBoard(numOfFrogs),
                numHop);

            showStatus(("Next Suggested Move: ") + done.get(0));

        }

        //if right clicked reset counter to 0
        //else get point location and reference
        //click method and increment counter
        if(SwingUtilities.isRightMouseButton(e))
        {
            clicked = 0;
        }
        else
        {
            int xCoor;
            int yCoor;  

            if(clicked == 0)
            {

                if((e.getX()>45&&e.getX()<127)&&
                (e.getY()>30&&e.getY()<114))
                {
                    clicked++;
                    click(0);
                }

                if((e.getX()>224&&e.getX()<307)&&
                (e.getY()>28&&e.getY()<114))
                {
                    clicked++;
                    click(1);
                }

                if((e.getX()>415&&e.getX()<519)&&
                (e.getY()>30&&e.getY()<114))
                {
                    clicked++;
                    click(2);
                }

                if((e.getX()>129&&e.getX()<221)&&
                (e.getY()>157&&e.getY()<241))
                {
                    clicked++;
                    click(3);
                }

                if((e.getX()>330&&e.getX()<423)&&
                (e.getY()>160&&e.getY()<234))
                {
                    clicked++;
                    click(4);
                }

                if((e.getX()>25&&e.getX()<124)&&
                (e.getY()>280&&e.getY()<366))
                {
                    clicked++;
                    click(5);
                }

                if((e.getX()>228&&e.getX()<319)&&
                (e.getY()>280&&e.getY()<371))
                {
                    clicked++;
                    click(6);
                }

                if((e.getX()>434&&e.getX()<524)&&
                (e.getY()>282&&e.getY()<373))
                {
                    clicked++;
                    click(7);
                }

                if((e.getX()>119&&e.getX()<219)&&
                (e.getY()>424&&e.getY()<506))
                {
                    clicked++;
                    click(8);
                }

                if((e.getX()>333&&e.getX()<423)&&
                (e.getY()>424&&e.getY()<501))
                {
                    clicked++;
                    click(9);
                }

                if((e.getX()>41&&e.getX()<131)&&
                (e.getY()>562&&e.getY()<633))
                {
                    clicked++;
                    click(10);
                }

                if((e.getX()>240&&e.getX()<319)&&
                (e.getY()>566&&e.getY()<637))
                {
                    clicked++;
                    click(11);
                }

                if((e.getX()>422&&e.getX()<516)&&
                (e.getY()>568&&e.getY()<636))
                {
                    clicked++;
                    click(12);
                }

            }
            else 
            {
                if((e.getX()>50&&e.getX()<135)&&
                (e.getY()>32&&e.getY()<122))
                {
                    clicked++;
                    click(0);
                }

                if((e.getX()>230&&e.getX()<315)&&
                (e.getY()>34&&e.getY()<124))
                {
                    clicked++;
                    click(1);
                }

                if((e.getX()>441&&e.getX()<526)&&
                (e.getY()>31&&e.getY()<121))
                {
                    clicked++;
                    click(2);
                }

                if((e.getX()>143&&e.getX()<228)&&
                (e.getY()>161&&e.getY()<251))
                {
                    clicked++;
                    click(3);
                }

                if((e.getX()>347&&e.getX()<432)&&
                (e.getY()>152&&e.getY()<242))
                {
                    clicked++;
                    click(4);
                }

                if((e.getX()>46&&e.getX()<131)&&
                (e.getY()>285&&e.getY()<375))
                {
                    clicked++;
                    click(5);
                }

                if((e.getX()>240&&e.getX()<325)&&
                (e.getY()>288&&e.getY()<378))
                {
                    clicked++;
                    click(6);
                }

                if((e.getX()>447&&e.getX()<532)&&
                (e.getY()>292&&e.getY()<382))
                {
                    clicked++;
                    click(7);
                }

                if((e.getX()>140&&e.getX()<225)&&
                (e.getY()>425&&e.getY()<515))
                {
                    clicked++;
                    click(8);
                }

                if((e.getX()>347&&e.getX()<432)&&
                (e.getY()>420&&e.getY()<510))
                {
                    clicked++;
                    click(9);
                }

                if((e.getX()>53&&e.getX()<138)&&
                (e.getY()>552&&e.getY()<642))
                {
                    clicked++;
                    click(10);
                }

                if((e.getX()>241&&e.getX()<326)&&
                (e.getY()>558&&e.getY()<648))
                {
                    clicked++;
                    click(11);
                }

                if((e.getX()>440&&e.getX()<525)&&
                (e.getY()>554&&e.getY()<644))
                {
                    clicked++;
                    click(12);
                }
            }
        }  
    }

    /**
     * This method is used to help hop frogs
     * over each other. It repaints the image
     * and calls the playBoard clas in order 
     * to determine the possible jump.
     * 
     * @param int value for location on board
     */
    public void click(int im)
    {
        //boolean variable initialized to false
        boolean move = false;

        //if clicked is 1 set first to im and repaint
        if(clicked==1)
        {
            first = im;
            repaint();
        }
        else
        {
            //set last to im
            last = im;

            //determine move on board
            move = pBoard.isPossible(board, first, last);

            //if move is true jump frogs
            if(move)
            {
                board = pBoard.hopped(board, first, last);
                clicked = 0;
                //plays the frog sound when a frog is jumped
                play( getDocumentBase(), soundfile );
                repaint();
            }
            else
            {
                //error message saying move not possible
                JOptionPane.showMessageDialog(null,
                    "Move Not Possible", "",
                    JOptionPane.PLAIN_MESSAGE);
                clicked = 0;
                repaint();
            }
        }
    }

    /**
     * This method is used when
     * the mouse is released in the window.
     * 
     * @param MouseEvent e used for mouseListener
     */
    public void mouseReleased(MouseEvent e){} 
}
