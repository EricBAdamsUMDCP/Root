# Root
A log of code and notes for using root in the Mignerey lab

a ; tells the pc the line is over 

 Finding Errors

⭐Line number; Character Number

/home/ebadams/Starting_code/2,14,18/./uncommented,Pos_2d2017Centrality_Pbside.C:286:138: error
286:138

286 is the line number, 138 is the character number\

⭐ Failed to declare variable before it was used
/home/ebadams/Starting_code/2,14,18/./uncommented,Pos_2d2017Centrality_Pbside.C:301:3: error: use of
      undeclared identifier 'c1'
  c1 = new TCanvas();
  ^
  
  Therefore I need to tell it what the type of variable is (only first time)
  ergo solution is 
  TCanvas c1 = new TCanvas();
  
  BUT...
  
  CAN TELL PC TO FIGURE OUT WHAT A VARIABLE IS WITHOUT ME TELLING IT!!!!
  
  auto c1 = new TCanvas();
  
  AUTO TELLS THE COMPUTER TO FIGURE IT OUT
  
  
 ⭐ pointers
  Canvas* c1  = new TCanvas();
TCanvas *c1 = new TCanvas();

are equivalent and are both pointers

⭐  {} (blocks of text)
if (value == 0)   //(== means compare it to something)
{
printf("YES");
}
 
 >> e.g.
 TCanvas* c1  = new TCanvas();
{ TCanvas* c1  = new TCanvas(); }
//If you allocate memory using new or malloc in a block (curly brackets) and assign its address to a variable, 
the variable no longer exists after the block BUT THE BLOCK OF MEMORY STILL DOES

However everything inside of the block stays inside of the block, its like Vegas


 
⭐ comment blocks (how to comment out a shit load of code)

/* 
code
*/

⭐ Classes

TCanvas()
MyClass
MyClass()
