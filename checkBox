import javax.swing.JCheckBox;
import javax.swing.JOptionPane;
import java.util.*;
import java.applet.*;
import javax.swing.*;

/**
 * This class is used to create all the JOptionPane pop up boxes
 * that are used to select all the frogs, select the red frog, as
 * well as tell the user if they have won or lost. The user wins
 * if only the red frog is left on the board, the user loses if
 * there is no possible way to win based on the game solver.
 * 
 * @author Sean Walsch, Andrew Ashline
 * @author Kaitlyn Boomhower, Kevin Conner
 * @version 1.0
 */
public class checkBox extends JApplet
{
    /**
     * Constructor for objects of class Test
     */
    public checkBox()
    {

    }

    /**
     * This method is used in order to create and show the
     * JOptionPane pop up boxes which are used to have the 
     * used place all frogs, the red frog, and tell the user if 
     * they have won the game or lost due to there being no way
     * for them to win.
     * 
     * @return an int array used for frog placement 
     */
    public int[] checkBoxes()
    {
        //arraylist toReturn
        int[] toReturn = new int[13];
        ArrayList<Integer> toReturnAL = new ArrayList<Integer>();

        //boolean array used to determin frog location
        boolean[] frogLocale = new boolean[13];
        boolean[] redFrogLocale = new boolean[13];

        int[] addInToReturn = new int[13];

        //used to reset red frog to end of array
        int redFrogPosition = 0;

        //adds checkbox for joptionpane
        JCheckBox pad0 = new JCheckBox("Pad1");
        JCheckBox pad1 = new JCheckBox("Pad2");
        JCheckBox pad2 = new JCheckBox("Pad3");
        JCheckBox pad3 = new JCheckBox("Pad4");
        JCheckBox pad4 = new JCheckBox("Pad5");
        JCheckBox pad5 = new JCheckBox("Pad6");
        JCheckBox pad6 = new JCheckBox("Pad7");
        JCheckBox pad7 = new JCheckBox("Pad8");
        JCheckBox pad8 = new JCheckBox("Pad9");
        JCheckBox pad9 = new JCheckBox("Pad10");
        JCheckBox pad10 = new JCheckBox("Pad11");
        JCheckBox pad11 = new JCheckBox("Pad12");
        JCheckBox pad12 = new JCheckBox("Pad13");

        //string variables used for message display
        String message = "Please select frog starting locations";
        String redFrogMessage = "Please select which is the red frog";

        Object[] locales = {message, pad0, pad1, pad2, pad3,
                pad4, pad5, pad6, pad7, pad8, pad9, pad10,
                pad11, pad12};

        //Have to make fourteen to incorporate redfrogmessage
        Object[] locales2 = new Object[14];
        locales2[0] = redFrogMessage;

        //JOptionPane pop up for user input
        int frog = JOptionPane.showConfirmDialog(null,locales,
                "Set Frogs", JOptionPane.DEFAULT_OPTION,
                JOptionPane.PLAIN_MESSAGE);

        //to determine if user has input too many frogs
        int userCheckedFrogs = 0;

        //nested if statements to determine selected frogs
        if (frog == JOptionPane.OK_OPTION)
        { 
            if(pad0.isSelected() == true)
            {
                frogLocale[0] = true;
                addInToReturn[0] = 0;
                locales2[1] = pad0;
                pad0.setSelected(false);
                userCheckedFrogs++;
            }
            if(pad1.isSelected() == true)
            {
                frogLocale[1] = true;
                addInToReturn[1] = 1;
                locales2[2] = pad1;
                pad1.setSelected(false);
                userCheckedFrogs++;
            }
            if(pad2.isSelected() == true)
            {
                frogLocale[2] = true;
                addInToReturn[2] = 2;
                locales2[3] = pad2;
                pad2.setSelected(false);
                userCheckedFrogs++;
            }
            if(pad3.isSelected() == true)
            {
                frogLocale[3] = true;
                addInToReturn[3] = 3;
                locales2[4] = pad3;
                pad3.setSelected(false);
                userCheckedFrogs++;
            }
            if(pad4.isSelected() == true)
            {
                frogLocale[4] = true;
                addInToReturn[4] = 4;
                locales2[5] = pad4;
                pad4.setSelected(false);
                userCheckedFrogs++;
            }
            if(pad5.isSelected() == true)
            {
                frogLocale[5] = true;
                addInToReturn[5] = 5;
                locales2[6] = pad5;
                pad5.setSelected(false);
                userCheckedFrogs++;
            }
            if(pad6.isSelected() == true)
            {
                frogLocale[6] = true;
                addInToReturn[6] = 6;
                locales2[7] = pad6;
                pad6.setSelected(false);
                userCheckedFrogs++;
            }
            if(pad7.isSelected() == true)
            {
                frogLocale[7] = true;
                addInToReturn[7] = 7;
                locales2[8] = pad7;
                pad7.setSelected(false);
                userCheckedFrogs++;
            }
            if(pad8.isSelected() == true)
            {
                frogLocale[8] = true;
                addInToReturn[8] = 8;
                locales2[9] = pad8;
                pad8.setSelected(false);
                userCheckedFrogs++;
            }
            if(pad9.isSelected() == true)
            {
                frogLocale[9] = true;
                addInToReturn[9] = 9;
                locales2[10] = pad9;
                pad9.setSelected(false);
                userCheckedFrogs++;
            }
            if(pad10.isSelected() == true)
            {
                frogLocale[10] = true;
                addInToReturn[10] = 10;
                locales2[11] = pad10;
                pad10.setSelected(false);
                userCheckedFrogs++;
            }
            if(pad11.isSelected() == true)
            {
                frogLocale[11] = true;
                addInToReturn[11] = 11;
                locales2[12] = pad11;
                pad11.setSelected(false);
                userCheckedFrogs++;
            }
            if(pad12.isSelected() == true)
            {
                frogLocale[12] = true;
                addInToReturn[12] = 12;
                locales2[13] = pad12;
                pad12.setSelected(false);
                userCheckedFrogs++;
            }
        }

        //checks to see if too many frogs selected
        if(userCheckedFrogs > 12)
        {
            JOptionPane.showMessageDialog(null,
                "You Can Only Place At Most 12 Frogs",
                "Alert", JOptionPane.WARNING_MESSAGE);

            int[] work = checkBoxes();
            return work;
        }

        //for loop that adds in each frog into an arraylist
        for(int i = 0; i < addInToReturn.length; i++)
        {
            if(frogLocale[i] == true)
            {
                toReturnAL.add(addInToReturn[i]);
            }
        }

        //red frog selector JOptionPane
        int redfrog = JOptionPane.showConfirmDialog(null,
                locales2, "Set Red Frog",
                JOptionPane.DEFAULT_OPTION,
                JOptionPane.PLAIN_MESSAGE);

        //checks to see if too many red frogs selected
        int userCheckedRed = 0;

        //nested if statements to determine which red frog selected
        if (redfrog == JOptionPane.OK_OPTION)
        { 
            if(pad0.isSelected() == true)
            {
                redFrogLocale[0] = true;
                userCheckedRed++;
            }
            if(pad1.isSelected() == true)
            {
                redFrogLocale[1] = true;
                userCheckedRed++;
            }
            if(pad2.isSelected() == true)
            {
                redFrogLocale[2] = true;
                userCheckedRed++;
            }
            if(pad3.isSelected() == true)
            {
                redFrogLocale[3] = true;
                userCheckedRed++;
            }
            if(pad4.isSelected() == true)
            {
                redFrogLocale[4] = true;
                userCheckedRed++;
            }
            if(pad5.isSelected() == true)
            {
                redFrogLocale[5] = true;
                userCheckedRed++;
            }
            if(pad6.isSelected() == true)
            {
                redFrogLocale[6] = true;
                userCheckedRed++;
            }
            if(pad7.isSelected() == true)
            {
                redFrogLocale[7] = true;
                userCheckedRed++;
            }
            if(pad8.isSelected() == true)
            {
                redFrogLocale[8] = true;
                userCheckedRed++;
            }
            if(pad9.isSelected() == true)
            {
                redFrogLocale[9] = true;
                userCheckedRed++;
            }
            if(pad10.isSelected() == true)
            {
                redFrogLocale[10] = true;
                userCheckedRed++;
            }
            if(pad11.isSelected() == true)
            {
                redFrogLocale[11] = true;
                userCheckedRed++;
            }
            if(pad12.isSelected() == true)
            {
                redFrogLocale[12] = true;
                userCheckedRed++;
            }
        }

        //checks to see if too many red frogs selected
        if((userCheckedRed > 1) || (userCheckedRed == 0))
        {
            JOptionPane.showMessageDialog(null,
                "You Must Select 1 Red Frog, Please Start Again",
                "Alert", JOptionPane.WARNING_MESSAGE);

            int[] work = checkBoxes();
            return work;
        }

        //for loop to determine the location of red frog input by user
        for(int i = 0; i < redFrogLocale.length; i++)
        {
            if(redFrogLocale[i] == true)
            {
                redFrogPosition = i;
            }
        }

        //for loop that changes red frog location to last in array
        for(int i = 0; i < toReturnAL.size(); i++)
        {
            if(toReturnAL.get(i) == redFrogPosition)
            {
                toReturnAL.remove(i);
                toReturnAL.add(redFrogPosition);
            }
        }

        //for loop that transfers contents of arraylist to an array
        for(int i = 0; i < toReturnAL.size(); i++)
        {
            toReturn[i] = toReturnAL.get(i);
        }

        //makes rest of toReturn -1
        for(int x = toReturnAL.size(); x<toReturn.length; x++)
        {
            toReturn[x] = -1;
        }

        //return int array
        return toReturn;
    }
}
