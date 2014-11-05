import java.util.ArrayList;
import java.applet.*;
import javax.swing.*;

/**
 * This class is used as the game solver for Hoppers.
 * It uses a 3-D array to determine possible moves as
 * well as if the game is possible to win or not.
 * 
 * @author Andy Ashline, Sean Walsch
 * @author Kevin Conner, Kaitlyn Boomhower
 * @version 1.0
 */
public class playBoard 
{
    //int array named board
    protected int[] board = new int[13];

    //int value for index of the red hopper
    protected int red;

    // arraylist of type string for the moves taken
    protected ArrayList<String> moves = new ArrayList<String>();

    //3-D array for the 30 different moves
    protected int[][][] posMoves = new int[13][13][13];

    //int variable h for number of hoppers on board
    protected int h;

    /**
     * Constructor for objects of type playBoard.
     */
    public playBoard()
    {
        //sets the board to zero
        for(int i = 0; i<13; i++)
        {
            board[i] = 0;
        }

        //initializes the 30 possible moves
        posMoves[0][1][2] = 1;
        posMoves[0][5][10] = 1;
        posMoves[0][3][6] = 1;
        posMoves[1][3][5] = 1;
        posMoves[1][4][7] = 1;
        posMoves[1][6][11] = 1;
        posMoves[2][1][0] = 1;
        posMoves[2][4][6] = 1;
        posMoves[2][7][12] = 1;
        posMoves[3][6][9] = 1;
        posMoves[4][6][8] = 1;
        posMoves[5][3][1] = 1;
        posMoves[5][6][7] = 1;
        posMoves[5][8][11] = 1;
        posMoves[6][3][0] = 1;
        posMoves[6][4][2] = 1;
        posMoves[6][8][10] = 1;
        posMoves[6][9][12] = 1;
        posMoves[7][4][1] = 1;
        posMoves[7][6][5] = 1;
        posMoves[7][9][11] = 1;
        posMoves[8][6][4] = 1;;
        posMoves[9][6][3] = 1;
        posMoves[10][5][0] = 1;
        posMoves[10][8][6] = 1;
        posMoves[10][11][12] = 1;
        posMoves[11][6][1] = 1;
        posMoves[11][8][5] = 1;
        posMoves[11][9][7] = 1;
        posMoves[12][11][10] = 1;
        posMoves[12][9][6] = 1;
        posMoves[12][7][2] = 1;
    }

    /**
     * This methods gets the index
     * of the red frog.
     * 
     * @return int value of the index
     */
    public int getRed()
    {
        return red;
    }

    /**
     * This method is used to make
     * swaps depending on locations of frogs
     * which is determined by the int array
     * paremeter.
     * 
     * @param int array with locations of frogs
     * @return int array after jump made
     */
    public int[] swap(int[] x)
    {
        //int array of size 13
        int[] array = new int[13];

        //int variable to hold index
        int index;

        //for loop to initiliaze array to -1's
        for(int i = 0; i<13; i++)
        {
            array[i] = -1;
        }

        //int variable counter
        int counter = 0;

        //for loop that determines if swap possible
        //if possible makes swap
        for(int z = 0; z< 13; z++)
        {
            if((x[z] == 1)&&(z!=red))
            {
                array[counter] = z;
                counter++;
            }
        }

        //sets array at counter to red
        array[counter] = red;

        return array;
    }

    /**
     * This method is used to take in
     * an array of hoppers and adjust
     * the array to be used by other 
     * methods as well as other classes.
     * 
     * @param int array of frog locations
     * @return int array of frog locations
     */
    public int[] doBoard(int[] b)
    {
        //initilaize x to 0
        int x = 0;

        //sets h to length of b
        h = b.length;

        //sets board to all 0's
        for(int i = 0; i<13; i++)
        {
            board[i] = 0;
        }

        //sets red as the last element in the array
        for(x = 0; x < b.length; x++)
        {
            if(b[x]<0)
            {
                red = b[x-1];
                break;
            }
            else
            {
                board[b[x]] = 1;
            }
        }

        moves = new ArrayList<String>();
        int[] graphic = board;
        return graphic;
    }

    /**
     * This method is used in order to determine
     * if a particular move is possible.
     * 
     * @param int array of board state
     * @param int variable for 3-D array
     * @param int variable for 3-D array
     * @return boolean value if move is possible
     */
    public boolean isPossible(int[] B, int x, int z)
    {
        //gets middle value for jump
        int y = (x+z)/2;

        //nested if statements to determine if jump possible
        if(posMoves[x][y][z] == 1)
        {
            if((B[x] == 1)&&(B[y] == 1)&&(B[z] == 0))
            {
                if(y != red)
                {
                    return true;
                }
            }
        }
        return false;
    }

    /**
     * This method is used in order to make a hop
     * based upon the 3-D array
     * 
     * @param int array of board state
     * @param int variable for 3-D array
     * @param int variable for 3-D array
     * @return int array for board state
     */
    public int[] hopped(int[] b, int x, int z)
    {
        if(x==red)
        {
            //if the first frog is red
            int y = (x+z)/2;
            red = z;
            b[x]=0;
            b[y]=0;
            b[z]=1;
            h--;
            return b;
        }
        else
        {
            //if the first frog is green
            int y = (x+z)/2;
            b[x]=0;
            b[y]=0;
            b[z]=1;
            h--;
            return b;
        }
    }

    /**
     * This method is used to determine if a solution
     * is possible for the current board state.
     * 
     * @param int array of board state
     * @param int varaible for hop
     * @return arraylist of type string for board state
     */
    public ArrayList<String> getSolution(int[] bo, int hop)
    {
        if(solve(bo, moves, hop, false) != true)
        {
            moves = new ArrayList<String>();
            moves.add("No Solution Possible");
        }
        return moves;        
    }

    /**
     * This method is the recursive solver for the game.
     * It determines all possible moves and all possible
     * jumps that can be made as well as every possible
     * solution.
     * 
     * @param int array of board state  
     * @param arraylist from getSoluton method
     * @param int value for number of hoppers
     * @param boolean value of true or false
     * @return boolean value of true or false
     */
    public boolean solve(int[] bo,ArrayList<String> m,
    int hoppers,boolean s)
    {
        //sets int array B to parameter array bo
        int[] B = bo;

        //base case if there is only one hopper left on the board
        if (hoppers < 2)
        {
            for(int i = 0; i < B.length; i++)
            {
                if((B[i] == 1)&&(i==red))
                {
                    moves = m;
                    return true;
                }
            }
            return s;
        }
        else 
        {
            for(int x = 0; x<13; x++)
            {
                for(int z = 0; z<13; z++)
                {
                    /*
                     *if there is a possible move to be made 
                     *this removes the middle peg(y) and puts 
                     *x at z and it updates red
                     */
                    int y = (x+z)/2;
                    if(posMoves[x][y][z] == 1)
                    {
                        if((B[x] == 1)&&(B[y] == 1)&&(B[z] == 0))
                        {
                            if(y == red)
                            {
                                continue;
                            }
                            if(x==red)
                            {
                                red=z;
                            }
                            B[x]=0;
                            B[y]=0;
                            B[z]=1;
                            m.add((x+1)+"-"+(z+1));
                            s = solve(B, m, hoppers-1, s);
                            //this undos the previous move made
                            if(s == false)
                            {
                                B[x]=1;
                                B[y]=1;
                                B[z]=0;
                                m.remove(m.size()-1);
                                if(z==red)
                                {
                                    red=x;
                                }
                            }
                        }
                    }
                }
            }
        }
        return s;
    }
}

